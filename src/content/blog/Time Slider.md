---
title: 'Time Slider（時間滑塊）'
description: 'maya Time Slider（時間滑塊）'
pubDate: '2026/09/24'
outline: 'Animation'
tags:
  - maya
  - Animation
---


# 用途
1. 設key
2. 反覆撥放查看動畫
3. 紀錄動畫長度的時間軸
4. 可用書籤作記號



***

# Time Slider

- `Display` > `UI Elements` > `Time Slider` 和 `Range Slider`

重設工作區（兩個方法）：
1. `Windows` > `Workspaces` > `Reset "Workspace" to Factory Default`
2.  界面右上角 `Workspaces`下拉選單 > `Reset Current Workspace`

> Time Slider是界面預設，就在視窗下方的時間軸 <br>
> maya2023（舊版）與maya2024（新版）的版面有些許不同

# Bookmarks 書籤
- **Maya 2020** 版本之後新增

## 新增書籤
1. 選取書籤範圍：`Shift` + `滑鼠左鍵拖曳` 
2. 新增書籤： `Alt `+ `T` 、 點擊 `橘色书签(Bookmark)图标`
3. 命名後按確認

## 移動書籤範圍
- 按住 `ctrl` + 拖動 `前面`或`後面` 進行縮放

## 快速新增書籤
- `Alt` + `Shift` + `T`
- 建立一個沒有名稱的書籤,並指定隨機色彩
- 右鍵書籤可設置書籤設定


# 快捷鍵
> 下文取自[animation快捷鍵](/blog/animation-快捷鍵/)

## 播放控制
**播放 / 暫停：** `Alt` + `V` <br>
**暫停：**`Esc` <br>
**前進 / 後退一格：** `Alt` + `<`和 `Alt` + `>` <br>
**移至上一個關鍵幀：** `<` <br>
**移至下一個關鍵幀：** `>` <br>
**跳至動畫最末格：** `Alt` + `Shift` + `<` <br>
**跳至動畫最前格：** `Alt` + `Shift` + `>` <br>

<hr>


## 設Key

**設定關鍵影格（所有屬性）：**  `S` <br>
**僅設定平移（Translate）：** `Shift` + `W` <br>
**僅設定旋轉（Rotate）：** `Shift` + `E` <br>
**僅設定縮放（Scale）：** `Shift` + `R` <br>
**在目前影格設定平移（Translate）：** `Ctrl-Shift` + `W` <br>
**在目前影格設定旋轉（Rotate）：**`Ctrl-Shift` + `E` <br>
**在目前影格設定縮放（Scale）：** `Ctrl-Shift` + `R` <br>

<hr>

## 時間軸（Timeline）
**藍色/紅色選取區**：按住 `Shift` 鍵並在時間軸上**按住滑鼠左鍵拖曳**，可以選取一段特定的時間範圍（會變成**藍色/紅色區塊**） <br>
**集體移動**：選取藍色區塊後，點擊區塊中間的**雙向箭頭**，就能把這整段動畫影格一起往左或往右移動 <br>
**等比例縮放**：點擊藍色區塊兩端的**外側箭頭**拖曳，可以將這段動作集體「放慢（拉長影格）」或「加快（壓縮影格）」 <br>
**移動單一/多個關鍵影格：** 按住 `Shift` 鍵並點選關鍵幀，接著按滑鼠左鍵或中鍵拖曳 <br>
**在時間軸上快速搓動（Scrub）：** 按住 `K` 鍵 + 滑鼠中鍵並左右拖曳（無需將游標移至時間軸） <br>
**複製key：** 中鍵按住要複製的key不放，拖曳到要貼上的地方放開，按`S`





***



# 參考資料
## maya2023
* [时间滑块(Time Slider)_ 2023](https://help.autodesk.com/view/MAYAUL/2023/CHS/?guid=GUID-827ED8CD-C6AA-4495-8B5E-2FC98C8D49EE)
* [Time Slider Bookmarks_2023](https://help.autodesk.com/view/MAYAUL/2023/ENU/?guid=GUID-E15891DF-BC48-43B4-BD03-08918CD4D0C0)
* [时间滑块书签管理器_2023](https://help.autodesk.com/view/MAYAUL/2023/CHS/?guid=GUID-7E26C8C9-6F27-4A56-8119-DC4A75DAC265)
* [播放选项(Playback Options)_ 2023](https://help.autodesk.com/view/MAYAUL/2023/CHS/?guid=GUID-9853B7B5-8AD5-46F6-A921-A3771A505AD1)
* [播放控件(Playback Controls)_ 2023](https://help.autodesk.com/view/MAYAUL/2023/CHS/?guid=GUID-277ADCBF-6277-4B32-81E0-AEB6D081153F)
* [“动画控件”(Animation controls)菜单_2023](https://help.autodesk.com/view/MAYAUL/2023/CHS/?guid=GUID-4A45C257-9E4D-4C63-A181-B2F94EA0C8B4)

## maya2024
* [时间滑块(Time Slider)_ 2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-827ED8CD-C6AA-4495-8B5E-2FC98C8D49EE)
* [Time Slider Bookmarks_2024](https://help.autodesk.com/view/MAYAUL/2024/ENU/?guid=GUID-E15891DF-BC48-43B4-BD03-08918CD4D0C0)
* [时间滑块书签管理器_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-7E26C8C9-6F27-4A56-8119-DC4A75DAC265)
* [播放选项(Playback Options)_ 2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-9853B7B5-8AD5-46F6-A921-A3771A505AD1)
* [播放控件(Playback Controls)_ 2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-277ADCBF-6277-4B32-81E0-AEB6D081153F)
* [“动画控件”(Animation controls)菜单_2024](https://help.autodesk.com/view/MAYAUL/2024/CHS/?guid=GUID-4A45C257-9E4D-4C63-A181-B2F94EA0C8B4)









