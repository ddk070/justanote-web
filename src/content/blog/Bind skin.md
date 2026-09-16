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




### Normalize Weights



***

# 參考資料
* [Bind Skin Options _Maya2024](https://help.autodesk.com/view/MAYAUL/2024/ENU/?guid=GUID-CF2C698A-44BB-4CA0-BCB9-DB36500DA812)
* [Question about 'bind skin' setting in Maya (Beginner) ](https://www.reddit.com/r/Maya/comments/1eu9lex/question_about_bind_skin_setting_in_maya_beginner/)











