---
title: 'playblast設定與輸出'
description: 'maya playblast設定與輸出'
pubDate: '2026/09/18'
outline: 'Animation'
tags:
  - maya
  - Animation
---


# 用途
快速錄製視口（Viewport）動畫並輸出成影片的功能，用於檢視影片動畫。

> 建議可以搭配[DuBlast](/blog/dublast/)外掛使用

***

# playblast設定
- `Window` > `Playblast` > `點擊右側的「方形圖示」 (□)`
- 對時間軸開頭`右鍵` > `Playblast ▢`
- `Animation` > `Playback` > `Playblast`


## 設定格式與解析度
- **format**：選擇儲存格式，首選QT或avi
- **Encoding**：選擇 H.264或video
- **Quality**：將影片解析度品質拉到100


## 尺寸大小與比例
- **Display Size**：
	- Custom：尺寸自訂，寬度1920、高度1080（可靠）
	- From Render Settings：根據Render Settings設定尺寸，有設定Render Settings尺寸就可用
	- From Window：直接抓取你目前 Maya 工作視窗的大小（最不推薦）
- **Scale**：畫面比例拉到1.00，輸出時就不會自動幫你縮小尺寸
- **Frame padding**：影格編號的位數，輸出圖片序列用，建議使用4



## 輸出位置
- 開啟 **Save to flie**
- **Movie flie**：點資料夾圖示，選擇影片輸出位置




***

# 參考資料
* [Playblast an animation_maya2022](https://help.autodesk.com/view/MAYAUL/2022/ENU/?guid=GUID-1C6EDC8D-DA67-490E-81F1-1205336DEBD9)
* [Playblast Options_maya2022](https://help.autodesk.com/view/MAYAUL/2022/ENU/?guid=GUID-2D865271-2873-4EDB-82C4-7FB9D7B311E7)









