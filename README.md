# School Enrollment Decision – Agent-Based Model (NetLogo)

This project implements a simplified **Agent-Based Model (ABM)** in NetLogo to simulate household decisions regarding school enrollment in Pakistan.  
The model was developed as part of the **Equity Equation Project** to explore how socioeconomic and demographic factors affect the likelihood of children attending school.

## Project Context
In Pakistan, over 26 million children are out of school.  
This simulation models 200 households as agents, each with randomly assigned attributes such as:
- Food insecurity
- Transport availability
- Parents' education level
- Neighborhood safety
- Daughter’s ability to work
- Distance to school

These attributes influence the household’s decision to enroll a child in school using a simple **scoring and penalty system**.

## ⚙ Model Details

### Agent Attributes
Each household (`turtle`) has:
- `has-food-insecurity?` (boolean)
- `no-transport?` (boolean)
- `parents-uneducated?` (boolean)
- `unsafe-neighborhood?` (boolean)
- `has-daughter-can-work?` (boolean)
- `distance-over-5km?` (boolean)
- `is-enrolled?` (boolean – outcome variable)

### Decision-Making Logic
1. Start with **score = 1.0**
2. Apply penalties:
   - Food insecurity → -0.3
   - No transport → -0.2
   - Parents uneducated → -0.2
   - Unsafe neighborhood → -0.2
   - Daughter can work → -0.2
   - Distance over 5km → -0.2
3. If **score > 0.5** → enrolled (`is-enrolled? = true`, color = green)  
   Else → not enrolled (`is-enrolled? = false`, color = red)

### Visualization
- **Green** = enrolled
- **Red** = not enrolled
- Agents positioned randomly in the NetLogo world

## 📊 Outputs
The model reports:
- Overall enrollment rate (%)
- Enrollment rate by **Food Insecurity** (Yes/No)
- Enrollment rate by **Daughter Can Work** (Yes/No)

Example results from one run:
| Metric                        | Percentage (%) |
|--------------------------------|---------------:|
| Overall Enrollment Rate        | 30             |
| Food Insecurity (Yes)          | 4.30           |
| Food Insecurity (No)           | 52.33          |
| Daughter Can Work (Yes)        | 18.68          |
| Daughter Can Work (No)         | 39.44          |
*(Values vary each run due to random household attributes.)*

## 🚀 How to Run
1. Download [NetLogo](https://ccl.northwestern.edu/netlogo/).
2. Open `school_enrollment_model2.nlogo` in NetLogo.
3. In the **Interface Tab**:
   - Click `Setup` → creates households
   - Click `Run Decisions` → applies decision logic
   - Click `Report Stats` → prints results to the Command Center
4. View visual results in the world view and monitors.

## 📷 Screenshots
<img width="1912" height="914" alt="Screenshot 2025-08-12 171346" src="https://github.com/user-attachments/assets/0a8d5f65-38ae-4890-89ef-fa0fb30d3dfd" />
<img width="1912" height="811" alt="Screenshot 2025-08-12 171424" src="https://github.com/user-attachments/assets/1e56872e-e63e-4dfb-a4c5-a0f99a274530" />

