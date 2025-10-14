## IT Incident SLA Breach Analysis (Python)

### Overview  
This project looks at ServiceNow IT incident management data to find out where and why SLA breaches happen.  
It also checks if ticket priority, handle time, and workload have any link to delays.  
The goal is to help teams reduce breach rates and improve response time.

---

### Tools & Libraries  
- **Python:** Pandas, Matplotlib, Seaborn, Statsmodels, Scipy  
- **Jupyter Notebook**  
- **Dataset:** IT Incident Log (Kaggle, ServiceNow)

---

### Project Steps  
1. **Data Cleaning:** Parsed dates, dropped missing values, and ran basic data checks  
2. **Feature Creation:** Calculated handle time (in hours), SLA breach flag, and ticket month  
3. **Exploratory Analysis:** Analyzed breach rates by priority, category, and assignment group  
4. **Statistical Tests:**  
   - Two-proportion Z-test → compared SLA breaches (High vs Low priority)  
   - One-way ANOVA → compared average handle times across all priorities  
5. **Trend & Correlation:** Checked monthly SLA breach trend and correlations between variables  
6. **Key Metrics & Insights:** Found main areas causing delays and suggested improvement ideas

---

### Dataset Info  
- Around **140,000+** incident records  
- Key columns:  
  `priority`, `category`, `assignment_group`, `opened_at`, `closed_at`, `handle_time_hours`, `sla_breached`, `reassignment_count`

---

### 📈 Main Insights  
- **SLA breach rate:** 60.6%  
- **Average handle time:** 409 hours (17 days)  
- **Max handle time:** 8,190 hours (341 days)  
- Reassignments and long handle times both increase SLA breach chances  
- Some assignment groups have breach rates above 90%  

---

### 📊 Statistical Findings  
- **Z-Test:** No major difference in SLA breach rate between High and Low priority tickets  
- **ANOVA:** Clear difference in average handle times across all priority levels  

---

### Recommendations  
- Rebalance work between overloaded support groups  
- Add alerts for tickets getting close to SLA limits  
- Review SLA limits for lower priorities  
- Investigate tickets taking over 500 hours and remove blockers  
- Track SLA and handle time trends monthly in a dashboard  

---

### 📉 Business Impact  
- Fewer SLA breaches and faster ticket resolutions  
- Better customer satisfaction and SLA compliance  
- Higher team productivity with fewer delays  

---

