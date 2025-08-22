# Binary Classification Challenge

## ML Problem Definition
This is a **Binary Classification** problem using structured tabular data (`.csv`).  
The goal is to predict the outcome of matches based on player statistics.

---

## Credits

- **Yandex Data School** (Pavel Gein)  
- **Higher School of Economics** (Konstantin Vorontsov)  
- **ODS.AI** (Yuriy Kashnitskiy)  


---

## Description
Participants are tasked with predicting outcomes in a competitive match setting.  
The dataset contains player-level statistics (Radiant vs Dire teams) recorded during gameplay.  

---

## Evaluation
The evaluation metric is **ROC AUC**.  

- ROC AUC measures the ability of a classifier to distinguish between two classes.  
- A perfect model will have an ROC AUC of **1.0**, while a random model will score around **0.5**.  

📖 ROC AUC: [Google ML Crash Course](https://developers.google.com/machine-learning/crash-course/classification/roc-and-auc)

---

## Dataset Description

### File Descriptions
- **`train_data.csv`** – training dataset  
- **`test_data.csv`** – testing dataset  

### Data Fields
Player statistics are prefixed to indicate **team** and **player number**:
- `r` → Radiant team  
- `d` → Dire team  

Each player has the following fields:

- **hero_id** – unique hero identifier  
- **K/D/A** – kills, deaths, assists  
- **lh** – last hits (enemy creeps killed)  
- **denies** – allied creeps killed to deny gold  
- **gold** – current gold  
- **xp** – experience points  
- **level** – player level  
- **health / max_health** – current and maximum health  
- **max_mana** – maximum mana capacity  
- **x, y** – map coordinates (player location)  
- **stuns** – total stun duration caused  
- **creeps_stacked** – number of neutral creeps stacked  
- **camps_stacked** – number of camps stacked  
- **rune_pickups** – number of runes picked up  
- **firstblood_claimed** – whether the player claimed first blood  
- **teamfight_participation** – participation ratio in team fights  
- **towers_killed** – towers destroyed  
- **roshans_killed** – roshan kills  
- **obs_placed** / **sen_placed** – observer and sentry wards placed  

### Time Series Fields
Some statistics are provided as time series:

- **`times`** – array of time marks  
- **gold_t** – gold values at time marks  
- **xp_t** – experience at time marks  
- **lh_t** – last hits  
- **dn_t** – denied creeps  

---

## Goal
- Perform data preprocessing and feature engineering  
- Train binary classification models  
- Evaluate models using ROC AUC  
- Explore time series features for additional predictive power  
