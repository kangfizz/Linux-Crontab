# Linux-Crontab
This topic is talking about how to use crontab to run some web crawler files for get data periodic.
### 前言: 
### 此文將介紹使用ubuntu系統之crontab定時排程技術，去實行在R程式抓取即時資料之方法。

### 1.	Crontab指令:
+ Crontab –e   編輯
+ Crontab –l		列出排程
+ Crontab –r		刪除所有排程

### 2.	
在進入 Crontab –e 後，案”i”編輯 編輯完後按”ctrl+c”兩次後 打上”:wq”   
 (也就是儲存後關閉)  
 寫入格式可參考: [這個網址](https://sites.google.com/site/stevenattw/linux/crontab)  
 舉個例子: */2 * * * * Rscript /PATH/TO/FILE.R  
 此情況為每兩分鐘執行一次.R檔   

### 3.	
看執行狀況可從 /var/mail/root 看 

### 4.	 
此外，在你的R程式裡面，要加上兩個  
1)#!/usr/bin/Rscript  
2).libPaths(“/your/path/for/package”)  
↑上面的如果你不知道你的rstudio的package你可以先輸入.libPaths()查看  
因為這個問題其實是我的ubuntu的R與Rstudio的library不一樣地方。  
