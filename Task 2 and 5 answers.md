# Task 2
## Which XML tags were used to extract the headlines?
To extract headlines from the RSS feeds, the find("title") method was used on each <item> element. This means the <title> XML tag, nested within the <item> tag, was specifically targeted to retrieve the headline text
## What is the role of the <item> tag in RSS feeds?
The <item> tag in an RSS feed is a fundamental element that represents a single article, entry, or piece of news content. It acts as a container for various pieces of information related to that specific item, such as its title, publication date, description, and a link to the full content.
## How does an RSS feed differ from a normal HTML webpage?
RSS feeds and normal HTML webpages serve different purposes and have distinct structures:

Purpose: An HTML webpage is designed for human consumption, providing rich visual layouts, interactive elements, and formatted text for users to read and navigate. An RSS feed, on the other hand, is designed for machine consumption, providing structured, summarized content in a standardized XML format.

Content Structure: HTML uses a wide array of tags (<div>, <p>, <img>, <a>, etc.) to define layout, formatting, and content presentation. RSS uses a limited set of XML tags (<channel>, <item>, <title>, <link>, <pubDate>, <description>, etc.) to provide a concise, structured summary of content updates, without any presentation or layout information.

Readability: HTML webpages are visually rich and intended to be browsed directly by users through a web browser. RSS feeds are plain text XML documents that are typically consumed by RSS readers, aggregators, or applications that parse the structured data to display updates to users in a consistent format across different sources.

Updates: RSS feeds are primarily used for syndication, allowing users or applications to subscribe to updates from a website without repeatedly visiting the site. HTML webpages require direct visits to see changes.
# Task 5
## Which dates in your news data are non-trading days?
Based on our merged_df, the non-trading days identified are those where the is_trading_day column is False. From the news_volume_per_day DataFrame (or by inspecting merged_df where is_trading_day is False), the non-trading days are 2026-01-01 and 2025-12-31.
## Why does the stock market not trade on those days?
Stock markets typically do not trade on weekends (Saturdays and Sundays) and observed public holidays. In this specific dataset, if 2026-01-01 was a public holiday (New Year's Day) and 2025-12-31 was also a non-trading day (e.g., in observance of New Year's or a weekend), then these would be the reasons for no stock trading activity. Without a specific calendar lookup for 2025-2026, we infer this from the is_trading_day column.
## How many news articles fall on non-trading days?
From the news_frequency_by_trading_day analysis, 7 out of 10 news articles fall on non-trading days. This means a significant portion of the news in this dataset was published on days when the stock market was closed.
