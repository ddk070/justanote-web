---
title: '檔案類型'
description: 'maya檔案格式類型'
pubDate: '2026/7/15'
outline: '基礎'
tags:
  - maya
  - 基礎
  - 檔案格式
---

> # maya原生檔

## Maya ASCII  (.ma)

- 檔案比mb大
- 讀取速度慢
- 有文字編輯器（可修復檔案）


## Maya Binary(.mb)

- 檔案比ma小
- 讀取速度快
- 無文字編輯器（無法修復檔案）


***


> # 模型

## FBX (.fbx)

- 包含模型以及其他資訊（材質、紋理、rig、animation、攝影機、燈光)


## OBJ (.obj)

- 只有模型資訊（純粹的模型檔）


***


> # Animation 

## Anim Export/Import (.anim)

- Animation動作檔（無角色模型）
- 僅基礎關鍵影格
- 不支援動畫圖層(Anim Layers)
- 角色骨架與控制器命名、層級，必須完全一致


## Animation Transfer(.atom)

- Animation動作檔（無角色模型）
- 包含基礎關鍵影格及其他更複雜的骨架資訊（支援Driven Keys、Constraints、blend shape...）
- 支援動畫圖層（Anim Layers)
- 命名與層級可用“搜尋與取代”更改名稱
