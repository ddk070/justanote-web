---
title: 'Animation Layers'
description: 'maya Animation Layers'
pubDate: '2026/10/08'
outline: 'Animation'
tags:
      - maya
      - Animation 
  
---


# 用途
- 用圖層隔開每層動畫
- 在不破壞原始動畫下，新增或合併新動畫
- 用圖層建立各種不同動畫，進行比對或微調修改


***

# Animation Layers
兩種方法：
1. 右下方界面切換成`Anim`
2. `Windows` > `Animation Editors` > `Animation Layers`

## 建立新圖層
1. 選取你想要操作的角色控制器（骨架或物體）
2. 點擊 `Create Layer from Selected` (一個藍色圖層帶有一個小球的圖示)


> **BaseAnimation**（這層是無法刪除或調整順序的）。


## 設定圖層模式
- **A (Additive，疊加模式 - 預設)**：對圖層`右鍵`，`Layer Mode` > `Additive`
- **O (Override，覆蓋模式)**：對圖層`右鍵`，`Layer Mode` > `Override`

> 能設key的都能加入圖層，建議只加入設key對象（控制器），保持簡單即可。<br>
> Additive：疊加，相加所有圖層為最終顯示數值。<br>
> Override：覆蓋，以最上層數值為最終顯示數值。<br>
> Passthrough：通過，可調整值的透明度。


## 刪除圖層
1. 選取圖層
2.  `Layers` > `Delete` 


## 管理與合併
- **Mute（靜音）**：點擊圖層旁的 綠色圓圈 (M)，可以暫時關閉該圖層效果。
- **Lock（鎖定）**：點擊 鎖頭圖示，防止意外修改到該圖層。
- **Merge（合併圖層）**：選取多個圖層，右鍵選擇 Layers > Merge Layers，可以將多個圖層合併。
- **Bake（烘焙動作）**：如果你要導出到遊戲引擎（如 Unity/Unreal），必須將所有圖層融合回單一軌道。選取圖層，右鍵選擇 Layers > Bake Layer，Maya 就會把所有疊加的動作重新計算並壓回 BaseAnimation 或生成一個乾淨的新圖層。




***

# 參考資料
* [动画层编辑器(Animation Layer Editor)_ 2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-46091038-7F23-467C-8FEC-844A26C11EDA)
* [动画层_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-5C202CB8-EB3C-4ADE-B203-5F93A9FD9104)
* [设定动画层模式_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-1826C845-9FEF-4297-9575-A3A9D889C8B8)
* [动画层工具栏_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-DA89FA46-9528-40E6-A74D-E3707C213B08)








