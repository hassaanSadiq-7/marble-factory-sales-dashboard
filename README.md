# Marble Factory Sales Dashboard

I'm a CS student getting into data analytics, and this is a Power BI dashboard I built to practice. It looks at sales and profit for an imaginary marble factory from January 2025 to June 2026.

The data is **made up (sample data)**. It isn't from a real company, so please don't read the numbers as real business results.

<img width="1359" height="864" alt="Dashboard" src="https://github.com/user-attachments/assets/17459dac-6d83-43dc-8a12-4a63b8469f8d" />

## Why I built it

My uncle owns a marble factory, and I've been curious how a small business like that could track its sales without digging through Excel sheets all day. This was my first attempt at turning that idea into a proper dashboard.

## What's in it

- Four KPI cards: Total Sales (344.91M), Total Profit (94.29M), Profit Margin (27.34%) and Total Quantity (262K)
- Sales by city
- Profit by product
- Monthly sales trend
- Profit margin % by product
- Slicers for product, city and date

## What I noticed

- Lahore and Karachi sell the most (about 46M each), Sialkot the least (about 39M).
- Margins are almost the same for every product, between 26.6% and 28.2%. That's a bit too neat for real data, which is one reason I know it's synthetic.
- Sales peak twice, around Aug 2025 and May 2026.
- The drop at the end of the trend line is just because June 2026 only has data up to the 25th.

## How it's built

One table, `Marble_Sales`, with the date, product, city, sales, profit and quantity. The margin is a simple DAX measure:

```
Profit Margin % = DIVIDE(SUM(Marble_Sales[Total_Profit]), SUM(Marble_Sales[Total_Sale]))
```

Built with Power BI Desktop and DAX.

## What I learned

Layout matters more than I thought. Most of my time went into small things: aligning cards, picking sensible chart titles, fixing a misleading partial month, and making slicers fit. I also learned that cross-filtering can quietly change every number on the page if you click a bar by accident.

## Next

I want to rebuild this with data loaded through a proper pipeline (Python and SQL), since I'm aiming for data engineering.

## Files

- `Marble_Sales_Dashboard.pbix`: the Power BI file

## Contact

Syed Hassaan Sadiq
[LinkedIn](https://linkedin.com/in/hassaan-sadiq-h7) | [GitHub](https://github.com/hassaanSadiq-7)
