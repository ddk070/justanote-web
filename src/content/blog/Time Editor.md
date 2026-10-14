---
title: 'Time Editor'
description: 'maya Time Editor'
pubDate: '2026/10/14'
outline: 'Animation'
tags:
      - maya
      - Animation 
  
---


# 用途
- 仿影片編輯器
- 管理、創建、編輯、混和動畫片段

> Time Editor於2017新增，用於取代Trax Editor。<br>
> 比Trax Editor有更完善的剪輯功能與界面。<br>
> 不能與Trax Editor混用，彼此物件不相容。（角色集、動畫片段）


***

# Time Editor
兩種開啟方法：
1. `Windows` > `Animation Editors` > `Time Editor`
2. `Panels` > `Panel` > `Time Editor`


## 編輯器視窗移動
- 平移： `alt` + `中鍵`
- 縮放： `alt` + `右鍵`


## 調整撥放範圍
- `左鍵`移動暗區域的邊界


## 顯示片段
**全部顯示：** `A` <br>
**顯示當前：** `F` <br>
**顯示撥放範圍：** `G`

> [工具列圖示說明_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-6137119F-CEDF-4998-BF76-C946722C9EE8)

## 時間指示器
兩種移動方法：
1. 左鍵黃色頂部左右拖移
2. 按`K`，即可在中間拖移指示器

> （黃色那根負責顯示當前影格的東西）


# 編輯動畫片段

## 新增
第一種方法：
- 選取 動畫角色的**群組**
- 點擊`+`（新增來自場景中選取的動畫）

第二種方法：
- `File` > `Add animation from scene selection`

## 分割
1. 移動 時間標記到想分割的地方（黃色的時間指示器）
2. `Edit` > `Split clip at current frame`（`W`或是 `1`）

> 使用保持或循環後，需群組才能分割。

**剪去前方(Trim Before)：** `G` <br>
**剪去后方(Trim After)：** `H` <br>


## 複製
1. 選擇片段
2. `Ctrl` + `C`
3. `Ctrl` + `V`


## 群組片段
1. `shift` 加選片段
2. `Ctrl` + `G`

> 解開群組：`Ctrl`+`Shift`+`G`<br>
> 群組後可以打開群組查看片段


## 其他功能

動畫片段編輯：<br>
**修剪(Trim)：** `E` <br>
**縮放(Scale)：** `R` <br>
**循環(Loop)：** `T` <br>
**保持(Hold)：** `Y` <br>
**切換漣漪(Toggle Ripple)：** `U`

> 選取片段後，按住快捷鍵，拖移片段前/後方。 <br>
> Toggle Ripple功用：拖動中間片段，後方片段也能一起移動。


關鍵幀：
**顯示關鍵幀：** `V` <br>

> 或點擊片段最左邊灰色的方框 開啟顯示



# 過渡片段
將上一個片段平滑接上到下一個片段，而不是下段開頭突然抖動。<br>
無縫撥放，創造更多混和效果。

1. 將片段放在同一個軌道上
2. 給與一個空白空間
3. 選起來後，對片段`右鍵`> `Create Transition`

> [片段右鍵菜單](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-AD0AC3AC-EA7C-4B0F-A80E-53DD62ED628D)


## 重疊片段 (crossfade)
`左鍵`拖移到另一個片段，重疊在一起。




# 新增音頻
- `File` > `Import Audio Clip`

時間編輯器支援以下音檔格式：<br>
 .wav<br>
  .aiff

> maya不支援MP3格式。<br>
> 撥放速度只能使用Real-time，請至Time Slider 右鍵 > Playback Speed > Real-time調整。<br>


# 烘焙
合併同條軌道中的每個片段，將關鍵幀保持簡潔：
- `右鍵` > `BAKE` > `Bake to New Clip/Bake to New Clip and Delete`

將剪輯成果的動畫片段，烘焙到場景物件上，並刪除原始動畫（也刪除在時間編輯器的片段）：
- `右鍵` > `BAKE` > `Bake To Scene and Delete`

合併片段圖層，將關鍵幀保持簡潔：
- `右鍵` > `BAKE` > `Flatten Layers`

# 匯出片段
- 對片段`右鍵`> `Export Selected`（匯出選定的物件）

官方支援匯出的格式：
- FBX
- Maya .ma
- Maya .mb

> 匯出物件為Time Editor片段內容節點，而非動畫關鍵幀或角色物件。

***

# 參考資料
* [时间编辑器_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-E4B5DB7D-7351-4561-BD8B-60AC9D48DDF6)
* [在时间编辑器中编辑动画_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-86B70295-2A93-458C-9D3E-F153EB048E5B)
* [创建时间编辑器片段之间的过渡_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-8AAE8C17-C5C7-4EC0-9748-10B2105501FC)
* [将音频添加到时间编辑器_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-B92021F8-E73A-4989-B26F-6E3A0883E876)
* [时间编辑器“片段”(Clip)上下文菜单_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-AD0AC3AC-EA7C-4B0F-A80E-53DD62ED628D)
* [时间编辑器工具栏_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-6137119F-CEDF-4998-BF76-C946722C9EE8)
* [时间编辑器的导出当前选择(Export Selction)选项_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-E82AD7B5-8E88-4DB9-A8F5-1C9CEBEAA598)
* [导出时间编辑器片段_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-C62227B0-09D6-4C93-962E-B71EA06C2052)
* [将时间编辑器片段导出到游戏导出器_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-9C4E33D5-8C60-4715-98AC-A3FEBFFF1805)







