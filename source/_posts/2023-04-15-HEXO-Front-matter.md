---
title: HEXO Front-matter
top_img: 'linear-gradient(#e9619b, 15%, #fbd1e3);'
categories:
  - 随写
tags:
  - hexo
  - theme
  - front-matter
date: 2023-04-15 07:58:16
---

### Fron-matter概念

* Front-matter 是 markdown 文件最上方以 —- 分隔的区域，用于指定个别档案的变数。
* Page Front-matter 用于页面配置; Post Front-matter 用于文章页配置
* 可在scaffolds模板中自定义配置相关参数

```bash
# Page Front-matter 用于页面配置
title				【必需】頁面標題
date				【必需】頁面創建日期
type				【必需】標籤、分類和友情鏈接三個頁面需要配置
updated			【可選】頁面更新日期
description	【可選】頁面描述
keywords		【可選】頁面關鍵字
comments		【可選】顯示頁面評論模塊(默認 true)
top_img			【可選】頁面頂部圖片
mathjax			【可選】顯示mathjax(當設置mathjax的per_page: false時，才需要配置，默認 false)
katex				【可選】顯示katex(當設置katex的per_page: false時，才需要配置，默認 false)
aside				【可選】顯示側邊欄 (默認 true)
aplayer			【可選】在需要的頁面加載aplayer的js和css,請參考文章下面的音樂 配置
highlight_shrink	【可選】配置代碼框是否展開(true/false)(默認為設置中highlight_shrink的配置)

# Post Front-matter 用于文章页配置
title							【必需】文章標題
date							【必需】文章創建日期
updated						【可選】文章更新日期
tags							【可選】文章標籤
categories				【可選】文章分類
keywords					【可選】文章關鍵字
description				【可選】文章描述
top_img						【可選】文章頂部圖片
cover							【可選】文章縮略圖(如果沒有設置top_img,文章頁頂部將顯示縮略圖，可設為false/圖片地址/留空)
comments					【可選】顯示文章評論模塊(默認 true)
toc								【可選】顯示文章TOC(默認為設置中toc的enable配置)
toc_number				【可選】顯示toc_number(默認為設置中toc的number配置)
copyright					【可選】顯示文章版權模塊(默認為設置中post_copyright的enable配置)
copyright_author	【可選】文章版權模塊的文章作者
copyright_author_href	【可選】文章版權模塊的文章作者鏈接
copyright_url					【可選】文章版權模塊的文章連結鏈接
copyright_info				【可選】文章版權模塊的版權聲明文字
mathjax								【可選】顯示mathjax(當設置mathjax的per_page: false時，才需要配置，默認 false)
katex									【可選】顯示katex(當設置katex的per_page: false時，才需要配置，默認 false)
aplayer								【可選】在需要的頁面加載aplayer的js和css,請參考文章下面的音樂 配置
highlight_shrink			【可選】配置代碼框是否展開(true/false)(默認為設置中highlight_shrink的配置)
aside									【可選】顯示側邊欄 (默認 true)
```

