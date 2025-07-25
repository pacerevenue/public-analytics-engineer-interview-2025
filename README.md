# Analytics Engineer Pair Programming Interview

---

### 📂 Available Tables

We’ll provide a structured dataset containing hotel bookings, properties, and more. You’ll work with these tables:

- `reservation_pickups`
    
    This table contains all booking data for our demo properties in Q1 2025. The data is on a transactional level, i.e. for one `reservation_id` you may find multiple rows. Additionally, this data set is already pre-transformed to deal with changes to reservations over time. E.g. when a booking is cancelled you will find the revenue and occupancy created (positive values) and deducted (negative values) - summing across these rows will yield the latest state of each reservation.
    
- `d_properties`
    
    This table contains information about the properties.
    
- `daily_capacity_inventory`
    
    This table provides a full list of all different room types and their capacities on any given stay date. 
    

---

## 🧩 The Exercises

### **Part 1: Reservation Metrics (SQL Challenge)**

You’ll write a SQL query to calculate core monthly booking metrics, by property, that are essential to our users’ workflows. These include:

- **Total Net Revenue**
    
    The sum of net revenue for each booking by stay date.
    
- **Total Units Occupied**
    
    Sum of occupancy per booking.
    
- **Average Daily Rate (ADR)**
    
    Net revenue ÷ units occupied, for confirmed bookings only
    

You’ll discuss your approach and write a query that correctly calculates these metrics.

---

### **Part 2: Data Visualisation**

- Using the results of your previous query, create visualisations in Omni with Revenue as the measure, broken down by Property and Month.
- Next focus on visualising the revenue mix per property per month.

Feel free to experiment with different chart types and formatting options, the aim is to communicate the insights as clearly and effectively as possible.

---

### **Part 3: Further Analysis**

In this section, we’ll dive into some additional data to explore how it could be leveraged for further analysis. 

---