---
title: bootstrap scss 分類
date: 2022-03-26 18:22:01
tags:  
    - bootstrap5
    - css
    - furlove
---
使用 bootstrap 會有客製化樣式的時候

客製化 scss 可以獨立出來一個資料夾並且把它分類，越細越好，這樣在修改往回尋找會比較好找，基本會分成元件（components）及排版通用類別（utilities）
![Imgur](https://i.imgur.com/KHrhimf.png)

把一個元件寫好，之後如果需要用同樣的就可以直接加上。通用類別則是一個東西可能需要的功能

也可以用同樣的方式，在 all.scss 的地方把字型（font）導入，這樣就不用加在 head 上

另外如果要用全域字型，在 variable.scss 中找到 font-family-sans-serif 在把字型名稱加到最前面即可
![Imgur](https://i.imgur.com/k1iKegK.png)

---

還有文字外框的 css 叫做
-webkit-text-stroke: 5px black;

粗細 顏色

參考文章 [CSS：text-stroke 文字外框](https://ithelp.ithome.com.tw/articles/10192091)