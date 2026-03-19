# Final Project – Business Analytics (Power BI)
**Universidad Cenfotec**  
**Course:** Business Analytics  
**Student:** Jennifer Victoria Arriola Salazar

This is my **Final Project for Business Analytics at Universidad Cenfotec**.  
The objective is to design a business‑ready **Power BI dashboard** using a call center dataset (100 calls, 20/03/2024) to analyze operations by **Agent, Call Type, Department, Result, and Duration**, including an **Agent slicer** for interactivity.

## 
![Dashboard Overview](fpbi.png)  
*Page 1 – Overview (Agent • Type • Department • Result • Slicer by Agent)*

![Matrix & Duration](fppbi.png)  
*Page 2 – Matrix by Department and Calls by Duration (Rango Duración)*

---

## ✅ Project Requirements (Completed)
1. Chart: number of calls **by Agent**  
2. Chart: number of calls **by Call Type**  
3. Chart: number of calls **by Department**  
4. Chart: number of calls **by Result**  
5. **Slicer by Agent**  
6. Chart: number of calls **by Duration** (bucketed)  
7. Clean, readable design with titles, labels, and filters

*A supplemental **Matrix** view was included to enrich analysis.*

---

## 📊 Key Findings (Summary)
- **Total calls:** 100 (all on 20/03/2024)  
- **By Agent:** Agente 1 **40**, Agente 2 **30**, Agente 3 **30** → *Agente 1 has the highest workload (40%).*  
- **By Type:** **Consulta 39%**, Venta 21%, Soporte 20%, Queja 20% → *Consultas dominate the volume.*  
- **By Department:** Atención al Cliente **39**, Ventas 21, Soporte Técnico 20, Servicio al Cliente 20 → *Highest load in Atención al Cliente.*  
- **By Result:** Información proporcionada **29**, Exitosa **21**, Técnico resuelto **11**, Transferido/Resuelto/En proceso ~**10** each, Problema sin resolver **9**.  
- **By Duration (Rango Duración):** **11–15 min: 22**, **16–20 min: 78** → *78% of calls last 16–20 minutes.*

---

## 🧾 Dataset
**Original columns**
- `ID Llamada` (Whole Number), `Cliente` (Text), `Agente` (Text), `Fecha` (Date),  
  `Hora de inicio` (Time), `Hora de finalización` (Time), `Duración (min)` (Whole Number),  
  `Tipo de Llamada` (Text), `Resultado` (Text), `Nivel de satisfacción` (Text), `Departamento` (Text)

**Derived columns**
- `FechaHoraInicio`, `FechaHoraFin` (Date/Time)  
- `Duración calculada (min)` (validation)  
- `Duración correcta` (True/False)  
- `Rango Duración` (<=10, 11–15, 16–20, 21–30, >30)

---

## 🧹 Data Preparation (Power Query)
- Trim de textos y tipificación correcta (Date / Time / Whole Number / Text).  
- Cálculo y validación de duración (Start–End).  
- **Bucketing** de duración en `Rango Duración` para análisis claro.  
- Consistencia verificada: las duraciones calculadas coinciden con las reportadas.

---

## 📈 Dashboard Contents
- **Bar**: Calls by Agent  
- **Column**: Calls by Type  
- **Bar**: Calls by Department  
- **Column**: Calls by Result  
- **Column**: Calls by Duration (Rango Duración)  
- **Slicer**: Agent  
- **Matrix (optional)**: e.g., Department × Type or Duration × Agent

**Title suggestions**
- *Llamadas atendidas por Agente*  
- *Cantidad de llamadas por Tipo de Llamada*  
- *Llamadas por Departamento*  
- *Resultado de la Llamada*  
- *Cantidad de llamadas atendidas por Duración*  
- *Slicer: Filtrar por Agente*

---

## 🧮 Helpful DAX
```DAX
Total Llamadas = COUNT('Tabla'[ID Llamada])

% por Tipo =
DIVIDE([Total Llamadas], CALCULATE([Total Llamadas], ALL('Tabla'[Tipo de Llamada])))

% por Resultado =
DIVIDE([Total Llamadas], CALCULATE([Total Llamadas], ALL('Tabla'[Resultado])))
``
