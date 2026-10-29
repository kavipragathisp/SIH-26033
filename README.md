# Smart India Hackathon Workshop

**Date:** 23/10/2026
**Reference Number:** 26010384
**Name:** Kavi Pragathi S P

## Problem Title

SIH 26033: Multiple intermediaries reduce farmers' earnings and increase consumer prices.

## Problem Creator's Organization

Ministry of Consumer Affairs, Food & Public Distribution

## Theme

Agriculture, FoodTech & Rural Development

## Problem Description

Expected Solution: Create a digital marketplace that:

- Connects farmers/FPOs directly with consumers and bulk buyers.
- Provides logistics support.
- Uses AI for demand forecasting and route optimization.

Benefits:

- Better prices for farmers.
- Lower prices for consumers.
- Reduced supply chain inefficiencies.

## Proposed Solution

A single digital marketplace, **FarmBridge AI**, lets farmers and FPOs sell straight to consumers and bulk buyers. The main aim is to help farmers earn a fair price for their hard work and make agricultural products more affordable for consumers. Built-in logistics and AI for demand forecasting and route planning take over the work that middlemen do today, so their margin goes back to farmers and consumers and the whole process becomes more efficient.

At present, agricultural products often pass through several intermediaries before reaching consumers. Each intermediary may add extra costs, which can reduce the profit received by farmers and increase the final price paid by consumers. FarmBridge AI aims to reduce this gap by allowing farmers to sell their products directly through an online marketplace.

### 1. Detailed explanation of the proposed solution

FarmBridge AI will provide a simple platform where farmers can list their products, mention their prices, and update the available quantities. Consumers and bulk buyers can browse the products, compare prices, and place orders directly.

The platform will include the following features:

- **Seller side:** farmers and FPOs list produce with crop, quantity, grade, harvest date and photos. They can do this by voice in their regional language, through a lightweight mobile app, or through WhatsApp and IVR where connectivity is poor.
- **Buyer side:** households buy single items or weekly baskets. Bulk buyers (retailers, restaurants, hostels, government canteens, processors) place standing or one-off orders and bid on lots.
- **Transparent pricing:** every listing shows the farmer's ask next to the current mandi reference price. Each order shows the farmer's share of what the buyer pays.
- **Logistics support:** FPO-run collection points aggregate small lots, and partner transporters carry them to city hubs and doorsteps. Cold-chain options cover perishables.
- **Payments:** buyers pay by UPI. Money is held until delivery is confirmed, then released directly to the farmer's bank account.
- **AI layer:** demand forecasting tells farmers what to harvest and when, and route optimization cuts delivery time, fuel and spoilage.

### 2. How it addresses the problem

| Cause of the problem | How FarmBridge AI responds |
| --- | --- |
| Several traders and agents each add a margin between farm and plate | Direct farmer/FPO-to-buyer orders, with only logistics and a small platform fee in between |
| Farmers do not know buyer demand or fair prices, so they accept what traders offer | Forecasts and price references shown before harvest; farmers can set their own ask |
| Small lots are costly to move, which forces farmers to sell locally at low prices | FPO aggregation and shared transport combine small lots into full loads |
| Spoilage and delays between farm and market | Optimized routes, shorter chains, cold-chain partners |
| Delayed or uncertain payment from traders | Escrow payment released on delivery, straight to the farmer's account |

### 3. Innovation and uniqueness

- **Demand-first harvest planning:** buyers' standing orders and forecasts are shown to farmers before harvest, so supply is matched to demand instead of dumped on a mandi.
- **Farmer-share meter:** every order shows how much of the price reached the farmer. This builds trust on both sides and gives the Ministry a live measure of intermediary cost.
- **Pooled logistics with return-load matching:** FPO collection points and trucks returning empty from cities are matched, which lowers transport cost per kilogram.
- **Built for rural access:** voice and regional-language input, offline-first design, and WhatsApp/IVR access, so a farmer without a smartphone can still use it.
- **Built on public data:** it uses open government data (mandi prices, weather, FPO registry) instead of building everything from scratch.

## Technical Approach

The platform is a mobile-first web and app system on a cloud backend, with an AI service for forecasting and routing, and data feeds from public agriculture sources.

### 1. Technologies to be used

| Layer | Technology | Purpose |
| --- | --- | --- |
| Farmer and buyer apps | React Native or Flutter app, plus a React web app | One codebase for Android, iOS and web; offline-first listings |
| Low-access channels | WhatsApp Business API, IVR, speech-to-text in regional languages | Farmers without smartphones can list produce and check prices |
| Backend | Python (FastAPI) or Node.js REST services, PostgreSQL with PostGIS, Redis | Listings, orders, user accounts, location queries |
| AI and ML | Python, scikit-learn, XGBoost or Prophet for demand and price forecasting; Google OR-Tools for route optimization | Demand forecasts, price suggestions, delivery routes |
| Maps and tracking | OpenStreetMap or Google Maps API, GPS tracking on partner vehicles | Route display and live delivery status |
| Payments | UPI gateway with escrow-style hold and release | Safe, direct payment to farmers |
| Data sources | Agmarknet and e-NAM mandi prices, IMD weather, FPO registry | Price references and forecasting inputs |
| Hosting | Cloud (AWS, Azure or MeitY-empanelled), Docker containers | Scalable, secure deployment |

### 2. Methodology and process for implementation

1. **Pilot design:** choose one district with active FPOs and one nearby city, and 4 to 5 high-volume crops such as tomato, onion, potato and leafy greens.
2. **Core build:** listings, ordering, escrow payment and FPO dashboard first, then the buyer app.
3. **Logistics integration:** onboard partner transporters, set up FPO collection points, and add delivery tracking.
4. **AI layer:** begin with price and demand baselines from historical mandi data, then retrain on platform orders as they accumulate.
5. **Pilot run and feedback:** measure farmer price, buyer price, delivery time and spoilage against the traditional mandi route.
6. **Scale-up:** extend to more districts, crops and bulk buyers.

The diagram below shows how an order moves through the system.

![FarmBridge AI order flow](diagram.png)

## Feasibility and Viability

The idea is feasible because its building blocks already exist: UPI payments, a large FPO network, e-NAM and open mandi price data. The hard parts are trust, logistics cost and getting buyers and sellers onto the platform together.

### 1. Analysis of the feasibility

| Dimension | Assessment |
| --- | --- |
| Need | An [RBI survey of rabi crops](https://www.rbi.org.in/Scripts/BS_ViewBulletin.aspx?Id=23198) put farmers' share of the consumer price at 40% to 67%, and [fruits and vegetables sat at the lower end, 40% to 63%](https://www.drishtiias.com/daily-updates/daily-news-analysis/farmers-earning-in-agri-produce-rbi). An RBI study of tomato, onion and potato found [farmers' shares of 33%, 36% and 37%](https://tribuneindia.com/news/farmers-lose-out). |
| Proof that direct selling works | An [RBI bulletin](https://www.rbi.org.in/scripts/bs_viewbulletin.aspx?id=18527) cites a government study of direct farmer-to-consumer markets (Uzhavar Sandhai in Tamil Nadu, Rythu Bazaar in Andhra Pradesh): farmers earned 15% to 40% more than wholesale prices, and consumers paid 15% to 30% less than retail. |
| Supply side | The government's [scheme to form 10,000 FPOs](https://www.drishtiias.com/daily-news-analysis/formation-promotion-of-10-000-fpos) gives ready-made aggregation points. By March 2026, [4,724 FPOs were registered on e-NAM](https://visionias.in/current-affairs/news-today/2026-04-14/economy/e-nam-completes-10-years-of-transforming-agricultural-trade). |
| Data | [Agmarknet](https://data.gov.in/resource/current-daily-price-various-commodities-various-markets-mandi) publishes daily wholesale prices (maximum, minimum and modal) through the open data portal, which feeds price references and forecasting. |
| Technology | Mobile apps, UPI, maps and standard ML libraries are mature and low-cost. No new hardware is required. |
| Revenue | A small commission on orders, a delivery fee, and subscriptions from bulk buyers. Farmers pay nothing to list. |
| Regulation | The platform must follow state APMC rules, GST and food-safety norms. It is designed to work with e-NAM, not against it. |

### 2. Potential challenges and risks, and 3. Strategies to overcome them

| Challenge or risk | Strategy |
| --- | --- |
| Low digital literacy and weak connectivity in villages | Voice and regional-language input, offline-first app, WhatsApp and IVR access, and FPO staff acting as local help agents |
| Buyers and sellers must both be present from day one | Start with one district and a few crops; sign up bulk buyers first so farmers see real demand |
| Quality disputes between farmer and buyer | Grading at FPO collection points, photo and weight records at pickup, ratings, and a refund process tied to escrow |
| High transport and cold-chain cost for perishables | Pool lots at FPO hubs, match return loads, and use route optimization; add cold chain only for high-value, short-life crops |
| Forecasts that are wrong because of weather or price swings | Show forecasts as ranges, retrain on live orders, and let farmers see the reasoning |
| Resistance from traders and local mandi interests | Invite traders to join as verified buyers and logistics partners, and integrate with e-NAM |
| Payment fraud and data privacy | KYC for sellers, escrow payments, encrypted data storage, and compliance with India's data protection law |

## Impact and Benefits

By shortening the chain between farm and buyer, FarmBridge AI moves money from intermediary margins to farmers and consumers, and makes prices and supply easier to see for everyone.

### 1. Potential impact on the target audience

- **Small and marginal farmers and FPOs:** a larger share of the consumer price, earlier and more certain payment, and demand and price information before harvest.
- **Consumers:** fresher produce at lower prices, with clear information on where it came from and how much of the price reached the farmer.
- **Bulk buyers (retailers, restaurants, institutions, processors):** reliable supply of graded produce, standing orders, and fewer rounds of negotiation.
- **Ministry and State governments:** a live view of prices, arrivals and the farmer's share, which supports price monitoring and policy decisions.

### 2. Benefits of the solution

**Economic benefits:**

- Improved market access for farmers.
- Potential reduction in unnecessary supply-chain costs.
- More transparent prices for buyers.

**Social benefits:**

- Better access to digital agricultural services.
- More opportunities for small farmers.
- Improved access to market information.

**Environmental benefits:**

- Reduced unnecessary travel through route optimization.
- Potential reduction in fuel consumption.
- Better demand planning to help reduce food wastage.

## Research and References

**Government and data sources**

- Ministry of Agriculture and Farmers Welfare, Government of India: https://agriwelfare.gov.in/
- e-NAM – National Agriculture Market: https://www.enam.gov.in/
- Open Government Data Platform India: https://www.data.gov.in/
- AGMARKNET – Agricultural Market Information: https://agmarknet.gov.in/
- Food and Agriculture Organization (FAO): https://www.fao.org/

**Research on farmers' share and direct selling**

- [RBI Bulletin: Dynamics of agriculture supply chain, rabi crops](https://www.rbi.org.in/Scripts/BS_ViewBulletin.aspx?Id=23198)
- [RBI Bulletin: Supply Chain Dynamics and Food Inflation in India](https://www.rbi.org.in/scripts/bs_viewbulletin.aspx?id=18527)
- [Drishti IAS: summary of the RBI survey on farmers' earnings](https://www.drishtiias.com/daily-updates/daily-news-analysis/farmers-earning-in-agri-produce-rbi)
- [The Tribune: Farmers lose out](https://tribuneindia.com/news/farmers-lose-out)
- [Vision IAS: e-NAM completes 10 years](https://visionias.in/current-affairs/news-today/2026-04-14/economy/e-nam-completes-10-years-of-transforming-agricultural-trade)
- [Drishti IAS: Formation and Promotion of 10,000 FPOs](https://www.drishtiias.com/daily-news-analysis/formation-promotion-of-10-000-fpos)

**Technology**

- OpenStreetMap – Mapping Data: https://www.openstreetmap.org/
- OSRM – Routing: https://project-osrm.org/
- Google OR-Tools – Route Optimization: https://developers.google.com/optimization
- Scikit-learn – Machine Learning Tools: https://scikit-learn.org/stable/# Smart India Hackathon Workshop

**Date:** 23/10/2026
**Reference Number:** 26010384
**Name:** Kavi Pragathi S P

## Problem Title

SIH 26033: Multiple intermediaries reduce farmers' earnings and increase consumer prices.

## Problem Creator's Organization

Ministry of Consumer Affairs, Food & Public Distribution

## Theme

Agriculture, FoodTech & Rural Development

## Problem Description

Expected Solution: Create a digital marketplace that:

- Connects farmers/FPOs directly with consumers and bulk buyers.
- Provides logistics support.
- Uses AI for demand forecasting and route optimization.

Benefits:

- Better prices for farmers.
- Lower prices for consumers.
- Reduced supply chain inefficiencies.

## Proposed Solution

A single digital marketplace, **FarmBridge AI**, lets farmers and FPOs sell straight to consumers and bulk buyers. The main aim is to help farmers earn a fair price for their hard work and make agricultural products more affordable for consumers. Built-in logistics and AI for demand forecasting and route planning take over the work that middlemen do today, so their margin goes back to farmers and consumers and the whole process becomes more efficient.

At present, agricultural products often pass through several intermediaries before reaching consumers. Each intermediary may add extra costs, which can reduce the profit received by farmers and increase the final price paid by consumers. FarmBridge AI aims to reduce this gap by allowing farmers to sell their products directly through an online marketplace.

### 1. Detailed explanation of the proposed solution

FarmBridge AI will provide a simple platform where farmers can list their products, mention their prices, and update the available quantities. Consumers and bulk buyers can browse the products, compare prices, and place orders directly.

The platform will include the following features:

- **Seller side:** farmers and FPOs list produce with crop, quantity, grade, harvest date and photos. They can do this by voice in their regional language, through a lightweight mobile app, or through WhatsApp and IVR where connectivity is poor.
- **Buyer side:** households buy single items or weekly baskets. Bulk buyers (retailers, restaurants, hostels, government canteens, processors) place standing or one-off orders and bid on lots.
- **Transparent pricing:** every listing shows the farmer's ask next to the current mandi reference price. Each order shows the farmer's share of what the buyer pays.
- **Logistics support:** FPO-run collection points aggregate small lots, and partner transporters carry them to city hubs and doorsteps. Cold-chain options cover perishables.
- **Payments:** buyers pay by UPI. Money is held until delivery is confirmed, then released directly to the farmer's bank account.
- **AI layer:** demand forecasting tells farmers what to harvest and when, and route optimization cuts delivery time, fuel and spoilage.

### 2. How it addresses the problem

| Cause of the problem | How FarmBridge AI responds |
| --- | --- |
| Several traders and agents each add a margin between farm and plate | Direct farmer/FPO-to-buyer orders, with only logistics and a small platform fee in between |
| Farmers do not know buyer demand or fair prices, so they accept what traders offer | Forecasts and price references shown before harvest; farmers can set their own ask |
| Small lots are costly to move, which forces farmers to sell locally at low prices | FPO aggregation and shared transport combine small lots into full loads |
| Spoilage and delays between farm and market | Optimized routes, shorter chains, cold-chain partners |
| Delayed or uncertain payment from traders | Escrow payment released on delivery, straight to the farmer's account |

### 3. Innovation and uniqueness

- **Demand-first harvest planning:** buyers' standing orders and forecasts are shown to farmers before harvest, so supply is matched to demand instead of dumped on a mandi.
- **Farmer-share meter:** every order shows how much of the price reached the farmer. This builds trust on both sides and gives the Ministry a live measure of intermediary cost.
- **Pooled logistics with return-load matching:** FPO collection points and trucks returning empty from cities are matched, which lowers transport cost per kilogram.
- **Built for rural access:** voice and regional-language input, offline-first design, and WhatsApp/IVR access, so a farmer without a smartphone can still use it.
- **Built on public data:** it uses open government data (mandi prices, weather, FPO registry) instead of building everything from scratch.

## Technical Approach

The platform is a mobile-first web and app system on a cloud backend, with an AI service for forecasting and routing, and data feeds from public agriculture sources.

### 1. Technologies to be used

| Layer | Technology | Purpose |
| --- | --- | --- |
| Farmer and buyer apps | React Native or Flutter app, plus a React web app | One codebase for Android, iOS and web; offline-first listings |
| Low-access channels | WhatsApp Business API, IVR, speech-to-text in regional languages | Farmers without smartphones can list produce and check prices |
| Backend | Python (FastAPI) or Node.js REST services, PostgreSQL with PostGIS, Redis | Listings, orders, user accounts, location queries |
| AI and ML | Python, scikit-learn, XGBoost or Prophet for demand and price forecasting; Google OR-Tools for route optimization | Demand forecasts, price suggestions, delivery routes |
| Maps and tracking | OpenStreetMap or Google Maps API, GPS tracking on partner vehicles | Route display and live delivery status |
| Payments | UPI gateway with escrow-style hold and release | Safe, direct payment to farmers |
| Data sources | Agmarknet and e-NAM mandi prices, IMD weather, FPO registry | Price references and forecasting inputs |
| Hosting | Cloud (AWS, Azure or MeitY-empanelled), Docker containers | Scalable, secure deployment |

### 2. Methodology and process for implementation

1. **Pilot design:** choose one district with active FPOs and one nearby city, and 4 to 5 high-volume crops such as tomato, onion, potato and leafy greens.
2. **Core build:** listings, ordering, escrow payment and FPO dashboard first, then the buyer app.
3. **Logistics integration:** onboard partner transporters, set up FPO collection points, and add delivery tracking.
4. **AI layer:** begin with price and demand baselines from historical mandi data, then retrain on platform orders as they accumulate.
5. **Pilot run and feedback:** measure farmer price, buyer price, delivery time and spoilage against the traditional mandi route.
6. **Scale-up:** extend to more districts, crops and bulk buyers.

The diagram below shows how an order moves through the system.

![FarmBridge AI order flow](<img width="1214" height="1295" alt="flowchart" src="https://github.com/user-attachments/assets/093b9761-2f1b-4adb-9dfd-ef58679f9e38" />


## Feasibility and Viability

The idea is feasible because its building blocks already exist: UPI payments, a large FPO network, e-NAM and open mandi price data. The hard parts are trust, logistics cost and getting buyers and sellers onto the platform together.

### 1. Analysis of the feasibility

| Dimension | Assessment |
| --- | --- |
| Need | An [RBI survey of rabi crops](https://www.rbi.org.in/Scripts/BS_ViewBulletin.aspx?Id=23198) put farmers' share of the consumer price at 40% to 67%, and [fruits and vegetables sat at the lower end, 40% to 63%](https://www.drishtiias.com/daily-updates/daily-news-analysis/farmers-earning-in-agri-produce-rbi). An RBI study of tomato, onion and potato found [farmers' shares of 33%, 36% and 37%](https://tribuneindia.com/news/farmers-lose-out). |
| Proof that direct selling works | An [RBI bulletin](https://www.rbi.org.in/scripts/bs_viewbulletin.aspx?id=18527) cites a government study of direct farmer-to-consumer markets (Uzhavar Sandhai in Tamil Nadu, Rythu Bazaar in Andhra Pradesh): farmers earned 15% to 40% more than wholesale prices, and consumers paid 15% to 30% less than retail. |
| Supply side | The government's [scheme to form 10,000 FPOs](https://www.drishtiias.com/daily-news-analysis/formation-promotion-of-10-000-fpos) gives ready-made aggregation points. By March 2026, [4,724 FPOs were registered on e-NAM](https://visionias.in/current-affairs/news-today/2026-04-14/economy/e-nam-completes-10-years-of-transforming-agricultural-trade). |
| Data | [Agmarknet](https://data.gov.in/resource/current-daily-price-various-commodities-various-markets-mandi) publishes daily wholesale prices (maximum, minimum and modal) through the open data portal, which feeds price references and forecasting. |
| Technology | Mobile apps, UPI, maps and standard ML libraries are mature and low-cost. No new hardware is required. |
| Revenue | A small commission on orders, a delivery fee, and subscriptions from bulk buyers. Farmers pay nothing to list. |
| Regulation | The platform must follow state APMC rules, GST and food-safety norms. It is designed to work with e-NAM, not against it. |

### 2. Potential challenges and risks, and 3. Strategies to overcome them

| Challenge or risk | Strategy |
| --- | --- |
| Low digital literacy and weak connectivity in villages | Voice and regional-language input, offline-first app, WhatsApp and IVR access, and FPO staff acting as local help agents |
| Buyers and sellers must both be present from day one | Start with one district and a few crops; sign up bulk buyers first so farmers see real demand |
| Quality disputes between farmer and buyer | Grading at FPO collection points, photo and weight records at pickup, ratings, and a refund process tied to escrow |
| High transport and cold-chain cost for perishables | Pool lots at FPO hubs, match return loads, and use route optimization; add cold chain only for high-value, short-life crops |
| Forecasts that are wrong because of weather or price swings | Show forecasts as ranges, retrain on live orders, and let farmers see the reasoning |
| Resistance from traders and local mandi interests | Invite traders to join as verified buyers and logistics partners, and integrate with e-NAM |
| Payment fraud and data privacy | KYC for sellers, escrow payments, encrypted data storage, and compliance with India's data protection law |

## Impact and Benefits

By shortening the chain between farm and buyer, FarmBridge AI moves money from intermediary margins to farmers and consumers, and makes prices and supply easier to see for everyone.

### 1. Potential impact on the target audience

- **Small and marginal farmers and FPOs:** a larger share of the consumer price, earlier and more certain payment, and demand and price information before harvest.
- **Consumers:** fresher produce at lower prices, with clear information on where it came from and how much of the price reached the farmer.
- **Bulk buyers (retailers, restaurants, institutions, processors):** reliable supply of graded produce, standing orders, and fewer rounds of negotiation.
- **Ministry and State governments:** a live view of prices, arrivals and the farmer's share, which supports price monitoring and policy decisions.

### 2. Benefits of the solution

**Economic benefits:**

- Improved market access for farmers.
- Potential reduction in unnecessary supply-chain costs.
- More transparent prices for buyers.

**Social benefits:**

- Better access to digital agricultural services.
- More opportunities for small farmers.
- Improved access to market information.

**Environmental benefits:**

- Reduced unnecessary travel through route optimization.
- Potential reduction in fuel consumption.
- Better demand planning to help reduce food wastage.

## Research and References

**Government and data sources**

- Ministry of Agriculture and Farmers Welfare, Government of India: https://agriwelfare.gov.in/
- e-NAM – National Agriculture Market: https://www.enam.gov.in/
- Open Government Data Platform India: https://www.data.gov.in/
- AGMARKNET – Agricultural Market Information: https://agmarknet.gov.in/
- Food and Agriculture Organization (FAO): https://www.fao.org/

**Research on farmers' share and direct selling**

- [RBI Bulletin: Dynamics of agriculture supply chain, rabi crops](https://www.rbi.org.in/Scripts/BS_ViewBulletin.aspx?Id=23198)
- [RBI Bulletin: Supply Chain Dynamics and Food Inflation in India](https://www.rbi.org.in/scripts/bs_viewbulletin.aspx?id=18527)
- [Drishti IAS: summary of the RBI survey on farmers' earnings](https://www.drishtiias.com/daily-updates/daily-news-analysis/farmers-earning-in-agri-produce-rbi)
- [The Tribune: Farmers lose out](https://tribuneindia.com/news/farmers-lose-out)
- [Vision IAS: e-NAM completes 10 years](https://visionias.in/current-affairs/news-today/2026-04-14/economy/e-nam-completes-10-years-of-transforming-agricultural-trade)
- [Drishti IAS: Formation and Promotion of 10,000 FPOs](https://www.drishtiias.com/daily-news-analysis/formation-promotion-of-10-000-fpos)

**Technology**

- OpenStreetMap – Mapping Data: https://www.openstreetmap.org/
- OSRM – Routing: https://project-osrm.org/
- Google OR-Tools – Route Optimization: https://developers.google.com/optimization
- Scikit-learn – Machine Learning Tools: https://scikit-learn.org/stable/
