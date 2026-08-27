---
title: 'Arnold 燈光屬性設定'
description: 'maya Arnold燈光屬性設定'
pubDate: '2026/08/19'
outline: 'Lighting'
tags:
  - maya
  - Lighting
  - Arnold
---


# 用途
調整燈光亮度、強度或其他燈光功能。


# Arnold 燈光屬性設定
> 須手動調整燈光亮度，才會有光。


### 打開燈光屬性界面
1. 選取燈光
2. 按`ctrl + A `打開 **Attribute Editor**（屬性編輯器）
3. 燈光屬性將顯示在畫面右側


## Base Attributes
- **Color（顏色）**：燈光的色彩，可直接選色，或連結 HDRI 貼圖（Skydome 常見）。
- **Intensity（強度）**：燈光的線性亮度。
- **Exposure（曝光度）**：以 2 次方倍增光量。<br>
  官方給的公式：
  ```
  實際亮度 = Intensity * 2^Exposure
  ```
```
1 * 1 * 2^4 = 16
```
```
1 * 16 * 2^0 = 16
```

- **Use Color Temperature（使用色溫）**：勾選後可直接輸入 **Kelvin（K）** 物理數值（例如 3000K 暖黃光、6500K 白光）。
  

## Color & Shadows / Sampling
決定畫面精細度與噪點（Noise）的控制關鍵：

- **Samples（採樣數）**：修正軟陰影與大面積光產生的**顆粒噪點**。數值越高陰影越細緻，但會增加算圖時間（通常預設 1~3，最終算圖會調高，建議Samples調3）。
- **Cast Shadows（投射陰影）**：開啟或關閉該燈光的陰影計算。
- **Shadow Color（陰影顏色）**：改變陰影的深淺或顏色（預設為全黑）。


## Contribution / Light Filters
- **Diffuse（漫反射）**：控制該燈光對物體表面色彩（色彩、霧面）的亮度和影響權重。
- **Specular（高光/反射）**：控制燈光在物體表面產生的**亮點（高光）與鏡面反射**強度。
- **SSS（次表面散射）**：控制燈光對皮膚、玉石、牛奶等半透明材質的穿透亮光。
- **Indirect（間接光）**：控制該燈光所產生的二次反彈光（GI 全局光）強度。
- **Volume（體積光）**：控制燈光對霧氣（Volume Scattering）或大氣效果的照明強度。


## Visibility & Light Group
- **Camera（相機可見性）**：數值為 0 時，彩現時背景或光源本身會隱形（例如隱藏 Skydome 的背景貼圖），但保留它投射的光影。
- **Transmission / Specular Reflection**：決定該燈光是否出現在物體的折射內部或反射鏡面中。
- **AOV Light Group（燈光分組）**：在此輸入自訂名稱（如 `rim_light`），可以將這盞燈單獨輸出成一個**獨立的 AOV 算圖圖層**，方便在 Nuke 或 Photoshop 中單獨調整這盞燈的亮度。



# 參考資料
* [Lights - Arnold User Guide](https://help.autodesk.com/view/ARNOL/ENU/?guid=arnold_user_guide_ac_lights_html)
