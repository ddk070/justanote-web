---
title: " Add Attribute "
description: " maya Add Attribute "
pubDate: " 2026/08/26 "
outline: " Rigging "
tags:
  - maya
  - Rigging
  - Channel Box
---


# 用途
在物件（骨架、控制器、模型...）的Channel Box增加新屬性。

***

# Add Attribute
物件的Channel Box 的 `Edit`  >  `Add Attribute`

## New 標籤

- Long Name ： 屬性在maya裡的id名稱

> 請勿使用中文、空格，建議用底線 `_` 代替。

- Override nice name：是否顯示屬性綽號
- Nice Name：可用英文、數字、空格、底線、連字號、中文，避免用其他符號引起檔案出錯或遺失屬性
- Make attribute：1. Keyable（可記關鍵影格）2. Displayable（僅顯示 / 不可記影格）3. Hidden（隱藏）


### Data Type
新屬性的數值類型要用什麼呈現：
- Vector：**向量**，物件的xyz軸的呈現方式
- integer：**整數**，-1、0、2
- String：**字串 / 文字**，建議使用英文（此類型在Maya 2022改版無顯示）
- Float：**浮點數**，0.1、-20.7、1.3、1.0、20.0
- Boolean：**布林值**，On / Off 或  True / False 或 1 / 0
- Enum：自訂的**下拉式選單**，自行命名，無上限數量（但不建議做太多）



***

# 參考資料
* [attributeName](https://download.autodesk.com/us/maya/2010help/CommandsPython/attributeName.html)


