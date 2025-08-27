# Adobe Analytics Implementation Framework – Case Study

## 📌 Overview
This repository documents a **theoretical case study on Adobe Analytics implementation**.  
It explores how Adobe Analytics can be set up and used to track user interactions, validate data flows, and generate insights through **Analysis Workspace**.

**Author:** Meda Sai Vrishyang Kumar  
**Date:** 26/08/2025  
**Tools Used:** Adobe Analytics Workspace, Adobe Experience Platform Tags (Adobe Launch), Adobe Experience Cloud Debugger  

---

## 📖 Summary
Adobe Analytics is a digital analytics platform that enables businesses to measure, analyse, and optimize user interactions across websites and applications.  

The process followed in this case study:
1. **Implementation** → Using Adobe Launch (tag manager) to configure rules, data elements, and variables.  
2. **Validation** → Debugging requests with Adobe Experience Cloud Debugger & browser console.  
3. **Analysis** → Building dashboards, visualizations, and segments in Adobe Analytics Workspace.

---

## 🏗️ System Flow
- Website/App → Adobe Launch → Adobe Server (via beacons) → Report Suite → Analysis Workspace  
- Verified with Adobe Debugger → Reported in Workspace dashboards

---

## 🛠️ Key Components

### 1. Adobe Analytics Workspace
- **Panels** (Freeform, Segment Comparison, Cohorts, etc.)  
- **Visualizations** (Tables, Line, Bar, Flow, Fallout, Maps)  
- **Segments & Date Ranges** for filtering data  
- **Metrics & Dimensions** for KPIs and performance tracking  

### 2. Variables
🔹 **Pre-Defined Variables**  
Built-in variables that capture standard data points like page name, campaigns, server, purchase ID, products, location, etc.  

🔹 **Success / Standard Events**  
Predefined events to measure business outcomes (e.g., prodView, scAdd, scCheckout, purchase).  

🔹 **eVars (Conversion Variables)**  
Persistent variables used for attribution; values persist across hits until expiry (e.g., campaign ID, user type).  

🔹 **Props (Traffic Variables)**  
Hit-level variables used for pathing and correlations; values apply only to the current page view.  

🔹 **Events (Custom Success Metrics)**  
Track user interactions such as purchases, downloads, or clicks; can be counter, numeric, or currency type.  

🔹 **Variable Scopes**  
- **Hit Scope** → Current server call  
- **Visit Scope** → Entire session  
- **Visitor Scope** → Across multiple visits until expiry  

🔹 **Other Key Notes**  
- **Allocation & Expiration**: Define how eVars attribute credit.  
- **Merchandising eVars**: Tie product-level attribution to `s.products`.  
- **List Variables**: Store multiple values in a single variable.  
- **Character Limits**: Props/eVars ~255 chars; Products string ~64k chars.  
- **Case Sensitivity**: Variables are case-sensitive; standardize values.

### 3. Adobe Experience Platform Tags (Launch)
- **Properties, Rules, Data Elements, Extensions**  
- **Publishing Workflow:** Dev → Staging → Production  
- **Rules:** Event → Conditions → Actions  
- **Data Elements:** Capturing values from JS variables, cookies, DOM, or URL parameters  

### 4. Adobe Cloud Debugger
- Real-time inspection of rules, variables, data elements, and beacons  
- Helps validate correct tracking implementation  

---

## 📊 Implementation Scenarios

1. **Purchase Event Tracking**  
   - Capturing order, customer, and cart details  
   - Mapping to eVars, props, and events  
   - Reporting in Workspace with revenue, shipping, and tax breakdown  

2. **Campaign Tracking (UTM Parameters)**  
   - Capturing `utm_campaign` from URL  
   - Mapping to eVars for campaign attribution  
   - Configuring Marketing Channel Processing Rules  

3. **User Properties (Beginner vs. Professional)**  
   - Tracking logged-in user type  
   - Using separate rules and events for segmentation  
   - Reporting differences in behaviour and conversions  

---

## 🎯 Learnings
- Understood **data flow** from website → Launch → Analytics → Workspace  
- Learned how to configure **eVars, props, and events** for accurate reporting  
- Gained insights on **purchase, campaign, and user segmentation tracking**  
- Identified best practices:  
  - Use eVars for persistence, props for pathing  
  - Validate all rules/events via Debugger before production  
  - Apply conditions/exceptions for accurate data  

---

## 📚 References
- [Adobe Analytics Implementation Guide (Udemy Course)](https://www.udemy.com/course/adobe-analytics-implementation-guide/)
> Additional references include tutorials, browser-based testing, and ChatGPT for JavaScript snippets and implementation guidance.

---

## 📌 Notes

- This repository is **for demonstration and learning purposes**.

---

## License

This repository and its contents (including the case study PDF) are licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).
