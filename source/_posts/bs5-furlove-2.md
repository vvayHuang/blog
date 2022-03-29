---
title: offcanvas、fixed-bottom、css 畫出對話框
date: 2022-03-27 22:19:12
tags: 
    - bootstrap
    - css
---
bs5 預設導覽列漢堡選單點擊後的效果預設是導覽列從上往下推，在官方文件中有另一種效果，就是[offcanvas](https://bootstrap5.hexschool.com/docs/5.1/components/navbar/#offcanvas) 

![Imgur](https://i.imgur.com/2ZrkRk4.png)

要修改樣式可以在 offcanvas 或 offcanvas-end 裡面調整

效果是用**transformX**

更多效果可參考官方文件 [transform](https://developer.mozilla.org/zh-TW/docs/Web/CSS/transform)

---
如果有像是需要把圖固定在畫面上的效果，可以用 fixed-bottom,fixed-top

![Imgur](https://i.imgur.com/MN4913Y.gif)

這個區塊因為不受畫面控制，html 可以寫在 body 最前面或任何地方

---

用 css 偽元素 畫出tooltips 對話框

    .dialog-border-bottom {
    border: 5px solid #888888;
    height: 65px;
    margin-bottom: 10px;
    position: relative;
    width: 80px;
    }
    .dialog-border-bottom:before {
    border-color: #888888 transparent transparent; 
    border-style: solid solid solid; 
    border-width: 20px 20px 20px 20px; 
    bottom: -40px;
 
    /* 必須指定，才能顯示內容 */
    content: "";
 
    height: 0px;
 
    /* 必須指定，否則會變梯形 */
    position: absolute;
        left: 17px; 
 
    width: 0px;
    }
    .dialog-border-bottom:after {
    border-color: #fff transparent transparent; 
    border-style: solid solid solid solid; 
    border-width: 20px; 
 
    /* 必須指定，才能顯示內容 */
    content: "";
 
    height: 0px;
 
    /* 必須指定，否則會變梯形 */
    position: absolute;
        left: 17px;
        bottom: -33px;

    width: 0px;
    }

參考文章 
[使用 CSS border 製作梯形、三角形、對話框](https://www.footmark.com.tw/news/web-design/css/css-border-create-triangle/)
[CSS: 偽元素應用- tooltip對話框](https://ithelp.ithome.com.tw/articles/10200537)

bootstrap 也有 [tooltips](https://bootstrap5.hexschool.com/docs/5.1/components/tooltips/) ，但是可以編輯範圍有限