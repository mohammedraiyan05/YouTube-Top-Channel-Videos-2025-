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

