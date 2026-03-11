# Solution Priority & Implementation Roadmap

**Author:** VP of Product (AI Persona)  
**Target Audience:** Engineering, Product, and Design Teams  
**Date:** March 11, 2026

## Executive Summary
This document aggregates all strategic recommendations from the **Shipping, Invoice, CRM, and MCA** gap analyses. It serves as a prioritized backlog for UI/UX Designers and Developers. 

Tasks are categorized by **Criticality** (Business Impact vs. User Pain) to guide the next development sprint.

---

## 🔴 CRITICAL PRIORITY (Immediate Action)
*High impact on conversion and revenue; resolves major user friction.*

### 1. Payment Status Visibility (Invoice Module)
*   **Designer Task**: Design "Paid," "Pending," and "Expired" status badges for the Invoice dashboard.
*   **Developer Task**: Integrate payment gateway callbacks to auto-update invoice status in real-time.
*   **Target**: Eliminate manual payment verification for merchants.

### 2. Smart Address Parser (Shipping Module)
*   **Designer Task**: Create a "Quick Paste" text area that allows merchants to paste raw WhatsApp/Social chat text.
*   **Developer Task**: Implement an NLP-based parser to split raw text into Name, Phone, and Address (Sub-district/City) fields.
*   **Target**: Reduce shipment creation time by 60%.

### 3. Integrated "Nudge" for Cart Recovery (CRM Module)
*   **Designer Task**: Add a "Send Checkout Reminder" button inside the `Detail Customer > Keranjang Belanja Aktif` view.
*   **Developer Task**: Create a workflow that generates a unique Invoice/Payment link for the items in the active cart and triggers a WhatsApp share.
*   **Target**: Recapture abandoned sales directly from the CRM.

---

## 🟠 HIGH PRIORITY (Strategic Growth)
*Improves retention and scales the product for power users.*

### 1. Package Dimension Presets (Shipping Module)
*   **Designer Task**: Design a library/modal for merchants to save "Standard Package Sizes" (e.g., "Standard Box", "Large Mailer").
*   **Developer Task**: Create a CRUD system for package presets and a one-click "Apply" button in the shipment creation flow.
*   **Target**: Eliminate repetitive manual input of 9x9x9 dimensions.

### 2. MCA Repayment Simulation (MCA Module)
*   **Designer Task**: Design an interactive slider/calculator on the first step of the funding request.
*   **Developer Task**: Build a logic engine that estimates total repayment and daily/weekly installments based on requested amount and tenure.
*   **Target**: Increase trust and application completion rates.

### 3. High-Risk COD Flagging (CRM/Shipping Module)
*   **Designer Task**: Design a "High Risk" warning badge for customer profiles with high Return-to-Origin (RTO) or COD rejection history.
*   **Developer Task**: Cross-reference shopper phone numbers across the FLIK network to identify serial COD rejectors.
*   **Target**: Protect merchant margins from failed deliveries.

---

## 🟡 MEDIUM PRIORITY (Operational Excellence)
*Optimizes the workflow and improves professional branding.*

### 1. Direct WhatsApp Share Template (Invoice/CRM Module)
*   **Designer Task**: Create a customizable WhatsApp message template (e.g., "Hi [Name], here is your invoice for [Total]...").
*   **Developer Task**: Implement the `wa.me` deep-link integration to replace the "Copy Link" button with a direct share icon.
*   **Target**: Reduce taps for link distribution.

### 2. Auto-Order Naming (Invoice Module)
*   **Designer Task**: Ensure the "Nama Order" field is intelligently pre-filled (e.g., "Order for [Shopper Name]").
*   **Developer Task**: Set a fallback naming convention (Order #[ID]) to prevent empty dash ("-") entries in the dashboard.
*   **Target**: Improve dashboard searchability and reconciliation.

### 3. Unified Customer History (CRM Module)
*   **Designer Task**: Update the "Detail Customer" view to show a unified timeline of both **Invoices Created** and **Shipments Sent**.
*   **Developer Task**: Aggregate data across the Invoice and Shipping tables using the phone number as the unique identifier.
*   **Target**: Provide a 360-degree view of the customer relationship.

---

## 🟢 LOW PRIORITY (Future Roadmap)
*Enhancements for long-term scalability and platform maturity.*

### 1. Tiered MCA Underwriting (MCA Module)
*   **Task**: Create a "Micro-funding" tier for requests < Rp 10M that only requires KTP, skipping the heavy legal document (Akta) requirement.

### 2. Courier Success Rate Metrics (Shipping Module)
*   **Task**: Display "Success Rate %" next to courier prices to help merchants choose reliability over just the lowest cost.

### 3. Branded Tracking Pages (Shipping Module)
*   **Task**: Replace generic courier tracking links with a FLIK-hosted page featuring the merchant's logo and upsell recommendations.

---

## Summary of Priority by Module
| Module | Critical | High | Medium |
| :--- | :---: | :---: | :---: |
| **Shipping** | Smart Address Parser | Package Presets | Success Rates |
| **Invoice** | Payment Status | - | WhatsApp Share |
| **CRM** | Cart Recovery | High-Risk Flags | Unified History |
| **MCA** | - | Repayment Sim | Tiered Apps |
