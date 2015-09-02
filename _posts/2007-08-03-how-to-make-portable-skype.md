---
title: 便携版 Skype 制作过程
author: esperisto
layout: post
archive: true
comments: true
categories:
  - 经验之谈
tags:
  - skype
  - 便携版
  - 软件
---
[Skype][1] 是一個 VoIP 電話客戶端，可以呼叫座機和手機，也可像普通 IM 軟件一樣發送即時消息。如果你擁有支持 U3 Smart 技術的 U 盤便可以使用 U3 版的便攜 Skype。可是如果我用的是 PortableApps 呢？沒有官方和非官方版的呀。那只有我自己做了。 如果你瞭解 Skype 的話就會知道 Skype 其實自身就是便攜的（也就是通常說的“綠色”）。那麽，爲了使它和 PortableApps 整合，我們要做下面的步驟：

  1. 準備工作： 
      * 下載并安裝 [Quick Batch File Compiler][2] [破解版][3]（一定要是經過注册或可破解的，不然編譯出的可執行文件會彈出一個對話框來）；
      * 下載并安裝 [Icons from File][4]（用于抓取圖標）；
      * 下載并安裝 Skype；
  2. 制作便攜版： 
      * 在安裝了 PortableApps 的 U 盤上建立如下文件夾結構：  
        `[USB 盤符]:\PortableApps\SkypePortable\`  
        `[USB 盤符]:\PortableApps\SkypePortable\App\`  
        `[USB 盤符]:\PortableApps\SkypePortable\Data\`
      * 將 skype.exe 復制到 [USB 盤符]:\PortableApps\SkypePortable\App\ 中；
      * 在 [USB 盤符]:\PortableApps\SkypePortable\ 中建立一個批處理文件，名為 SkypePortable.bat，內容為：``
    
    `@echo off<br />
set DATA=%~dp0Data<br />
if not exist "%~dp0DATA" mkdir "%~dp0DATA"<br />
start "Skype 2.0" /D"%~dp0" "%~dp0\App\skype.exe" /datapath:"%DATA%" /removable`
    
      * 抓取圖標：運行 Icons from File，打開 skype.exe，選取第一個圖標，保存為 .ico 文件；
      * 用 Quick Batch File Compiler 打開剛才建立的 SkypePortable.bat，選中“定制資源”選項卡，填寫“文件描述”為 SkypePortable，如圖所示：
    
    ![Figure 1](/assets/images/quickbc-1.png)  
    在“應用程序圖標”中瀏覽剛才抓取的 Skype 圖標；
    
      * 按“選項”按鈕，“常規”選項卡中選中“魅影應用程序”，如圖所示：  
        ![Figure 2](/assets/images/quickbc-2.png)
      * 點擊“生成”按鈕生成可執行文件；
      * 將生成的可執行文件命名為 SkypePortable.exe 放在 [USB 盤符]:\PortableApps\SkypePortable\ 文件夾下，啟動 PortableApps，就可在菜單中看到 Skype 啦！

 [1]: http://www.skype.com
 [2]: http://www.abyssmedia.com/quickbfc/ "訪問軟件主頁"
 [3]: http://www.downxia.com/downinfo/2716.html "進入下載頁面"
 [4]: http://www.vlsoftware.net/exico/ "訪問軟件主頁"
