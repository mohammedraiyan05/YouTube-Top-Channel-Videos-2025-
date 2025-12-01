# 📊 YouTube Top Channel Videos – Power BI Dashboard

This Power BI dashboard provides an in-depth analytical overview of the **Top YouTube Channels and Videos**, generated from a dataset containing **155,000+ videos**.  
It highlights performance metrics such as **views, likes, comments, engagement rate, upload timing trends, and monthly view behavior**.

---

## 📸 Dashboard Preview

![Dashboard](https://github.com/mohammedraiyan05/YouTube-Top-Channel-Videos-2025-/blob/main/Dashboard.png)

---

## 📁 Dataset Description

The dataset contains detailed information about top YouTube channels and their recently uploaded videos.

### **Columns Included**

| Column | Description |
|--------|-------------|
| `video_id` | Unique ID of the YouTube video |
| `title` | Title of the video |
| `channel_name` | Name of the channel |
| `channel_id` | Unique ID of the channel |
| `view_count` | Total number of views |
| `like_count` | Total number of likes |
| `comment_count` | Total number of comments |
| `published_date` | Date & time of video upload |
| `thumbnail` | URL of the video thumbnail |

### **Created Columns (Power Query + DAX)**

| New Column | Description |
|-----------|-------------|
| `Published Date` | Extracted date of upload |
| `Published Time` | Extracted time of upload |
| `Year` | Year of upload |
| `Month` | Month name |
| `Upload Hour` | Hour extracted for time analysis |
| `Engagement Rate` | `(likes + comments) / views` |

---

## 🛠️ Tech Stack Used

- **Power BI Desktop**
- **Power Query Editor**
- **DAX (Data Analysis Expressions)**
- **Data Modeling**
- **Interactive Visualizations**

---

## ⭐ Key Features of the Dashboard

### 🔹 KPI Cards
- Total Channels  
- Total Videos  
- Total Views  
- Total Likes  
- Total Comments  
- Average Engagement Rate  

### 🔹 Top Performance Analytics
- **Top 10 Channels by Total Views**
- **Top 10 Videos by Views**

### 🔹 Audience Engagement Insights
- **Engagement Rate by Channel**
- **Daily Views Trend**

### 🔹 Upload Behavior & Time-Based Insights
- **Uploads by Hour of Day**
- **Monthly Views Trend**

### 🔹 Interactive Filters (Slicers)
- Channel Name  
- Year  
- Month  

---

## 📈 Visuals Included in the Dashboard

- **Top 10 Channels by Total Views**
- **Top 10 Videos by Views**
- **Uploads by Hour of Day**
- **Monthly Views Trend**
- **Engagement Rate by Channel**
- **Daily Views Trend**

---

## 🔧 Data Cleaning & Transformation

### ✔ Performed in Power Query:
- Removed null/error rows  
- Fixed incorrect data types  
- Split date/time into components  
- Handled inconsistent formats  
- Replaced null values  

### ✔ Calculated Columns and Measures (DAX):

#### **Engagement Rate**
```DAX
Engagement Rate =
IF(
    youtube_video[view_count] = 0,
    0,
    (youtube_video[like_count] + youtube_video[comment_count])
        / youtube_video[view_count]
)
