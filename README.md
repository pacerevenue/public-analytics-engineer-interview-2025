# Analytics Engineer Pair Programming Interview

---

### 📂 Available Tables

In this repository, you'll find a structured dataset containing hotel bookings, properties, and more. Please note that not all columns in the tables will be used in the SQL questions, as the dataset as a whole will also serve as a basis for our subsequent technical discussions. You are encouraged to explore the dataset prior to the interview and to raise any clarifying questions before/during the interview.

Below is an overview of the tables in the dataset:

- `reservation_pickups`
    
    This table contains all booking (or reservation) data for our demo properties in Q1 2025. 
    
    The data is on a transactional level, i.e. for one `reservation_id` you may find multiple rows. Additionally, this data set is already pre-transformed to deal with changes to reservations over time - e.g. when a booking is cancelled you will find the revenue and occupancy created (positive values) in one version and deducted (negative values) in a later version, resulting in a total of 0 units sold and a total revenue of 0 - i.e. summing across these rows will yield the latest state of each reservation.

    Other points to note about the table / terminologies:
    - "inventory type" is often referred to as "room type"; you may explore the `inventory_type_name` column for some example values
    - `property_name` is included in this table for easy access
    - `stay_date` is the date on which the room was stayed in; when we say units sold in a "stay month", we mean units sold on any stay date within the month
    - `latest_status` reflects the latest (or final) status of the booking, and can be either `confirmed` or `cancelled`
    - `occupancy` is the number of units sold
    - unless otherwise specified, we often refer to "net revenue" as just "revenue"
    - there are multiple revenue columns whose values are the revenue amounts in either the local currency of the property, USD, or EUR (i.e., the amounts have all been converted when preparing the table, so no additional currency conversion is needed)
    
- `d_properties`
    
    This table contains information about the properties, such as each property's opening date and booking currency.
    
- `daily_capacity_inventory`
    
    This table provides a full list of all different room types and their capacities on any given stay date. 

---

## 🧩 The Exercises

### **Part 1: Reservation Metrics (SQL Challenge)**

You’ll write a SQL query to calculate core booking metrics, by property and by stay month, that are essential to our users’ workflows. These include:

- **Total Net Revenue**
    
    Sum of net revenue
    
- **Total Units Occupied**
    
    Sum of occupancy
    
- **Average Daily Rate (ADR)**
    
    Net revenue ÷ units occupied

You’ll discuss your approach and write a query that correctly calculates these metrics.

---

### **Part 2: Data Visualisation**

- Using the results of your previous query, create visualisations in Omni with revenue as the measure, broken down by property and stay month.
- Next, focus will be on visualising what we call the "revenue mix". More details will be given during the interview.

Feel free to experiment with different chart types and formatting options; the aim is to communicate the insights as clearly and effectively as possible.

---

### **Part 3: Further Analysis**

In this section, we'll dive into some additional tasks/discussions on data modelling related to the given dataset.

---