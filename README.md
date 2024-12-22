# Traffic Flow Prediction  


This project predicts traffic flow using historical data, such as vehicle counts (cars, bikes, buses, trucks), time, and the day of the week. The goal is to analyze traffic patterns, forecast situations, and provide actionable insights to reduce congestion, optimize traffic control, and minimize environmental impact.  

---

## Data Dictionary  

The dataset includes:  
- **Time:** Timestamp of observation  
- **Date:** Date of observation  
- **Day of the Week:** Day corresponding to the observation  
- **CarCount:** Count of cars  
- **BikeCount:** Count of bikes  
- **BusCount:** Count of buses  
- **TruckCount:** Count of trucks  
- **Total:** Total vehicle count  
- **Traffic Situation:** Categorized traffic condition (e.g., congestion levels)  

---

## Data Preprocessing  

- **Time & Date Formatting:** Converted to `datetime`. Extracted new features like `Hour`, `Month`, and `Day` to capture temporal patterns.  
- **Handling Categorical Data:** Encoded `Day of the Week` and `Traffic Situation` into numerical values for modeling.  
- **Missing Values:** Replaced missing values with median values of respective columns.  

---

## Exploratory Data Analysis (EDA)  

Key findings:  
- **Peak Hours:** Rush hours show spikes in car and bike counts; bus and truck counts remain stable.  
- **Vehicle Types:** Cars dominate traffic; trucks have the lowest volume.  
- **Traffic Situations:** Higher truck counts worsen traffic conditions.  
- **Day Variability:** Total traffic is stable across days, but individual vehicle types vary.  

---

## Model Building and Evaluation  

- **Model:** Random Forest Classifier  
- **Performance:** Effective in predicting high-traffic periods, aiding traffic management.  
- **Metrics:**  
  - **Confusion Matrix:** Analyzed prediction errors.  
  - **Classification Report:** Provided precision, recall, and F1-scores.  
  - **Accuracy:** Achieved satisfactory accuracy in classifying traffic situations.  

### Feature Importance  

The most significant features for traffic flow prediction:  
1. **CarCount**  
2. **BikeCount**  
3. **Day of the Week**  
4. **Hour of the Day**  

### Visual Insights  

- **Traffic Volume Over Time:** Cars and bikes dominate during peak hours, while trucks remain steady.  
- **Day-Wise Traffic Patterns:** Unique distributions for each vehicle type across the week.  
- **Pairwise Correlation:** Positive correlation between `CarCount` and `BikeCount`; negative correlation between `TruckCount` and `Traffic Situation`.  

---

## Conclusion  

The Traffic Flow Prediction project highlights how vehicle counts, time, and day influence traffic patterns. It provides insights for managing urban traffic effectively by predicting congestion, optimizing signal timings, and scheduling public transport.  

This project contributes to building smarter cities by enabling dynamic traffic management, reducing emissions, and improving transportation systems, ultimately supporting sustainable urban mobility.  
