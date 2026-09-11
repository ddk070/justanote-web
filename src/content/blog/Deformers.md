---
title: 'Deformers'
description: 'maya Deformers'
pubDate: '2026/09/11'
outline: 'Rigging'
tags:
  - maya
  - Rigging
---


# 用途
變形器工具欄用於綁骨，用Channel Box調整數值做變化。<br>
自行判斷每個功能用於何處。
- Animation、 Rigging > Deform

> 變形器裡的其他數值和功能也可嘗試動動看，但嘗試前建議先備份模型或檔案。

# Blend Shape
用兩個模型面數與點相同，來切換變形成不同樣式。
1. 把原本的角色頭 Duplicate（複製 Ctrl + D） 好幾個到旁邊。
2. 把複製出來的頭分別雕刻成其他形狀（微笑、哭泣）。
3. 同時選取這些「複製出來的頭」，最後加選「原本的頭」，然後Blend Shape。

> 可用Shape Editor替代Blend Shape，不必用很多模型複製在旁邊。

# Lattice（晶格變形器）
用晶格來變形模型。
- ffd1LatticeShape 調整 S、T、U Divisions 的數值，可調整格子切分量

1. 在晶格（綠色盒子）上按住滑鼠右鍵，選擇 Lattice Point。
2. 使用選取工具選中晶格的控制點。
3. 切換到 Move（移動鍵 W）、Rotate（旋轉鍵 E） 或 Scale（縮放鍵 R） 來拉動這些點，裡面的模型就會跟著平滑地變形。

> 如果直接把晶格刪除，模型會彈回原狀。<br>
> Edit > Delete by Type > History（快速鍵 Alt + Shift + D）<br>
> 保留形狀並刪除晶格。


# Proximity Wrap（近接包裹變形器）
將配件附著在模型上。

1. 鼠左鍵點選 「配件 、 衣服」（包裹配件 Wrap Influence）
2. 按住 Shift，加選 「角色身體 、 基礎模型」（基礎物件 Base）
3. Animation、 Rigging > Deform > Proximity Wrap 

> 傳統的 Wrap 變形器在計算大量頂點時非常消耗電腦效能。<br>
> Maya 2024 Proximity Wrap（近接包裹變形器）算速度比傳統 Wrap 快上好幾倍，而且非常穩定，不容易因為模型靠太近而產生破面。

# Wire
用線來控制面。

1. 在你的模型旁邊，使用 **EP Curve Tool** 或 **CV Curve Tool** 畫一條貼合模型線條的 **NURBS 曲線**
2. Animation、 Rigging > Deform > Wire
3. 看 Maya 視窗最左下角的提示文字，做動作：
	- 「Select shape(s) to deform, and press Enter」：先用滑鼠點選你的模型（網格），然後按鍵盤的 Enter。
	- 「Select wire curves, and press Enter」：接著點選你剛剛畫好的那條 NURBS 曲線，然後再按一次 Enter。
4. 在網格上或大綱視窗選取你的那條 NURBS 曲線。
5. 按住滑鼠右鍵切換到 Control Vertex（CV 點模式）。
6. 移動曲線的 CV 點，調整變形參數。

- Dropoff Distance（衰減距離）： 控制這條線的「磁力範圍」。數值越大，曲線能帶動模型周圍的面積就越廣；數值太小，可能只有貼近曲線的幾個點會動。
- Scale（縮放權重）： 用來整體放大或縮小這條曲線對模型的影響力（預設為 1）。


# texture
用紋理貼圖變形物體。
1. 選取你的模型（注意：模型面數必須夠多，否則沒有足夠的點可以產生凹凸細節）
2. Animation、 Rigging > Deform > texture
3. 選中模型，在右側的 Attribute Editor（屬性編輯器） 中找到 textureDeformer1 標籤頁
4. 屬性 Texture，點擊右側的 「黑白相間棋盤格按鈕」
5. 選擇 File 載入你自己的黑白圖片，或者直接點選 Maya 內建的程式化紋理（例如 Noise 雜訊 或 Fractal 分形）
	Strength（強度）： 調整這個數值，數值越大，模型被圖片推開的幅度就越高。
	Direction（方向）： 決定模型要往哪裡凸。


# Non-linear（非線性變形）
- Animation、 Rigging > Deform > Non-linear

## Bend (彎曲)
讓物件沿著一條軸向彎曲<BR>
- curvature（曲率）：控制彎曲的角度
可調整變形器本身方向，改變物品彎曲的方向。

## Flare (錐形化)
讓物體的一端變大或變小。

## Twist（扭曲）
讓物品像擰毛巾一樣扭轉，頂端或尾端朝左方向或右方向集體扭曲變形。
- start angle（起始角度）：控制手把「底端」的扭轉度數
- end angle （結束角度）：控制手把「頂端」的扭轉度數

## Squash (擠壓拉伸)
模擬物體被壓扁或拉長的效果。

## Wave / Ripple (波浪/漣漪)
讓表面產生上下起伏的波紋。
- amplitude（振幅）：控制波浪的「高度」
- wavelength（波長）：控制波浪的「疏密（寬度）」



