# inmind.ai_Electra_Pulse_Board

## ElectraPulse board

During the internship at inmind.ai, the final project involved developing a dashboard for the admin of an electronics retail business operating several branches across different countries. This project is a supply chain project, with the admin acting as the retailer.

Note:This project is done in Palantir Foundry and Due to Palantir’s limitations, only screenshots with explanations will be provided for this project.

This is how the data lineage looks and how the data flows. Additionally, health checks are performed on the input, such as schema validation, and expectations are applied to the output, including last build time and primary key checks. A schedule is also set up to trigger the output whenever the connected input is updated.

<img width="1284" height="550" alt="Data Lineage" src="https://github.com/user-attachments/assets/3697d7a8-a0c9-497d-aa5d-dc63bfc74bba" />

Tools used in Palantir Foundry:
- Code repository (For data cleaning using PySpark and creating functions using TypeScript)
- Pipeline Builder
- Data Lineage
- Monitoring View
- Quiver
- Workshop 
- Ontology Manager (Actions)
- Solution Designer
- Jupyter Notebook (For Machine Learning)
- Health Checks & Schedules

Inventory: On the first page, the admin can Create, Edit, or Delete any device in the inventory. In addition, the admin can create scenarios to change prices (either by editing the price or applying a discount) and observe how the dashboard reacts. This feature helps the admin make informed business decisions. Scenarios can be saved for later use, shared with other admins, or applied directly to update the real data in the dashboard.

<img width="1544" height="723" alt="page1" src="https://github.com/user-attachments/assets/907e75a9-a1c2-467a-b84c-aad4e8d7a44a" />

<img width="1551" height="722" alt="Page1Overlay" src="https://github.com/user-attachments/assets/c44a8c45-978c-451f-9366-6f0b751d20cb" />

Price Prediction :The second page focuses on predictions. The admin can predict the price of any device based on market data. Two machine learning models based on Linear Regression were used: one predicts the best price of a laptop, and the other predicts the best price of a phone.


<img width="1550" height="722" alt="Predictions Page2" src="https://github.com/user-attachments/assets/39fc8a54-b4b3-46a1-abf3-859cd563326f" />

Repair and Orders : The main focus of this page is to display customer repair requests and order requests. The admin can toggle the status of any request once it is completed, and the sales details (cost, revenue, and profit) will automatically be added to the Sales and Profits table (last page).

<img width="1551" height="725" alt="Repair request page 3" src="https://github.com/user-attachments/assets/41611512-7ed6-43be-a7a0-013af24144bf" />

<img width="1551" height="728" alt="Repair Request page3 overlay" src="https://github.com/user-attachments/assets/514f082d-abd0-470c-8e4b-50c527618ee6" />



<img width="1550" height="720" alt="Order Request page 3" src="https://github.com/user-attachments/assets/c3f63cf4-40d9-436c-8af1-87139b1219ef" />

<img width="1549" height="725" alt="Order Request page 3 overlay" src="https://github.com/user-attachments/assets/8eece965-5bae-4bf9-b6b1-6ac7fbb438cb" />

Order Tab: Two cases are considered. If the requested quantity exists in stock, the customer directly receives the order. If the quantity is not available, the retailer must request it from the supplier, and this is where Page 4 comes into play.

Suppliers : The idea is that the retailer selects the nearest supplier to minimize transportation costs. The map is used for this purpose, and by simply clicking on any supplier, the admin can either place a call or create an order with that supplier.

<img width="1307" height="613" alt="Example Page4" src="https://github.com/user-attachments/assets/050fc9b3-fa36-44f3-84ab-efd5d6da2b09" />

Phone Details: 

<img width="1550" height="726" alt="Phone Details in a Company page4" src="https://github.com/user-attachments/assets/800b9cfa-0452-4d37-90c0-40cbab403d60" />

Order Details: 

<img width="1550" height="721" alt="Supplier and Order Details" src="https://github.com/user-attachments/assets/bdf67b41-1d68-4f97-a58f-f0907f70f152" />

Sales and Profits : Sales and Profits: This page displays all transactions in a table, representing completed order requests or repair requests. On the right, the most frequently asked questions by the admin are answered dynamically using charts.

<img width="1550" height="718" alt="Sales and profits page5" src="https://github.com/user-attachments/assets/a5c5b7eb-77af-4297-82f0-867051464995" />

For example, let’s assume the admin clicks on Revenue and Cost per Month: an overlay will open displaying the charts, with an option to download them as a PDF. The charts are dynamic, meaning any applied filter will affect all of them.

<img width="1549" height="723" alt="Q5 page5" src="https://github.com/user-attachments/assets/752b5e14-a39e-4899-8947-d97d5eae5f7d" />

