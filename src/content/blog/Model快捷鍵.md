---
title: 'Model快捷鍵'
description: 'maya Model模型快捷鍵'
pubDate: '2026/7/10'
outline: 'Model'
tags:
  - maya
  - 快捷鍵
  - Model
---

# 頂部功能選單(Modeling) 
**切換至 建模 (Modeling) 選單集：** `F2` <br>


***

# 滑鼠預設視窗
**切換模式：** `右鍵 (長按)模型` <br>
**模型選單：**`Shift` + `滑鼠右鍵 (長按)` <br>


***

# 模型操作

## 切換物件模式（滑鼠）
**切換 物件模式 / 組件模式 (Object / Component)：** `F8` <br>


## 獨立顯示
**獨立顯示 (Isolate Select)：** `Ctrl` + `1` <br>
**獨立顯示 (Isolate Select)：**`Shift` + `I` <br>
**反向獨立顯示：** `Ctrl + Shift` + `I` <br>
**隱藏選取物件（Hide）：** `H` <br>
**顯示上一次被隱藏的物件：** `Ctrl` + `Shift` + `H` <br>




## 點線面操作

### 模式切換（滑鼠）
**切換到 頂點模式 (Vertex)：** `F9` <br>
**切換到 邊模式 (Edge)：**`F10` <br>
**切換到 面模式 (Face)：** `F11` <br>


### 筆刷式選取
**筆刷式選取點線面 (Paint Selection Mode)：** `Tab` + `滑鼠左鍵拖曳` <br>
**筆刷式取消選取點線面：**`Tab` + `滑鼠左鍵拖曳（在已選取組件上` <br>



### 選取點線面
**選取該方向的整條：** `點選第一個，按住 Shift 在隔壁相鄰的點雙擊左鍵` <br>
**選一圈：**`雙擊左鍵` <br>
**擴大選取（Grow Selection）**：`Shift` + `.`（即大於號 `>`）<br>
**縮小選取（Shrink Selection）**：`Shift` + `,`（即小於號 `<`）<br>



### 移動線
**切換為沿線/沿面滑動模式 (Slide Edge / Slide Vertex)：** `移動工具 (W)` +` Shift` + `Ctrl (長按)` <br>



### 移動頂點
**移動頂點：** `方向鍵 (↑ / ↓ / ← / →)` <br>

 
### 轉換成點線面
**點 (Vertices)：**`F9` <br>
**線 (Edges)：** `F10` <br>
**面 (Faces)：** `F11` <br>


 
### 徹底清除點線
**徹底刪除選取的邊線並清除殘留頂點**：** `Ctrl` + `Delete` <br>


## 切割工具
**多功能切割工具（Multi-Cut Tool）：**`Ctrl` + `Shift` + `X` <br>
**預覽/放置循環線 (Edge Loop)：** `Ctrl` <br>
**在正中央（50% 處）精準插入循環線：** `Ctrl` +` 滑鼠中鍵` <br>
**沿著邊線進行百分比吸附切線（預設每 10% 一格）：** `Shift` <br>
**啟用/關閉切割工具視窗 (Multi-Cut Tool)：** `Alt` + `c` <br>
**穿透切割 (Slice Plane)：** `滑鼠左鍵拖曳（在模型外圍空白處）` <br>
**結束當前切線，直接開始新的一刀：** `滑鼠右鍵` <br>



## 模型變形
**擠出 (Extrude)：** `Ctrl` + `E` <br>
**倒角 (Bevel)：**`Ctrl` + `B` <br>
**重複上一次建模操作（極適用於連續擠出或倒角）：** `G` <br>

 

## 軟選取
**軟選取 (Soft Selection)：** `B` <br>
**調整軟選取半徑：**`B` + `滑鼠左鍵拖曳` <br>



## 物體軸向
 **D / Insert**：進入/退出編輯軸向模式 (Edit Pivot)。<br>
 **D + 滑鼠左鍵點擊組件**：將軸向對齊至該點的法線 (Normal) 或線的走向。<br>
 **D + V (長按)** / **D + C (長按)**：將軸向精準吸附至目標頂點/邊線。<br>
 **W / E / R + 滑鼠左鍵 (長按)**：彈出座標系標記選單（快速切換 Object, World, Component, Normal, Parent）。<br>
 **Ctrl + 滑鼠中鍵拖曳軸向控制桿**：鎖定該軸向，在與其垂直的平面上進行二維平移。<br>
 **Shift + 滑鼠中鍵在空白處拖曳**：沿著目前選定的**軸向**（反白顯示的軸）進行複製或擠出。<br>
 **J (長按)**：啟用步進式變形 (Discrete Transform)，依設定的角度（如 15°）或距離跳格。<br>
 **中鍵拖曳（無選取軸向）**：<br>
   **W 狀態下**：沿著當前視角平面移動。<br>
   **E 狀態下**：沿著視鏡頭垂直軸旋轉（Tumble 旋轉）。


## 吸附功能
> *註：皆為長按啟用，放開關閉*

 **X**：吸附到網格 (Snap to Grid)。<br>
 **C**：吸附到曲線/邊緣 (Snap to Curve)。<br>
 **V**：吸附到頂點/樞紐點 (Snap to Point)。<br>
 **滑鼠中鍵拖曳（啟用吸附時）**：直接將物件扣定到最接近鼠標的目標點/線/網格上。<br>

***

# UV 編輯器 ( UV Editor )
請在 UV 編輯器視窗使用：<br>

## UV快捷鍵視窗
**F12**：切換到 UV 模式
 **滑鼠右鍵 (長按)**：切換選取模式（UV、UV Shell、Edge、Face、Vertex）。<br>
 **Shift + 滑鼠右鍵 (長按)**：展開 UV 工具快顯選單（包含 Unfold、Layout、Cut、Sew）。<br>
 
## 點線面編輯
**W / E / R**：與主視窗相同的移動、旋轉、縮放。<br>
 **Shift + X**：剪開 UV 線 (Cut UVs)。<br>
 **Shift + S**：縫合 UV 線 (Sew UVs)。<br>
 **Ctrl + U**：執行**自動展開 (Unfold UVs)**。<br>
 **Ctrl + L**：執行**UV 排版排滿 (Layout UVs)**。<br>
 **Tab + 滑鼠左鍵拖曳**：在 UV 視窗中同樣適用的筆刷選取。<br>
 **雙擊 UV 點**：選取整個 UV 殼 (UV Shell)。<br>

***

# 拓撲
 **滑鼠左鍵點擊**：放置綠色控制點。<br>
 **Shift + 滑鼠左鍵（在四點中點擊）**：生成四邊面 (Quad Face)。<br>
 **Tab + 滑鼠左鍵拖曳（在邊緣上）**：延伸單一邊緣 (Extend Edge)。<br>
 **Tab + 滑鼠中鍵拖曳**：延伸整條邊緣迴路 (Extend Edge Loop)。<br>
 **Ctrl + 滑鼠左鍵**：直接插入循環線。<br>
 **Ctrl + Shift + 滑鼠左鍵**：刪除控制點、線或面。<br>
 **Shift + 滑鼠左鍵拖曳**：放鬆網格布線 (Relax)。<br>
 **M + 滑鼠左鍵拖曳**：拖曳點以進行吸附焊接 (Merge Point)。<br>
 **Tab + 滑鼠左鍵點擊並沿邊線拖曳**：快速沿著拓撲路徑進行延伸選取。<br>
 **點擊 A 點 \rightarrow Shift + 雙擊 B 點**：自動選取兩點之間最短拓撲路徑 (Shortest Edge Path)。<br>

