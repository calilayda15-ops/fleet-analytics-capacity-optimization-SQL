# fleet-analytics-capacity-optimization-SQL
# International Logistics & Fleet Capacity Analytics (SQL)

## 📌 Project Overview
This project focuses on data-driven decision-making in supply chain operations. Using SQL, I built a relational database simulation to analyze truck fleet utilization, route efficiencies, and driver performances for an international distribution center. 

The core objective is to identify operational blind spots, such as under-utilized vehicle capacities on global routes (e.g., Berlin, Paris, London), which directly impact transportation costs and carbon footprints.

---

## 👩‍💻 Author
- **Name:** Ilayda Cal
- **Field:** Logistics Management Student
- **Focus:** Green Supply Chain, Data Analytics, and Inventory Optimization
- **Target Industries:** Global Pharmaceuticals & Investment Banking Operations

---

## 🛠️ Database Structure & Tech Stack
- **Environment:** SQLite / SQL Server
- **Tables Created:** - `Trucks`: Holds fleet data including unique Truck IDs, License Plates, Driver Names, and Maximum Weight Capacities.
  - `Shipments`: Tracks active international voyages, destination cities, and actual cargo weights.

---

## 📈 Key SQL Queries & Operations Covered
1. **Data Definition & Insertion (`CREATE`, `INSERT INTO`):** Established the core infrastructure of the fleet database.
2. **Data Integration (`INNER JOIN`):** Merged logistics operational data with fleet capacity data to create comprehensive performance reports.
3. **Capacity Utilization Analysis:** Calculated the gap between `CargoWeight_Ton` and `Capacity_Ton` to detect under-loaded trucks and optimize resource allocation.

### Sample Fleet Efficiency Query:
```sql
SELECT Shipments.ShipmentID, Trucks.DriverName, Shipments.CargoWeight_Ton, Trucks.Capacity_Ton
FROM Shipments
INNER JOIN Trucks ON Shipments.TruckID = Trucks.TruckID;
