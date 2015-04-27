---
layout: post
title: Prerequisites　(事前準備)
---

This page explains the steps that you have to do before attending the workshop.
このページはワークショップまでに必要な事前準備を説明しています．

The prerequisites for attending each workshop are different. Please complete these before the start of workshop.

* Table of Contents:
{:toc}

---

## [Machine Learning Workshop]({{ site.baseurl }}/ML)

* Please prepare a Laptop with these minimum requirements for doing the exercises.　（必要最低限性能は以下の二点です．)
  - Intel i3 Processor
  - 2 GB RAM

* Install Matlab on the Laptop by one of the following ways:
  - Obtain Matlab from the LSSE Server following the instructions provided [here](http://www.lsse.kyutech.ac.jp/~techman/portal/modules/compsys/index.php?ml_lang=en).
  - Obtain Matlab trial license from the Mathworks website available [here](https://jp.mathworks.com/programs/trials/trial_request.html?s_iid=hp_trial_hpg_cta2). For this you will need to create a Mathworks account from [here](https://jp.mathworks.com/accesslogin/login.do?uri=http://jp.mathworks.com/index.html%3Fs_tid%3Dgn_logo).

---

## [Motion Capture Workshop]({{ site.baseurl }}/Mocap)

The requirements for the Motion Capture Workshop are similar to Machine Learning Workshop:

* Please prepare a Laptop with these minimum requirements for doing the exercises.　（必要最低限性能は以下の二点です．)
  - Intel i3 Processor
  - 2 GB RAM

* Install Matlab on the Laptop by one of the following ways:
  - Obtain Matlab from the LSSE Server following the instructions provided [here](http://www.lsse.kyutech.ac.jp/~techman/portal/modules/compsys/index.php?ml_lang=en).
  - Obtain Matlab trial license from the Mathworks website available [here](https://jp.mathworks.com/programs/trials/trial_request.html?s_iid=hp_trial_hpg_cta2). For this you will need to create a Mathworks account from [here](https://jp.mathworks.com/accesslogin/login.do?uri=http://jp.mathworks.com/index.html%3Fs_tid%3Dgn_logo).

### Optional Requirement

An optional exercise is to access motion capture data through network streaming. For this install a C++ compiler on the Laptop.

* **Windows**: Install Visual Studio software by obtaining the software installer from the LSSE offce.
* **Linux**: Install **g++** compiler in the system.

---

## [Baxter Workshop]({{ site.baseurl }}/Baxter)

To conduct experiments with Baxter robot, Ubuntu operating system has to be used.

### Software Environment Setup　(ソフトウェア環境セットアップ)

* Please prepare a Laptop with these minimum requirements for doing the exercises.　（必要最低限性能は以下の二点です．)
  - Intel i3 Processor
  - 2 GB RAM

* Download VirtualBox software from [here](https://virtualbox.org/wiki/Downloads) and install the software on your laptop.　（”VirtualBox"をこのページからノートPCにダウンロードしてインストールしてください．）

* Copy the Ubuntu VirtualBox image from the shared PC of ShibataLab to your Laptop. The file is available in the **Desktop\Workshop** folder titled **Workshop.ova**.　（柴田研究室の共有パソコンから"Ubuntu"（OS）をコピーしてください．ファイル名は"Workshop.ova"となっており，デスクトップにあります．)

* Open VirtualBox and import the Ubuntu image as shown below.　（次の手順でインポートしてください．）

  - Open VirtualBox:
  
  ![VB1](../images/VB1.png)
  
  - Import Appliance:
  
  ![VB2](../images/VB2.png)
  
  - Open the OVA file:
  
  ![VB3](../images/VB3.png)
  
  - Start importing:
  
  ![VB4](../images/VB4.png)
  
  - Start Ubuntu 14.04:
    
  ![VB5](../images/VB5.png)

* This will start Ubuntu operating system. The login password is **workshop** and the sudo password is also **workshop**.　（ログインパスワードと管理者として実行するときのパスワードはどちらも"workshop"です．）

With this you have finished setting up the software environment for the workshops.　（これでワークショップに必要なソフトウェア環境は整います．）

---

### Getting used to Ubuntu

Ubuntu is a free Operating System that is based on the Linux kernel. In the workshop, we will be using the Command Line Interface (CLI) called **Terminal**.

Please read these tutorial pages to get used to Terminal:

* **日本語**: [Official](https://wiki.ubuntulinux.jp/UbuntuTips/Others/HowToUseTerminal).

Please comment at the bottom of this page, if you know a better tutorial to learn about Terminal.

* **English**: [Official](https://help.ubuntu.com/community/UsingTheTerminal). 

---

### Getting used to Git/Github

One of the workshops will be on Version Control Software called [Git](http://git-scm.com/) and on the Git online interface called [Github](http://github.com).

For accessing the materials of the workshop, you need to create an account on the Github website:

* Please create a Github account from this [link](https://github.com/). 
* Follow the user **shibatalab** from this [link](https://github.com/shibatalab) as shown in the figure below:

![Github](../images/github.png)  

* Practice editing the contents of this [site](http://shibatalab.github.io) from the Github website as shown below:
  - Open a browser and go to Github website and login with your account.

  - Go to the repository of this [site](https://github.com/shibatalab/GW2015Workshop) and check the contents of the repository.

  - Edit the contents of this page available at this [link](https://github.com/shibatalab/GW2015Workshop/blob/gh-pages/_posts/2015-4-24-Prerequisites.md) and read the raw content of this page.

---

## Comment below

If you have completed all the steps required for attending the workshops, then please comment below with your name. Also please comment if you have any problems with the steps.    