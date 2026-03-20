# ShieldGig: AI-Powered Income Resilience for the Gig Economy

## 📌 1. The Problem: The "Safety Gap"
Gig workers—the backbone of our urban economy—operate without a financial floor. When extreme weather (monsoons/heatwaves) or hazardous pollution levels hit, their income drops to zero. Traditional insurance is too slow, too expensive, and focuses on accidents rather than the daily reality of income loss.

## 👥 2. Target Persona
**The Urban Delivery Partner:** A 24-year-old Swiggy/Zomato rider in a Tier-1 city.
**The Pain Point:** "If I don't ride during the heavy rains, I can't pay my weekly bike EMI. If I do ride, I risk my health and my vehicle."

## 🚀 3. Our Solution: ShieldGig
ShieldGig is a **Parametric Insurance Platform**. It doesn't wait for a human to file a claim. By using AI to monitor real-time environmental data, the system identifies "Work-Stop" events and automatically issues payouts to workers’ wallets.

## ⚙️ 4. The Workflow
1. **Enrollment:** User syncs their delivery ID via our React dashboard.
2. **Dynamic Premium:** AI analyzes the 7-day weather forecast for the user's specific region to set a micro-premium (e.g., ₹20 for the week).
3. **Live Monitoring:** Our Backend (FastAPI) polls Weather and AQI APIs every 60 minutes.
4. **Trigger Event:** If rainfall > 50mm or AQI > 350, the "Parametric Trigger" is activated.
5. **Fraud Filter:** The AI engine verifies the user's GPS history via a heatmap to ensure they were actually active and in the affected zone.
6. **Instant Credit:** The payout is pushed to the user’s account via an automated payment gateway.

## 💰 5. Weekly Pricing Model (Risk-Adjusted)
| Zone Risk | Weekly Premium | Payout Triggered |
| :--- | :--- | :--- |
| **Low (Clear Skies)** | ₹15 | ₹300 / day of disruption |
| **Medium (Monsoon Season)** | ₹25 | ₹450 / day of disruption |
| **High (Heatwave/High AQI)** | ₹35 | ₹600 / day of disruption |

## 📡 6. Parametric Triggers (Core Logic)
We bypass manual intervention using code-based logic:
- **Rain:** Cumulative 40mm+ within any 4-hour window.
- **Heat:** Peak temperature sustained > 42°C for 3+ hours.
- **Air Quality:** AQI > 300 for 5+ hours (Urban zones).

## 🧠 7. AI & Security
- **Risk Modeling:** Predicting premium volatility based on historical weather patterns.
- **Integrity Guard:** Our "Fraud Detection" module cross-references delivery app activity logs with real-time GPS pings to prevent "couch-claiming."

## 🛠️ 8. Tech Stack
- **Frontend:** React / Vite (Mobile-Responsive)
- **Backend:** FastAPI (Python)
- **Database:** MongoDB
- **Intelligence:** Scikit-Learn (Risk) & Geopy (GPS Validation)
