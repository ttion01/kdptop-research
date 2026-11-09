# How KDPTop Research makes its numbers

Where the data in every report comes from, how each metric is calculated, what the limits are, and how reports are updated and corrected.

## Data sources

- **Amazon Best Sellers and New Releases lists**: KDPTop captures every Amazon.com Books and Kindle eBooks Best Sellers list and New Releases list once a day (Top 100 per list), plus Kindle Top 100 Free. Full daily coverage started on 2026-10-27.
- **Book pages and Keepa**: Title, author, price, reviews, rating, publisher, publication date, page count and trim size come from the list cards, the book pages and Keepa's sales-rank history.
- **Search demand**: Monthly Amazon search volume, purchases and month-over-month growth for book search terms come from a third-party keyword tool (SellerSprite). They are estimates and lag by about a month.
- **Book classification**: Each book is tagged with a product type (coloring book, journal, cookbook…), an age band, holidays and audiences by a language model reading its title, description and categories, with rules as a fallback.

## Definitions

<a id="unique-bestsellers"></a>
### Unique Best Sellers books

Distinct books (ASINs) on any Best Sellers list on a given day. A book on ten lists counts once.

<a id="breakout"></a>
### Breakout book

A book published in the report window that first reached any Best Sellers list in the same window. Days to chart = first Best Sellers day minus publication date.

<a id="indie"></a>
### Independently published (indie)

Published through KDP or CreateSpace, read from the publisher field ("Independently published", empty publisher) or, when that is missing, from the author. Shares are over books whose publisher is known.

<a id="opportunity-score"></a>
### Opportunity score

KDPTop's 0-100 score per category for how much room it leaves a new indie book: the review barrier, the share of low-review books, list turnover, the share of new releases and price room. Categories need at least 20 fully parsed books; scores on smaller samples are pulled toward 50.

<a id="niche"></a>
### Niche

A cross-category product market: product type × holiday × audience × age band (for example Christmas coloring books for kids 6-8), over the books on current Best Sellers and New Releases lists.

<a id="niche-score"></a>
### Niche score

0-100 from demand (estimated sales and search volume, 30%), review barrier (20%), new-release inflow (15%), price room (15%), indie share (10%) and breakouts (10%), plus timing for seasonal niches; multiplied down when many books are not something KDP can print, and shrunk toward the average on small samples.

<a id="sales-estimate"></a>
### Estimated sales

Daily and monthly unit sales estimated from Amazon sales rank (BSR) with a rank-to-sales curve per store, calibrated against books with known sales. A single book can be off by ±30% or more; use estimates to compare books and markets, not as anyone's income.

<a id="review-barrier"></a>
### Review barrier

How many reviews the books already on a list have: the median, and the share with fewer than 10, 50 or 100 reviews. A low barrier means books with few reviews still rank.

<a id="launch-window"></a>
### Launch window

For seasonal books: publish two to four months before the peak month, so the book has a rank and reviews when demand arrives. The peak month comes from Google Trends for the niche's search term, else the holiday.

<a id="median"></a>
### Median and quartiles

Prices, reviews and pages are medians (the middle book), so a few outliers do not move them; P25 and P75 are the quarter and three-quarter points.

## Limits

- Lists show rank, not sales. Sales figures are estimates from rank.
- Books KDPTop has not seen on a list are not counted; long-tail books that never chart are missing.
- Adult content categories are excluded from every report.
- Reports with less than a full period of data say how many days they cover.

## Versions and corrections

Reports are versioned. When a report is refreshed with newer data, the new version replaces the page at the same URL, its version history lists the date and what changed, and every version stays on GitHub as a tag. Errors are corrected the same way and noted in the history. Report a problem: support@kdptop.com.

---

# KDPTop 研究报告的方法说明

每份报告的数据从哪来、指标怎么算、有哪些局限，以及报告如何更新和更正。

## 数据来源

- **亚马逊畅销榜和新品榜**: KDPTop 每天抓取一次亚马逊美国站全部图书和 Kindle 电子书类目的畅销榜和新品榜（每个榜 Top 100），以及 Kindle 免费榜 Top 100。完整的每日抓取从 2026-10-27 开始。
- **书籍页面和 Keepa**: 书名、作者、价格、评论数、评分、出版社、出版日期、页数和开本来自榜单卡片、书籍页面和 Keepa 的销售排名历史。
- **搜索需求**: 图书搜索词的亚马逊月搜索量、购买量和环比来自第三方关键词工具（卖家精灵），是估算值，大约滞后一个月。
- **图书分类**: 每本书的产品类型（涂色书、日记本、菜谱……）、年龄段、节日和人群标签，由语言模型读取书名、简介和类目判断，没有模型结果时按规则判断。

## 指标定义

<a id="unique-bestsellers-zh"></a>
### 畅销榜上的书（去重）

某一天出现在任一畅销榜上的不重复的书（ASIN），同一本书上了十个榜也只算一次。

<a id="breakout-zh"></a>
### 突围新书

在报告区间内出版、并在同一区间内首次进入任一畅销榜的书。冲榜天数 = 首次上畅销榜的日期减出版日期。

<a id="indie-zh"></a>
### 独立出版

通过 KDP（或早年的 CreateSpace）自出版的书，按出版社字段识别（"Independently published" 或空），没有出版社字段时按作者识别。占比只在出版社已知的书里计算。

<a id="opportunity-score-zh"></a>
### 机会分

KDPTop 给每个类目算的 0-100 分，衡量新的独立出版书有多少空间：评论门槛、低评论书占比、榜单更替、新书占比和价格空间。类目至少要有 20 本信息完整的书；样本小的类目分数会向 50 收缩。

<a id="niche-zh"></a>
### 细分市场

跨类目的产品市场：产品类型 × 节日 × 人群 × 年龄段（比如给 6-8 岁孩子的圣诞涂色书），统计的是当前畅销榜和新品榜上的书。

<a id="niche-score-zh"></a>
### 细分评分

0-100 分：需求（估算销量和搜索量，30%）、评论门槛（20%）、新书流入（15%）、价格空间（15%）、独立出版占比（10%）和突围（10%），节日细分另加时机分；KDP 做不了的书占比高时打折，样本小时向平均值收缩。

<a id="sales-estimate-zh"></a>
### 估算销量

根据亚马逊销售排名（BSR）按店铺的排名-销量曲线估算的日销量和月销量，用已知销量的书校准。单本书可能有 ±30% 以上的误差，适合比较书和市场，不能当作任何人的真实收入。

<a id="review-barrier-zh"></a>
### 评论门槛

榜单上已有的书有多少评论：中位数，以及少于 10、50、100 条评论的书占比。门槛低说明评论少的书也能上榜。

<a id="launch-window-zh"></a>
### 上架窗口

针对节日书：在旺季月份前 2-4 个月上架，需求来的时候书已经有排名和评论。旺季月份取自细分搜索词的 Google 趋势，没有时按节日月份。

<a id="median-zh"></a>
### 中位数和四分位

价格、评论数和页数用中位数（排在中间的那本书），少数极端值不会影响结果；P25 和 P75 是 1/4 和 3/4 位置的值。

## 局限

- 榜单反映的是排名，不是销量。销量数字都是根据排名估算的。
- 没有在榜单上出现过的书不在统计里，从不上榜的长尾书会漏掉。
- 所有报告都排除了成人内容类目。
- 数据不满一个完整周期的报告会写明覆盖了几天。

## 版本和更正

报告有版本号。用新数据更新时，新版本在同一网址替换旧版本，页面的版本记录写明日期和改动，每个版本都在 GitHub 上保留标签。发现错误也按同样方式更正并写入记录。反馈问题：support@kdptop.com。
