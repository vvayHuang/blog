---
title: hexo 樣式失效及設定網站站內連結
date: 2022-03-24 11:21:00
tags: 
    - hexo 
---
如果樣式沒有出現，可能就是連結出現錯誤，仔細看程式碼就會看到
![樣式沒有出現](https://i.imgur.com/qGoxpUx.png)

此時你需要進入 hexo 的 config.yml 將 relative_link 改成 true
```
relative_link: true
```

重新編譯後會變成這個樣子
![重新編譯後會變成這個樣子](https://i.imgur.com/7vTtEgF.png)

在檢查程式碼內的 css 及 js 連結，順利的話，完成後樣式就會出現

（由於每個主題樣式的安裝方式都不同，所以有可能會需要手動調整）

- - -

參考[六角學院的 hexo 教學影片](https://www.youtube.com/watch?v=jOJI9ekTzK8)製作的朋友，應該會發現上傳至 github 把樣式搞定之後又會遇到一個問題，就是點選文章連結會找不到頁面，這個問題就是連結出錯了

例如你的網址是 vvayhuang.github.io/blog/，但是點選文章的時候會發現網址會變成 vvayhuang.github.io/年/月/日/文章名稱，中間的 blog 專案名稱不見了

此時就必須打開 hexo 的 config.yml ，在 url 的地方把你主頁面的網址貼上，意思就是未來文章就會在這個連結下打開，點選就不會找不到頁面

![必須打開 hexo 的 config.yml](https://i.imgur.com/jdEmdEE.png)