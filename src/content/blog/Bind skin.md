---
title: 'Bind skin'
description: 'maya Bind skin'
pubDate: '2026/09/16'
outline: 'Rigging'
tags:
  - maya
  - Rigging
---


# 用途
將骨架與模型綁定在一起，賦予每個頂點權重。

> 關於綁定推薦使用[ngSkinTools](/blog/ngskintools/)外掛。<br>
> 免費下載（可用於商業），相容於 Maya 2018 至 Maya 2026，maya2027為內建。

***

# Bind skin
1. 先用滑鼠點選你的 3D 模型
2. 按住 Shift 鍵，再點選骨架的根骨頭（Root Joint）或主要關節
3. `Rigging` > `Skin` > `Bind Skin`



# Bind Skin 設定

### Bind To 
將模型綁定到哪裡
- Joint Hierarchy：綁定從這骨頭開始上下延伸所有連接到的全部骨頭（預設選項）
- Selected Joints：只綁定選中的骨頭
- Object Hierarchy：將非骨頭（含有 **Transform 節點**）當作骨頭與模型綁定，例如：群組（Group）、定位器（Locator）、基本幾何體（如：另外一個方塊、球體）、曲線（NURBS Curve）

### Bind Method
怎麼自動分配控制權（權重）
- Closest Distance：距離最近的骨頭與模型頂點（預設選項）
- Closest In Hierarchy：算距離時會參考骨頭的階層
- Heat Map：權重依照模型表面慢慢傳遞，距離越遠，權重數值越小
- Geodesic Voxel：用方塊包住模型，在內部算骨架權重

> Closest Distance可能會沾黏到其他部位的權重。<br>
> Heat Map遇到模型破洞就罷工，Geodesic Voxel不會。


### Skinning Method
當關節開始旋轉、扭曲時，模型的皮膚要怎麼折疊和變形

- Classic Linear（經典線性蒙皮）：當關節扭轉時，讓體積縮減和塌陷變形
- Dual Quaternion（雙四元數蒙皮）：當關節扭轉時，保持網格的體積
- Weight Blended（權重混合蒙皮）：用權重決定，讓哪裡變形，讓哪裡保持體積。


### Normalize Weights
怎麼幫你把權重總和湊成 1.0

- Interactive（互動式正規化）：當你增加A骨頭權重時，幫你自動減少B、C、D骨頭的權重
- None（不進行正規化）：什麼都不做，允許你創造出總和小於 1.0 或大於 1.0 的權重
- Post（後置正規化）：撥放動畫後（或算圖），才自動計算或分配你畫好的權重

>  Post可能最終算圖出來的與maya上撥放的畫面可能不一樣。


### Weight Distribution
畫少時多出來的權重要如何分配。<br>
Normalize Weights 設定為 Interactive（互動式）時才會啟動的輔助設定。

- Distance（距離導向）：誰離得近就分給誰（預設）
- Neighbors（鄰居導向）：看附近的頂點在哪個骨頭上，就一起跟隨同個骨頭


### Allow Multiple Bind Poses
（允許個複數綁定姿勢） 

- 開啟：不管骨架姿勢，想綁什麼就綁
- 關閉：所有綁定必須用同一個相同姿勢，才允許綁骨

### Max Influences
決定最多能有幾個骨頭來平分頂點的權重。


### Maintain Max Influences
嚴格執行上面的數量限制，不准超標。

### Remove Unused Influences
把權重是 0 的骨頭踢出清單。

### Colorize Skeleton
骨架彩虹化/顏色視覺化：用顏色來告訴你，誰歸誰管。


### Include hidden selections on creation
在視窗中被隱藏的物件也要一起被綁定。



### Deformer Node
用哪一種「變形驅動引擎」執行綁定

- Skin Cluster（傳統骨骼皮膚節點）：在每個頂點紀錄權重數字
- Proximity Wrap（近接包裹變形節點）用空間距離來隔空控制，調整「衰減率」來決定吸力的範圍


***

# 參考資料
* [Bind Skin Options _Maya2024](https://help.autodesk.com/view/MAYAUL/2024/ENU/?guid=GUID-CF2C698A-44BB-4CA0-BCB9-DB36500DA812)












