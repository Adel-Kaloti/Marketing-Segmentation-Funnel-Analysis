<p align="center">
  <img src="https://github.com/user-attachments/assets/7e22a616-a356-441d-9364-85d03d0ac62f" width="200" />
</p>

###   <h1 align="center">Marketing Segmentation & Funnel Analysis</h1>   
Data-driven marketing project analyzing campaign performance, audience segments, and funnel KPIs using SQL Server &amp; Tableau.

<img width="1402" height="936" alt="image" src="https://github.com/user-attachments/assets/2923cdb4-8fb9-4bae-a77e-9d352a64b212" />


-----

###   <h1 align="center">🎯 Main Business Questions & KPIs</h1> 
This project focuses on answering 4 important campaigns performance questions:

### 1️⃣ Which target audiences deliver the best performance across campaigns?
Identify which **Target_Audience** (like .. *Women 35–44, Men 25–34, All Ages*) achieves the best mix of:
- **High CTR**, **High Conversion Rate**, **Low CAC**, **High ROI**

Understanding this helps optimize audience targeting and improve overall campaign profitability.

---

### 2️⃣ How does performance change across channels for each target audience?
Analyze how the same **Target_Audience** performs across different channels  
(*Google Ads, Facebook, Instagram, YouTube, Email*):
- Which channels require **more budget**?
- Which channels should have spending **reduced or stopped** based on low ROI?
- Which audience × channel combination brings the highest engagement?

---

### 3️⃣ Where do we lose potential customers in the marketing funnel?
Evaluate the drop-off across the funnel:  **Impressions → Clicks → Conversions**

Key goals:
- Identify **which stage has the highest drop rate**
- Compare funnel performance across different **audience segments**
- Detect segments with unusually strong or weak conversion paths

---

### 4️⃣ What data-driven recommendations can optimize budget allocation?
If the company operates with a fixed marketing budget, we determine how to **redistribute spend** across:
- **Target_Audience**, **Channel**

To: - Reduce **CAC**
    - Increase **ROI**
    - Focus spending on the **highest-value segments**

This ensures maximum impact with limited funds.




-----
###   <h1 align="center"> Data Structure & ERD</h1> 

To improve data quality, performance, and analytical flexibility, the original Raw_Data table was normalized and split into three separate tables:
- **dim_campaign** – campaign attributes  
- **dim_date** – full date intelligence  
- **fact_campaign_performance** – all measurable KPIs  

This structure makes analysis faster, cleaner, and BI-ready.



<p align="center">
  <a href="ETL_SQL.txt">
    <img src="https://img.shields.io/badge/View%20 ETL SQL%20File-ff9933?style=for-the-badge&logo=database&logoColor=white" />
  </a>
  <a href="Data_Cleaning_SQL.txt" >
    <img src="https://img.shields.io/badge/Data%20Cleaning%20SQL-006699?style=for-the-badge&logo=tableau&logoColor=white" />
  </a>
  </p>

<p align="center"> 
<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/b1364cf1-7ff4-402b-81ca-adac9c68101b" />
  </p>

  
-----

 <tr>
    <h1 align="center">Data Dimentions</h1>
   <p align="center">
<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/775f688e-a8c4-42c2-ab4b-b8ba10e66a58" />

  </p>

  </tr>

-----

 <tr>
    <h1 align="center"> Project Measures &  KPIs </h1>

  </tr>
<table>
  <tr>
    <td width="50%" valign="top">

  <h2>📌 Clicks</h2>
  <p>
  - Number of times users clicked on the ad.<br>
  - A direct indicator of how attractive and engaging the campaign content is.
  </p>
  <hr>

  <h2>📌 Impressions</h2>
  <p>
  - Total number of times the ad was displayed to users.<br>
  - Reflects the campaign’s overall reach and visibility.
  </p>
  <hr>

  <h2>📌 Engagement_Score</h2>
  <p>
  - A quality interaction score (0–10) representing how strongly users engaged 
  with the campaign (likes, comments, shares, video views, etc.).
  </p>
  <hr>

</td>

<td width="50%" valign="top">

  <h2>📌 Conversion_Rate</h2>
  <p>
  - The percentage of users who completed a desired action 
  (purchase, signup, download) after clicking the ad.<br>
  - A core metric for evaluating campaign effectiveness.
  </p>
  <hr>

  <h2>📌 Acquisition_Cost</h2>
  <p>
  - The total advertising spend for the campaign.<br>
  - Essential for calculating CAC, CPA, and ROI.
  </p>
  <hr>

  <h2>📌 ROI</h2>
  <p>
  - Return on Investment — measures how much revenue or value is generated 
  for every dollar spent. Higher ROI = more profitable campaign.
  </p>

</td>
  </tr>
</table>












  







