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

#### gdb041:
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
              
