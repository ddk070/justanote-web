---
title: 'Graph Editor（曲線編輯器）'
description: 'maya Graph Editor（曲線編輯器）'
pubDate: '2026/10/02'
outline: 'Animation'
tags:
  - maya
  - Animation
  - 快捷鍵
---


# 用途
- 檢視動畫關鍵幀、曲線、線條狀態
- 控制運動節奏與加減速
- 編輯Tangents狀態
- 編輯曲線狀態


***

# Graph Editor
三種方法：
1. `Windows` > `Animation Editors` >` Graph Editor`
2. `Panels` >` Panel`> `Graph Editor`
3. 右上角`工作區` > `Animation`


# Graph Editor 快捷鍵

## 視窗
**平移：**` Alt` + `中鍵` <br>
**縮放：** `Alt` + `右鍵` <br>
**水平縮放：** `Alt` + `Shift` + `右鍵` <br>

**絕對視圖：** `1` <br>
**堆疊視圖：** `2` <br>
**歸一化視圖：** `3` <br>

> 絕對視圖 （Absolute View 預設）：所有曲線使用相同的座標數值（曲線疊在一起）。<br>
> 堆疊視圖 （Stacked View）：所有曲線分開顯示。<br>
> 歸一化視圖 （Normalized View）：顯示所有曲線的上下波浪程度。<br>
>  歸一化視圖重算 ：`View` > `Renormalize`


## 曲線
**顯示所有曲線：** `A` <br>
**聚焦曲線：** `F` <br>
**鎖定曲線：** `H` <br>
**解鎖曲線：** `J` <br>
**上一段曲線：** `[` <br>
**下一段曲線：** `]`


## 關鍵幀
> 在曲線上編輯關鍵幀


### 快捷選單
**開啟關鍵幀快捷選單：** `Shift` + `s`<br>


### 設KEY
**直接插入關鍵幀：** `中鍵` + `i`<br>
**在當前時間標記器（黃色）插入關鍵幀：** `Alt` + `i` <br>

**設平移(Translation)關鍵幀：** `Ctrl` +` Shift `+ `W` <br>
**設旋轉(Rotation)關鍵幀：** `Ctrl` +` Shift `+ `E` <br>
**設縮放(Scaling)關鍵幀：**  `Ctrl` +` Shift `+ `R` <br>


### 移動關鍵幀
**向左移動一格：** `Shift` + `9`（鍵盤上排） <br>
**向右移動一格：** `Shift` + `0`（鍵盤上排）<br>


### 時間標記
**移至所選的關鍵幀：** `Alt`+ `/` <br>
**選擇上一幀：** `Ctrl` + `Alt` + `<` <br>
**選擇下一幀：** `Ctrl` + `Alt` + `>`



# 開啟線循環 
- **前方無限：** `Curves` > `Pre-Infinity` ![cyclebefore.png](../../assets/cyclebefore.png)
- **後方無限：** `Curves` > `Post-Infinity` ![cycleafter.png](../../assets/cycleafter.png)

1. 循環(Cycle)：尾接頭，重複循環
2. 偏移量循環(Cycle with Offset)：接續終點重複曲線形狀，向上或向下延伸
3. 往返(Oscillate)：重複反轉線來延伸
4. 線性(Linear)：順著開頭和結尾數值，分別向上或向下延伸
5. 恆定(Constant)：開頭與結尾數值保持0，無限延伸（預設）


# 在密集的曲線上選擇關鍵幀
1. `Select` > `Prefer Selected Curves`
2. 選取線 > `左鍵`移動關鍵幀


# Tangent 類型
- 點擊key會出現的翹翹板就是Tangent

## Auto Span (Legacy)
自動（預設）。

## Spline Tangents
用於緩衝。

## Linear Tangents
用於打尖。

## Flat Tangents
用水平。

## Step Tangents
可用於檢查動作，類似定格效果。

## Break Tangents
用於打斷，可自由調整兩邊的角度。


***

# 參考資料
* [Graph Editor_2024](https://help.autodesk.com/view/MAYAUL/2024/ENU/?guid=GUID-6D38EAEA-6032-471E-BD0E-54A74D4443C0)
* [曲线图编辑器”(Graph Editor)界面概述_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-1C521455-9DF8-47D6-AD9C-6AD5C91FFAA3)
* [曲线图编辑器”(Graph Editor)菜单_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-94768B58-65F0-4715-97E0-625AEDA18F2A)
* [曲线图编辑器工具栏_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-A6061A36-81FF-4F57-A081-C967F749D546)








