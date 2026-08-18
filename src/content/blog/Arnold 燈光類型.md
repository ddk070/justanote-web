---
title: 'Arnold 燈光類型'
description: 'maya Arnold 燈光類型'
pubDate: '2026/08/18'
outline: 'Lighting'
tags:
    - maya
    - Lighting
    - Arnold
---


# 用途
為Arnold算圖引擎提供強大且逼真的燈光系統


# Arnold 燈光類型
總共七總燈光類型。<br>
最常用的燈光為Area Light、Sky Dome Light。


## Area Light（區域光）
是 Arnold 中最核心、最常使用的燈光。<br>
有三種樣式可以使用。
1. **Quad（四邊形）** ：預設燈光
2. **Disk（圓盤）** 
3. **Cylinder（圓柱體）**


## Sky Dome Light（天空穹頂光）
全局照明，可在屬性連結一張 **HDRI 高動態範圍貼圖**搭配使用。


## Mesh light（物件光）
將場景中的**任何自訂 3D 模型** 直接轉換成發光體。


## Photometric Light（光度學燈光）
透過讀取真實世界燈具廠商提供的 **IES 數據檔案**（包含光源強度、角度與衰減範圍）來發光的燈光。


## Directional Light（平行光 / 定向光）
模擬距離無限遠、光線完全平行的光源。<br>
與區域光差別為，區域光會受距離影響燈光強弱，但平行光不會。


## Point Light（點光源）
以點作為出發點的光源。可用於蠟燭火苗、小燈泡、炸彈爆炸瞬間的火球閃光。



## Spot Light（聚光燈）
從單一點發射出一個**圓錐形束狀**的方向性光源。



## Light Filters（燈光濾鏡）
為以上每個燈光屬性裡已內建的遮光器，類似於光的遮罩。<br>
有以下四種遮光可使用：
1. **aiGobo（圖案濾鏡）**：透過連結一張黑白貼圖，將光線「過濾」出花紋。常用於模擬陽光穿過樹葉的碎影、窗櫺的格子光，或舞台上的文字投影。圖案位置受燈光移動而改變位置。
2. **aiLightBlocker（擋光濾鏡）**：會在畫面中產生一個虛擬的方塊、球體或平面，任何穿過這個形狀的光線都會被「擋住」或變暗。可以用來人為製造陰影，或防止特定道具穿幫被照亮。圖案位置不受燈光移動而改變位置。
3. **aiBarndoors（穀倉門濾鏡）**：模擬真實攝影棚燈具的四片金屬擋板，可以單獨控制上下左右的邊界，精準切出一道門縫光或聚光束。
4. **aiDecay（衰減濾鏡）**：用來突破真實物理限制。你可以自由設定光線在距離多遠時才開始亮，或是到多遠的距離就突然完全熄滅。




# 參考資料
* [Lights - Arnold User Guide](https://help.autodesk.com/view/ARNOL/ENU/?guid=arnold_user_guide_ac_lights_html)
* [Arnold tutorial - Using the gobo light filter in MtoA](https://youtu.be/xYj_2TkSPfE?si=AmvPyXP164sgNydL)
* [Arnold tutorial - Using the light_blocker in MtoA ](https://youtu.be/2jO_-mSJnWA?si=LbQsw5xWgn5IkZ_T)
* [Arnold tutorial - Using the barndoor light filter in MtoA](https://youtu.be/NTJ3nmVS2V0?si=rg0XmlK_idOB7lo-)
* [Arnold Light Decay Explained | Realistic Lighting Falloff Guide](https://youtu.be/JyiUXB5fTpQ?si=u_3EVgZWEFODWf26)
