# 🩺 Facial Temperature Explorer

Quickly spot potential fevers or facial heat anomalies using **ambient-aware thermal mapping**, empowering smarter, faster wellness checks at a glance.

![App Screenshot](writeup/screenshot.png) <!-- replace with actual path if you want to show a screenshot -->

---

## ✨ Motivation
Our dashboard answers the question:  
**“How well do different facial regions (forehead, inner canthi, mouth) track true oral temperature under various ambient conditions and demographics?”**

By making these patterns visible and interactive, we help bridge the gap between raw thermographic data and meaningful health insights.

---

## 📊 Data Source
Dataset: [Facial and oral temperature data from a large set of human subject volunteers](https://physionet.org/) (PhysioNet)  

- **Volunteers:** 1,020 (IRT-1) and 1,009 (IRT-2)  
- **Measurements:** Infrared thermography (facial) + internal oral temps  
- **Demographics:** Gender, age, ethnicity, cosmetic use, and room conditions  
- **Regions recorded:** Forehead (center/left/right), inner canthi, mouth  

We focused on **facial thermographic data**, grouping by room temperature:

- **Group 1:** 20.0–24.0 °C  
- **Group 2:** 24.0–28.0 °C  

After cleaning and filtering, two final CSV files (per group) support our real-time offset calculations.

---

## 🖼️ Features
### Visual Encodings
- **Color Gradient (Blue → Red):** Intuitive mapping of cooler vs. hotter regions.  
- **Red Glow (≥ 38 °C):** Fever threshold indicator.  
- **Circle Markers:** Interactive probes at forehead, eyes, mouth.

### Interactions
- **Temperature Slider:** Simulate measured temps with real-world offsets.  
- **Medical Alert Toggle:** Flag regions ≥ 38 °C automatically.  
- **Demographic Filters:** Adjust by age or gender.  
- **Tooltips:** Hover to see exact values.  
- **Auto-Diagnosis Panel:** Contextual feedback (e.g., fever, sinus congestion).  
- **Dynamic Face Image:** Gender-specific templates update automatically.  

---

## 🛠️ Development
- **Frontend:** HTML, CSS, JavaScript, [D3.js](https://d3js.org/)  
- **Data Processing:** Custom preprocessing + temperature offset modeling  
- **Files:**  
  - `index.html` — main app  
  - `main.js` — interactive logic with D3  
  - `style.css` — styling  
  - `data/` — processed CSVs  
  - `writeup/` — final documentation  

---

## 👩‍💻 Team Contributions
- **Manasa:** Dashboard design, auto-diagnosis logic, interface styling.  
- **Rakshan:** D3 integration, data preprocessing, offset calculations.  
- **Andrew:** Layout responsiveness, write-up section, visual design.  

Collaboration included weekly syncs, shared notes, and iterative testing.

---

## 📚 Lessons Learned
- **Data Wrangling:** Cleaning and offset modeling was more complex than expected.  
- **Design Simplicity:** Interactive face > raw heatmaps for usability.  
- **UI Challenges:** Aligning gender-specific overlays required coordinate re-mapping.  
- **Actionable Insights:** Auto-Diagnosis panel reinforced the need to translate data into plain-language health guidance.  

Total effort: ~30 hours.

---

## 🚀 Getting Started
1. Clone the repo:
   ```bash
   git clone https://github.com/manasamaddi1/d3-facial-thermography.git
   cd d3-facial-thermography
