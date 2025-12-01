# 📊 YouTube Top Channel Videos – Power BI Dashboard (2025)

This project presents a full-featured **YouTube Analytics Dashboard** built using **Power BI**, based on a dataset of **155,702 videos** from top-performing channels.  
The dashboard provides insights into **views, uploads, engagement, timing patterns**, and **channel-wise performance**.

This README includes everything: dataset details, transformations, visuals, KPI logic, DAX formulas, slicers, dashboard design, and future improvements.

---

## 📸 Dashboard Preview

![Dashboard](https://github.com/mohammedraiyan05/YouTube-Top-Channel-Videos-2025-/blob/main/Dashboard.png)

---

# 📁 Dataset Overview

The dataset contains the last 10 uploaded videos of the top YouTube channels, including key metrics.

### **Columns in the Source Dataset**

| Column | Description |
|--------|-------------|
| `video_id` | Unique ID of the video |
| `title` | Video title |
| `channel_name` | Name of the YouTube channel |
| `channel_id` | Unique identifier of the channel |
| `view_count` | Total number of views |
| `like_count` | Total number of likes |
| `comment_count` | Total number of comments |
| `published_date` | Upload date & time (ISO format) |
| `thumbnail` | High-resolution thumbnail URL |

---

# 🔧 Data Transformation (Power Query)

Power Query was used to clean and structure the dataset.

### ✔ Steps Performed:

- Removed invalid or error rows  
- Converted incorrect data types  
- Extracted:
  - Date → **Published Date**
  - Time → **Published Time**
  - Year  
  - Month  
  - Upload Hour  
- Replaced null values  
- Removed unnecessary columns  
- Cleaned column names  
- Ensured date hierarchy works properly  
- Sorted Month using Month Number  

---

# 🧮 DAX Calculated Columns

### **1️⃣ Engagement Rate**
Formula used to measure how engaged the audience is:

```DAX
Engagement Rate =
IF(
    youtube_video[view_count] = 0,
    0,
    (youtube_video[like_count] + youtube_video[comment_count])
        / youtube_video[view_count]
)

### **2️⃣ Upload Hour**

`Upload Hour = HOUR(youtube_video[published_date])`

* * * * *

### **3️⃣ Day Name (Optional)**

`Day Name = FORMAT(youtube_video[published_date], "dddd")`

### **4️⃣ Day Number (For Sorting)**

`Day Number = WEEKDAY(youtube_video[published_date], 2)`

* * * * *

🛠 Tech Stack
=============

-   **Power BI Desktop**

-   **Power Query**

-   **DAX**

-   **Data Modeling**

-   **Interactive Visuals**

-   **YouTube-Inspired UI Theme**

* * * * *

⭐ Dashboard Features
====================

### 🔹 KPI Cards

-   Total Channels

-   Total Videos

-   Total Views

-   Total Likes

-   Total Comments

-   Average Engagement Rate

### 🔹 Performance Visuals

-   **Top 10 Channels by Total Views**

-   **Top 10 Videos by Views**

### 🔹 Time-Based Insights

-   **Uploads by Hour of Day**

-   **Daily Views Trend**

-   **Monthly Views Trend**

### 🔹 Engagement Analytics

-   **Engagement Rate by Channel**

### 🔹 Interactive Slicers

-   Select Channel Name

-   Select Year

-   Select Month

* * * * *

📈 Visuals Included
===================

### 1\. **Top 10 Channels by Total Views**

Highlights channels generating the most views.

### 2\. **Top 10 Videos by Total Views**

Displays best-performing videos across all channels.

### 3\. **Uploads by Hour of Day**

Identifies creators' peak upload time preferences.

### 4\. **Monthly Views Trend**

Shows month-wise performance across selected years.

### 5\. **Engagement Rate by Channel**

Ranks channels with the highest engagement.

### 6\. **Daily Views Trend**

Provides an overview of day-to-day fluctuations in views.

* * * * *

🎨 Dashboard Design
===================

### 🎯 Theme Elements:

-   YouTube-inspired **#E10600 Red Theme**

-   White card backgrounds for KPIs

-   Line charts styled with solid & clean strokes

-   Bar charts with consistent color palette

-   High-contrast labels for readability

-   Clean slicer design with minimal borders

### 🎨 Primary Colors Used:

| Purpose | Hex Code |
| --- | --- |
| Primary Red | `#E10600` |
| Dark Red | `#B30000` |
| Soft Red | `#FF6B6B` |
| White | `#FFFFFF` |
| Black Text | `#000000` |

* * * * *

📝 How to Use the Dashboard
===========================

1.  Open the `.pbix` file in Power BI Desktop

2.  Use slicers to filter:

    -   Channel

    -   Year

    -   Month

3.  Hover over visuals for detailed tooltips

4.  Export charts for reporting

5.  Explore time-based patterns using the trend visuals

* * * * *

🔮 Future Enhancements
======================

-   Add YouTube API for live data refresh

-   Add video category analysis

-   Predict trends using AI/ML forecasting

-   Add subscriber growth analytics

-   Embed report in Power BI Service with scheduled refresh

* * * * *

📬 Contact
==========

If you wish to connect or collaborate: