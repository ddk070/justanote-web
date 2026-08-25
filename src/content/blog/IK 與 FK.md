---
title: ' IK 與 FK '
description: ' maya IK 與 FK '
pubDate: ' 2026/08/25 '
outline: ' Rigging '
tags:
    - maya
    - Rigging
    - ik
    - fk
---


# 用途
兩種控制骨架的運動方式


***

# IK 與 FK

> 自行判斷要用在哪裡

## FK (Forward Kinematics, 順向動力學)
- 從上往下控制（上方會影響下方的位置）
- 末端位置匯被影響位置（腳掌、手掌）
- 四肢上有一圈一圈的控制器（手臂、腿）

例如：上手臂>手軸>手腕、大腿>膝蓋>小腿




## IK (Inverse Kinematics, 逆向動力學)
- 從末端控制（上方不會影響下方的位置）
- 末端位置是固定的（腳掌、手掌）
- 手腕或腳踝的小方塊/十字

例如：腳掌>膝蓋（調整）>root、手掌>手軸（調整）>上手臂



### RP Solver (Rotate-Plane Solver / 旋轉平面解算器)
- 提供 Pole Vector 向量約束
- 可控制手肘/膝蓋朝向

例如：手、腳


### SC Solver (Single-Chain Solver / 單鏈解算器)
- 沒有Pole Vector 向量約束（手肘控制球）
- 已固定關節走向，無法改變關節朝向

例如：腳趾、手指的自動抓握、腳後跟、腳趾抬起（用數值調整）


### Spline IK Solver (曲線 IK 解算器)
- 同時讓十幾根甚至幾十根骨頭一起平滑彎曲
- 有三種綁法

例如：脊椎、尾巴、觸手、繩索、長辮子、馬尾、披風邊......

#### 骨架控制法（Joints / Cluster + Controller）
- 用圓圈圈控制器（NURBS Controller）約束頭、中、尾這幾個大骨頭


#### 變形器控制法（Spline IK + Wave / Sine Deformer）
- 直接在那條 NURBS 曲線上面加上 Maya 的**非線性變形器（Non-linear Deformers）**，例如 **Wave（波浪）** 或 **Sine（正弦波）**。



#### 動態模擬法（Hair System / 變形為動態曲線）
- 把那條 NURBS 曲線轉換成 Maya 的 **Hair System（毛髮動力學曲線）**，讓它具備物理重力、風力與碰撞。



***


# IK / FK 切換與混合（Switch & Blend）

- Switch（切換）：0 或 1來開關，決定骨架要用 FK 還是 IK。

> 每個綁定師的習慣不同，所以自行看骨架0和1是FK 還是 IK。

- Blend（混合）：可在 0 到 1 之間的轉換（含 0.1～0.9）。

> 可以使用工具或腳本讓ik、fk之間切換順暢<br>
> 不會產生極度不自然的瞬間彈跳（Popping）


***

# 參考資料
* [IK 控制柄工具(IK Handle Tool)](https://help.autodesk.com/view/MAYACRE/CHS/?caas=caas/documentation/mayalt2014/zh-cn/files/CST-IK-Handle-Tool-htm.html)
* [IK 解算器](https://help.autodesk.com/view/MAYACRE/CHS/?caas=caas/documentation/mayalt2014/zh-cn/files/CSS-IK-solvers-htm.html)
* [Setting up the foot IK control](https://www.autodesk.com/learn/ondemand/curated/realtime-rigging-reverse-foot-systems/7qu98pHE31w7dhNe8TmNSX)