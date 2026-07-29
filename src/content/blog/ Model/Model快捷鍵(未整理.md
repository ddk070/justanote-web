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

# 變形操縱桿與座標軸極控制
 * **D / Insert**：進入/退出編輯樞紐點模式 (Edit Pivot)。
 * **D + 滑鼠左鍵點擊組件**：將樞紐點對齊至該點的法線 (Normal) 或線的走向。
 * **D + V (長按)** / **D + C (長按)**：將樞紐點精準吸附至目標頂點/邊線。
 * **W / E / R + 滑鼠左鍵 (長按)**：彈出座標系標記選單（快速切換 Object, World, Component, Normal, Parent）。
 * **Ctrl + 滑鼠中鍵拖曳軸向控制桿**：鎖定該軸向，在與其垂直的平面上進行二維平移。
 * **Shift + 滑鼠中鍵在空白處拖曳**：沿著目前選定的**軸向**（反白顯示的軸）進行複製或擠出。
 * **J (長按)**：啟用步進式變形 (Discrete Transform)，依設定的角度（如 15°）或距離跳格。
 * **中鍵拖曳（無選取軸向）**：
   * **W 狀態下**：沿著當前視角平面移動。
   * **E 狀態下**：沿著視鏡頭垂直軸旋轉（Tumble 旋轉）。

# 2. 骨灰級選取與組件調校 (Advanced Selection & Layout)
 * **Tab + 滑鼠左鍵拖曳**：筆刷式選取 (Paint Selection Mode)。
 * **Tab + 滑鼠左鍵拖曳（在已選取組件上）**：筆刷式**取消選取**。
 * **Tab + 滑鼠左鍵點擊並沿邊線拖曳**：快速沿著拓撲路徑進行延伸選取。
 * **選取面 \rightarrow Ctrl + 滑鼠右鍵 \rightarrow To Edges \rightarrow To Edge Perimeter**：將選取的面快速轉換為其**外圍邊緣**。
 * **點擊 A 點 \rightarrow Shift + 雙擊 B 點**：自動選取兩點之間最短拓撲路徑 (Shortest Edge Path)。
 * **選取面 \rightarrow 雙擊相鄰面**：選取該方向的整條面迴路 (Face Loop)。
 * **Shift + >** / **Shift + <**：擴大 / 縮小選取範圍 (Grow / Shrink Selection)。
 * **Ctrl + 1**：隔離顯示切換 (Isolate Select)。
 * **B**：切換軟選取 (Soft Selection)。
 * **B + 滑鼠左鍵拖曳**：調整軟選取影響半徑。
 * **縮放工具 (R) + 雙擊組件圖示**：在 Tool Settings 中將選取元素的軸向打平（拉至 0）。

# 3. 全指令建模工具箱 (Modeling Toolkit & Commands)
 * **Ctrl + E**：擠出 (Extrude)。
 * **Shift + 滑鼠右鍵 (長按)**：動態上下文選單（核心：Bevel Edge、Bridge、Merge Vertices、Collapse、Target Weld）。
 * **G**：重複上一次建模操作（極適用於連續擠出或倒角）。
 * **Alt + c``**：啟用/關閉多功能切刀 (Multi-Cut Tool)。
 * **Shift + I``**：將新選取物件加進已隔離顯示的視窗中。

## 🛠️ Multi-Cut (切刀) 隱藏組合鍵
 * **Ctrl**：預覽/放置循環線 (Edge Loop)。
 * **Ctrl + 滑鼠中鍵**：在正中央（50% 處）精準插入循環線。
 * **Shift**：沿著邊線進行百分比吸附切線（預設每 10% 一格）。
 * **滑鼠左鍵拖曳（在模型外圍空白處）**：穿透切割 (Slice Plane)。
 * **滑鼠右鍵**：結束當前切線，直接開始新的一刀。

## 🛠️ Quad Draw (拓撲) 隱藏組合鍵
 * **滑鼠左鍵點擊**：放置綠色控制點。
 * **Shift + 滑鼠左鍵（在四點中點擊）**：生成四邊面 (Quad Face)。
 * **Tab + 滑鼠左鍵拖曳（在邊緣上）**：延伸單一邊緣 (Extend Edge)。
 * **Tab + 滑鼠中鍵拖曳**：延伸整條邊緣迴路 (Extend Edge Loop)。
 * **Ctrl + 滑鼠左鍵**：直接插入循環線。
 * **Ctrl + Shift + 滑鼠左鍵**：刪除控制點、線或面。
 * **Shift + 滑鼠左鍵拖曳**：放鬆網格布線 (Relax)。
 * **M + 滑鼠左鍵拖曳**：拖曳點以進行吸附焊接 (Merge Point)。

# 4. 頂點與邊線微調 (Vertex & Edge Tweaking)
 * **移動工具 (W) + Shift + Ctrl (長按)**：切換為**沿線/沿面滑動模式 (Slide Edge / Slide Vertex)**。
 * **Alt + 方向鍵 (↑ / ↓ / ← / →)**：以微小像素為單位精準微調 (Nudge) 選中的頂點。
 * **Ctrl + F9**：將目前的選取轉換為頂點 (To Vertices)。
 * **Ctrl + F10**：將目前的選取轉換為邊線 (To Edges)。
 * **Ctrl + F11**：將目前的選取轉換為面 (To Faces)。
 * **Ctrl + Delete**：徹底刪除選取的邊線**並清除殘留頂點**（建模必備，勿只按 Delete）。

# 5. 吸附系統 (Snapping System)
> *註：皆為長按啟用，放開關閉*
> 
 * **X**：吸附到網格 (Snap to Grid)。
 * **C**：吸附到曲線/邊緣 (Snap to Curve)。
 * **V**：吸附到頂點/樞紐點 (Snap to Point)。
 * **滑鼠中鍵拖曳（啟用吸附時）**：直接將物件扣定到最接近鼠標的目標點/線/網格上。

# 6. UV 編輯器核心快捷鍵 (UV Editor Pro)
在 UV 編輯器視窗激活狀態下：
 * **W / E / R**：與主視窗相同的移動、旋轉、縮放。
 * **滑鼠右鍵 (長按)**：切換選取模式（UV、UV Shell、Edge、Face、Vertex）。
 * **Shift + 滑鼠右鍵 (長按)**：展開 UV 工具快顯選單（包含 Unfold、Layout、Cut、Sew）。
 * **Shift + X**：剪開 UV 線 (Cut UVs)。
 * **Shift + S**：縫合 UV 線 (Sew UVs)。
 * **Ctrl + U**：執行**自動展開 (Unfold UVs)**。
 * **Ctrl + L**：執行**UV 排版排滿 (Layout UVs)**。
 * **Tab + 滑鼠左鍵拖曳**：在 UV 視窗中同樣適用的筆刷選取。
 * **雙擊 UV 點**：選取整個 UV 殼 (UV Shell)。
