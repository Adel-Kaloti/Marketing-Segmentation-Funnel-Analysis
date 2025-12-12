<p align="center">
  <img src="https://github.com/user-attachments/assets/7e22a616-a356-441d-9364-85d03d0ac62f" width="200" />
</p>

###   <h1 align="center">Marketing Segmentation & Funnel Analysis</h1>   

# Executive Summary

Full marketing analytics pipeline using SQL Server and Tableau to analyze campaigns performance, audience segments, channels and funnel KPIs (CTR, conversion rate, CPA, ROI), funnel benchmarks (863.4M impressions, 73.4M clicks, 4.7M conversions) and showed that Youtube and women aged 35–44 in Los Angeles are the most profitable segments.

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

---

# CPA by Target Audience

<p align="center">
<img width="400" height="400" alt="Screenshot 2025-12-04 225326" src="https://github.com/user-attachments/assets/a5972385-0692-48a8-b787-aa84dc313570" />
  </p>
  
### 🎯Insights

- **Men 18–24 are the most expensive segment**, with an average CPA of **$4.7K**, almost **3x higher** than the overall “All Ages” benchmark (~$1.7K).
- **Women 35–44 are the most cost-efficient audience**, with an average CPA of only **$0.8K**, making them a strong candidate for budget scaling.
- **Men 25–34 also perform efficiently** at around **$1.0K CPA**, staying below the overall average and offering a cheaper alternative to Men 18–24.
- **Women 25–34 sit in the middle** (~**$2.3K CPA**), suggesting that performance is acceptable but less efficient than older women or Men 25–34.

----


# 📈 CTR & Conversion Rate over Time

<p align="center">
<img width="800" height="400" alt="Screenshot 2025-12-04 225311" src="https://github.com/user-attachments/assets/0189b13e-4868-46ef-a3f1-742e4ebcf935" />
  </p>
  
### 🎯Insights

- **CTR is consistently strong** throughout the year, fluctuating in a narrow band between **11.7%–12.3%**, which indicates stable ad relevance and engagement.
- **Mid-year spike in July** shows the **highest CTR at ~12.3%**, suggesting a particularly successful campaign or creative during that period.
- **Conversion rate starts and ends strong** (≈**5.4% in Jan** and **5.4% in Nov**), with a softer period in the middle of the year, hinting that later optimizations helped recover efficiency.
- The **gap between CTR and conversion rate widens mid-year**, implying that while people still clicked, fewer completed actions — a signal to review landing pages, offers, or audience targeting for those months.

-------

# 🖱️ Share of Clicks by Channel

<p align="center">
<img width="400" height="400" alt="Screenshot 2025-12-04 225302" src="https://github.com/user-attachments/assets/b26da461-b0f0-4d07-87d9-46236552bd1a" />
  </p>

### 🎯Insights

- **YouTube is the top traffic driver**, capturing **27.3% of all clicks**, followed by **Google Ads (23.7%)** and **Instagram (21.0%)** — together these three channels generate **over 70% of total clicks**.
- **Social & video platforms dominate** (YouTube, Instagram, Facebook) compared to owned/low-intent channels (Website, Email), confirming that discovery and scroll-based environments are the primary click source.
- **Website (6.4%) and Email (9.2%) contribute a smaller share**, but can still be valuable as higher-intent channels — good candidates for nurturing and retargeting users initially acquired via YouTube and Google Ads.

-----


# 🎯 Audience × Channel Performance

<p align="center">
<img width="1000" height="450" alt="Screenshot 2025-12-04 225333" src="https://github.com/user-attachments/assets/2e73eeb1-5a96-475d-87ed-adf135e08f08" />
  </p>

### 🎯Insights

- **Women 35–44 are the strongest segment overall**, especially on **YouTube (538K conv)** and **Google Ads (460K conv)** — these cells are the darkest on the heatmap and should be top priority for budget allocation.
- **Men 25–34 also perform very well on Google Ads and Instagram** (≈379K and 322K conversions), making them a solid secondary segment for performance campaigns.
- **Email and Website are consistently weaker across all audiences**, suggesting they work better as support / retargeting channels rather than primary acquisition drivers.
- The matrix clearly shows that **performance is not uniform**: each audience has 1–2 “hero channels”, so optimizing budgets by **Audience × Channel** (instead of one-size-fits-all) can unlock additional conversions.


# 📍 ROI by Location

<p align="center">

<img width="600" height="400" alt="Screenshot 2025-12-04 225319" src="https://github.com/user-attachments/assets/76c0f247-429b-43a4-93e2-fda6d71470cb" />
  </p>

### 🎯Insights

- **Los Angeles and New York lead the map**, with ROI of **4.8%** and **4.5%** – these cities generate the strongest return per dollar spent and should keep or even receive extra budget.
- **Chicago is mid-tier at 3.5% ROI**, performing positively but not at the same efficiency level as the top two markets.
- **Miami (1.5%) and Houston (0.5%) are clear under-performers**, indicating either higher acquisition costs, weaker conversion rates, or both.
- Reallocating part of the spend from **Miami & Houston → LA & New York** (and testing new creative / targeting in low-ROI cities) is a direct opportunity to improve overall profitability.




#  🔻 Conversion Funnel – From Impressions to Conversions

<p align="center">
  
<img width="300" height="600" alt="Screenshot 2025-12-04 225251" src="https://github.com/user-attachments/assets/7d6d7d9a-18d4-4c5b-b0fe-98b78ebe2c91" />
  </p>

### 🎯Insights

- **Top of funnel:** `863.42M` impressions generated overall awareness.
- **Engagement drop (CTR):** Only `73.39M` clicks, which is ~`8.5%` Click-Through Rate. There is a large audience seeing ads but not engaging.
- **Bottom of funnel (Conversions):** Just `4.71M` conversions:
  - ~`6.4%` of clicks convert.
  - Only ~`0.55%` of total impressions turn into conversions.

**Takeaways & Actions**

- The **biggest loss** happens between **Impressions → Clicks** → test new creatives, clearer CTAs, and better audience targeting to lift CTR.
- The **Clicks → Conversions** step is still relatively efficient but has room to improve via:
  - faster landing pages,
  - simplified forms/checkout,
  - more aligned ad–landing page messaging.
- Even a **+1–2% improvement in CTR or post-click conversion rate** would translate into **hundreds of thousands of additional conversions** given the large impression volume.

---------
# 🤝 Stakeholder Recommendations

1. **Reallocate budget to high-value audiences**  
   Cut spend on **Men 18–24** (highest CPA ≈ $4.7K) and shift budget toward  
   **Women 35–44, Men 25–34 and “All Ages”** segments where CPA is closer to **$0.8–2K**.

2. **Prioritize top-performing channels**  
   Use **YouTube and Google Ads as primary acquisition channels**, supported by  
   **Instagram** for key segments. Limit prospecting spend on **Website & Email**  
   and keep them mainly for nurturing/retention.

3. **Focus on profitable locations**  
   Maintain or increase investment in **Los Angeles and New York** (ROI ≈ 4.5–4.8%)  
   and gradually reduce spend in **Houston and Miami** unless there is a strategic reason.

4. **Tighten the conversion funnel**  
   The big drop from **Impressions → Clicks → Conversions** indicates friction.  
   Run continuous A/B tests on **creatives (CTR)** and **landing pages (CVR)** with a target  
   of **+10–15% improvement in click-through and conversion rates**.

5. **Make the dashboard a decision ritual**  
   Use this Tableau dashboard in a **monthly performance review** to decide  
   which audiences, channels and locations get **more budget, less budget, or new tests**,  
   with **CPA and ROI** as the primary decision metrics.

--------
### 🧰 Tools Kit

<p align="center">
  <img src="tools.png" width="600" />
</p>

<p align="center">
  <!-- Tableau button -->
  <a href="https://public.tableau.com/app/profile/adel.kaloti1" target="_blank">
    <img src="https://img.shields.io/badge/View%20on%20Tableau-006699?style=for-the-badge&logo=tableau&logoColor=white" />
  </a>

  <!-- SQL file button -->
  <a href="EDA_SQL.txt">
    <img src="https://img.shields.io/badge/View%20SQL%20File-ff9933?style=for-the-badge&logo=database&logoColor=white" />
  </a>
</p>



