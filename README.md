# Financial-Transaction-Analysis-In-August 2026

## Project Overview
This project delivers a comprehensive data analytics and visualization solution for evaluating financial transaction logs from August 2026. Utilizing Power BI, the project implements a robust relational star schema to separate core operational metrics from risk-based exception monitoring. The analysis uncovers key transaction trends, payment channel dominances, customer segment behaviors, system friction points, and critical ledger anomalies to provide actionable business intelligence for operations and risk management teams.

## Executive Summary
This report provides an analytical evaluation of the August 2026 financial transaction dataset, encompassing 1,487 transactions, GHS 240.06K in total volume, and 299 unique customers. The analysis highlights a robust operational baseline driven primarily by Mobile App and USSD channels, while uncovering critical friction points—specifically systemic gateway timeouts and frequent insufficient balances. Furthermore, deep-dive exception monitoring isolated 9 severe ledger anomalies representing GHS 89.86K in mismatched balance movements. Strategic mitigation of these payment failures and the introduction of automated balance validation checks will recover processing revenue and safeguard platform integrity.

## Detailed Analytical Report & Task Deliverables
### A. Important Patterns & Transaction Trends
- **Mobile-First Dominance:** Mobile App transactions capture the largest volume share at GHS 115.03K (47.91%), followed by USSD at GHS 51.62K (21.5%), indicating that mobile channels drive nearly 70% of platform turnover. 
- **Consumer-Led Volume:** The Consumer segment generates the overwhelming majority of transaction value at GHS 170K, compared to Microbusinesses (GHS 51K) and SMEs (GHS 19K).
- **Weekly Transaction Flow:** Daily trends normalized from Monday to Sunday show volume peaks occurring early in the week (Tuesday at GHS 48K) and during the weekend (Saturday at GHS 42K). 

### B. Anomalies & Suspicious Behavior
- **Ledger Mismatch Anomalies:** Exactly 9 transactions were isolated in the exception monitoring tab, representing GHS 89.86K in total anomalous volume (averaging GHS 9.98K per transaction) where pre- and post-balances failed normal accounting logic.  
- **Gateway Risk Discrepancies:** Risk scoring across payment gateways highlights MobiLink carrying the highest average risk score (89.71), followed closely by KasaPay (80.51), requiring active transaction throttling.

### C. Failed-Transaction Patterns
- **Primary Friction Bottleneck:** Insufficient Funds dominates failure metrics with 90 occurrences, highlighting a major liquidity barrier for everyday platform users.
- **Network & Gateway Instability:** System-side performance issues compound user friction, led by 38 Network Timeout occurrences and 30 Awaiting Confirmation delays. 

### D. Customer & Merchant Insights
- **Customer Segment Distribution:** The Consumer segment leads platform activity by a wide margin at GHS 170K, followed by Microbusinesses (GHS 51K) and SMEs (GHS 19K), confirming that individual consumer P2P transactions form the core volume driver.

## Potential Business Opportunities
- **Pre-Transaction Balance Prompts:** Implementing automated balance validation before transfers execute to mitigate the 90 insufficient fund failures.  
- **Smart Gateway Routing:** Routing traffic away from high-risk gateways like MobiLink during peak volume windows.  

## Methodology
1. Cleaned raw transaction records to eliminate duplicates and standardize timestamps.
2. Modeled dimensional tables in Power BI for channels, segments, and risk scores using a relational star schema.
3. Designed a clean, dual-tab Power BI dashboard designed for executive oversight and risk exception monitoring:
- **Tab 1: Executive Overview**: Displays core KPIs (1.48K total transactions, GHS 240.06K volume, 299 unique customers) alongside interactive charts tracking daily transaction trends, volume share by payment channel, and customer segment distributions.
- **Tab 2: Risk & Exception Monitoring**: Focuses on operational governance, isolating transaction failure reasons, gateway risk scoring discrepancies, and the 9 severe ledger balance mismatches totaling GHS 89.86K.
  
<img width="734" height="401" alt="Transaction Overview" src="https://github.com/user-attachments/assets/829d7c98-febb-4ead-92f0-c6ae30925f62" />
<img width="734" height="401" alt="Exception   Failures" src="https://github.com/user-attachments/assets/967aa183-fd5e-4c34-845f-6551c5a44ded" />




  

## Limitations
Restricted to a single month (August 2026), preventing long-term seasonality analysis.  
Lack of customer demographic data (such as age or occupation) to analyze spending behaviors across different age groups.  

## Additional Data You Would Request
Transaction location data (regions or cities where transfers happen most often).  

## Future Roadmap (Next 72 Hours)

If I had another 72 hours, I would set up automated daily summary reports for operations teams, create a customer segmentation breakdown report, and refine merchant category groupings.
