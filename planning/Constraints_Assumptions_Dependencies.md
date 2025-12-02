# Constraints, Assumptions, and Dependencies (CAD)

## Purpose

This document identifies the constraints, assumptions, and dependencies that affect The Artisan Vault project. These factors help define realistic expectations for scope, schedule, and resource use. Early identification of CAD elements reduces project risk and ensures better planning accuracy.

## Constraints

*Constraints are fixed limitations that the project must operate within.*

### 1. Timeline Constraints

- Content Acquisition Window: The project timeline is constrained by the artisan’s limited availability to provide item photos and descriptions. The system cannot progress to the MVP without this content, which may only be supplied during specific time windows based on the artisan’s schedule.


### 2. Budget & Resource Constraints

- Low-Cost Tools Required: Development and hosting must rely on free or low-cost platforms due to the absence of a formal project budget.

- Single Developer Limitation: All analysis, development, testing, and support depend on one developer, limiting available capacity.

### 3. Technical Constraints

- Hosting Capacity: Free hosting tiers restrict bandwidth, storage, compute resources, and database size.

- No Advanced Automation: Phase 1 *cannot* include complex automation, payment workflows, or integrated financial systems.

- Device Limitations: Artisans may use older smartphones with limited storage and processing power, restricting UI complexity.

- Internet Stability: Some areas in Cancún have inconsistent internet speeds, affecting photo uploads and system responsiveness.

### 4. User Skill & Adoption Constraints

- Low Digital Literacy Among Artisans: Many artisans have limited experience with web platforms, requiring a simple, intuitive design.

- Cultural Preference for Personal Interaction: Local selling culture often relies on face-to-face trust, which may slow digital adoption.

- Buyer Familiarity With WhatsApp/Facebook: Customers in Cancún typically use informal channels instead of websites, reducing initial usage.

### 5. Scope Constraints

- Manual Sales Confirmation: Sales will be confirmed manually by the artisan due to lack of payment and automation features.

### 6. Cultural & Regional Constraints

- Trust-Based Selling Norms: Local buyers may prefer verifying items in person rather than trusting online descriptions.

- Language Requirements: The system must operate primarily in Spanish; English support may be needed later.

- Regional Economic Patterns: Local purchasing patterns may affect initial demand and usage behavior.

### 7. Legal & Compliance Constraints

- **Mexican Data Privacy Laws (LFPDPPP):** Customer contact information must be securely stored and protected; the system cannot mishandle personal data.

- **Truth-in-Advertising Requirements:** Item descriptions must be accurate to avoid consumer protection issues.

### 8. Operational Constraints

- **Artisan Availability:** The platform’s ability to display new items depends on the artisan submitting photos and descriptions reliably.

- **Limited Admin Resources:** Ongoing maintenance and system oversight rely on a single administrator.

- **Manual Inventory Management:** All inventory updates depend on artisan input and cannot be automated in Phase 1.

## Assumptions:

### 1. Artison Participation

- Artisan will consistently provide photos, descriptions, prices, and updates for each item.

- Artisan will manually confirm sales and update item statuses.

- Artisan has access to a smartphone or computer capable of accessing the system.


### 2. Customer Behavior

- Initial customer base will be small but engaged enough to test the system.  

- Customers are willing to submit a request form instead of messaging through social media.  

- Customers will rely on artisan follow-up for final sale confirmation.  



### 3. System & Technology 

- Free hosting tiers will be stable enough to support MVP traffic levels.  

- Email notification services will function reliably for customer requests.  

- Image uploads will remain within capacity limits of free hosting/storage solutions.  


### 4. Environmental & Cultural 

- Artisans will accept a semi-manual workflow because it aligns with local selling habits.  

- Regional internet variability will not prevent basic system use.  


### 5. Operational

- Administrator will be available to manage system data when necessary.  

- Developer (you) will have full access to required tools throughout the semester.  

- Testing can be performed with live artisan data or mock data if needed.  


## Dependencies

### 1. Content & Artisan Participation Dependencies
- System depends on the artisan providing item photos, descriptions, prices, and updates.  

- Artisan availability for feedback and usability testing.  

### 2. Hosting & Infrastructure Dependencies
- Availability of free hosting platforms such as Vercel, Render, or GitHub Pages.  
  (*If free tiers fail or go offline, the site cannot be deployed*.)

- Stable internet connectivity for both artisan and customers.  

- Storage availability for uploaded images.  


### 3. Third-Party Service Dependencies
- Email or SMS notification service must function for customer requests.  
  (If email/SMS fails, artisans won’t see customer requests.)

- GitHub and VS Code must remain accessible for development and version control.  
  (Without development tools, project progress stops.)

---

### 4. Legal & Compliance Dependencies
- Compliance with Mexican data privacy laws (**LFPDPPP**).  
  (You must follow privacy rules when storing customer info.)

- Accurate representation of handmade items as required by consumer protection rules.  
  (The artisan must describe items *truthfully*.)

---

### 5. Operational Dependencies
- Administrator availability to handle basic system maintenance and data accuracy.  
  (Someone must maintain the platform’s content and settings.)

- Continued willingness of early customers to use the request form instead of WhatsApp/Facebook.  
  (Early customer adoption is needed for testing and validation.)

- Availability of the developer (you) for bug fixes and updates during Phase 1.  
  (If you cannot work on the project, nothing gets updated.)
