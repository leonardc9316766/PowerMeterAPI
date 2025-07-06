# ⚡ PowerMeterAPI

> 🧠 Route your API traffic to the cleanest electricity grid in real-time.  
> 🚀 Infrastructure just got smarter — and quietly cleaner.

---

## 🧩 What It Does

PowerMeterAPI is a **real-time, carbon-aware traffic router**. It dynamically selects the cleanest electricity region (starting with California ISO) for your API requests — improving infrastructure efficiency, reducing emissions, and avoiding latency spikes caused by grid congestion.

This is not a report or dashboard. It’s a live routing layer that actually makes infrastructure decisions smarter, cleaner, and more resilient.

---

## 🌎 Why It Matters

Most API traffic today is routed based on latency or availability — but not **energy cleanliness** or **grid stability**.

- 🟢 Clean grids = faster, more stable infrastructure
- 🔴 Dirty grids = legacy risk, latency spikes, hidden cost

By routing traffic based on real-time CO₂ intensity, you unlock smarter infrastructure decisions with no code changes.

---

## 🔧 How It Works

1. You send a request to `https://api.powermeterapi.dev/route`
2. The system evaluates real-time carbon intensity (currently for CAISO)
3. It returns the cleanest region for your API to target
4. (Coming soon: Direct proxy routing and multi-cloud auto-routing)

---

## 📦 Plans & Pricing

| Tier      | Monthly Price | API Calls Included | Regions       |
|-----------|---------------|--------------------|----------------|
| Dev       | $49           | 50,000             | California ISO |
| Core      | $400          | 500,000            | CAISO + [Beta regions] |
| Scale     | $1,250        | 2M+                | Global (coming soon) |

🔓 Use promo code `POWERMETER30` for a **free 30-day Dev Tier trial**

---

## 🚀 Quickstart

```bash
curl -X POST https://api.powermeterapi.dev/route \
     -H "Authorization: Bearer YOUR_API_KEY" \
     -H "Content-Type: application/json" \
     -d '{"source_region": "us-west1", "payload_size": 128}'

Response:

{
  "chosen_region": "CAISO",
  "co2_g_per_kwh": 92,
  "total_emissions_g": 11.78,
  "alternatives": [
    { "region": "CAISO", "co2_g_per_kwh": 92 },
    { "region": "BPA", "co2_g_per_kwh": 115 }
  ]
}

📚 Docs

📖 Full documentation: https://powermeterapi.dev/docs
💬 Support: powermeterapi@gmail.com
🔗 App dashboard: https://app.powermeterapi.dev

🛠 Tech Stack
	•	Python + FastAPI
	•	Supabase for DB
	•	Stripe for billing & usage
	•	CAISO live grid data feed
	•	Future: Multi-region routing, SDKs, and Terraform plugins

🌱 Roadmap
	•	CAISO real-time support
	•	Developer dashboard + API key issuance
	•	Tiered billing with metered usage
	•	Multi-region rollout (ERCOT, PJM, etc.)
	•	Auto-proxy routing mode (infrastructure-native)
	•	Open-source lightweight router SDK

💡 Who It’s For
	•	Cloud Ops & SRE teams optimizing API delivery
	•	Devs building ESG-aligned infrastructure
	•	Platforms needing reliable, low-carbon delivery logic

🧠 Made by humans, for machines.

PowerMeterAPI turns real-time energy intelligence into actionable infrastructure routing
