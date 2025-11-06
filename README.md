# Meta Ads Performance Analysis

## Project Overview
This project analyzes Meta (Facebook & Instagram) ad performance using an Excel dataset.  
The focus is on **campaign reach, user engagement, and conversions**.  
Insights are displayed in a **Power BI dashboard** to help the marketing team optimize campaigns and budget allocation.

---

## 📂 Dataset Description

The project uses a single Excel file with multiple sheets or separate Excel files:

### 1. `ad_events.xlsx`
- Stores user interactions with ads (Impressions, Clicks, Shares, Comments, Purchases).  
- Key Fields:  
  - `event_id` → Unique event ID  
  - `ad_id` → Ad identifier  
  - `user_id` → User identifier  
  - `timestamp` → Event time  
  - `event_type` → Type of interaction  

### 2. `ads.xlsx`
- Ad metadata (platform, ad type, targeting).  
- Key Fields:  
  - `ad_id` → Primary key  
  - `campaign_id` → Links to campaigns  
  - `ad_platform` → Facebook / Instagram  
  - `ad_type` → Image, Video, Carousel, Story  
  - `target_gender`, `target_age_group`, `target_interests`  

### 3. `campaigns.xlsx`
- Campaign-level info (budget, start/end date).  
- Key Fields:  
  - `campaign_id` → Primary key  
  - `name`, `start_date`, `end_date`  
  - `total_budget` → Campaign spend  

### 4. `users.xlsx`
- User demographics and interests.  
- Key Fields:  
  - `user_id` → Primary key  
  - `user_gender`, `user_age`, `age_group`  
  - `country`, `location`  
  - `interests`  

---

## 🔗 How the Data Works
- **ad_events → ads → campaigns** → Track events at ad & campaign level.  
- **ad_events → users** → Link interactions to demographics for audience analysis.  

This forms a **star schema** in Power BI:  
- Fact Table: `ad_events`  
- Dimension Tables: `ads`, `campaigns`, `users`  

---

## 📊 Key Metrics / KPIs

| KPI | Definition | Formula |
|-----|------------|---------|
| Impressions | Total times ads shown | Count of `event_type = Impression` |
| Clicks | Number of clicks | Count of `event_type = Click` |
| Shares | Number of shares | Count of `event_type = Share` |
| Comments | Number of comments | Count of `event_type = Comment` |
| Purchases | Number of conversions | Count of `event_type = Purchase` |
| Engagements | Total interactions | Clicks + Shares + Comments |
| CTR | Click-through rate | `(Clicks ÷ Impressions) × 100` |
| Engagement Rate | Engagements ÷ Impressions | `(Engagements ÷ Impressions) × 100` |
| Conversion Rate | Click-to-purchase rate | `(Purchases ÷ Clicks) × 100` |
| Purchase Rate | Impressions-to-purchase | `(Purchases ÷ Impressions) × 100` |
| Total Budget | Total campaign spend | Sum of `campaigns.total_budget` |
| Avg Budget per Campaign | Average campaign budget | `Total Budget ÷ Campaign Count` |

---

## 📈 Power BI Dashboard Features

1. **Target Gender – Donut Chart**  
   Visualizes performance by gender (dynamic metric selection).  

2. **Target Age Group – Bar Chart**  
   Engagement across age groups.  

3. **Country – Map**  
   Geographic distribution of engagement.  

4. **Calendar Heat Map**  
   Monthly engagement trends.  

5. **Weekly Trend – Stacked Column**  
   Compare ad type performance week by week.  

6. **Hourly Trend – Area Chart**  
   Identify peak hours of user activity.  

7. **Ad Type – Matrix**  
   Performance by ad type and platform.  

---

## 🔍 Insights & Recommendations

- Strong engagement (high CTR & Engagement Rate) but low conversion → improve landing pages.  
- Target audience: **Females, 18–30**, particularly in **India & Brazil**.  
- Best ad types: **Video > Stories > Carousel/Image**.  
- Schedule ads in **afternoon & evening** for max engagement.  
- Optimize budget to focus on **high-performing geographies and ad formats**.  

---

## 🛠 Tools & Technologies

- **Data Source:** Excel files  
- **Dashboard:** Power BI Desktop  
- **Visualization:** Power BI built-in charts & matrix  

---

## 📁 Folder Structure

