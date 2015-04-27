---
layout: post
title: Matlab Tutorial
---

The [Machine Learning]({{ site.baseurl }}/ML) and [Motion Capture]({{ site.baseurl }}) will be conducted using Matlab. Given below are some basic operations that can be performed in Matlab. 

* Table of Contents:
{:toc}

## Basic Operations
---

Basic folder operations

{% highlight matlab %}
% Print working folder
pwd

% Change working folder
cd 'C:/Path/to/folder'

% Show folder contents
ls
{% endhighlight %}

Elementary operations

{% highlight matlab %}
% Basic computations
5+6
3-2
5*8
1/2

% Exponent
2^6

% Binary operations
1 == 2 % false
1 ~= 2 % true
1 && 0
1 || 0
xor(1,0)
{% endhighlight %}

Variable assignment and printing

{% highlight matlab %}
% Variable assignment
a = 3; % semicolon suppresses output
b = 'hi';
c = 3>=1;

% Display commands
a = pi;
disp(a)
disp(sprintf('2 decimals: %0.2f', a))
disp(sprintf('6 decimals: %0.6f', a))

% Display format
format long
a
format short
a
{% endhighlight %}

Using help function

{% highlight matlab %}
% help function to get information about commands
help eye
help rand
help help
{% endhighlight %}

## Moving Data Around
---

Loading and Saving Data

{% highlight matlab %}
% Loading data
pwd 
cd 'Path\to\folder'   
ls 
load testy.dat  
load testx.dat

% Checking loaded data
who             % list variables in workspace
whos            % list variables in workspace (detailed view) 
clear testy       % clear w/ no argt clears all

% Saving data
v = testx(1:10);           % first 10 elements of q1x (counts down the columns)
save hello.mat v;        % save variable v into file hello.mat
save hello.txt v -ascii; % save as ascii
{% endhighlight %}

## Vector and Matrices
---

{% highlight matlab %}
% Vectors and matrices
A = [1 2; 3 4; 5 6]
v = [1 2 3]
v = [1; 2; 3]
v = [1:0.1:2]
v = 1:6          % assumes stepsize of 1

% Dimensions of matrix
sz = size(A) % 1x2 matrix: [(number of rows) (number of columns)]
size(A,1)  % number of rows
size(A,2)  % number of cols
length(v)  % size of longest dimension

% Standard matrices
w = ones(1,3)   
w = zeros(1,3)
w = rand(1,3)  % drawn from a uniform distribution 
w = randn(1,3) % drawn from a normal distribution (mean=0, var=1)
I = eye(4)     % 4x4 identity matrix

% Demonstration of randn function
w = -6 + sqrt(10)*(randn(1,10000))  % (mean = -6, var = 10)
hist(w)     % plot histogram using 10 bins (default)
hist(w,50)  % plot histogram using 50 bins

% Matrix Indexing
A = randn(3,3);
A(3,2)     % indexing is (row,col)
A(2,:)     % get the 2nd row
A(:,2)     % get the 2nd col
A([1 3],:) % print all  the elements of rows 1 and 3

A(:,2) = [10; 11; 12]     % change second column
A = [A, [100; 101; 102]]; % append column vec
A(:)                      % Select all elements as column vector

% Combining matrices
A = [1 2; 3 4; 5 6]
B = [11 12; 13 14; 15 16] % same dims as A
C = [A B]                 % concatenating A and B horizontally
C = [A; B]                % concatenating A and B vertically
{% endhighlight %}

## Computing on data
---

{% highlight matlab %}
% Initialize variables
A = [1 2;3 4;5 6]
B = [11 12;13 14;15 16]
C = [1 1;2 2]
v = [1;2;3]

% Matrix operations
A * C    % matrix multiplication
A .* B   % element-wise multiplication
A .^ 2   % element-wise square of each element in A
1./v     % element-wise reciprocal
log(v)   % functions that operate element-wise 
exp(v)
abs(v)

-v       % -1*v
v + ones(length(v), 1)  

A'       % matrix transpose

% Misc useful functions
% max and min
a = [1 15 2 0.5]
val = max(a)
[val,ind] = max(a) % val -  maximum element of the vector a and index
val = max(A)       % if A is matrix, returns max from each column

% find
a < 3
find(a < 3)
A = magic(3)
[r,c] = find(A>=7)  % row, column indices for values matching comparison

% sum, prod
sum(a)
prod(a)
floor(a) % or ceil(a)
max(rand(3),rand(3))
max(A,[],1) -  maximum along columns(defaults to columns - max(A,[]))
min(A,[],2) - maximum along rows
A = magic(9)
sum(A,1)
sum(A,2)
sum(sum( A .* eye(9) ))
sum(sum( A .* flipud(eye(9)) ))

% Matrix inverse (pseudo-inverse)
pinv(A) 
{% endhighlight %}

## Plotting data
---

{% highlight matlab %}
% 2D plot
t = [0:0.01:0.98];
y1 = sin(2*pi*4*t); 
plot(t,y1);
y2 = cos(2*pi*4*t);
hold on; 
plot(t,y2,'r');
xlabel('time');
ylabel('value');
legend('sin','cos');
title('my plot');
print -dpng 'myPlot.png'


close;                   % or,  "close all" to close all figs
figure(1); plot(t, y1);
figure(2); plot(t, y2);
figure(2), clf;          % can specify the figure number
subplot(1,2,1);          % Divide plot into 1x2 grid, access 1st element
plot(t,y1);
subplot(1,2,2);          % Divide plot into 1x2 grid, access 2nd element
plot(t,y2);
axis([0.5 1 -1 1]);      % change axis scale

% Display a matrix 
figure;
imagesc(magic(15)), colorbar, colormap gray;
{% endhighlight %}

## Control Statements
---

{% highlight matlab %}
% For Loop
v = zeros(10,1);
for i=1:10, 
    v(i) = 2^i;
end;

% While Loop
i = 1;
while i <= 5,
  v(i) = 100; 
  i = i+1;
end

% break
i = 1;
while true, 
  v(i) = 999; 
  i = i+1;
  if i == 6,
    break;
  end;
end

% if/else
if v(1)==1,
  disp('The value is one!');
elseif v(1)==2,
  disp('The value is two!');
else
  disp('The value is not one or two!');
end
{% endhighlight %}