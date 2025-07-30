# Funnel Drop-Off Analysis Report

## 🎯 Objective

This project analyzes user behavior through an onboarding funnel to identify where users drop off and how to optimize conversions.

## 🧮 Funnel Stages

1. Account Created → Email Verified
2. Email Verified → KYC Submitted
3. KYC Submitted → KYC Approved
4. KYC Approved → First Deposit
5. First Deposit → First Transaction

## 📊 Key Metrics

| Funnel Step                         | Entered | Converted | Dropped | Conversion Rate (%) | Total Conversion (%) |
|------------------------------------|---------|-----------|---------|----------------------|-----------------------|
| Account Created → Email Verified   | 5000    | 4493      | 507     | 89.86%               | 89.86%                |
| Email Verified → KYC Submitted     | 4493    | 3496      | 997     | 77.81%               | 69.92%                |
| KYC Submitted → KYC Approved       | 3496    | 2928      | 568     | 83.75%               | 58.56%                |
| KYC Approved → First Deposit       | 2928    | 1934      | 994     | 66.05%               | 38.68%                |
| First Deposit → First Transaction  | 1934    | 1444      | 490     | 74.66%               | 28.88%                |

## 🌍 Segment-Based Drop-Off

### By Country (KYC Approved → First Deposit)

| Country | Conversion Rate (%) | Drop-off Rate (%) |
|---------|---------------------|-------------------|
| UK      | 64.39               | 35.61             |
| France  | 64.80               | 35.20             |
| India   | 66.10               | 33.90             |
| Nigeria | 66.67               | 33.33             |
| Germany | 68.28               | 31.72             |

### By Acquisition Channel

| Channel  | Conversion Rate (%) | Drop-off Rate (%) |
|----------|---------------------|-------------------|
| Organic  | 64.37               | 35.63             |
| Social   | 66.19               | 33.81             |
| Referral | 66.48               | 33.52             |
| Paid     | 67.23               | 32.77             |

## ⏱️ Time-Based Insights

- KYC approved in 1–6 hrs has highest conversion (~67.2%)
- KYC submitted within 1–6 hrs of signup also leads to better outcomes (~64.7%)
- Delays beyond 1 day reduce conversion to below 56%

## ✅ Recommendations

- Simplify the deposit experience post-KYC
- Encourage rapid KYC submission
- Tailor interventions for Organic traffic and users in UK/France
- Continuously monitor drop-off patterns and test improvements

