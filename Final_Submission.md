# The Artisan Vault System  
## Systems Analysis – Final Marketplace Submission  

**Student:** Israel  
**Course:** System Analysis and Design  
**Date:**  

---

## Table of Contents

1. Stakeholder Persona  
2. Context Diagram  
3. Workflow Diagrams  
4. Use Case Diagram  
5. Use Case Descriptions  
6. Use Case Dialogue  
7. Functional Requirements  
8. Non-Functional Requirements  
9. Preliminary Data Model  
10. Requirements Validation Log  

---

## 1. Stakeholder Persona


**project**: The Artisan Vault

**Persona** Type: Primary Stakehokder/End User

**Role**: Craftsman & Business Owner

## Background
My father-in law, Mr Carrion is an experienced craftsman specializing in handmande decor, furniture, and custom household pieces. With decades of hands on practice, he maintains a highly personal and manual approach to managing his business. He has experience using Excel and Word since the 90s, but refers keeping his workflow simple and lean. He often balances crafting with a separate 9-5 job and works entirely from home, using dedicated spaces in his home for storage, preparation and pickup.

## Goals and Motivations
* Maintain complete control over every piece he creates
* Provides customers with reliable craftsmanship and timely communications.
* Keep processes simple without unnecessary technologies
* Track sales and inventory in the least intrusive way
* Make sure prices are fair, consistent, and is a reflection of real costs in labor and materials
* Avoids over commiting with large custom or high-cost projects

## Technology Skill Level
* Comfortable with basic Excel (tracking sales and inventory)
* Uses Word templates for invoices
* Communicates via WhatsApp, SMS, and email
* Struggles with complex apps; rather have simple direct tools
* Heavily realies on a notebook for notes before updating his digital tools of choice

## Current Tools
* Excel: sale logs, inventory tracking, and customer order details
* Word: invoice templates
* Notebook: primary tool for quick entries
* Iphone: customer communication and sending images
* Home storage areas: Bedroom 1, 2, 3 and Living Room

## Pain Points
* Manually switching between Excel, Word, Whatsapp and visible notes
* Customer delays in confirming design changes causes workflow to slowdown or stop
* Wheather delays (rain in Cancun) affecting drying/painting
* Struggles to maintain consistent project updates
* Time spent retyping invoice details repeatedly
* Ocassion late pickups requires tracking of storage fees

## Workflow Habits
* Responds to customers within ~15 minutes
* Confirms availability only after physically checking inventory
* records customer information only after they confirm **item** and **price**
* Sets items aside immediately once they are reserved
* Tracks all financial entries after full payment
* Follows a First Come First Out (FIFO) unless costs exceed 500$ AND has urgency (then priority jumps)
* Accepts max number of four high cost urgent project at the same time
* Uses a 2 day grace period for late pickups before applying daily storage fees

## Constraints and Fears
* Does not want overly complex or rigid system
* Prefers tools that mimic his current workflow instead of replacing it
* Worried about losing the personal quality of his craft through automation
* Limited time due to 9 to 5 job; system **must** reduce his workload; not increase it

## Definition of Success
A system that:
* Save some time on repetitive tasks (Invoices updates, inventory adjustments)
* Centralizes his communication, orders, and inventory without overwhelming him
* Respects his pricing rules and workflow habits
* Helps prevent delays, miss updates, or forgotten adjustments
* Feels natural, simple and aligned with the way he already works



---

## 2. Context Diagram


![Context Diagram](contextdiagram_AVS.png)



---














## 3. Workflow Diagrams


## 1. Purpose

These workflows describe the **current workflow** business processes used by Mr. Carrión to manage The Artisan Vault. They focus on the **sequence of activities** performed by the artisan and the customer, and will later be used to derive **use cases** and **functional requirements**.

<br>
<br>


## 2. Workflow #1 – Stock Item `non-custom` Purchase  (As-Is)

### 2.1 Description

This workflow shows how a **non-custom**, stock craft item is sold today, from the moment a customer expresses interest to the point where the item is picked up, paid for, and recorded as sold in Excel.

Actors:
- **Customer**
- **Artisan (Mr. Carrión)**

Systems / tools involved:
- WhatsApp / SMS / Email
- Physical inventory (home storage)
- Notebook
- Excel (sales + inventory file)
- Word (invoice template)

---

### 2.2 Main Flow (Successful Stock Item Sale)

**Step 1 – Customer expresses interest**  
- **Actor:** Customer  
- **Action:** Customer contacts the artisan (usually via WhatsApp/SMS, sometimes word of mouth) asking about available items.  

**Step 2 – Artisan reviews request**  
- **Actor:** Artisan  
- **Action:** Reads the message and interprets what type of craft the customer is looking for (mirror, frame, chair, table, décor, etc.).  

**Step 3 – Artisan checks inventory physically**  
- **Actor:** Artisan  
- **Action:** Physically checks his home inventory to see which items match the customer’s interest.  
- **Note:** This is based on memory plus what he has set aside or stored in bedrooms/living areas.

**Step 4 – Artisan responds with availability and price**  
- **Actor:** Artisan  
- **Action:** Sends the customer a response listing:  
  - which items are available,  
  - the price of each,  
  - and an image if the customer requests one.  

**Step 5 – Customer chooses item and confirms**  
- **Actor:** Customer  
- **Action:** Customer confirms which stock item they want and agrees to the stated price.  

**Step 6 – Artisan records order details in notebook**  
- **Actor:** Artisan  
- **Action:** Only after confirmation, he writes the order in his notebook, including:  
  - customer name  
  - item name/type  
  - quantity  
  - price  
  - date  
  - pickup details  
  - payment status (pending)

**Step 7 – Artisan physically reserves the item**  
- **Actor:** Artisan  
- **Action:** Removes the item from general display/storage and sets it aside (bedroom or living room).  
- **Note:** If the item is fragile (e.g., glass), he wraps it in bubble wrap or cloth.

**Step 8 – Pickup date is agreed**  
- **Actors:** Customer, Artisan  
- **Action:** Through WhatsApp/SMS, they agree on a pickup date.  
- **Constraint:** Artisan aligns pickup time with his 9–5 work schedule but remains flexible.

**Step 9 – Artisan continues normal work until pickup approaches**  
- **Actor:** Artisan  
- **Action:** Continues working on other crafts and possibly other orders; the reserved stock item is mentally prioritized but does not block other work.

**Step 10 – First notification with photo (2 days before pickup)**  
- **Actor:** Artisan  
- **Action:** Two days before the agreed pickup date, the artisan:  
  - takes a photo of the finished/ready piece with his phone,  
  - sends the photo and a short message via WhatsApp/SMS/Email to the customer.  

**Step 11 – Day-of pickup reminder (no photo)**  
- **Actor:** Artisan  
- **Action:** On the day of pickup, sends a simple reminder message (no additional photo) to confirm that the customer is still coming.

**Step 12 – Customer arrives for pickup**  
- **Actors:** Customer, Artisan  
- **Action:** Customer comes to the artisan’s home to inspect and pick up the piece.  

**Step 13 – Payment before handing over item**  
- **Actor:** Customer, Artisan  
- **Action:**  
  - Customer pays **in full**, either cash or bank transfer.  
  - Artisan **never** hands over the item until payment is confirmed.  

**Step 14 – Artisan prepares and finalizes invoice**  
- **Actor:** Artisan  
- **Action:** Using his Word template (often prepared right before the visit), he fills in the invoice details and gives the customer a typed invoice/receipt.

**Step 15 – Item is handed over to customer**  
- **Actor:** Artisan  
- **Action:** Only after payment is confirmed and the invoice is ready, the artisan gives the physical craft item to the customer.

**Step 16 – Excel sales and inventory update**  
- **Actor:** Artisan  
- **Action:** Later (often at night), the artisan:  
  - logs the sale in his Excel sales file,  
  - updates the inventory quantity for that item,  
  - effectively marking the item as **sold**.  

---

### 2.3 Alternate / Exception Path – Customer Cancels Before Pickup (High-Level)

**A1 – Customer cancels reservation**  
- Customer sends a message cancelling the order before pickup.  

**A2 – Artisan eventually frees up inventory**  
- Artisan physically returns the reserved item to general inventory storage.  
- At some later time (not always immediately), he updates Excel to show the item as available again.  
- No follow-up is performed; the artisan does not chase cancelled customers.

*(This alternate path will be expanded later into its own workflow if needed.)*

---

<br>
<br>

## 3. Workflow #2 – Custom Order Process (As-Is)

### 3.1 Description

This workflow models the complete **custom craft order** process used today by Señor Carrión. A custom order involves evaluating feasibility, calculating material and labor costs, collecting a mandatory deposit, managing updates and complications, communicating with the customer, and final delivery with full payment. This process is significantly more complex than a stock sale and includes multiple decision points that affect cost, timeline, and workflow continuity.

Actors:
- **Customer**
- **Artisan (Señor Carrión)**

Tools/Systems involved:
- WhatsApp / SMS / Email  
- Notebook  
- Excel (tracking details and materials)  
- Word (invoice template)  
- Physical workspace and storage areas  

---

### 3.2 Main Flow – Successful Custom Order

**Step 1 – Customer requests a custom craft**  
- Customer contacts the artisan through WhatsApp/SMS asking if a specific custom piece is possible.  
- Customer may send an idea, reference photo, or general description.

**Step 2 – Artisan evaluates feasibility**  
- Artisan takes time to analyze the request.  
- He determines whether the project is realistic based on:  
  - required materials  
  - skill complexity  
  - size  
  - labor hours  
  - his current workload  
- If the project is not feasible, he declines politely.

**Step 3 – Artisan performs material cost estimation**  
- Gathers receipts or past references for material costs.  
- Estimates total materials required.  
- Calculates cost based on what is typically needed for that type of craft.

**Step 4 – Artisan estimates labor cost**  
- Applies his standard labor rate of **$15/hour**.  
- Makes an educated guess based on past experience for similar builds.

**Step 5 – Artisan determines overhead cost**  
- If materials < $120 → overhead = $25  
- If materials > $150 → overhead = $50  
- Overhead represents tool usage, storage, and general workshop costs.

**Step 6 – Artisan applies the markup multiplier**  
Multiplier depends on the size or purpose of the project:  
- Small pieces → **2.0×**  
- Medium pieces (chairs, benches, tables) → **2.2×**  
- Large pieces (headboards, toy chests, dining tables) → **3.0×**  
- Commercial clients (hotels/restaurants) → **always 3.0×**

**Step 7 – Artisan calculates the initial price**  
Total Price = (Materials + Labor + Overhead) × Multiplier

**Step 8 – Artisan sends initial quote to the customer**  
- Sent via WhatsApp/SMS/email.  
- Customer reviews the cost.  
- Customer may request clarification or adjustments.

**Step 9 – Customer partially pays or waits to gather funds**  
- Customers sometimes send small amounts (e.g., 10%) early.  
- **These do NOT authorize the project to begin.**  
- Artisan does not start until full 50% deposit is met.

**Step 10 – Customer pays the 50% deposit**  
- Required deposit to authorize materials purchase.  
- Customer sends via cash or bank transfer.  
- Artisan records deposit in notebook.

**Step 11 – Artisan purchases materials**  
- After the 50% deposit is received.  
- Keeps receipts for accurate tracking.

**Step 12 – Artisan updates timeline**  
- Within two days of purchasing materials, artisan provides an updated and more realistic timeline for completion.  
- Timeline is primarily based on **size category**:  
  - Small → 2–5 days  
  - Medium → 7–10 days  
  - Large → 14+ days  

**Step 13 – Artisan begins crafting the item**  
- Work starts only after materials are purchased and timeline is sent.

**Step 14 – Artisan may encounter complications**  
Examples:  
- Weather delays (rain interfering with drying/painting)  
- Material defects  
- Unexpected adjustments needed  
- Tool-related slowdowns  
- Customer delayed responses  

**Step 15 – Artisan logs issues in notebook**  
- Records complications or delays.  
- These may affect timeline but he continues unless customer action is required.

**Step 16 – Mid-project update (optional but ideal)**  
- Artisan attempts to give a progress update halfway through.  
- However, customer response delays can stall work.

**Step 17 – Customer requests design change (optional)**  
- If customer changes design mid-project:  
  - Artisan recalculates cost **the same day**.  
  - Adjusts timeline accordingly.  
  - Communicates new price and requirements.  
  - Customer must reconfirm.

**Step 18 – Artisan completes the custom craft**  
- Once done, the artisan prepares the piece for pickup storage.

**Step 19 – First notification with photo (2 days before pickup)**  
- Sends photo of finished project through SMS/WhatsApp/email.  
- Confirms that the agreed pickup date still works.

**Step 20 – Day-of pickup reminder (no photo)**  
- Sends a simple reminder message on the day of pickup.

**Step 21 – Customer arrives for pickup**  
- Customer inspects the piece.  

**Step 22 – Customer pays remaining 50% balance**  
- Artisan receives final payment (cash or bank transfer).  
- **No item is released without full payment.**

**Step 23 – Artisan prepares and prints invoice**  
- Uses Word template.  
- Gives customer the printed copy.

**Step 24 – Artisan hands over the custom craft**  
- Only after payment and invoice are finalized.

**Step 25 – Artisan updates Excel**  
- Logs sale and financial details.  
- Marks the custom product as completed.  
- No physical “inventory” update is required since this is not a stock item.

---

### 3.3 Alternate / Exception Paths

**A1 – Insufficient deposit**  
- Customer pays less than 50%.  
- Artisan does NOT begin the project.  
- Materials are NOT purchased.  

**A2 – Project not feasible**  
- Artisan declines the request at Step 2.

**A3 – Customer disappears or delays confirmation**  
- Artisan may pause the timeline and await a response.  
- This can delay multiple projects.

**A4 – Weather delay**  
- Rain delays drying, painting, or outdoor steps.  
- Artisan logs delay and notifies customer if delay > 2 days.

**A5 – Design change after work has started**  
- Artisan recalculates cost immediately.  
- Timeline is reset or extended.  
- Customer must reconfirm.

**A6 – Late pickup**  
- After 2-day grace period, daily storage fee begins (100 pesos/day or $5/day).  
- Artisan communicates fees via WhatsApp/SMS/email.

---

<br>
<br>

## 4. Workflow #3 – Late Pickup & Storage Fee Handling (As-Is)

### 4.1 Description

This workflow models what happens when a **customer does not pick up a finished item on the agreed date**, and how Mr. Carrion applies his **grace period** and **daily storage fee** policy. This applies to both **stock items** and **custom crafts** that have been fully completed and set aside for pickup.

Actors:
- **Customer**
- **Artisan (Mr. Carrion)**

Tools/Systems involved:
- WhatsApp / SMS / Email  
- Physical storage space (bedroom/living room)  
- Notebook  
- Excel (optional, if he chooses to record storage charges)  

---

### 4.2 Main Flow – On-Time Pickup (No Fees)

**Step 1 – Pickup date is agreed in advance**  
- During the order or completion process, the customer and Mr. Carrion agree on a specific pickup date and, roughly, time.

**Step 2 – First notification with photo (2 days before pickup)**  
- Already part of the main workflows for stock and custom orders.  
- Confirms that the item is ready and reminds the customer of the pickup date.

**Step 3 – Day-of pickup reminder**  
- On the agreed day, Mr. Carrion sends a reminder message (no photo) to confirm that the customer is still coming.

**Step 4 – Customer arrives on or before agreed date**  
- Customer picks up the item on time.  
- No storage fee is applied.  
- Payment and handover follow the normal workflow.  

*(In this case, Workflow #3 does not deviate from the main stock/custom flows.)*

---

### 4.3 Late Pickup Flow – Applying Grace Period and Storage Fees

**Step 1 – Agreed pickup date passes without pickup**  
- The scheduled pickup date arrives and the customer does not show up.  
- The item remains stored in Mr. Carrion’s home (bedroom/living room or protected area).

**Step 2 – Grace period begins (Day 1 and Day 2 after pickup date)**  
- Mr. Carrion applies a **2-day grace period** after the agreed pickup date.  
- During these 2 days, no fee is charged.  
- The item continues to occupy storage space.

**Step 3 – Storage fee starts on Day 3**  
- Starting on the **3rd day after the agreed pickup date**, a **daily storage fee** is applied.  
- Fee rule: **100 pesos/day (≈ $5/day)**.  
- This fee is tied to the customer’s delay, not to the type of craft.

**Step 4 – Artisan may notify customer about accumulating fees**  
- Using WhatsApp/SMS/email, Mr. Carrion may send a message explaining:  
  - that the agreed date has passed,  
  - that a 2-day grace period was given,  
  - that daily storage charges are now accumulating.  

**Step 5 – Customer eventually responds and schedules a new pickup**  
- Customer contacts Mr. Carrion to arrange a new pickup date.  
- At this point, the total days of delay can be counted.

**Step 6 – Customer arrives for late pickup**  
- Customer comes to pick up the item on the new date.

**Step 7 – Calculation of total amount due**  
- Total due includes:  
  - remaining balance for the craft (if any), plus  
  - accumulated storage fees (number of chargeable days × daily fee).  

**Step 8 – Customer pays full amount (craft + fees)**  
- Payment is made via cash or bank transfer.  
- As with all other workflows, **no item is released without full payment**, including storage fees.

**Step 9 – Item is handed over to customer**  
- Item is given to the customer only after payment is confirmed.

**Step 10 – Optional recording of storage fee in Excel**  
- If desired, Mr. Carrion may log the additional storage revenue in Excel.  
- The item is treated as sold/closed in his normal tracking.

---

### 4.4 Alternate / Exception Paths

**A1 – Customer never returns**  
- Item remains stored long-term.  
- At some point, Mr. Carrion may decide to:  
  - reclassify the item as available for sale again,  
  - resell it to another customer.  
- Storage fee may be considered forfeited or ignored if no final pickup occurs.

**A2 – Artisan chooses not to enforce fees**  
- For certain customers (e.g., family or special cases), he may waive or reduce the fee.  
- This is handled informally and not always recorded.

**A3 – Cancellation after grace period**  
- Customer cancels after the pickup date.  
- Item is returned to general inventory.  
- Any prior payments (if any) are handled according to his personal judgment (case by case).  

---




---

## 4. Use Case Diagram



## 1. Purpose

These workflows describe the **current workflow** business processes used by Mr. Carrión to manage The Artisan Vault. They focus on the **sequence of activities** performed by the artisan and the customer, and will later be used to derive **use cases** and **functional requirements**.

<br>
<br>


## 2. Workflow #1 – Stock Item `non-custom` Purchase  (As-Is)

### 2.1 Description

This workflow shows how a **non-custom**, stock craft item is sold today, from the moment a customer expresses interest to the point where the item is picked up, paid for, and recorded as sold in Excel.

Actors:
- **Customer**
- **Artisan (Mr. Carrión)**

Systems / tools involved:
- WhatsApp / SMS / Email
- Physical inventory (home storage)
- Notebook
- Excel (sales + inventory file)
- Word (invoice template)

---

### 2.2 Main Flow (Successful Stock Item Sale)

**Step 1 – Customer expresses interest**  
- **Actor:** Customer  
- **Action:** Customer contacts the artisan (usually via WhatsApp/SMS, sometimes word of mouth) asking about available items.  

**Step 2 – Artisan reviews request**  
- **Actor:** Artisan  
- **Action:** Reads the message and interprets what type of craft the customer is looking for (mirror, frame, chair, table, décor, etc.).  

**Step 3 – Artisan checks inventory physically**  
- **Actor:** Artisan  
- **Action:** Physically checks his home inventory to see which items match the customer’s interest.  
- **Note:** This is based on memory plus what he has set aside or stored in bedrooms/living areas.

**Step 4 – Artisan responds with availability and price**  
- **Actor:** Artisan  
- **Action:** Sends the customer a response listing:  
  - which items are available,  
  - the price of each,  
  - and an image if the customer requests one.  

**Step 5 – Customer chooses item and confirms**  
- **Actor:** Customer  
- **Action:** Customer confirms which stock item they want and agrees to the stated price.  

**Step 6 – Artisan records order details in notebook**  
- **Actor:** Artisan  
- **Action:** Only after confirmation, he writes the order in his notebook, including:  
  - customer name  
  - item name/type  
  - quantity  
  - price  
  - date  
  - pickup details  
  - payment status (pending)

**Step 7 – Artisan physically reserves the item**  
- **Actor:** Artisan  
- **Action:** Removes the item from general display/storage and sets it aside (bedroom or living room).  
- **Note:** If the item is fragile (e.g., glass), he wraps it in bubble wrap or cloth.

**Step 8 – Pickup date is agreed**  
- **Actors:** Customer, Artisan  
- **Action:** Through WhatsApp/SMS, they agree on a pickup date.  
- **Constraint:** Artisan aligns pickup time with his 9–5 work schedule but remains flexible.

**Step 9 – Artisan continues normal work until pickup approaches**  
- **Actor:** Artisan  
- **Action:** Continues working on other crafts and possibly other orders; the reserved stock item is mentally prioritized but does not block other work.

**Step 10 – First notification with photo (2 days before pickup)**  
- **Actor:** Artisan  
- **Action:** Two days before the agreed pickup date, the artisan:  
  - takes a photo of the finished/ready piece with his phone,  
  - sends the photo and a short message via WhatsApp/SMS/Email to the customer.  

**Step 11 – Day-of pickup reminder (no photo)**  
- **Actor:** Artisan  
- **Action:** On the day of pickup, sends a simple reminder message (no additional photo) to confirm that the customer is still coming.

**Step 12 – Customer arrives for pickup**  
- **Actors:** Customer, Artisan  
- **Action:** Customer comes to the artisan’s home to inspect and pick up the piece.  

**Step 13 – Payment before handing over item**  
- **Actor:** Customer, Artisan  
- **Action:**  
  - Customer pays **in full**, either cash or bank transfer.  
  - Artisan **never** hands over the item until payment is confirmed.  

**Step 14 – Artisan prepares and finalizes invoice**  
- **Actor:** Artisan  
- **Action:** Using his Word template (often prepared right before the visit), he fills in the invoice details and gives the customer a typed invoice/receipt.

**Step 15 – Item is handed over to customer**  
- **Actor:** Artisan  
- **Action:** Only after payment is confirmed and the invoice is ready, the artisan gives the physical craft item to the customer.

**Step 16 – Excel sales and inventory update**  
- **Actor:** Artisan  
- **Action:** Later (often at night), the artisan:  
  - logs the sale in his Excel sales file,  
  - updates the inventory quantity for that item,  
  - effectively marking the item as **sold**.  

---

### 2.3 Alternate / Exception Path – Customer Cancels Before Pickup (High-Level)

**A1 – Customer cancels reservation**  
- Customer sends a message cancelling the order before pickup.  

**A2 – Artisan eventually frees up inventory**  
- Artisan physically returns the reserved item to general inventory storage.  
- At some later time (not always immediately), he updates Excel to show the item as available again.  
- No follow-up is performed; the artisan does not chase cancelled customers.

*(This alternate path will be expanded later into its own workflow if needed.)*

---

<br>
<br>

## 3. Workflow #2 – Custom Order Process (As-Is)

### 3.1 Description

This workflow models the complete **custom craft order** process used today by Señor Carrión. A custom order involves evaluating feasibility, calculating material and labor costs, collecting a mandatory deposit, managing updates and complications, communicating with the customer, and final delivery with full payment. This process is significantly more complex than a stock sale and includes multiple decision points that affect cost, timeline, and workflow continuity.

Actors:
- **Customer**
- **Artisan (Señor Carrión)**

Tools/Systems involved:
- WhatsApp / SMS / Email  
- Notebook  
- Excel (tracking details and materials)  
- Word (invoice template)  
- Physical workspace and storage areas  

---

### 3.2 Main Flow – Successful Custom Order

**Step 1 – Customer requests a custom craft**  
- Customer contacts the artisan through WhatsApp/SMS asking if a specific custom piece is possible.  
- Customer may send an idea, reference photo, or general description.

**Step 2 – Artisan evaluates feasibility**  
- Artisan takes time to analyze the request.  
- He determines whether the project is realistic based on:  
  - required materials  
  - skill complexity  
  - size  
  - labor hours  
  - his current workload  
- If the project is not feasible, he declines politely.

**Step 3 – Artisan performs material cost estimation**  
- Gathers receipts or past references for material costs.  
- Estimates total materials required.  
- Calculates cost based on what is typically needed for that type of craft.

**Step 4 – Artisan estimates labor cost**  
- Applies his standard labor rate of **$15/hour**.  
- Makes an educated guess based on past experience for similar builds.

**Step 5 – Artisan determines overhead cost**  
- If materials < $120 → overhead = $25  
- If materials > $150 → overhead = $50  
- Overhead represents tool usage, storage, and general workshop costs.

**Step 6 – Artisan applies the markup multiplier**  
Multiplier depends on the size or purpose of the project:  
- Small pieces → **2.0×**  
- Medium pieces (chairs, benches, tables) → **2.2×**  
- Large pieces (headboards, toy chests, dining tables) → **3.0×**  
- Commercial clients (hotels/restaurants) → **always 3.0×**

**Step 7 – Artisan calculates the initial price**  
Total Price = (Materials + Labor + Overhead) × Multiplier

**Step 8 – Artisan sends initial quote to the customer**  
- Sent via WhatsApp/SMS/email.  
- Customer reviews the cost.  
- Customer may request clarification or adjustments.

**Step 9 – Customer partially pays or waits to gather funds**  
- Customers sometimes send small amounts (e.g., 10%) early.  
- **These do NOT authorize the project to begin.**  
- Artisan does not start until full 50% deposit is met.

**Step 10 – Customer pays the 50% deposit**  
- Required deposit to authorize materials purchase.  
- Customer sends via cash or bank transfer.  
- Artisan records deposit in notebook.

**Step 11 – Artisan purchases materials**  
- After the 50% deposit is received.  
- Keeps receipts for accurate tracking.

**Step 12 – Artisan updates timeline**  
- Within two days of purchasing materials, artisan provides an updated and more realistic timeline for completion.  
- Timeline is primarily based on **size category**:  
  - Small → 2–5 days  
  - Medium → 7–10 days  
  - Large → 14+ days  

**Step 13 – Artisan begins crafting the item**  
- Work starts only after materials are purchased and timeline is sent.

**Step 14 – Artisan may encounter complications**  
Examples:  
- Weather delays (rain interfering with drying/painting)  
- Material defects  
- Unexpected adjustments needed  
- Tool-related slowdowns  
- Customer delayed responses  

**Step 15 – Artisan logs issues in notebook**  
- Records complications or delays.  
- These may affect timeline but he continues unless customer action is required.

**Step 16 – Mid-project update (optional but ideal)**  
- Artisan attempts to give a progress update halfway through.  
- However, customer response delays can stall work.

**Step 17 – Customer requests design change (optional)**  
- If customer changes design mid-project:  
  - Artisan recalculates cost **the same day**.  
  - Adjusts timeline accordingly.  
  - Communicates new price and requirements.  
  - Customer must reconfirm.

**Step 18 – Artisan completes the custom craft**  
- Once done, the artisan prepares the piece for pickup storage.

**Step 19 – First notification with photo (2 days before pickup)**  
- Sends photo of finished project through SMS/WhatsApp/email.  
- Confirms that the agreed pickup date still works.

**Step 20 – Day-of pickup reminder (no photo)**  
- Sends a simple reminder message on the day of pickup.

**Step 21 – Customer arrives for pickup**  
- Customer inspects the piece.  

**Step 22 – Customer pays remaining 50% balance**  
- Artisan receives final payment (cash or bank transfer).  
- **No item is released without full payment.**

**Step 23 – Artisan prepares and prints invoice**  
- Uses Word template.  
- Gives customer the printed copy.

**Step 24 – Artisan hands over the custom craft**  
- Only after payment and invoice are finalized.

**Step 25 – Artisan updates Excel**  
- Logs sale and financial details.  
- Marks the custom product as completed.  
- No physical “inventory” update is required since this is not a stock item.

---

### 3.3 Alternate / Exception Paths

**A1 – Insufficient deposit**  
- Customer pays less than 50%.  
- Artisan does NOT begin the project.  
- Materials are NOT purchased.  

**A2 – Project not feasible**  
- Artisan declines the request at Step 2.

**A3 – Customer disappears or delays confirmation**  
- Artisan may pause the timeline and await a response.  
- This can delay multiple projects.

**A4 – Weather delay**  
- Rain delays drying, painting, or outdoor steps.  
- Artisan logs delay and notifies customer if delay > 2 days.

**A5 – Design change after work has started**  
- Artisan recalculates cost immediately.  
- Timeline is reset or extended.  
- Customer must reconfirm.

**A6 – Late pickup**  
- After 2-day grace period, daily storage fee begins (100 pesos/day or $5/day).  
- Artisan communicates fees via WhatsApp/SMS/email.

---

<br>
<br>

## 4. Workflow #3 – Late Pickup & Storage Fee Handling (As-Is)

### 4.1 Description

This workflow models what happens when a **customer does not pick up a finished item on the agreed date**, and how Mr. Carrion applies his **grace period** and **daily storage fee** policy. This applies to both **stock items** and **custom crafts** that have been fully completed and set aside for pickup.

Actors:
- **Customer**
- **Artisan (Mr. Carrion)**

Tools/Systems involved:
- WhatsApp / SMS / Email  
- Physical storage space (bedroom/living room)  
- Notebook  
- Excel (optional, if he chooses to record storage charges)  

---

### 4.2 Main Flow – On-Time Pickup (No Fees)

**Step 1 – Pickup date is agreed in advance**  
- During the order or completion process, the customer and Mr. Carrion agree on a specific pickup date and, roughly, time.

**Step 2 – First notification with photo (2 days before pickup)**  
- Already part of the main workflows for stock and custom orders.  
- Confirms that the item is ready and reminds the customer of the pickup date.

**Step 3 – Day-of pickup reminder**  
- On the agreed day, Mr. Carrion sends a reminder message (no photo) to confirm that the customer is still coming.

**Step 4 – Customer arrives on or before agreed date**  
- Customer picks up the item on time.  
- No storage fee is applied.  
- Payment and handover follow the normal workflow.  

*(In this case, Workflow #3 does not deviate from the main stock/custom flows.)*

---

### 4.3 Late Pickup Flow – Applying Grace Period and Storage Fees

**Step 1 – Agreed pickup date passes without pickup**  
- The scheduled pickup date arrives and the customer does not show up.  
- The item remains stored in Mr. Carrion’s home (bedroom/living room or protected area).

**Step 2 – Grace period begins (Day 1 and Day 2 after pickup date)**  
- Mr. Carrion applies a **2-day grace period** after the agreed pickup date.  
- During these 2 days, no fee is charged.  
- The item continues to occupy storage space.

**Step 3 – Storage fee starts on Day 3**  
- Starting on the **3rd day after the agreed pickup date**, a **daily storage fee** is applied.  
- Fee rule: **100 pesos/day (≈ $5/day)**.  
- This fee is tied to the customer’s delay, not to the type of craft.

**Step 4 – Artisan may notify customer about accumulating fees**  
- Using WhatsApp/SMS/email, Mr. Carrion may send a message explaining:  
  - that the agreed date has passed,  
  - that a 2-day grace period was given,  
  - that daily storage charges are now accumulating.  

**Step 5 – Customer eventually responds and schedules a new pickup**  
- Customer contacts Mr. Carrion to arrange a new pickup date.  
- At this point, the total days of delay can be counted.

**Step 6 – Customer arrives for late pickup**  
- Customer comes to pick up the item on the new date.

**Step 7 – Calculation of total amount due**  
- Total due includes:  
  - remaining balance for the craft (if any), plus  
  - accumulated storage fees (number of chargeable days × daily fee).  

**Step 8 – Customer pays full amount (craft + fees)**  
- Payment is made via cash or bank transfer.  
- As with all other workflows, **no item is released without full payment**, including storage fees.

**Step 9 – Item is handed over to customer**  
- Item is given to the customer only after payment is confirmed.

**Step 10 – Optional recording of storage fee in Excel**  
- If desired, Mr. Carrion may log the additional storage revenue in Excel.  
- The item is treated as sold/closed in his normal tracking.

---

### 4.4 Alternate / Exception Paths

**A1 – Customer never returns**  
- Item remains stored long-term.  
- At some point, Mr. Carrion may decide to:  
  - reclassify the item as available for sale again,  
  - resell it to another customer.  
- Storage fee may be considered forfeited or ignored if no final pickup occurs.

**A2 – Artisan chooses not to enforce fees**  
- For certain customers (e.g., family or special cases), he may waive or reduce the fee.  
- This is handled informally and not always recorded.

**A3 – Cancellation after grace period**  
- Customer cancels after the pickup date.  
- Item is returned to general inventory.  
- Any prior payments (if any) are handled according to his personal judgment (case by case).  

---




---

## 5. Use Case Descriptions



## **UC-01 — Inquire About Stock Item**

**Use Case Name:** Inquire About Stock Item
**ID:** UC-01
**Actor:** Customer
**Goal:** Check availability and pricing for stock craft items.
**Trigger:** Customer contacts Mr. Carrion with interest in an item.

**Preconditions:**

* Customer has a communication method (WhatsApp/SMS/email).
* Inventory exists in system.

**Postconditions:**

* Customer receives availability and pricing details.

### Main Flow:

1. Customer sends an inquiry message.
2. System retrieves available stock items.
3. Artisan reviews list and selects items that match.
4. System sends availability and pricing to customer.

### Alternate / Exceptions:

* A1: No items available → System notifies customer.
* A2: Customer inquiry is unclear → System requests clarification.

---

## **UC-02 — Purchase Stock Item**

**Use Case Name:** Purchase Stock Item
**ID:** UC-02
**Actor:** Customer
**Goal:** Reserve and purchase a stock craft item.
**Trigger:** Customer selects an available item and confirms purchase.

**Preconditions:**

* Customer has received availability and pricing.
* Item is still in stock.

**Postconditions:**

* Item is reserved and then sold.
* Payment is recorded.
* Inventory is updated.

### Main Flow:

1. Customer confirms selection.
2. System records the reservation.
3. Customer and artisan set a pickup date.
4. System sends reminder and photo update.
5. Customer arrives on pickup day.
6. Customer pays the full amount.
7. System confirms payment.
8. System finalizes the sale.
9. Artisan hands the item to the customer.
10. System updates inventory and sales records.

### Alternate / Exceptions:

* A1: Customer cancels → System removes reservation.
* A2: Payment not completed → System loops to request payment.
* A3: Item unavailable → System notifies customer.

---

<br>

## **UC-03 — Request Custom Order**

**Use Case Name:** Request Custom Order
**ID:** UC-03
**Actor:** Customer
**Goal:** Request a custom craft item.
**Trigger:** Customer sends idea, description, or reference image.

**Preconditions:**

* Customer provides enough information to begin evaluation.

**Postconditions:**

* System records that a custom order evaluation has begun.

### Main Flow:

1. Customer submits custom request.
2. System notifies artisan.
3. Artisan evaluates feasibility.
4. System records the request for quoting.

### Alternate / Exceptions:

* A1: Artisan determines request is not feasible → System notifies customer.

---

<br>

## **UC-04 — Approve Custom Order Quote**

**Use Case Name:** Approve Custom Order Quote
**ID:** UC-04
**Actor:** Customer
**Goal:** Approve calculated quote and authorize the job.
**Trigger:** Customer receives quote.

**Preconditions:**

* Artisan has estimated cost, labor, materials, overhead, and markup.

**Postconditions:**

* Deposit received.
* Order activated.

### Main Flow:

1. System sends quote to customer.
2. Customer reviews.
3. Customer approves terms.
4. Customer pays 50% deposit.
5. System records deposit.
6. Order becomes active.

### Alternate / Exceptions:

* A1: Customer delays → Order remains pending.
* A2: Customer pays less than 50% → Order remains pending.

---

<br>
<br>

## **UC-05 — Manage Custom Order Progress**

**Use Case Name:** Manage Custom Order Progress
**ID:** UC-05
**Actor:** Artisan
**Goal:** Track and update progress of a custom order.
**Trigger:** Deposit received and order activated.

**Preconditions:**

* Materials purchased.
* Timeline set.

**Postconditions:**

* Progress is documented.
* Complications or changes recorded.

### Main Flow:

1. Artisan begins crafting.
2. System records updated timeline.
3. Artisan logs complications.
4. System recalculates timeline if needed.
5. Artisan provides mid-project update.

### Alternate / Exceptions:

* A1: Customer changes design → System recalculates price and timeline.
* A2: Customer replies slowly → Workflow pauses.

---

<br>
<br>

## **UC-06 — Complete Order and Pickup**

**Use Case Name:** Complete Order and Pickup
**ID:** UC-06
**Actors:** Customer, Artisan
**Goal:** Finalize payment and deliver completed item.
**Trigger:** Item is completed.

**Preconditions:**

* Item is ready.
* Pickup date set.

**Postconditions:**

* Item delivered.
* Payment completed.
* Order closed.

### Main Flow:

1. System sends photo update (2 days before pickup).
2. System sends pickup reminder on the day of pickup.
3. Customer arrives.
4. Customer pays remaining balance.
5. System confirms payment.
6. Artisan prepares invoice.
7. Artisan hands item to customer.
8. System marks order complete.

### Alternate / Exceptions:

* A1: Customer attempts pickup without payment → Item not released.
* A2: Customer reschedules → New pickup date recorded.

---

<br>
<br>


## **UC-07 — Handle Late Pickup Fees**

**Use Case Name:** Handle Late Pickup Fees
**ID:** UC-07
**Actors:** System, Artisan
**Goal:** Apply grace period and storage fees for late pickups.
**Trigger:** Pickup date passes without customer arrival.

**Preconditions:**

* Order is complete.
* Pickup date recorded.

**Postconditions:**

* Fees calculated or waived.
* Order eventually closed or item returned to inventory.

### Main Flow:

1. Pickup date passes.
2. System applies 2-day grace period.
3. If no pickup, system starts daily storage fee.
4. System notifies customer.
5. Customer schedules new pickup.
6. Customer pays balance and fees.
7. System closes order.

### Alternate / Exceptions:

* A1: Customer never returns → Artisan re-lists item.
* A2: Artisan waives fees.

---

<br>
<br>


## **UC-08 — Update Inventory and Sales**

**Use Case Name:** Update Inventory and Sales
**ID:** UC-08
**Actor:** Artisan
**Goal:** Maintain accurate records of sales and inventory.
**Trigger:** Order is completed or canceled.

**Preconditions:**

* Item exists in inventory.

**Postconditions:**

* Inventory and sales data updated.

### Main Flow:

1. Artisan logs sale in system.
2. System decrements inventory.
3. System records transaction.

### Alternate / Exceptions:

* A1: Customer cancels → System re-adds item.

---

<br>
<br>


## **UC-09 — Manage Notifications**

**Use Case Name:** Manage Notifications
**ID:** UC-09
**Actor:** System
**Goal:** Automate customer notifications.
**Trigger:** Order status changes.

**Preconditions:**

* Active order exists.

**Postconditions:**

* Customer receives appropriate notifications.

### Main Flow:

1. Order status changes.
2. System schedules notifications.
3. System sends reminders and updates.

### Alternate / Exceptions:

* A1: Customer opts out.
* A2: Notification fails to send.







---

## 6. Use Case Dialogue


<br>
<br>


## **Custom Order Dialogue**

**1. Customer:**
I would like to request a custom craft. Here is a photo and description of what I want.

**2. System:**
The system stores the request and alerts the artisan that a new custom inquiry has been submitted.

**3. Artisan:**
Reviews the customer request within the system and examines the photo, dimensions, and materials needed.

**4. System:**
Displays feasibility checklist fields for the artisan (materials required, estimated time, labor complexity, potential risks).

**5. Artisan:**
Assesses feasibility and enters preliminary notes into the system (possible, not possible, or needs clarification).

**6. System:**
Prompts artisan to provide required clarifications if needed.

**7. Artisan:**
Requests more details from the customer through the system (e.g., size, finish type, color, wood type).

**8. Customer:**
Provides the requested clarifications.

**9. System:**
Updates the custom request record and notifies the artisan.

**10. Artisan:**
Begins cost estimation by entering:

* Estimated material cost
* Estimated labor hours at $15/hr
* Applicable overhead ($25 or $50)
* Size category for markup multiplier (2.0x, 2.2x, 3.0x)

**11. System:**
Automatically calculates the total quote based on inputs and prepares a draft price.

**12. Artisan:**
Reviews the system-generated quote and sends it to the customer through the system interface.

**13. System:**
Delivers full written quote to the customer with:

* Total price
* Estimated completion timeline
* Deposit requirement (50%)
* Conditions for updates and design changes

**14. Customer:**
Reviews the quote and approves it in the system.

**15. System:**
Confirms approval and prompts customer to submit the mandatory 50% deposit.

**16. Customer:**
Submits the deposit via the system-supported payment method.

**17. System:**
Verifies payment and marks the order status as “Deposit Received – Active.”

**18. Artisan:**
Purchases materials and updates the system with receipts and material details.

**19. System:**
Logs purchased materials and recalculates projected completion date based on artisan input.

**20. Artisan:**
Sends an updated timeline to the customer through the system (required within two days of materials purchase).

**21. Customer:**
Receives the update and acknowledges the revised timeline.

**22. System:**
Records customer acknowledgment and sets internal reminders for mid-project updates, delay notifications, and completion notifications.

**23. Artisan:**
Begins work. System continues tracking progress, complications, and any updates that must be communicated.

<br>
<br>

**End of Dialogue...**




---

## 7. Functional Requirements



**Project:** The Artisan Vault

**Phase:** Analysis

**Artifact:** Functional Requirements

**Purpose:** Define what The Artisan Vault System must do in order to support the business processes currently performed by Mr. Carrion.

<br>
<br>
<br>

## **1. Customer Interaction & Inquiry Requirements**

**FR-1.1**
The system shall allow customers to submit inquiries about stock items through a supported communication method or system interface.

**FR-1.2**
The system shall retrieve and display available stock items, including item name, description, quantity, and price.

**FR-1.3**
The system shall notify Mr. Carrion when a customer’s inquiry has been submitted.

**FR-1.4**
The system shall return item availability and pricing information to the customer.

---

## **2. Stock Item Purchase Requirements**

**FR-2.1**
The system shall allow a customer to select and reserve a stock item.

**FR-2.2**
The system shall record stock item reservations and mark items as “Reserved.”

**FR-2.3**
The system shall allow Mr. Carrion to set a pickup date for the reserved item.

**FR-2.4**
The system shall send reminder notifications before the pickup date.

**FR-2.5**
The system shall process the final payment at the time of pickup.

**FR-2.6**
The system shall mark a reserved item as “Sold” when final payment is completed.

**FR-2.7**
The system shall update inventory quantities automatically after a sale.

---

## **3. Custom Order Intake Requirements**

**FR-3.1**
The system shall accept custom order requests containing text, photos, or descriptions.

**FR-3.2**
The system shall notify Mr. Carrion when a new custom order request is received.

**FR-3.3**
The system shall store feasibility notes entered by Mr. Carrion.

**FR-3.4**
The system shall support clarification requests between customer and artisan.

**FR-3.5**
The system shall maintain a record of the customer’s custom order details.

---

## **4. Custom Order Quoting & Approval Requirements**

**FR-4.1**
The system shall allow Mr. Carrion to enter estimated material costs, labor hours, overhead, and size classification.

**FR-4.2**
The system shall automatically calculate the total quote based on provided parameters.

**FR-4.3**
The system shall send the formal quote to the customer.

**FR-4.4**
The system shall allow customers to approve or decline custom order quotes.

**FR-4.5**
The system shall require a 50% deposit before activating a custom order.

**FR-4.6**
The system shall verify and record customer deposit payments.

---

## **5. Custom Order Production Requirements**

**FR-5.1**
The system shall allow Mr. Carrion to log material purchases and upload receipts.

**FR-5.2**
The system shall update the estimated completion timeline when materials are purchased.

**FR-5.3**
The system shall allow Mr. Carrion to record complications (weather delays, material shortages, design changes).

**FR-5.4**
The system shall adjust the projected timeline based on complications or design changes.

**FR-5.5**
The system shall send mid-project updates to customers when prompted by the artisan.

---

## **6. Pickup, Payment, and Completion Requirements**

**FR-6.1**
The system shall send a “completed item” photo update two days before pickup.

**FR-6.2**
The system shall send a reminder notification on the day of pickup.

**FR-6.3**
The system shall calculate any remaining balance owed.

**FR-6.4**
The system shall verify payment and update the order status to “Payment Complete.”

**FR-6.5**
The system shall generate and store an invoice for each completed order.

**FR-6.6**
The system shall mark the order as “Completed” once payment is finalized and item is picked up.

---

## **7. Late Pickup & Storage Fee Requirements**

**FR-7.1**
The system shall track the agreed pickup date for each order.

**FR-7.2**
The system shall apply a two-day grace period after the missed pickup date.

**FR-7.3**
The system shall automatically begin adding daily storage fees after the grace period.

**FR-7.4**
The system shall notify customers when storage fees begin accruing.

**FR-7.5**
The system shall calculate the total amount owed (remaining balance plus accumulated fees).

**FR-7.6**
The system shall allow the artisan to waive, reduce, or override storage fees.

---

## **8. Inventory & Sales Tracking Requirements**

**FR-8.1**
The system shall maintain an inventory database for stock items.

**FR-8.2**
The system shall update inventory when items are reserved, sold, or re-listed after cancellation.

**FR-8.3**
The system shall store sales records, including transaction date, item sold, and price.

**FR-8.4**
The system shall store payment records, including deposits and final balance.

---

## **9. Notification System Requirements**

**FR-9.1**
The system shall send automated notifications for:

* custom order status
* deposit confirmation
* timeline updates
* mid-project updates
* photo before pickup
* pickup day reminder
* late pickup notice

**FR-9.2**
The system shall allow customers to opt out of non-essential notifications.

**FR-9.3**
The system shall retry failed notification attempts.

---

## **10. User & System Interaction Requirements**

**FR-10.1**
The system shall allow Mr. Carrion to view a dashboard of active, pending, and completed orders.

**FR-10.2**
The system shall provide search and filtering features for orders.

**FR-10.3**
The system shall allow customers to view order status, timeline, and payment history.

**FR-10.4**
The system shall securely store all customer communication and interactions.

---

<br>
<br>



---

## 8. Non-Functional Requirements


<br>
<br>

## **1. Performance Requirements**

**NFR-1.1**
The system shall respond to customer inquiries within 2 seconds under normal operating conditions.

**NFR-1.2**
The system shall process pricing calculations for custom orders in under 1 second.

**NFR-1.3**
The system shall send scheduled notifications (updates, reminders, alerts) within 1 minute of the scheduled time.

**NFR-1.4**
The system shall support up to 50 concurrent users without performance degradation.

---

<br>
<br>

## **2. Reliability & Availability Requirements**

**NFR-2.1**
The system shall maintain an uptime of 99% or higher, excluding scheduled maintenance.

**NFR-2.2**
The system shall ensure that all order data, inventory updates, and payment records are saved immediately and never lost due to system failure.

**NFR-2.3**
The system shall recover from unexpected outages within 5 minutes using automated backup restoration.

**NFR-2.4**
Scheduled notifications shall not be lost; undelivered messages must be retried at least three times.

---
<br>
<br>

## **3. Security Requirements**

**NFR-3.1**
All customer data, payments, and communications shall be encrypted in transit using TLS 1.2 or higher.

**NFR-3.2**
Stored data shall be encrypted at rest, including inventory, customer profiles, order history, and payment logs.

**NFR-3.3**
Access to the artisan dashboard shall require secure authentication.

**NFR-3.4**
The system shall prevent unauthorized modification of pricing formulas, inventory, and order records.

**NFR-3.5**
Payment operations shall comply with standard financial security guidelines (e.g., PCI-equivalent best practices).

---
<br>
<br>

## **4. Usability Requirements**

**NFR-4.1**
The customer interface shall be simple enough for first-time users with no training.

**NFR-4.2**
The artisan dashboard shall be optimized for use on mobile and desktop, accommodating Mr. Carrion’s preferred working style.

**NFR-4.3**
All interfaces shall use clear labels, readable text, and minimal steps for common tasks (e.g., updating order status).

**NFR-4.4**
Notifications shall be concise and easy for customers to understand.

---

<br>
<br>

## **5. Maintainability Requirements**

**NFR-5.1**
The system’s internal components shall be modular, allowing updates to individual features without impacting the entire system.

**NFR-5.2**
Pricing formulas, fee policies, and timeline rules shall be stored in configurable tables or logic components that can be updated without redeploying the whole system.

**NFR-5.3**
Error logs, system logs, and activity logs shall be accessible to administrators for troubleshooting.

---
<br>
<br>

## **6. Scalability Requirements**

**NFR-6.1**
The system shall support additional artisans, product categories, or storefronts without required redesign of core components.

**NFR-6.2**
The system shall allow inventory expansion up to 10,000 items without performance loss.

**NFR-6.3**
Notification services shall scale horizontally to handle increased customer volume.

---
<br>
<br>

## **7. Data Integrity Requirements**

**NFR-7.1**
No order shall transition to “Active” status until the 50% deposit is verified.

**NFR-7.2**
No item shall transition to “Sold” status until full payment is confirmed.

**NFR-7.3**
Inventory updates must occur atomically, preventing double-selling or race conditions.

**NFR-7.4**
Late pickup fees must be calculated based on verified timestamps, not manually entered dates.

---
<br>
<br>

## **8. Legal & Compliance Requirements**

**NFR-8.1**
Customer personal data shall comply with relevant privacy standards (GDPR-style principles for minimalism and control).

**NFR-8.2**
Stored photos, messages, and receipts shall follow data retention policies determined by the artisan’s business rules.

**NFR-8.3**
Financial data shall be stored securely and maintained for audit purposes for a minimum of five years.

---

<br>
<br>

## **9. Portability Requirements**

**NFR-9.1**
The system shall run on modern web browsers (Chrome, Safari, Firefox, Edge).

**NFR-9.2**
The system’s mobile experience shall support iOS and Android through responsive web design.

**NFR-9.3**
System architecture shall support future migration to a mobile app without reworking core logic.

---

<br>
<br>


## **10. Supportability Requirements**

**NFR-10.1**
The system shall provide usage logs for diagnosing customer interaction issues.

**NFR-10.2**
System failures shall generate automated alerts for administrators.

**NFR-10.3**
Documentation shall include user guides for both customers and artisans.


---

## 9. Preliminary Data Model


**Project:** The Artisan Vault

**Phase:** Analysis

**Artifact:** Preliminary Data Model (Logical View)

**Purpose:** Identify the core data entities and relationships required to support The Artisan Vault business processes (stock sales, custom orders, payments, notifications, and late pickup fees).

---

### 1. Overview

This preliminary data model defines the main entities and relationships for The Artisan Vault. It is a **logical model**, not a final physical database design. The goal is to capture the key business objects found in the workflows and use cases:

* Customers placing stock or custom orders
* Orders and their pricing/deposits
* Items that are being sold or crafted
* Payments (deposits, final payments, late fees)
* Notifications sent to customers
* Late pickup fee tracking

---

### 2. Core Entities and Key Attributes

Note: Attribute lists are preliminary and can be refined in the design phase.

#### 2.1 Customer

Represents a person who purchases stock items or requests custom orders.

* **CustomerID** (PK)
* Name
* PhoneNumber
* Email
* PreferredContactChannel (WhatsApp, SMS, Email)

#### 2.2 Order

Represents a single customer order (stock or custom).

* **OrderID** (PK)
* CustomerID (FK → Customer)
* OrderType (Stock, Custom)
* Status (PendingQuote, QuoteSent, AwaitingDeposit, Active, InProgress, ReadyForPickup, Completed, Cancelled)
* CreatedDate
* PickupDatePlanned
* CompletionDatePlanned
* CompletionDateActual
* TotalPriceQuoted
* TotalPriceFinal

#### 2.3 Item

Represents an individual craft item associated with an order. This supports both:

* Stock items (already made)

* Custom items (made for the order)

* **ItemID** (PK)

* OrderID (FK → Order)

* Name (e.g., “Seashell Mirror”, “Rope Curtain”, “Dining Table”)

* Description

* SizeCategory (Small, Medium, Large)

* Type (Stock, Custom)

* Status (Available, Reserved, Sold, InProduction, Completed)

#### 2.4 Payment

Represents any payment associated with an order, including deposits, final payments, and late fees.

* **PaymentID** (PK)
* OrderID (FK → Order)
* PaymentType (Deposit, Final, LateFee)
* Amount
* PaymentMethod (Cash, BankTransfer, Other)
* PaymentDate

#### 2.5 Notification

Represents a message sent to the customer by the system (quote, update, reminder, late fee notice).

* **NotificationID** (PK)
* OrderID (FK → Order)
* NotificationType (QuoteSent, DepositConfirmed, ProgressUpdate, PhotoBeforePickup, PickupReminder, LateFeeNotice, DelayNotice)
* SentDateTime
* DeliveryStatus (Sent, Failed, Pending)

#### 2.6 LatePickupRecord

Represents late pickup tracking for an order once the agreed pickup date is missed.

* **LatePickupID** (PK)
* OrderID (FK → Order)
* GracePeriodEndDate
* DailyStorageRate
* ChargeStartDate
* ChargeEndDate (optional, when item picked up)
* TotalDaysCharged
* TotalLateFeeAmount

---

### 3. Relationships (Logical)

1. **Customer – Order**

   * One **Customer** can have many **Orders**.
   * Each **Order** belongs to one **Customer**.
   * Cardinality: Customer 1..* — Order *..1

2. **Order – Item**

   * One **Order** can have one or more **Items** (support future multi-item orders).
   * Each **Item** is associated with one **Order**.
   * Cardinality: Order 1..* — Item *..1

3. **Order – Payment**

   * One **Order** can have multiple **Payments** (deposit, final payment, late fee payments).
   * Each **Payment** belongs to one **Order**.
   * Cardinality: Order 1..* — Payment *..1

4. **Order – Notification**

   * One **Order** can have multiple **Notifications**.
   * Each **Notification** is tied to one **Order**.
   * Cardinality: Order 1..* — Notification *..1

5. **Order – LatePickupRecord**

   * One **Order** can have zero or one **LatePickupRecord**.
   * Each **LatePickupRecord** belongs to one **Order**.
   * Cardinality: Order 1..1 — LatePickupRecord 0..1





---

## 10. Requirements Validation Log

**Project:** The Artisan Vault  
**Phase:** Analysis  
**Artifact:** Requirements Validation Log  

<br>
<br>

## 1. Purpose

This log is used to review and validate the captured requirements (functional, non-functional, and business rules) for The Artisan Vault. It ensures that each requirement:

- Aligns with stakeholder goals (especially Mr. Carrion)  
- Supports the core business workflows  
- Is clear, testable, and realistic  

---

<br>
<br>
<br>

## 2. Functional Requirements Validation

| ID       | Requirement Summary                                      | Source (Use Case / Workflow)                         | Stakeholder Priority (H/M/L) | Validation Notes                                                |
|----------|-----------------------------------------------------------|------------------------------------------------------|------------------------------|-----------------------------------------------------------------|
| FR-2.2   | System records stock item reservations                   | UC-02 Purchase Stock Item, Stock Workflow           | H                            | Prevents double-selling and manual confusion.                  |
| FR-2.7   | System updates inventory after each sale                 | UC-02, Inventory Workflow                           | H                            | Directly replaces manual Excel updates; critical for accuracy. |
| FR-3.1   | System accepts custom order requests with text/photos    | UC-03 Request Custom Order                          | H                            | Matches how customers already send ideas via WhatsApp today.   |
| FR-4.5   | System requires 50% deposit before activating custom job | UC-04 Approve Custom Order Quote                    | H                            | Reflects current rule: no work starts until deposit is paid.   |
| FR-5.3   | System records complications and timeline changes        | UC-05 Manage Custom Order Progress                  | M                            | Helps handle delays due to weather or late customer responses. |
| FR-6.2   | System sends pickup reminder on pickup day               | UC-06 Complete Order & Pickup                       | M                            | Reduces no-shows, supports late-pickup and fee logic.          |
| FR-7.3   | System calculates daily storage fees after grace period  | UC-07 Handle Late Pickup Fees                       | H                            | Automates an existing manual rule; important for fairness.     |
| FR-8.3   | System stores sales records (date, item, price)          | Inventory & Sales Tracking Workflow                 | H                            | Replaces manual Excel logging; required for basic reporting.   |
| FR-9.1   | System sends automated notifications for key events      | UC-09 Manage Notifications                          | M                            | Mirrors existing manual messaging; adds consistency.           |



---

<br>
<br>
<br>

## 3. Non-Functional Requirements Validation

| ID        | Requirement Summary                                     | Category        | Priority (H/M/L) | Validation Notes                                                 |
|-----------|----------------------------------------------------------|-----------------|------------------|------------------------------------------------------------------|
| NFR-1.1   | Respond to customer inquiries within 2 seconds          | Performance     | M                | Reasonable for a small web system; supports good user experience.|
| NFR-2.1   | Maintain 99% uptime                                     | Reliability     | M                | Sufficient for a small artisan shop; does not require full 24/7. |
| NFR-3.2   | Encrypt stored customer and order data                  | Security        | H                | Protects personal/contact data and basic payment records.        |
| NFR-4.2   | Dashboard works on mobile and desktop                   | Usability       | H                | Critical for Mr. Carrion, who often works from home and phone.   |
| NFR-5.2   | Pricing and fee rules are configurable                  | Maintainability | M                | Needed as pricing may evolve without redesigning the system.     |
| NFR-7.2   | No item marked “Sold” until full payment confirmed      | Data Integrity  | H                | Essential to avoid inconsistencies in financial tracking.        |
| NFR-9.1   | Works on major browsers (Chrome, Safari, Firefox, Edge) | Portability     | M                | Standard expectation for a web-based system.                     |


---

<br>
<br>
<br>

## 4. Business Rules Validation

Business rules are specific policies that must always be enforced by the system.

| Rule ID | Business Rule Description                                                                 | Source (Interview / Workflow)                             | Must the System Enforce It? (Y/N) | Notes                                                     |
|---------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|-----------------------------------|----------------------------------------------------------|
| BR-01   | No custom job starts until a 50% deposit is received.                                      | Custom Order Interview, Workflow #2                       | Y                                 | Core protection rule for material and time cost.         |
| BR-02   | No item (stock or custom) is released without full payment.                                | Multiple workflows, Mr. Carrion interview                | Y                                 | Must be enforced before order status becomes “Completed”.|
| BR-03   | Two-day grace period after missed pickup date before daily storage fees apply.             | Workflow #3 Late Pickup                                   | Y                                 | Needed to automatically start fee calculation.           |
| BR-04   | Daily storage fee is a fixed rate (e.g., 100 pesos/day or equivalent) after grace period. | Workflow #3 Late Pickup                                   | Y                                 | Should be configurable but always applied consistently.  |
| BR-05   | Materials for a custom job are only purchased after the 50% deposit is confirmed.         | Custom Order Interview, Workflow #2                       | Y                                 | Prevents cash flow issues and sunk costs.                |
| BR-06   | Markup multipliers depend on size and commercial exposure (2.0x, 2.2x, 3.0x).             | Pricing discussion with Mr. Carrion                       | M                                 | System should support this logic; artisan can adjust later.|
| BR-07   | Customer design changes after work starts require recalculation of price and timeline.    | Custom Order Workflow                                     | Y                                 | Protects against scope creep and underpricing.           |

---

## 5. Summary

- Functional requirements were validated against:  
  - key use cases,  
  - the three main workflows,  
  - and the interview with Mr. Carrion.  

- Non-functional requirements ensure that the system is not only functional, but secure, usable, maintainable, and aligned with realistic expectations for a small artisan business.

- Business rules capture the most critical policies that define how Mr. Carrion operates today. These rules must either be enforced or strongly supported by the system.




