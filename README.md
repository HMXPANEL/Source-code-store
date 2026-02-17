# CodeStore

A modern Firebase-powered source code marketplace with authentication, live purchase tracking, manual payment verification, and dynamic product rendering.

---

## Overview

CodeStore is a full-featured digital marketplace built using Vanilla JavaScript and Firebase services.

The platform allows developers to:

- Browse source code products
- View detailed previews
- Purchase via UPI QR payment
- Upload payment proof
- Track purchase status in real time
- Download purchased source code
- Receive system notifications

This project demonstrates a complete frontend + Firebase integration architecture without using frameworks.

---

## Core Features

### 🔐 Authentication System
- Email & password login
- Account registration
- Persistent auth state
- User profile storage in Firebase
- Editable profile name

### 🛍 Product Marketplace
- Dynamic product rendering from Firebase
- Category-based filtering
- Live search functionality
- Featured product ribbons
- Rating & download indicators
- Full-page product preview system

### 💳 Manual Payment Verification System
- UPI QR payment support
- Screenshot upload for proof
- Payment status tracking (PENDING / APPROVED / REJECTED)
- Real-time purchase updates
- Confetti success feedback

### 📦 My Purchases & Downloads
- Live purchase history tab
- Status badges (Approved / Pending / Rejected)
- Download access after approval
- Demo & GitHub link support

### 🔔 Notifications System
- Real-time notification feed
- Targeted notifications (ALL / SINGLE user)
- Unread badge counter
- Local read-state tracking

### ⚙ Admin-Controlled Settings
- Dynamic app name & logo
- Editable privacy policy content
- Promotions banner system
- Admin QR / UPI configuration

### 🎨 UI / UX
- Dark / Light mode toggle
- Responsive mobile-first design
- Bottom navigation system
- Slide-up modal sheets
- Toast notifications
- Loading states
- Full-screen product preview

---

## Tech Stack

**Frontend**
- HTML5
- CSS (Custom theme system with variables)
- Vanilla JavaScript

**Backend Services**
- Firebase Authentication
- Firebase Realtime Database

**Architecture Highlights**
- Centralized app state
- Modular rendering logic
- Real-time database listeners
- Purchase approval workflow
- Payment verification pipeline

---

## Firebase Database Structure (Example)

```
products/
  productId/
    title
    description
    price
    bannerUrl
    categoryName
    featured
    rating
    downloads
    fileUrl
    demoUrl
    githubUrl

users/
  uid/
    name
    email

payments/
  paymentId/
    userId
    userEmail
    productId
    productTitle
    amount
    screenshot
    status
    timestamp

notifications/
  notificationId/
    message
    icon
    timestamp
    targetType
    targetEmail

appSettings/
  appName
  appLogo
  policyText

adminSettings/
  qr
  upi
```

---

## Installation & Setup

1. Clone the repository
2. Replace Firebase configuration with your own project credentials
3. Enable Email/Password authentication in Firebase
4. Create required database nodes
5. Deploy using:
   - Firebase Hosting
   - Netlify
   - Any static hosting provider

---

## Security Notes

- Payments are manually verified by admin
- Purchase approval required before download
- Sensitive configuration stored in Firebase
- Auth state required for marketplace access

---

## Future Improvements

- Admin dashboard for payment approval
- File storage via Firebase Storage
- Role-based access (Admin / User)
- Razorpay / Stripe integration
- Server-side validation
- Advanced analytics
- Product reviews & comments

---

## What This Project Demonstrates

- Real-time Firebase integration
- Payment verification workflow
- Scalable marketplace logic
- Modular UI architecture
- Clean responsive design
- State-driven frontend rendering

---

## License

This project is built for educational and demonstration purposes.
