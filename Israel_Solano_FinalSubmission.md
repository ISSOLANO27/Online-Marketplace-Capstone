
# **The Artisan Vault System**

## **Analysis Phase – Final Marketplace Submission**

**Student:** Israel
**Course:** Systems Analysis & Design


# **1. Stakeholder Persona**

**Primary Stakeholder:** *Mr. Carrión – Artisan and Business Owner*
Mr. Carrión creates handcrafted furniture and décor from home while balancing a full-time job. He manages sales using Excel, Word, a physical notebook, WhatsApp/SMS, and in-home storage rooms.

**Goals**

* Keep workflow simple
* Maintain quality and customer satisfaction
* Track orders, payments, and inventory reliably

**Pain Points**

* Switching between tools
* Customer delays impacting workflow
* Manual tracking of inventory, pricing, and deadlines
* Late pickups creating storage issues

**Definition of Success**
A system that centralizes communication, tracks orders, automates reminders, manages inventory, and mirrors his natural workflow without adding complexity.

---


**External Entities:**

* Customer
* Artisan (Mr. Carrión)
* Bank/Payment Service
* Communication Channels

**System Purpose:**
The Artisan Vault System supports: inquiries, custom quote creation, reservations, scheduling, payment tracking, notifications, and inventory updates.

---

# **Workflows**

## **Workflow A – Stock Item Purchase (As-Is)**

1. Customer contacts Mr. Carrión requesting item availability.
2. Artisan checks inventory and responds with availability + price.
3. Customer confirms item → artisan logs details and sets item aside.
4. Pickup date agreed via WhatsApp/SMS.
5. Two days before pickup → artisan sends a photo update.
6. On pickup day → reminder is sent.
7. Customer pays in full (cash/transfer).
8. Item is handed over.
9. Artisan updates Excel to mark item as sold.

**Exception:**
If the customer cancels, the item is placed back in inventory and Excel is updated later.

---

## **Workflow B – Custom Order Process (As-Is)**

1. Customer sends idea/photo for a custom item.
2. Artisan evaluates feasibility (materials, labor, workload).
3. Artisan calculates price: materials + labor + overhead × multiplier (2.0–3.0×).
4. Customer receives quote; work does not start until **50% deposit** is paid.
5. Materials purchased → timeline updated within 2 days.
6. Artisan creates the piece; logs complications (weather, delays).
7. Customer may request design changes → price/timeline recalculated.
8. When completed → photo update sent 2 days before pickup.
9. Customer pays final 50% and receives item.
10. Artisan updates Excel.

---

# **Use Case Diagram**

*(Insert your PNG here once you add it)*
`![Use Case Diagram](usecasediagram_AVS.png)`

**Main Actors:**

* Customer
* Artisan
* System

**Primary Use Cases:**

* Inquire About Stock Item
* Purchase Stock Item
* Request Custom Order
* Approve Custom Quote
* Manage Custom Order Progress
* Complete Order & Pickup
* Handle Late Pickup Fees
* Update Inventory
* Manage Notifications

---

# **Use Case Descriptions**

### **UC-01: Inquire About Stock Item**

**Actor:** Customer
**Goal:** Check availability and price.
**Flow:** Customer sends inquiry → system retrieves items → artisan confirms → customer receives details.

---

### **UC-02: Purchase Stock Item**

**Actor:** Customer
**Goal:** Reserve and buy a stock craft item.
**Flow:** Customer selects item → reservation recorded → reminders sent → payment made → inventory updated.

---

### **UC-03: Request Custom Order**

**Actor:** Customer
**Goal:** Submit custom item idea.
**Flow:** Customer uploads description/photo → artisan reviews → system records request.

---

### **UC-04: Approve Custom Order Quote**

**Actor:** Customer
**Goal:** Approve the quote and activate the job.
**Flow:** System sends quote → customer approves → deposit paid → order becomes active.

---

# **Functional Requirements (Condensed)**

### **Customer Interaction**

* FR1: System shall allow customers to submit inquiries about stock items.
* FR2: System shall return availability and pricing information.

### **Stock Item Orders**

* FR3: System shall reserve a stock item upon customer confirmation.
* FR4: System shall send pre-pickup reminders.
* FR5: System shall update inventory when an item is sold.

### **Custom Orders**

* FR6: System shall accept custom requests with text/photos.
* FR7: System shall calculate quotes based on materials, labor, and multipliers.
* FR8: System shall require a 50% deposit before activating a custom order.

### **Order Tracking & Notifications**

* FR9: System shall send timeline updates and photo notifications.
* FR10: System shall track late pickups and apply storage fees after a 2-day grace period.

### **Payments & Inventory**

* FR11: System shall store payment records (deposit, final, late fees).
* FR12: System shall maintain inventory for all stock items.

---

# **Non-Functional Requirements (Condensed)**

### **Performance**

* NFR1: System responds to user actions within 2 seconds.

### **Reliability**

* NFR2: System shall not lose customer, order, or payment data.

### **Security**

* NFR3: All communication and data shall be encrypted.
* NFR4: Only authenticated artisans can access order management.

### **Usability**

* NFR5: Interface must remain simple and mobile-friendly.

### **Maintainability**

* NFR6: Pricing rules and fee policies must be configurable.

### **Scalability**

* NFR7: System must support more items, artisans, or categories without redesign.

---

# **Preliminary Data Model (High-Level)**

**Entities:**

* Customer
* Order
* Item
* Payment
* Notification
* LatePickupRecord

**Key Relationship Example:**

* One customer → many orders
* One order → one or many items
* One order → multiple payments
* One order → multiple notifications


