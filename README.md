<p align="center">
  <img src="https://github.com/user-attachments/assets/7e22a616-a356-441d-9364-85d03d0ac62f" width="200" />
</p>

###   <h1 align="center">Marketing Segmentation & Funnel Analysis</h1>   

# Executive Summary

<img width="2400" height="1601" alt="Screenshot 2025-12-04 232246" src="https://github.com/user-attachments/assets/cdf3f15f-5865-48b5-93e1-92a624bcb90f" />


<p align="center">
  <a href="https://public.tableau.com/app/profile/adel.kaloti1" target="_blank">
    <img src="https://img.shields.io/badge/View%20Interactive Dashboard on%20Tableau-006699?style=for-the-badge&logo=tableau&logoColor=white"/>
  </a>
</p>

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

<h1 align="center">📊 Project Measures, KPIs & Calculated Fields</h1>
<hr>

<table>
  <tr>
    <!-- LEFT COLUMN -->
    <td width="50%" valign="top" style="padding-right:20px;">

  <h2>📌 Clicks</h2>
  <ul>
    <li>Number of times users clicked on the ad.</li>
    <li>A direct indicator of how attractive and engaging the campaign content is.</li>
  </ul>
  <hr>

  <h2>📌 Impressions</h2>
  <ul>
    <li>Total number of times the ad was displayed to users.</li>
    <li>Reflects the campaign’s overall reach and visibility.</li>
  </ul>
  <hr>

  <h2>📌 Engagement_Score</h2>
  <ul>
    <li>A quality interaction score (0–10) representing how strongly users engaged with the campaign.</li>
  </ul>
  <hr>

  <h2>📌 Calculated Field: CTR</h2>
  <pre><code>CTR = Clicks / Impressions</code></pre>
  <ul>
    <li>Measures how often people click after seeing an ad.</li>
    <li>Primary indicator of ad attractiveness.</li>
  </ul>

   <h2>📌 Calculated Field: Conversion Count</h2>
  <pre><code>Conversions = Clicks * Conversion_Rate</code></pre>
  <ul>
    <li>Total number of successful conversions.</li>
    <li>Key metric for funnel analysis.</li>
  </ul>
  <hr>

</td>

<!-- RIGHT COLUMN -->
<td width="50%" valign="top" style="padding-left:20px;">

  <h2>📌 Conversion_Rate</h2>
  <ul>
    <li>Percentage of users who completed a desired action after clicking.</li>
    <li>A core metric for evaluating campaign effectiveness.</li>
  </ul>
  <hr>

  <h2>📌 Acquisition_Cost</h2>
  <ul>
    <li>Total advertising spend for the campaign.</li>
    <li>Essential for calculating CAC, CPA, and ROI.</li>
  </ul>
  <hr>

  <h2>📌 ROI</h2>
  <ul>
    <li>Return on Investment — measures value generated per dollar spent.</li>
    <li>Higher ROI = more profitable campaign.</li>
  </ul>
  <hr>

  <h2>📌 Calculated Field: CPA</h2>
  <pre><code>CPA = Acquisition_Cost / (Clicks * Conversion_Rate)</code></pre>
  <ul>
    <li>Cost paid per successful conversion.</li>
    <li>Used to optimize budget allocation.</li>
  </ul>
  <hr>

  <h2>📌 Calculated Field: Engagement Rate</h2>
  <pre><code>Engagement Rate = Engagement_Score / Impressions</code></pre>
  <ul>
    <li>Shows how engaging the content is relative to its reach.</li>
  </ul>
  <hr>

 

</td>
  </tr>
</table>


-----
  <h1 align="center">📐 Calculated Fields Overview  </h1>

To enhance the analytical depth of the project, several calculated metrics were created directly in SQL, These fields (CTR, CPA, Conversion Count, Engagement Rate) provide essential visibility into campaign efficiency, cost-effectiveness, and user behavior.  
**They will later be used in Tableau to support data-driven insights and performance comparisons across campaigns.**


<img width="2066" height="826" alt="image" src="https://github.com/user-attachments/assets/9326fea0-8623-41ee-9119-9e52720ad6f5" />

<p align="center">
  <a href="EDA_SQL.txt">
    <img src="https://img.shields.io/badge/View Full 🔍 Exploratory Data Analysis with SQL %20File-ff9933?style=for-the-badge&logo=database&logoColor=white" />
  </a>
  </p>



-----

 <tr>
    <h1 align="center">Data Dimentions</h1>
   <p align="center">

Documenting the dimensions ensures a clear understanding of each campaign’s attributes—such as company, campaign type, target audience, channel, language, location, and duration. This validation step is essential before moving into performance analysis and KPI modeling.


<p align="center">
<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/775f688e-a8c4-42c2-ab4b-b8ba10e66a58" />
  </p>
  
  </p>

  </tr>


<img width="602" height="701" alt="Screenshot 2025-12-04 225326" src="https://github.com/user-attachments/assets/a5972385-0692-48a8-b787-aa84dc313570" />

  







