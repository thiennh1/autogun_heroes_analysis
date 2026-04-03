# Autogun Heroes: Run and Gun Analytics 🔫📊

## Project Description
In the highly competitive mobile gaming market, understanding player behavior is the key to sustainable growth. The Autogun Heroes Analysis project was developed to transition from basic metric tracking to "behavioral diagnostics." By analyzing granular event data, this project aims to help Game Operations and Product Teams identify exactly where players lose interest and which segments drive the core economy.

The primary objective is to provide a comprehensive visual tool to monitor the "health" of the game’s ecosystem, optimize the onboarding funnel, and implement data-driven monetization strategies to maximize both IAP and IAA revenue.

## Business Questions
This project is designed to address the following key business problems:
1. **Onboarding Efficiency:** Where is the primary bottleneck in the tutorial, and why are we losing nearly 60% of players at the "Claim Reward" step?
2. **Retention Barriers:** Which specific stages act as "difficulty walls" that trigger mass churn?
3. **Monetization Polarization:** How dependent is the game on "Whale" players (VIPs), and why are active segments like "Frequent" players yielding zero revenue?
4. **Engagement Quality:** Is there a correlation between high win rates and long-term player retention, or is the game becoming too easy and predictable?
5. **Re-activation Strategy:** How can we accurately identify "At-Risk" segments to trigger automated win-back campaigns before they churn?

## Dataset
The analysis is powered by four primary event-driven data sources representing the complete player lifecycle:
* **Tutorial:** Tracking completion rates and drop-off points in the first-time user experience.
* **Level End:** Recording stage progression, win/loss ratios, and difficulty spikes.
* **Ad Impressions (IAA):** Monitoring ad engagement frequency and revenue contribution.
* **In-App Purchases (IAP):** Granular transaction records for calculating player lifetime value and conversion.
* **Cost:** Includes information about daily expenses.
Data Integration Note: To optimize performance and create a unified analytical view, the four primary event tables (in_app_purchase, tutorial, level_end, and ad_impression) have been merged into a single consolidated table named overview_data.
<img width="607" height="458" alt="image" src="https://github.com/user-attachments/assets/f2ce789b-5fa4-42f4-b3ff-3860956a1fa9" />

## Analysis Approach
The dashboard employs a top-down analytical funnel across 4 specialized tabs:
1. **Overview:** A macro view of daily active users (DAU), global revenue distribution, and platform performance.
2. **Finance:** Deep dive into ARPU/ARPPU trends and the revenue share between IAP and IAA.
3. **Customer Journey:** A micro-level analysis of the tutorial funnel and stage-by-stage churn rates.
4. **Segmentation (RFM):** Behavioral profiling of the user base into 6 strategic tiers to guide personalized marketing.

## Key Metrics
* **Active Users:** The number of unique players who engaged with the game within a specific timeframe (Daily or Weekly). This metric reflects the overall scale and health of the player community.
* **Buyer Rate:** The percentage of unique players who have made at least one IAP transaction.
* **Viewer Rate:** The percentage of active players who interact with in-game advertisements. It is a primary indicator of engagement with the Integrated Advertising (IAA) system.
* **ROAS (Return on Ad Spend):** A marketing effectiveness metric that calculates the revenue generated for every dollar spent on User Acquisition (UA) campaigns.
* **Profit Margin:** The percentage of total revenue that remains as net profit after subtracting all operational and marketing costs. This indicates the financial sustainability and cost-efficiency of the game's operations.
* **Retention Day 1:** The percentage of players who return exactly 24 hours after their first session.
* **AVG Session**: The mean number of play sessions per user, indicating daily engagement.
* **ARPU (Average Revenue Per User):** Calculated as Total Revenue divided by the total number of Active Users. This measures the general monetization efficiency across the entire player base, including non-payers.
* **ARPPU (Average Revenue Per Paying User):** Calculated as Total Revenue divided by the number of unique "Buyers" (paying users). This highlights the spending power and value of the converted customer segment.
* **Tutorial Drop Rate**: The percentage of users who exit the game at specific tutorial steps.
* **Segment Monetary:** The total financial contribution of a specific RFM group (e.g., VIP vs. Big Spender).

## Key Insights
* **The Tutorial "Reward" Bottleneck:** A massive 58% drop-off occurs at Step 1000 (Claim Reward). This suggests a critical technical bug or a "flow-break" in the reward UI that prevents players from entering the core game loop.
<img width="1331" height="435" alt="image" src="https://github.com/user-attachments/assets/5e778f19-7e6d-4fe0-8a45-331460ff9be0" />

* **The Whale Dependency:**  Nearly 100% of the game’s revenue is generated by only two segments: VIP (5.3K) and Big Spenders (4.2K). Every other segment, including highly active "Frequent" players, currently generates ~0.06%, highlighting a missed opportunity for micro-transactions or "Starter Packs."
<img width="960" height="483" alt="image" src="https://github.com/user-attachments/assets/452536e1-5cba-4d71-9aed-2ce6d57c3c58" />

* **The "At-Risk" Tsunami:** The largest single segment is At-Risk (9.4K users). These players have a high historical value but haven't engaged recently. This represents a huge potential revenue loss if not addressed immediately.
<img width="1301" height="479" alt="image" src="https://github.com/user-attachments/assets/fc00eb71-f62a-4220-b1ee-5b5ddc953941" />

* **Difficulty Walls:** Stage 913 acts as a severe "Churn Wall" with an 80%+ drop rate, indicating that the difficulty curve spikes too sharply, frustrating players instead of challenging them.
<img width="765" height="477" alt="image" src="https://github.com/user-attachments/assets/6f0c223f-d747-478a-a6ba-84e8f2c56ec7" />

## Strategic Recommendations
1. **Immediate Tutorial Fix:** Redesign or debug Step 1000 (Claim Reward). Bridging this 58% gap would effectively double the number of players entering the actual game.
2. **IAP Conversion Hook:** Implement a "24-Hour Starter Bundle" priced at $0.99 for "Recent" and "Frequent" players to break the $0 revenue barrier in those segments.
3. **Automated Win-Back System:** Trigger personalized push notifications with high-value rewards specifically for the At-Risk and Big Spender segments to pull them back into the active loop.
4. **Difficulty Re-balancing:** Adjust the difficulty at Stage 101 and Stage 913. Smoothing out these "Churn Walls" will significantly improve D3 and D7 retention.

## Tools & Techniques Used
* **Excel**
* **Power BI**
* **SQL**

## Author
**Nguyen Huu Thien**
