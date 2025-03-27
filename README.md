# Multi-Language Patient Communication System

This project simulates a clinic communication system for interacting with patients in multiple languages using various communication channels. It automates sending appointment confirmations and wait-time updates based on patient preferences and response behavior.

## Features:
- Sends appointment confirmations in 5 different languages: **Tamil, Telugu, Malayalam, Hindi, and English**.
- Customizes messages based on patient **age group**, **language**, and **communication channel**.
- Implements **fallback channel selection** for patients with low response rates.
- Provides effectiveness metrics and visualizations, including **response rates by language, channel, and age group**.

---

## 1. Code Overview:
### 1.1 Constants and Config:
- Defines appointment types (e.g., "General Checkup," "Dermatology").

### 1.2 Patient Database:
- Stores patient details like `name`, `language`, `age_group`, `preferred communication channel`, and `response_rate`.

### 1.3 Message Templates:
- Contains appointment confirmation and wait-time update messages in **multiple languages**.

### 1.4 Core Functions:
- **`select_channel()`**:  
  Implements smart channel selection:
  - Time-sensitive updates are sent via **WhatsApp** to younger patients.
  - Applies fallback logic for patients with a low response rate.

- **`generate_message()`**:  
  Customizes messages using language-specific templates and formats time appropriately for elderly patients.

- **`send_message()`**:  
  Sends messages to patients with a simulated **90% success rate**.

---

### 1.5 Simulation Engine:
- **`simulate_clinic_operations(days=7)`**:  
  Runs a 7-day simulation:
  - Each day, 30% of the patients are randomly selected to receive appointment confirmations.
  - If a patient responds, they also get a **wait-time update message**.

- Stores the patient response data for analysis.

---

### 1.6 Analysis & Visualization:
- **`analyze_results(results)`**:  
  - Calculates key metrics:
    - **Overall response rate**.
    - **Response rates grouped by language, channel, and age group**.
  - Displays bar chart visualizations for effectiveness analysis.

---

## 2. How to Run the Code:
1. Ensure you have Python installed.
2. Install the required libraries by running:
   ```bash
   pip install pandas matplotlib
## 3.Video Explanation:
For a detailed explanation and code walkthrough, watch the video below:
🎥 Video Explanation:https://www.loom.com/share/5161a3dd1fd542bcae401eff45fed523?sid=c7a77186-f746-47df-95ce-6d3195366f23
## 4. Output:
After running the simulation, you will see:
1. Sent appointment confirmation messages in different languages.
2. Calculated patient responses.
3. Bar charts visualizing response effectiveness by language, communication channel, and age group.
