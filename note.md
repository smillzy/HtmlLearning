# 介紹

HTML 不是程式語言，是標記語言  
製作網頁的三大基石**➜**HTML(網頁內容)、CSS(網頁外觀)、JS(功能性)

## HTML 標籤包含四元素

- Opening tag 起始標籤

  包含元素的名字，夾在一對< >brackets 之間

- Closing tag 結束標籤

  夾在一對</ >brackets 之間，多”/”foward slash

- Content 內容
- Element 元素

  標籤是 HTML Element

![HTMLElement](./截圖/07.png)

## 巢狀元素 Nesting elements

把元素放到另一個元素  
必須要有正確的<> </>去完成，沒使用正確語法，容易導致無法解讀

## W3C 提供的 HTML Validator(驗證器)可以確認正確性

[Validator](https://validator.w3.org/#validate_by_uri)

- URL **➜**用網址驗證
- File Upload **➜**上傳檔案
- Direct input **➜**直接貼程式碼

## 物件導向 Object-Oriented (OOP) <u>ex.C,C++,Java,JS,Python</u>

生活中物件包含兩部分

- 屬性 Attributes/Property <u>ex.廠牌、出廠年份</u>
- 行為 Methods/Function/Behavior <u>ex.直走、左轉</u>

## 骨架 Skeleton

建構每個 HTML 網頁所需的一組標籤，告訴瀏覽器他正在讀取甚麼樣類型的文件

- `<head>`
- `<body>`

```HTML
// HTML
<!DOCTYPE html> #document_type文件類型
<html>
  <head></head>
  <body></body>
</html>
```

# head

**➜**包含網頁的特定信息，跟網頁有關的訊息 ex.誰寫的、語言、樣式(給搜尋引擎看)

**➜**通常是 meta data(我自己)

**➜**<u>title 文檔標題(強制性)、script、script linking、CSS</u>

## 總整理

[總整理](https://htmlhead.dev/)

Recommended Minimum 推薦的少一定要放的東西

```HTML
// HTML
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--
  The above 2 meta tags *must* come first in the <head>
  to consistently ensure proper document rendering.
  Any other head element should come *after* these tags.
 -->
<title>Page Title</title>
```

## lang 屬性**➜**設定網頁語言

lang="en”➜ 英文網頁

[語言設定寫法](https://www.w3schools.com/tags/ref_language_codes.asp)

## meta charset="UTF-8" 字集

會放在 head 標籤內容中的最上面

charset**➜** character set 字元集合

body 裡面顯示的內容符合 UTF-8 字集

```HTML
// HTML
<meta charset="UTF-8" />
```

## 視窗設定

meta name="viewport(視窗)"

意思 : 我要設定我 viewport(視窗)的範圍，他的 width(寬度)是 device-width(我裝置的寬度)initial-scale(最初始的放大程度)1.0**➜**沒有任何放大的值

```HTML
// HTML
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

## 網頁底下的描述

```HTML
// HTML
<meta name="description" content="A description of the page">
```

![網頁底下的描述](./截圖/08.png)

## 讓搜尋引擎找到我們的網頁

```HTML
// HTML
<meta name="robots" content="index,follow"><!-- All Search Engines -->
<meta name="googlebot" content="index,follow"><!-- Google Specific -->
```

## 顯示作者

```HTML
// HTML
<meta name="author" content="人名">
```

## 標記語法

快捷:Crtl+/(?鍵)

```HTML
// HTML
<!--文字-->
```
