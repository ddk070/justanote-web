---
title: 'import 與 reference 區別'
description: 'import與reference區別'
pubDate: '2026/7/6'
tags:
    - maya
    - import
    - reference
    - 匯入方式
---

## MAYA 的匯入方式
1. import
2. reference

<hr><br>

## import

import.ma讀取Model.ma的所有物件，並**生成**與Model.ma相同的所有物件進入檔案裡。<br>

* 兩個檔案的物件**無牽連**（各自獨立）
* 檔案大

![import](../..//assets/import.jpg)

<hr><br>

## reference

reference.ma讀取Model.ma的所有物件，並**顯示**在reference.ma上。<br>

* 兩個檔案的物件**有牽連**（僅Model.ma的物件牽動reference.ma）
* 檔案小

![reference](../../assets/reference.jpg)


