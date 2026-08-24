---
title: 約束系統（Constrain）
description: maya 約束系統（Constrain）
pubDate: 2026/08/24
outline: Rigging
tags:
  - maya
  - Rigging
  - Constrain
---


# 用途
- 讓兩個物體建立跟隨關係。
- 讓一個物件的位置、旋轉或縮放跟隨另一個物件的核心功能。



# Constrain（約束系統）
`Animation選單`或`Rigging選單`> `Constrain`


## Parent（父子約束）
結合位置與旋轉的跟隨，效果類似建立父子階層（Parent-Child）。<br>
為最常使用的基礎綁定約束。


## Point（點約束）
讓物件的**位置（Position）** 跟隨目標，但旋轉可以獨立。


## Orient（定向約束）
讓物件的**旋轉（Rotation）** 跟隨目標，但位置不變。


## Scale（縮放約束）
讓物件的**大小（Scale）** 隨目標等比例或按軸向放大縮小。


## Pole Vector（桿向量約束）
專門用來控制 IK 骨骼（如手肘或膝蓋）的轉向與朝向。


## Path（路徑約束）
讓物件沿著指定的曲線（Curve）軌跡移動。


# 如何使用約束
1. 先選取控制物件（父），在選取被控制物件（子）
2. 然後按上述任何一個約束功能

> 成功後，被控制物件（子）在outliner裡有一個紅色連結圖示，表示被綁定<br>
> 視窗右邊，被控制物件（子）的模型數值旁也會顯示藍色，表示被綁定。




# 參考資料
* [Constrain menu](https://help.autodesk.com/view/MAYAUL/2025/ENU/?guid=GUID-5EDA8C50-789D-4091-BAE6-4284761CDAC2)









