# Business Insights 360

## Project Overview

AtliQ Hardware has experienced rapid growth in recent years and, to maintain their competitive edge and facilitate data-driven decision-making, they have decided to implement data analytics using Power BI. This initiative aims to provide stakeholders with comprehensive insights across various aspects of the business, including finance, sales, marketing, and supply chain management.

This project was a part of the codebasics PowerBI course, Link to the course is [here](https://codebasics.io/bootcamps/dashboard/data-analytics-bootcamp-with-practical-job-assistance).

[Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiN2ZhOTc5YTUtOGQzZS00ZTYzLTg1YmEtYTA4NGNmYTg1ZTAzIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## Tech Stack

- PowerBI Desktop
- SQL
- MS Excel
- DAX language
- DAX studio

## Project Approach

### Questions to Ask Before Starting the Project:

#### Business Objectives:
- What are the primary goals of this Power BI implementation?
- Which business areas (finance, sales, marketing, supply chain) need the most attention?

#### Stakeholder Requirements:
- Who are the key stakeholders, and what specific insights do they need?
- Are there any existing pain points or data challenges that need addressing?

#### Data Sources:
- What data sources will be used, and how will data be integrated?
- Are there any data quality issues that need to be resolved beforehand?

#### Data Security and Compliance:
- What are the data security and compliance requirements?
- Who will have access to the reports and dashboards?

#### Technical Specifications:
- What are the technical requirements for the implementation?
- What is the current IT infrastructure, and how will Power BI fit into it?

#### Training and Support:
- What training will be provided to users?
- What support structures are in place for ongoing maintenance and troubleshooting?

### Key Steps in the Project:

#### Data Preparation and Modeling
- Creating Calculated Columns: Define new data columns using DAX (Data Analysis Expressions) for enhanced analysis.
- Creating Measures Using DAX Language: Develop complex calculations to summarize and analyze data effectively.
- Data Modeling: Establish relationships between different data tables to create a coherent data model.
- Creating Date Table Using M Language: Generate a date table to support time-based data analysis.

#### Visualizations and Interactivity
- Using Bookmarks to Switch Between Two Visuals: Implement bookmarks to allow users to toggle between different visual states seamlessly.
- Page Navigation with Buttons: Create interactive buttons for easy navigation between different report pages.
- Dynamic Titles Based on Applied Filters: Use DAX to create titles that change dynamically according to the filters applied.
- Using KPI Indicators: Implement Key Performance Indicators to monitor critical metrics.
- Conditional Formatting: Apply conditional formatting to highlight important values in visuals using icons or background colors.

#### Data Validation and Quality
- Data Validation Techniques: Ensure the accuracy and integrity of data through various validation methods.
- Using Divide Function to Prevent Zero Division Errors: Utilize the DIVIDE function in DAX to handle division operations safely.

#### Deployment and Maintenance
- Power BI Services: Use Power BI services to deploy and share reports.
- Publishing Reports to Power BI Services: Publish the developed reports to the Power BI service for broader access.
- Setting Up Personal Gateway for Auto-Refresh: Configure a personal gateway to enable automatic data refresh.
- Power BI App Creation: Develop a Power BI app for easier report distribution and access.
- Collaboration, Workspace, Access Permissions in Power BI Services: Manage collaboration and access permissions within Power BI workspaces.

#### Additional Considerations
- Regularly update and maintain the reports to ensure they remain relevant and accurate.
- Continuously gather feedback from stakeholders to refine and improve the reports and dashboards.

By addressing these areas, AtliQ Hardware can ensure a successful implementation of Power BI, providing valuable insights and supporting data-driven decision-making across the organization.

### Business Related Terms

- Gross Price: The total price of a product or service before any deductions such as discounts, rebates, or allowances. It represents the initial selling price.
- Pre-Invoice Deductions: Reductions applied to the gross price before the invoice is issued. These can include discounts, allowances, and promotional reductions agreed upon before invoicing.
-Post-Invoice Deductions: Deductions made after the invoice has been issued, such as returns, rebates, or allowances processed after the sale.
- Net Invoice Sale: The final amount billed to the customer after all pre-invoice and post-invoice deductions have been applied. It represents the actual revenue from the sale.
- Gross Margin: The difference between net sales and the cost of goods sold (COGS), expressed as a percentage. It measures the profitability of products before accounting for other operating expenses. Formula: (NetSales−COGS)/NetSales
- Net Sales: The total revenue from sales after deducting returns, allowances, and discounts. It represents the actual revenue earned from sales activities.
- Net Profit: The final profit after all expenses, including operating expenses, interest, taxes, and other costs, have been deducted from the gross margin. It is the bottom line of the income statement.
- COGS (Cost of Goods Sold): The direct costs attributable to the production of the goods sold by a company. This includes the cost of materials, labor, and manufacturing overhead used in creating the product.
- YTD (Year to Date): A period starting from the beginning of the current year to the present date. It is used to measure performance over this timeframe.
- YTG (Year to Go): The period from the present date to the end of the current year. It is used to project or plan for the remaining part of the year.
- Direct: Refers to sales made directly to the end consumer without intermediaries. This can include direct sales through company-owned stores or e-commerce sites.
- Retailer: A business or person that sells goods to the consumer, as opposed to selling to a wholesaler or distributor. Retailers buy products from distributors or manufacturers and sell them at a markup.
- Distributors: Intermediaries who purchase products from manufacturers and sell them to retailers or other businesses. They play a key role in the supply chain by facilitating product distribution.
- Consumer: The end user who purchases goods or services for personal use. Consumers are the final recipients in the supply chain.

## Understanding the data

Before starting the analysis, it is crucial to understand the available data thoroughly.
 - Dimension Table: Contains static data such as customer and product details.
 - Fact Table: Contains transactional data.

### Datasets

#### gdb0041:
    - dim_customer:
        - 27 distinct markets (e.g., India, USA, Spain)
        - 75 distinct customers across these markets
        - 2 types of platforms:
            - Brick & Mortar - Physical/offline stores
            - E-commerce - Online stores (e.g., Amazon, Flipkart)
        - 3 sales channels:
            - Retailer
            - Direct
            - Distributors
    
    - dim_market:
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    
    - dim_product:
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
    
    - fact_forecast_monthly:
        - This table is used to forecast customer needs in advance, leading to:
            - Higher customer satisfaction
            - Reduced warehouse storage costs
        - The table is denormalized by the data engineering team for analytical purposes.
        - All dates within the month are represented by the start date of the month.
        - It includes all relevant columns, with the final column indicating the forecasted quantity needed by the customer.

    - fact_sales_monthly:
        - This table is similar to the fact_forecast_monthly table.
        - The final column contains the actual sold quantity instead of the forecasted value.

#### gdb0056:

    - freight_cost: Contains details of travel and other costs associated with each market for the fiscal year.
    - gross_price: Provides information on gross prices associated with each product code.
    - manufacturing_cost: Details the manufacturing costs for each product code, including the year of the cost.
    - pre_invoice_deductions: Shows the pre-invoice deduction percentages for each customer, organized by year.
    - post_invoice_deductions: Includes details on post-invoice and other deductions.
    
## Importing data into PowerBI via MySQL

- Since the database for this project is MySQL, we need to import the datasets from the MySQL database into Power BI. This requires providing the necessary database access credentials.

## Data Model 
- Data modeling is crucial and forms the foundation of the report, as all visuals are built upon the data model.
- Ineffective data modeling can negatively impact the overall performance of the report.
- Adhering to best practices in data modeling is essential. For guidance on best practices, refer to this [Blog](https://addendanalytics.com/blog/data-modelling-best-practices).
- In this project, we have implemented the Snowflake data modeling method.


<img src = "https://github.com/yesh-ashok/Business-Insights-360/blob/main/Data_model_SS.jpg" class="center">

## Dashboard Designing

Based on the mock-ups provided as requirements, the team will begin designing the visuals and creating measures as needed.

### Home View

In the Home view, all view buttons will be available. Users can navigate to a specific view page by clicking the corresponding button:

- Info
- Finance View
- Sales View
- Marketing View
- Supply Chain View
- Executive View
- Support

### Overall Dashboard 
![Overall Report.gif](https://github.com/yesh-ashok/Business-Insights-360/blob/main/BI360_Dash_overview.gif)

Live dashboard can be accessed by clicking this [link](https://app.powerbi.com/view?r=eyJrIjoiN2ZhOTc5YTUtOGQzZS00ZTYzLTg1YmEtYTA4NGNmYTg1ZTAzIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9).

## Project Conclusion
By leveraging this report, you will be able to make informed decisions grounded in data-driven insights. The report provides a comprehensive analysis that helps in understanding various trends, patterns, and anomalies. This allows you to:
- Make Data-Driven Decisions: The report consolidates relevant data, enabling you to make strategic decisions based on factual evidence rather than intuition or guesswork.
- Analyze Situations Thoroughly: The detailed breakdown of data will assist in evaluating different scenarios and their outcomes, leading to more accurate and effective decision-making.
- Answer "Why" Questions: The report’s insights will help address numerous "why" questions related to your business or project. For instance, it can explain why certain trends are occurring, why specific metrics are changing, or why particular outcomes are observed. This deeper understanding is crucial for diagnosing issues, optimizing processes, and planning future strategies.
- Identify Root Causes: By examining the data, you can uncover the underlying factors contributing to observed results. This helps in identifying root causes of problems or successes, rather than just addressing symptoms.
- Improve Strategic Planning: The insights derived from the report can inform strategic planning, allowing you to anticipate future challenges and opportunities, and develop strategies that are aligned with actual data.

Overall, this report is a valuable tool for enhancing decision-making capabilities, understanding complex situations, and guiding strategic actions based on a robust analysis of the data.



