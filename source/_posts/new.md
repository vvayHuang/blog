---
title: 在 Hexo 安裝 GA
date: 2022-03-23 22:14:51
tags: hexo
---
Google Analytics 簡稱 GA，安裝 GA 可已知道來看你的網站的人士什麼時段、國家等等數據，所以一定要裝，安裝的方式很簡單

進入 GA 官網，點選左下角**管理**
![進入 GA 官網，點選左下角管理](https://i.imgur.com/00jIvnh.png)

選擇**設定輔助程式**
![選擇設定輔助程式](https://i.imgur.com/H3GOWz4.png)

在**網頁串流詳請**頁面中找到新增網頁內代碼>全域網站代碼
![在網頁串流詳請頁面中找到新增網頁內代碼>全域網站代碼](https://i.imgur.com/u2MGvCS.png)

接下來要把代碼放到網站上，根據 GA 的說明，是要把代碼放在網站的<head>裡面，但因為一個網站有很多分頁，不可能一個一個慢慢加進去，所以一定更快的方式。

以我用的這個 Next 主題為例，代碼主要是放在主題資料架下的 layout.njk，路徑如下： themes>hexo-themes-next>layout>_partials>_layout.njk

每個主題的格式語言都不一樣，遇到時可再自行應變