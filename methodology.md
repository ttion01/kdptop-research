# Methodology

## Data

- Lists: KDPTop captures every Amazon.com Books and Kindle eBooks Best Sellers list and New Releases list once a day
  (Top 100 per list), plus Kindle Top 100 Free.
- Books: title, author, price, reviews, publisher and publication date come from the list cards and the book pages.
  Independently published (KDP) books are identified from the publisher field, or from the author when the publisher
  is missing.
- Search demand: monthly Amazon search volume and month-over-month growth for book search terms, from a third-party
  keyword tool; these are estimates.

## Definitions

- Unique Best Sellers books: distinct books (ASINs) on any Best Sellers list on the last day of the report window.
- Breakout book: published in the report window and first reached any Best Sellers list in the window.
- Opportunity score (0-100): KDPTop's per-category score from the review barrier, the share of low-review books,
  list turnover, the share of new releases and price room. Categories need at least 20 fully parsed books on both
  compared days.
- Medians are used for price and reviews so a few outliers do not move them.

## Limits

- Lists show rank, not sales. Sales figures elsewhere on KDPTop are estimates from sales rank.
- Books KDPTop has not seen are not counted.
- KDPTop started its full daily crawl on 2026-10-27; reports before a full month of data say how many days they cover.

---

# 方法说明

## 数据

- 榜单：KDPTop 每天抓取亚马逊美国站全部图书和 Kindle 电子书类目的畅销榜和新品榜（每个榜 Top 100），以及 Kindle 免费榜。
- 书籍信息：书名、作者、价格、评论数、出版社和出版日期来自榜单卡片和书籍页面。独立出版（KDP）按出版社字段识别，没有出版社时按作者识别。
- 搜索需求：图书搜索词的亚马逊月搜索量和环比，来自第三方关键词工具，是估算值。

## 定义

- 畅销榜上的书（去重）：报告区间最后一天所有畅销榜上不重复的书（ASIN）。
- 突围新书：在报告区间内出版，并在区间内首次进入任一畅销榜的书。
- 机会分（0-100）：KDPTop 按类目计算，综合评论门槛、低评论书占比、榜单更替、新书占比和价格空间。比较的两天里类目都要有至少 20 本信息完整的书。
- 价格和评论数用中位数，少数极端值不会影响结果。

## 局限

- 榜单反映的是排名，不是销量。KDPTop 其他页面的销量是根据排名估算的。
- KDPTop 没有收录的书不在统计里。
- KDPTop 从 2026-10-27 开始完整的每日抓取；数据不满一个月的报告会写明覆盖了几天。
