# 📞 Call Center Performance Dashboard — Power BI

> **Final Project | Data Analytics | Universidad Cenfotec**
> Developed by: Jennifer Victoria Arriola Salazar

---

## 📌 Project Overview

This Power BI dashboard analyzes call center operations for a single day (**March 20, 2024**), providing actionable insights into agent performance, call types, department distribution, and resolution outcomes. The project was designed to simulate a real-world business intelligence scenario for a customer service environment.

---

## 🎯 Objectives

- Monitor and compare individual agent performance
- Identify the most common call types handled by the center
- Analyze call distribution across departments
- Evaluate call outcomes and resolution rates
- Segment calls by duration to uncover service efficiency patterns

---

## 📊 Dashboard Pages

### Page 1 — Call Center Performance Dashboard

![Dashboard Page 1](fpbi.png)

| Visual | Description |
|--------|-------------|
| **Llamadas Atendidas** (Bar Chart) | Compares total calls handled per agent: Esteban (40), Patricia (30), Rodrigo (30) |
| **Tipo de Llamada** (Bar Chart) | Breaks down call volume by type: Consulta (38), Venta (21), Queja (20), Soporte (20) |
| **Llamadas por Departamento** (Pie Chart) | Shows department share: Atención al Cliente (39%), Ventas (21%), Servicio al Cliente (20%), Soporte Técnico (20%) |
| **Resultado de la Llamada** (Bar Chart) | Displays outcomes ranging from unresolved issues to successful resolutions and information provided |

**Filters available:** Agent, Department

---

### Page 2 — Distribución por Departamento

![Dashboard Page 2](fppbi.png)

| Visual | Description |
|--------|-------------|
| **Department Summary Table** | Lists each department with call count and primary call type (e.g., Atención al Cliente → 39 calls, Consulta) |
| **Llamadas por Duración** (Donut Chart) | 78% of calls lasted 15–20 minutes (B.15-20), while 22% lasted under 15 minutes (A.0-15) |

**Filters available:** Department, Call Duration (min)

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Microsoft Power BI Desktop** | Dashboard creation and data modeling |
| **DAX (Data Analysis Expressions)** | Custom measures and calculated columns |
| **Power Query** | Data transformation and cleaning |

---

## 📁 Project Structure

```
📦 call-center-dashboard/
 ├── Proyecto_Final_Jennifer_Arriola.pbix   # Power BI project file
 ├── call_center_data.txt                   # Raw dataset (100 records)
 ├── fpbi.png                               # Dashboard screenshot — Page 1
 ├── fppbi.png                              # Dashboard screenshot — Page 2
 └── README.md                              # Project documentation
```

---

## 💡 Key Insights

- **Esteban** was the highest-performing agent, handling 40% more calls than his colleagues.
- **Consultas** were the most frequent call type, suggesting a potential need for better self-service resources.
- **Atención al Cliente** handled the most volume (39% of all calls), making it the most critical department.
- The majority of calls (**78%**) lasted between 15–20 minutes, indicating a relatively standardized service time.
- A significant share of calls resulted in **"Información proporcionada"** as the outcome, reflecting successful informational support.

---

## 🚀 How to Open

1. Download the `.pbix` file from this repository.
2. Open it with **Microsoft Power BI Desktop** (free download at [powerbi.microsoft.com](https://powerbi.microsoft.com)).
3. Explore using the slicers/filters on each page.

---

## 🎓 Academic Context

This project was developed as the **final capstone** for the *Data Analytics* program at **Universidad Cenfotec** (Costa Rica). It demonstrates proficiency in:

- Business intelligence dashboard design
- Data visualization best practices
- DAX formula authoring
- Storytelling with data

---

## 👩‍💻 Author

**Jennifer Victoria Arriola Salazar**
- 🎓 Technical Certificate in Data Analytics · Universidad Cenfotec
- 💼 [LinkedIn](https://www.linkedin.com/in/jennifervictoriaarriolasalazar/)
- 🐙 [GitHub](https://github.com/jenvic96)

---

*Feel free to explore the dashboard and reach out with any questions!*
