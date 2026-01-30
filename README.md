# LogiCompliance - WhatsApp-Based Document Compliance System

## 🎯 Problem Statement

In the logistics and healthcare sample collection industry, there's a critical compliance challenge: **collecting necessary documents from patients and third-party phlebotomists (flebos) before sample pickup**.

### The Ground Reality

- **40% of patients** are not literate in English
- Patients and flebos are **resistant to downloading new apps**
- Complex forms lead to **incomplete documentation**
- Manual follow-ups are **time-consuming and inefficient**
- **Delayed document collection** impacts lab processing and compliance

### Documents Required for Compliance

1. **Test Request Form (TRF)** - Patient and test details
2. **Doctor's Prescription (Rx)** - Medical authorization
3. **Histopathology Reports** - Previous medical reports (if applicable)
4. **Digital Consent** - Patient's authorization for sample collection

---

## 💡 Solution Overview

A **WhatsApp-based document compliance system** that leverages India's most popular messaging platform to:

- Automatically notify patients/flebos when an order is created
- Allow document submission via simple photo uploads
- Capture digital consent through OTP verification
- Track compliance and manage incentives for flebos
- Provide multilingual support (Hindi, Bengali, Tamil, English)

---

## 🎮 Demo Application

This repository contains a **working demo/prototype** of the solution built with pure HTML, CSS, and JavaScript.

### Files Included

| File             | Description                                     |
| ---------------- | ----------------------------------------------- |
| `index.html`     | Landing page with navigation to both interfaces |
| `dashboard.html` | Admin dashboard for logistics team              |
| `whatsapp.html`  | WhatsApp-like interface simulation              |

### How to Run the Demo

1. Simply open `index.html` in any modern web browser
2. No server or dependencies required
3. Click on either card to explore the interfaces

### Demo Features

#### Admin Dashboard

- 📊 Real-time statistics (Total Orders, Compliant, Pending, Overdue)
- 📋 Orders table with document status tracking
- 🔍 Search and filter functionality
- 👤 Manual assignment for follow-ups
- 💰 Flebo incentive tracking
- ➕ New order creation modal

#### WhatsApp Interface

- 💬 Realistic WhatsApp UI (dark theme)
- 🌐 Multilingual support (4 languages)
- 📷 Document upload simulation
- 🔐 OTP-based digital consent flow
- 📊 Progress tracking
- 👨‍⚕️ Separate flows for Patient and Phlebo demos

---

## 📋 Functional Requirements

### 1. Automated Order Initiation

- Trigger WhatsApp message on order creation
- Send clear instructions in patient's preferred language
- Automated reminders for pending documents

### 2. Document Capture

- Photo-based submission (no typing required)
- Support for TRF, Prescription, and Reports
- OCR integration for data extraction (future)

### 3. Multilingual Interface

- English, Hindi, Bengali, Tamil support
- Easy language switching
- Localized instructions and messages

### 4. Digital Consent

- OTP-based verification
- Mobile number validation
- Consent timestamp recording

### 5. Incentive Management

- Track compliant pickups per flebo
- ₹50 incentive per compliant pickup
- Automatic flagging for payment

### 6. Admin Dashboard

- Real-time compliance monitoring
- Manual follow-up assignment
- Document aggregation and audit trail
- Integration-ready for Zoho

---

## 🏗️ Technical Architecture (For Implementation)

```
┌─────────────────────────────────────────────────────────────┐
│                      Frontend Layer                          │
├─────────────────────────────────────────────────────────────┤
│  Admin Dashboard (React/Vue)  │  WhatsApp Business API      │
└─────────────────────────────────────────────────────────────┘
                              │
┌─────────────────────────────────────────────────────────────┐
│                      Backend Layer                           │
├─────────────────────────────────────────────────────────────┤
│  Node.js/Python API  │  Message Queue  │  OCR Service       │
└─────────────────────────────────────────────────────────────┘
                              │
┌─────────────────────────────────────────────────────────────┐
│                      Data Layer                              │
├─────────────────────────────────────────────────────────────┤
│  PostgreSQL/MongoDB  │  Redis Cache  │  File Storage (S3)   │
└─────────────────────────────────────────────────────────────┘
                              │
┌─────────────────────────────────────────────────────────────┐
│                   External Integrations                      │
├─────────────────────────────────────────────────────────────┤
│  Zoho CRM API  │  Twilio/Gupshup  │  Google Vision OCR      │
└─────────────────────────────────────────────────────────────┘
```

---

## 📱 User Flows

### Patient Flow

1. Receives WhatsApp message with order details
2. Views instructions in preferred language
3. Uploads photos of required documents
4. Receives OTP on registered mobile
5. Enters OTP to provide digital consent
6. Gets confirmation message

### Phlebotomist Flow

1. Receives assignment notification
2. Views patient details and requirements
3. Uploads documents on behalf of patient (if needed)
4. Triggers OTP to customer's phone
5. Enters OTP received from customer
6. Gets incentive confirmation (₹50)

### Admin Flow

1. Views dashboard with compliance statistics
2. Monitors pending and overdue orders
3. Assigns team members for manual follow-up
4. Tracks flebo incentives
5. Reviews and audits submitted documents

---

## 🔗 Related Documents

- [IMPLEMENTATION_ROADMAP.md](./IMPLEMENTATION_ROADMAP.md) - Detailed implementation plan
- `codingStandards.md` - Coding guidelines
- `LogiCompliance.js` - Business logic reference

---

## 👥 Target Users

1. **Patients** - Submit documents via WhatsApp
2. **Third-party Phlebotomists** - Collect and upload documents
3. **Logistics Team** - Monitor and manage compliance
4. **Sales Representatives** - Track order status by region

---

## 📄 License

This is a demo/prototype for educational and presentation purposes.

---

## 🤝 Contributors

Built as a capstone project for logistics document compliance optimization.
