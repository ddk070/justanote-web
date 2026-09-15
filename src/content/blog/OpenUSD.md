---
title: 'OpenUSD'
description: 'maya OpenUSD（Universal Scene Description）'
pubDate: '2026/09/14'
outline: '基礎'
tags:
  - maya
  - 基礎
  - 檔案格式
---


# 用途
- 3D 軟體之間的共通語言
- 用於跨軟體協作、承載超大型場景的檔案格式（Overriding & Referencing 技術）
- 負責組合所有（模型、動畫、特效......）為一個檔案（用連結（Referencing）與疊層（Layering））

> 支援maya2022 或更新的版本

***

# USD（Universal Scene Description）
- `Windows` > `Settings/Preferences` > `Plug-in Manager`
- `mayaUsdPlugin.mll` 勾選  `Loaded`（載入）與 `Auto Load`（每次開軟體自動載入）


## .usda（ASCII 文本檔）
- 可用程式碼修改 3D 場景
- 負責紀錄物件的位置、旋轉、材質路徑


## .usdc（Crate 二進位檔）
- 被電腦高度壓縮過的二進位檔案
- 3D 軟體讀取速度極快
- 專門用來處理幾百萬面數的超級大模型


## .usd（通用格式）
- 可用程式碼修改 3D 場景
- 3D 軟體讀取速度極快
- 3D 軟體之間的共通語言

***

# 關於匯出前的注意事項

## 模型與幾何體（Modeling）
- 清除歷史紀錄（Delete History）
- 凍結變更（Freeze Transformations）
- 檢查面法線（Mesh Normals）
- 命名空間（Naming / Hierarchy）

## 骨架與綁定（Rigging）
- 不能直接帶走「控制器（Rig Controls）」
- 必須建立 SkelRoot（USD 專用骨架根節點）


## 動畫（Animation）
- 勾選「Animation」
- 確認 Time Range（開始與結束格數）是否正確
- 決定是否要「烘焙（Bake）」
- 如果有使用到非標準的變形器（如：Blend Shape 表情、肌肉擠壓、布料模擬），請在匯出設定中開啟 「Bake Topology」 或 「Bake Deformers」，將它強行轉為每一格的頂點動畫（Point Cache）


## 材質與貼圖（LookDev / Shading）
- 不要使用 Maya 原生舊材質（如 Blinn, Lambert）
- 使用 PBR 國際標準材質（Preview Surface）
- 貼圖路徑改為「相對路徑」


## 匯出視窗的「關鍵勾選」
- `File` > `Export All` > `USD Export`
- Plug-in Configuration：確保選對你的目標軟體環境（例如：如果是要給 Unreal，可以勾選對應的預設集）。
- Geometry：如果要保持精準的四邊面，記得確認 Mesh Subdivisions 的設定，避免模型被強行平滑化（Smooth）導致形狀變形。



> 2016 年（誕生）：最初由皮克斯動畫工作室（Pixar）自主研發，並於 2016 年正式將技術開源（開放給全球免費使用） [Pixar OpenUSD]。<br>
> 2023 年（轉折）：皮克斯聯合了 Apple、NVIDIA、微軟、Adobe、Autodesk 等科技巨頭，共同成立了 AOUSD（OpenUSD 聯盟），將其推向全科技業的最高標準。<br>
> 是現代主流 3D 軟體（Maya、Houdini、Blender、Unreal Engine）之間，交換複雜資料的最高工業標準。


***

# 參考資料
* [為 Maya 安裝 USD_maya2026](https://help.autodesk.com/view/MAYAUL/2026/CHS/?guid=GUID-8FB49D7F-8651-47CE-80FC-5C940E568C97)
* [maya-usd_github](https://github.com/autodesk/maya-usd)



