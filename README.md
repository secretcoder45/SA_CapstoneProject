# Dynamic Pricing for Urban Parking Lots 🚗📊

This project implements real-time dynamic pricing for urban parking lots using **stream processing (Pathway)** and **interactive visualizations (Bokeh + Panel)**. It models how parking prices should adjust based on demand signals such as occupancy, queue length, traffic, and special events.

## 📁 Project Structure
├── dataset.csv                 # Original dataset with parking lot data
├── SA_Model_1.csv              # Model 1 code
├── SA_Model_2.ipynb            # Model 2 code
├── README.md                   # This file

## 📈 Models Implemented

### Model 1: Rule-Based Incremental Pricing
Price is updated once per day per lot:
Priceₜ = BasePrice + α × (Occupancy / Capacity)
or
Priceₜ = Priceₜ₋₁ + α × (Occupancy / Capacity)

### Model 2: Continuous Demand-Based Pricing
Price responds to a weighted demand function of:
- Occupancy%
- Queue Length
- Traffic Conditions
- Special Day Indicator

Final price is calculated and **rounded to 1 decimal place**.

## 🛠 Tech Stack

- **Language:** Python 3 (Google Colab)
- **Streaming Engine:** [Pathway](https://pathway.com/)
- **Visualization:** [Bokeh](https://docs.bokeh.org/) + [Panel](https://panel.holoviz.org/)
- **Report:** Written in LaTeX
- **Mermaid:** Flowchart Architecture

## 🛠 Mermaid Live Diagram
![Untitled diagram _ Mermaid Chart-2025-07-09-184411](https://github.com/user-attachments/assets/1ceff262-3b91-4cbf-944f-8dd5d4bb8c86)

## 📊 Visualizations

All daily pricing outputs for 14 unique parking lots are included:
- `model_1_plots/1_lot_1.png` to `1_lot_14.png`
- `model_2_plots/2_lot_1.png` to `2_lot_14.png`

## 📄 Report


The final [report.pdf](./SA_Capstone_report.pdf) explains:
- Dataset and preprocessing
- Assumptions and pricing logic
- Comparison between both models
- Visual results with commentary

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/urban-parking-pricing.git
   cd urban-parking-pricing
2.	Open the Jupyter/Colab notebook: notebook.ipynb
3.	Install required packages: pip install pathway bokeh panel
4.	Run the cells to:

	•	Clean the dataset
	•	Replay it with Pathway
	•	Compute pricing
	•	Visualize results with Bokeh/Panel

📬 Contact

Author: Palash Garg
Institute: IIT Guwahati
📧 palashgarg45@gmail.com
📎 LinkedIn: https://www.linkedin.com/in/palash-garg-003014345/
