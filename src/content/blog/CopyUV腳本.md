---
title: 'CopyUV腳本'
description: 'CopyUV腳本'
pubDate: '2026/7/6'

tags:
    - maya
    - CopyUV
    - 腳本推薦
    - mel
---



# 使用方法
* 只要貼在script Editor做成按鈕就能用了(全選後按圖中的按鈕
* 先選 UV 好的模型, 然後再選一個或多個要貼上UV的模型.


<hr><br>

## Mel腳本
[參考連結](https://maya-tricks.blogspot.com/2010/05/uv-copy-polygon-uv.html?m=1)


```
{
string $allObj[] =`ls -sl`;
string $source[];
$source[0] = $allObj[0];
string $target[] = stringArrayRemove($source,$allObj);

for($each in $target)
{
    if(`polyCompare -fd $each $source[0]`==4 || `polyCompare -fd $each $source[0]`==12)
    {
        polyNormal -normalMode 0 -userNormalMode 0 -ch 1 $each;
        polyTransfer -v 0 -vc 0 -uv 1 -ao $source[0] $each;
        polyNormal -normalMode 0 -userNormalMode 0 -ch 1 $each;

    }
    else if(`polyCompare -fd $each $source[0]`==0 || `polyCompare -fd $each $source[0]`==8)
    {
        polyTransfer -v 0 -vc 0 -uv 1 -ao $source[0] $each;
    }

}
}
```


