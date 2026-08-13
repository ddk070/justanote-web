---
title: '［疑難雜症］File contains unknown nodes or data'
description: 'File contains unknown nodes or data'
pubDate: '2026/07/30'
outline: '基礎'
tags:
    - maya
    - 基礎
    - mel
    - 疑難雜症
---


# 問題
當你打開檔案後，在右下角腳本編輯器發現紅色報錯顯示『File contains unknown nodes or data 』。


# 解決方法

1. 打開腳本編輯器
2. 將下方程式碼貼入MEL裡
3. Ctrl + A全選文字後Ctrl + Enter（或是點擊腳本編輯器頂部工具列的雙藍色三角形 ▷▷ 執行按鈕）。

```
string $unknownNodes[] = `ls -type "unknown"`;
for($node in $unknownNodes){
    if($node=="<done>")
        break;
    if(`objExists $node`){ 
        int $lockState[] = `lockNode -q -l $node`;
        if($lockState[0]==1)
            lockNode -l off $node;
        delete $node;
    }
}

```






