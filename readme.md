# 🚗 Electric Vehicle Sales Analysis - PowerBI

As part of the Codebasics Monthly Resume Challenge #12, I worked on this Electric Vehicle Sales Analysis project.

📌 [Challenge Link](https://codebasics.io/challenge/codebasics-resume-project-challenge)  
📊 [Interactive Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYTBkNmY2OTgtZjE3MS00M2UxLWEyYjMtNTQ0Y2IzOTkwNjdhIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)  
🔗 [LinkedIn Post](https://www.linkedin.com/posts/arindam430_electric-vehicle-sales-analysis-activity-7237154748016013315-mLLI?utm_source=share&utm_medium=member_desktop)\
🎥 [Video Presentation](https://youtu.be/L41LGK68HMU)

## 📝 Problem Statement

AtliQ Motors, a prominent automotive leader from the USA specializing in electric vehicles, has seen its market share in North America's electric and hybrid vehicle segment grow to 25% over the past five years. As part of its global expansion, the company aims to introduce its top-selling models in India, where its current market share is below 2%. To support this initiative, AtliQ Motors conducted an in-depth study of the existing EV and hybrid vehicle market in India.

## 📋 Task List

As a data analyst, I was provided with sample data and a PDF containing primary and secondary business questions. My task was to complete the following:

- Develop metrics based on the primary and secondary questions provided by the business stakeholders.
- Create a dashboard following the stakeholder mock-up, ensuring it is self-explanatory and easy to understand.
- Generate additional insights beyond the provided metrics and mock-up. I could incorporate additional data from my own research to support my recommendations.

## 🗄️ Dataset Understanding

Understanding the available data is crucial before analysis. Here's a breakdown:

- **Dimension Table**: Contains static data related to dates and fiscal years.
- **Fact Table**: Includes electric vehicle sales data from manufacturers and states.

#### **dim_date**

- 🌍 `date`: Ranges from April 1, 2021, to March 1, 2024.
- 👥 `fiscal_year`: Since the company's fiscal year starts in April, the fiscal years listed are from 2022 to 2024.
- 📅 `quarter`: Corresponds to the fiscal years' quarters.


#### **Electric Vehicle Sales by State**

- 🗓️ `Date`: The date on which the data was recorded (Format: DD-MMM-YY). Data is recorded monthly.
- 🏙️ `State`: The name of the state where the sales data is recorded, representing the geographical location within India.
- 🚗 `vehicle_category`: Indicates whether the vehicle is a 2-Wheeler or a 4-Wheeler.
- 🔋 `electric_vehicles_sold`: The number of electric vehicles sold in the specified state and category on the given date.
- 📊 `total_vehicles_sold`: The total number of vehicles (both electric and non-electric) sold in the specified state and category on the given date.

#### **Electric Vehicle Sales by Makers**

- 🗓️ `Date`: The date on which the sales data was recorded (Format: DD-MMM-YY). Data is recorded monthly.
- 🚗 `Vehicle Category`: Indicates whether the vehicle is a 2-Wheeler or a 4-Wheeler.
- 🏭 `Maker`: The name of the manufacturer or brand of the electric vehicle.
- 🔋 `Electric Vehicles Sold`: The number of electric vehicles sold by the specified maker in the given category on the given date.

## 🧠 Additional Calculated Metrics:

🚗 **Penetration Rate**: This metric represents the percentage of total vehicles that are electric within a specific region or category, indicating the adoption level of electric vehicles. It is calculated as:

$$
\text{PenetrationRate} = \left(\frac{\text{ElectricVehiclesSold}}{\text{TotalVehiclesSold}}\right) \times 100
$$

📈 **CAGR (Compound Annual Growth Rate)**: CAGR measures the average annual growth rate over a specified period longer than one year. It is calculated as:

$$
\text{CAGR} = \left(\frac{\text{LastYearEVSales}}{\text{FirstYearEVSales}}\right)^{\frac{1}{\text{NumberOfYears}}} - 1
$$

🔄 **Penetration Rate Change from 2022 to 2024**:

- **Absolute Change** - Subtracting one value from another gives the absolute change, providing a straightforward comparison in percentage points. It is calculated as:

$$
AbsoluteChange = PenetrationRate_{2024} - PenetrationRate_{2022}
$$

- **Relative Change** - Dividing one value by the other gives the relative change, offering insight into how significant the change is compared to the initial value. It is calculated as:

$$
\left(\frac{PenetrationRate_{2024} - PenetrationRate_{2022}}{PenetrationRate_{2022}}\right) \times 100
$$

## 📥 Importing Data into PowerBI

Three CSV files were imported directly from SharePoint into Power BI using the required account credentials. Additional datasets, such as charging data, were later added through the same method.

## 🗂️ Data Model

<p align="center">
    <img src='https://github.com/Arindam430/EV_Sales_Analysis_PowerBI/blob/main/Resources/Data%20Model.png' height="400">
</p>

## 📊 Home Page

<p align="center">
    <img src='https://github.com/Arindam430/EV_Sales_Analysis_PowerBI/blob/main/Resources/1.%20Home%20Page.gif' width="600">
</p>

## 🏭 Makers Page

<p align="center">
    <img src='https://github.com/Arindam430/EV_Sales_Analysis_PowerBI/blob/main/Resources/2.%20Makers%20Page.gif' width="600">
</p>

## 🏙️ States Page

<p align="center">
    <img src='https://github.com/Arindam430/EV_Sales_Analysis_PowerBI/blob/main/Resources/3.%20States%20Page.gif' width="600">
</p>

## 🌍 Statewise Comparison Page

<p align="center">
    <img src='https://github.com/Arindam430/EV_Sales_Analysis_PowerBI/blob/main/Resources/4.%20Statewise%20Comparison%20Page.gif' width="600">
</p>

## 🎓 Learnings from this Project 

- Created a new type of bar chart visual (Horizontal Bar chart with labels above), useful for various analysis purposes.
- Implemented dynamic ranking (top/bottom filtration with Top-N Slicer) on the Sales by Makers page and Sales by State pages.
- Built dynamic tooltips for every page except the home page, unlocking different use cases during data analysis.
- The colors of the KPI visual and arrows change dynamically based on performance compared to the previous year. The intensity of the color reflects the degree of change, among other visual enhancements.
- Categorized the measures into folders and subfolders and provided proper documentation for each measure.
- The electric vehicle market in India is witnessing rapid growth, with a year-on-year (YoY) surge of ~50% in CY2023.
- EVs made up 6.5% of total vehicle sales last year, with the Electric 2W segment leading at 56% of all EV sales in CY2023, highlighting the growing EV market share in India.
- In terms of YoY sales growth, the electric car segment saw the highest growth rate of 116% in 2023.
- Utilized bookmarks and selection for various purposes, such as page navigation and filter clearing on the dashboard. [YouTube tutorial](https://www.youtube.com/watch?v=xCSYLrcLW00).
- Adopted a color palette for consistency throughout the dashboard ([Color palette link](https://coolors.co/palette/139a43-66d17f-0dab76-d19c1d-fe5f55)).

## 🔍 Key Insights from the Dashboard

- Ola Electric has consistently dominated the top position in 2-Wheelers sales from 2023 to 2024.
- Tata Motors has been the top seller in 4-wheeler EV sales every quarter from 2022 to 2024.
- The CAGR is highest for BMW India from 2022-24 in the 4-Wheelers category (1141%).
- Meghalaya has the highest CAGR among all states (28.47%).
- Gujarat, Delhi, and Maharashtra are the states providing the most subsidies.
- Not only does Maharashtra lead in both EV sales and the number of operational public charging stations, but it also provides substantial incentives for charging infrastructure, highlighting its robust support for electric vehicles. This makes it the ideal state for AtliQ Motors to start building their manufacturing unit.
- The Indian government provides various subsidies and rebates to reduce the purchase cost of EVs, making them more affordable for consumers.
- Apart from Gujarat, Delhi, Maharashtra, Meghalaya, Assam, and Kerala provide 100% Road Tax Exemption.
- Maharashtra has higher projected sales in 2030 in the 2-wheelers category, but Karnataka has higher projected sales in the 4-wheelers category.
- Goa has the highest penetration rate in the 2-Wheeler vehicle category in 2024, but its charging infrastructure is lacking (only 113 public charging stations), as well as EV sales (19,684 in total EV sales from 2022-24). Goa also has lower projected sales in 2030 due to low EV sales.
