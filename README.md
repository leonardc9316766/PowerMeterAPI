PowerMeterAPI Quickstart
Instantly track and log energy usage & carbon emissions by API

What is PowerMeterAPI?
A drop-in API that lets you track, log, and audit energy usage (kWh) and carbon emissions (CO₂) for any cloud, AI, or GPU workload. Every API call returns a verifiable, audit-ready receipt.

Get Started in 60 Seconds
Step 1 — Sign Up & Get Your API Key
Go to app.powermeterapi.dev
Create an account and copy your API key from the dashboard
Step 2 — Make Your First Request
Paste this command into your terminal (replace the key with your actual API key):
curl -H "X-API-Key: pm_live_your_actual_key_here" \
     https://9ebd978c-21d3-4246-8762-5d7c801619a8-00-cldu5hvo6tqm.picard.replit.dev/v1/usage/summary
You’ll get a response like:
{
  "kwh": 0.0,
  "co2_g": 0.0,
  "fee_usd": 0.0,
  "plan": "dev"
}
Step 3 — Track a Job (optional)
Submit energy usage from a job or workload:
curl -X POST \
  -H "X-API-Key: pm_live_your_actual_key_here" \
  -H "Content-Type: application/json" \
  -d '{"device_id":"test-01","watt_seconds":10000,"geo_iso":"US","scope":"compute"}' \
  https://9ebd978c-21d3-4246-8762-5d7c801619a8-00-cldu5hvo6tqm.picard.replit.dev/v1/report
Step 4 — Get Your Audit-Ready Receipts
List all carbon receipts for your jobs:
curl -H "X-API-Key: pm_live_your_actual_key_here" \
     https://9ebd978c-21d3-4246-8762-5d7c801619a8-00-cldu5hvo6tqm.picard.replit.dev/v1/receipts









Need help? Email powermeterapi@gmail.com

