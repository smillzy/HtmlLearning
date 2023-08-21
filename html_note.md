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

# Tag

## opening tag &closing tag

&lt;p&gt;、&lt;a&gt;

## self-closing tag

&lt;img /&gt;、&lt;base /&gt;、&lt;meta /&gt;

# 路徑

## absolite linking/path 絕對路徑

需要連結到不在我們伺服器內的資源時，使用完整的**URL**當作連結對象

如果網頁被刪除就會抓取不到

## relative linking/path 相對路徑

連結到相對於目前文件所在位置的檔案，上傳到網站上就會比較占空間

**.** 目前 html 文件所在資料夾位置

**..** 上層的資料夾位置

**/** 可從 root directory (最上層的資料夾) 向下連結

<font color=red>**文件與檔案名稱不建議中間留空白鍵**</font>

# &lt;head&gt;

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

## &lt;a&gt; 全體屬性設定

一次設定所有&lt;a&gt;的屬性

```HTML
// HTML
<base target="   " />
```

# &lt;body&gt;

**➜**使用者可見的內容

**➜**定義文檔的正文 ex.內容、圖像、超連結、表格、列表

## H1~H6

HTML 標籤是定義整個**網頁的架構**，並非樣式(CSS 的工作)

應該把**最重要**的資料放進**H1**

正確使用可以做到 SEO(Search Engine Optimization)<u>搜尋引擎的最佳化</u>

## &lt;P&gt;

定義一個段，每個&lt;P&gt;元素前後會有空行

## &lt;a&gt; anchor tag

a+`tab`

網頁上創建超連結

提供 absolute linking 或 relative linking 作為其“href” (hyptertext reference)值

```HTML
// HTML
<a href="https://www.npm.gov.tw/">故宮網站連結</a>
```

### target 屬性

[屬性種類參考](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)

`_self` 原視窗開啟 The current browsing context.

`_blank` 開啟新視窗 Usually a new tab, but users can configure browsers to open a new window instead.

```HTML
// HTML
<a href="https://www.npm.gov.tw/" target="_self">故宮網站連結</a>
```

如果 &lt;a&gt; 比較多，可以在 &lt;head&gt; 使用 &lt;base&gt; 定義所有標籤屬性

```HTML
// HTML
<base target="_blank" />
```

## &lt;img&gt;

有兩個屬性要設定

1.src (source) 圖片來源

2.alt (alternative) 圖片無法顯示時的**替代**文字

### relative linking

```HTML
// HTML
<img
  width="400"
  height="300"
  src="./images/故宮圖片1.jpeg"
  alt="故宮圖片1"
/>
```

### absolite linking

```HTML
// HTML
<img
  width="500"
  height="300"
  src="https://upload.wikimedia.org/wikipedia/commons/b/b4/NationalPalace_MuseumFrontView.jpg"
  alt="故宮圖片_絕對路徑"
/>
```
