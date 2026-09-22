---
title: Cached Playback（缓存播放）
description: maya Cached Playback（缓存播放）
pubDate: 2026/09/22
outline: Animation
tags:
  - maya
  - Animation
---


# 用途
- 可直接在maya即時撥放動畫
- 儘可能「不需頻繁使用 Playblast」就能確認動畫


***

# Cached Playback
在背景將目前動畫預先計算，並儲存到記憶體(RAM)，等到需要觀看撥放時，再使用已儲存計算的動畫撥放。


## 使用注意
1. 動畫太長、場景太重：藍色條錄到一半卡住變灰色，代表你電腦記憶體（RAM）不夠塞了。
2. 跳黃字警告（Safe Mode）：場景裡有某些太古董或太複雜的外掛節點，錄影機不支援，功能會自動壞掉。


## 開啟
- 左鍵點擊 Maya 右下角`電影膠片撥放圖標`![Cached Playback](../..//assets/Cached Playback.jpg)
或是
- 在時間軸內`滑鼠右鍵` > `Cached Playback`

Cached Playback图标 顏色說明：
1. 藍色狀態 ： **已開啟** 
2. 灰色狀態 ： **已關閉** 
3. 黄色狀態 ： 觸發安全模式（Safe Mode）暫停運作

Time Slider 顏色說明：
1. 蓝色進度條：Maya 在背景「預先算好**角色動畫**」放入記憶體的進度
2. 粉紅色進度條：Maya 在背景「預先錄製衣服/毛髮等物理**特效**」的進度



## 設定FPS
1. 右下角`奔跑小黃人` > `Time Slider` 
2. `Playback speed` > `Real-time [24 fps]`
3. `Max playback speed` > `Real-time [24 fps]`


# Cached Playback模式
- 右鍵點擊 Maya 右下角`電影膠片撥放圖標`

1. Evaluation cache（預設）：相容性最高，速度會比下面兩種模式慢一點點
2. Viewport software cache：適合記憶體(RAM)超大
3. Viewport hardware cache：將數據存在GPU、VRAM裡，適合顯示卡記憶體超大






***

# 參考資料
* [缓存播放(Cached Playback_2022)](https://help.autodesk.com/view/MAYAUL/2022/CHS/?guid=GUID-C5EEF1E7-C24F-4BBC-8BB1-5036CA7D7D02)
* [选择缓存播放模式_2022](https://help.autodesk.com/view/MAYAUL/2022/CHS/?guid=GUID-D4E19F94-419A-4B3B-8121-883AEA127A1E)





