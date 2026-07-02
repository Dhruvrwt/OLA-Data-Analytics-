# 🚕 Ola Ride-Hailing Data Analytics Dashboard

A multi-page Power BI report built to analyze Ola ride-booking data — covering booking volume, revenue, vehicle-type performance, cancellations, and driver/customer ratings.

## 📝 Description

The Ola Data Analytics Dashboard is an interactive Power BI report designed to help users explore ride-booking data across a full month of operations. It breaks down bookings and revenue by vehicle type, tracks cancellation trends by both customers and drivers, and surfaces driver and customer satisfaction ratings. This tool is intended for ride-hailing operations teams, business analysts, and decision-makers who need a fast, visual read on demand, revenue, and service-quality performance.

## 🛠️ Tech Stack

The dashboard was built using the following tools and technologies:

* 📊 **Power BI Desktop** – Main data visualization platform used for report creation.
* 📂 **Power Query** – Data transformation and cleaning layer for reshaping and preparing the data.
* 🧠 **DAX (Data Analysis Expressions)** – Used for calculated measures such as `Total_bookings`, `CanceledBookings`, and `CanceledPercentage`.
* 📝 **Data Modeling** – A `Date` relationship links the ride-booking fact table to an auto-generated date table, enabling time-based filtering and trend analysis.
* 🧭 **Multi-Page Navigation** – Custom action buttons let users move between Overall, Vehicle Type, Revenue, Cancellation, and Ratings pages.
* 📁 **File Format** – `.pbit` (Power BI Template) for development.

## 📂 Data Source

The report is built on a ride-booking fact table (`July`) containing the following fields:

* **Booking details:** `Booking_ID`, `Booking_Status`, `Date`, `Time`, `Customer_ID`, `Vehicle_Type`, `Pickup_Location`, `Drop_Location`
* **Performance metrics:** `V_TAT` (vehicle turnaround time), `C_TAT` (customer turnaround time), `Ride_Distance`, `Booking_Value`, `Payment_Method`
* **Cancellations:** `Canceled_Rides_by_Customer`, `Canceled_Rides_by_Driver`, `Incomplete_Rides`, `Incomplete_Rides_Reason`
* **Ratings:** `Driver_Ratings`, `Customer_Rating`

Vehicle types covered include Prime Sedan, Prime SUV, Prime Plus, Mini, Auto, Bike, and eBike.

## ✨ Features / Highlights

### Business Problem
Ride-hailing platforms generate large volumes of daily booking data, but without a consolidated view it's difficult to answer key operational questions: Which vehicle types generate the most revenue? Where are cancellations concentrated — customer-side or driver-side? How satisfied are customers and drivers by vehicle segment?

### Goal of the Dashboard
To deliver an interactive, multi-page tool that:
* Tracks overall ride volume and booking value over time.
* Breaks down revenue and ride distance by vehicle type.
* Identifies cancellation patterns and their sources.
* Monitors driver and customer satisfaction by vehicle type.

### Walkthrough of Key Visuals

**Overall Page**
* **Total Bookings / Total Booking Value (Cards)** — Headline KPIs summarizing ride volume and revenue.
* **Ride Volume Over Time (Line Chart)** — Tracks daily booking counts to reveal demand trends.
* **Booking Status Breakdown (Pie Chart)** — Shows the share of successful, cancelled, and incomplete bookings.
* **Date Slicer** — Filters the entire page by date range.

**Vehicle Type Page**
* **Revenue & Ride Distance Cards by Vehicle Type** — Individual KPI cards for each vehicle type (Prime Sedan, Prime SUV, Prime Plus, Mini, Auto, Bike, eBike), showing booking value and ride distance for successful trips.

**Revenue Page**
* **Revenue by Payment Method (Column Chart)** — Compares total revenue across payment methods.
* **Revenue by Date (Column Chart)** — Tracks ride distance/revenue trends across the date hierarchy (year, quarter, month, day).
* **Top Customers Table** — Ranks customers by total booking value.

**Cancellation Page**
* **Cancel Rides by Customers / by Drivers (Pie Charts)** — Breaks down cancellation reasons by who initiated them.
* **Total, Success, and Cancelled Booking Cards** — Quick counts for volume comparison.
* **Cancellation Rate (Card)** — A calculated DAX measure showing the percentage of bookings cancelled.

**Ratings Page**
* **Driver Ratings by Vehicle Type (Cards)** — Average driver ratings segmented by vehicle type.
* **Customer Ratings by Vehicle Type (Cards)** — Average customer ratings segmented by vehicle type.

### Business Impact & Insights
* **Revenue Optimization:** Identify which vehicle types and payment methods drive the most revenue to guide pricing and fleet strategy.
* **Cancellation Management:** Distinguishing customer- vs. driver-initiated cancellations helps target the right process fixes to improve reliability.
* **Service Quality Monitoring:** Vehicle-type-level ratings highlight where driver or customer experience may need attention.
* **Demand Planning:** Ride volume trends over time support staffing and supply-side planning decisions.
* **Customer Insights:** The top-customers table helps identify high-value riders for retention efforts.

## 📸 Screenshots / Demo
https://github.com/Dhruvrwt/OLA-Data-Analytics-/tree/main/OLA%20Dashbord%20Snapshorts

## 🚀 How to Use

1. Clone or download this repository.
2. Open `Ola_Data_Analytics.pbit` in Power BI Desktop.
3. When prompted, load your ride-booking dataset (matching the schema above) or connect to your own data source.
4. Use the navigation buttons at the top of each page to move between Overall, Vehicle Type, Revenue, Cancellation, and Ratings views.
5. Use the date slicer on each page to filter results by a specific time period.

