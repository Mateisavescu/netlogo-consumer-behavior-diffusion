# netlogo-consumer-behavior-diffusion
Author: **Matei Sebastian Săvescu**  
Bachelor's Thesis | Economic Cybernetics, ASE Bucharest

## Overview
This repository contains an **Agent-Based Model (ABM)** implemented in **NetLogo** that simulates the diffusion of innovations and consumer purchasing behavior in a social network environment. 

The model extends classic growth models (e.g., Bass Model) by integrating individual psychological traits, preferential attachment networks, homophily, and dynamic influencer mechanisms.

## Key Features
- **Network Topology:** Scale-free network built via Preferential Attachment, incorporating social groups and tunable **Homophily**.
- **Agent Architecture:**
  - **Peers & Influencers:** Influencers are dynamically identified based on degree centrality (>$\mu + \sigma$).
  - **3-State Diffusion:** `Unaware` $\rightarrow$ `Aware` $\rightarrow$ `Adopted`.
  - **Psychological Factors:** Individual `Openness`, `Risk Aversion`, `Price Sensitivity`, and `Novelty Sensitivity`.
- **Optimization:** Parameter optimization using Genetic Algorithms via **BehaviorSearch** to evaluate `peer-effect` vs. `influencer-effect` across different price points.

## Experiments & Results
1. **Baseline Scenario:** Diffusion bottlenecks when relying solely on organic peer interactions without catalysts.
2. **Influencer Impact:** Influencers partially compensate for high product prices, though effectiveness depends on network positioning.
3. **Homophily & Structural Instability:** High homophily creates asymmetric adoption across social clusters without drastically reducing global adoption.
4. **Genetic Algorithm Optimization:** Shows that `influencer-effect` remains essential for high-priced products, whereas `peer-effect` effectiveness drops as price increases.

## How to Run
1. Download and install [NetLogo](https://ccl.northwestern.edu/netlogo/).
2. Open the `.nlogo` file inside NetLogo.
3. Click `Setup`, generate the network (`create-network`), calculate influencers (`calculate-influencers`), set seed adopters (`set-initial-adopters`), and hit `Go / Diffusion`.
