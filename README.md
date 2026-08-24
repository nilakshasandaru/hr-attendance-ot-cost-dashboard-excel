HR Attendance & Overtime Cost Dashboard (Excel)

A live, formula-driven Excel system that tracks daily attendance and overtime cost for a garment manufacturing factory, and auto-updates a management dashboard as new data is entered — no macros, no manual recalculation.

Built as a portfolio project for Industrial Engineering / Production Planning / Manpower Planning roles.

Business Scenario

Sithara Apparels (fictional) is a garment factory with four production departments — Cutting, Sewing, Packing, and Quality Control — running three shifts. Management needs a simple way to answer two questions every week: is attendance under control, and how much is overtime costing us? This workbook answers both from the same daily data entry.

Features
Single point of data entry — one row per employee per day (date, status, in-time, out-time); everything downstream is a formula, nothing is hardcoded
Automatic overtime engine — worked hours, OT hours, and OT cost calculate instantly, including correct handling of an overnight shift that crosses midnight
Live dashboard — KPI cards, department-wise comparison, weekly trend, and a top-5 overtime contributors table, all backed by charts
Built to scale — ~2,000 pre-formatted blank rows are ready below the sample data, so new entries auto-populate every formula and flow straight into the dashboard without editing a single formula
Data validation — a dropdown list on the Status column prevents bad entries
Editable inputs are colour-coded (yellow) so anyone using the sheet knows exactly where to type
Workbook Structure
Sheet	Purpose
README	How to use the workbook
Employee_Data	Master list of 24 employees — ID, name, department, designation, shift, standard hours, OT rate
Attendance_Data	Daily attendance log (30 days of sample data + ~2,000 ready-to-use blank rows)
Dashboard	KPI cards, department summary, weekly trend, employee OT summary, top-5 contributors, and 4 charts
Key Calculations
Metric	Formula
Attendance Rate	(Present + Late + Half-Day days) ÷ Total days
Absenteeism Rate	Absent days ÷ Total days
Worked Hours	Out-time − In-time (adjusts +24h for an overnight shift)
OT Hours	MAX(Worked Hours − Standard Hours, 0)
OT Cost	OT Hours × OT Rate (looked up per employee)

Implemented with INDEX/MATCH, SUMIFS, COUNTIFS, and IFERROR — Excel 2016/2019-compatible, no volatile or array formulas.

How to Add New Data
Open Attendance_Data and go to the next empty row
Fill in Date, Employee_ID, Status (from the dropdown), In_Time, Out_Time
Worked_Hours, OT_Hours, and OT_Cost calculate automatically
The Dashboard (KPIs, tables, charts) updates the moment the workbook recalculates
Skills Demonstrated

Excel data modelling · lookup formulas (INDEX/MATCH) · conditional aggregation (SUMIFS/COUNTIFS) · data validation · dashboard design · KPI definition · chart design · workforce cost analysis · industrial engineering fundamentals (attendance, absenteeism, overtime costing)
