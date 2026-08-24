---
title: Channel Box數值顏色
description: maya Channel Box數值顏色
pubDate: 2026/08/24
outline: 基礎
tags:
  - maya
  - 基礎
  - Channel Box
  - Animation
  - Rigging
---

# 用途
用於了解模型狀態。



# Channel Box 數值顏色
* 選物體 > `Ctrl + A (一次不夠就按兩次）` > 視窗右上角

Channel Box 有九種數值狀態（顏色將會依照螢幕色差、版本呈現不同顏色）：



## 紅色（Red）

**狀態**：已被設Key**動畫關鍵影格（Keyframe）**。


### 亮粉紅色 / 淺粉紅（Light Pink）
**狀態**：已編輯，但尚未設Key存檔的**動畫關鍵影格（Keyframe）** 。


### 暗粉紅色（Dark Pink）
**狀態**：此屬性在其他格有設key，但你當前時間軸踩的那一格（Frame）剛好沒有任何關鍵影格。


## 褐色(Brown)
**狀態**：此**動畫關鍵影格（Keyframe）** 被設為靜音(Muted)。

* 暫時靜音（關閉）數值效果，但數值保留。



## 藍色 / 藍綠色（Blue / Cyan）
**狀態**：受到**約束（Constraint）** 控制。


## 黃色（Yellow）
**狀態**：受到**直接連線（Connection）** 控制。

* 通常是透過節點編輯器（Node Editor）或連接編輯器（Connection Editor），將 A 物件的某個屬性直接牽線餵給 B 物件。


## 紫色 / 粉紅色（Purple / Magenta）
**狀態**：該屬性受到 **表達式（Expression）** 的控制。

- 它是被寫入的 Maya 數學程式碼或公式所驅動（例如：讓螺旋槳的旋轉數值等於時間乘以 10）。

> 因為算圖效能問題與保障動畫師做動作時的流暢體驗，
> 表達式（Expression）被 **Node Editor（節點編輯器）** 或 **驅動關鍵影格（Set Driven Key）** 取代。<br>
> 所以此顏色幾乎不會出現。



## 綠色（Green）

**狀態**：該屬性同時受到**多個多重來源**的控制，或處於**混合（Blend）狀態**。

* 最常見的狀況是：該物件同時被**多個物件約束（Constraints）**，或者同時有**動畫影格（Keyframe）和約束**在爭奪主導權，這時顏色會混色成綠色。



## 灰色（Gray）
**狀態**：該屬性已被**鎖定（Locked）**，無法使用。

- 選中該屬性點右鍵選擇了 "Lock Selected"。被鎖定後數值無法被任何方式修改、K 影格或約束，直到你點右鍵選擇 "Unlock Selected" 解鎖。




# 參考資料
* [Objects in Maya are locked in UI and Channel Box](https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Maya-Object-Locked-in-UI-and-Channel-Box.html)
* [Using Parallel Maya](https://download.autodesk.com/us/company/files/UsingParallelMaya/2020/UsingParallelMaya.html)
* [Maya Cached Playback](https://damassets.autodesk.net/content/dam/autodesk/www/html/maya-cached-playback/2023/MayaCachedPlaybackWhitePaper.html)







