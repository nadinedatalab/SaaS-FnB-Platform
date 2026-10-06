# SaaS F&B Platform

A comprehensive Software-as-a-Service (SaaS) platform tailored for the Food & Beverage industry. The platform empowers restaurant and café owners to manage their operations efficiently across multiple branches and tenants, offering a seamless experience for both staff and customers.

## 🚀 Architecture & Tech Stack

This repository is structured as a monorepo containing three core applications:

1. **Backend API (`backend/api`)**
   - **Framework:** NestJS
   - **Database:** Supabase (PostgreSQL)
   - **Caching & Real-time:** Redis
   - **Core Features:** Multi-tenant support, JWT Auth, Role-based access control, Socket.IO for real-time sync, automated cron jobs.

2. **Staff Dashboard (`apps/staff-dashboard`)**
   - **Framework:** React + Vite
   - **Core Features:** POS (Point of Sale), Order management, Live floor map (real-time table statuses), Menu & Inventory management, Staff scheduling, CDP (Customer Data Platform) for managing loyalties & vouchers.

3. **Customer PWA (`apps/customer-pwa`)**
   - **Framework:** Next.js
   - **Core Features:** Mobile-first web app, QR code ordering, Cart management, Voucher applications, Live order tracking, e-Wallet & Memberships.

## 🌟 Key Features

- **Multi-Tenant System:** Run multiple isolated F&B brands from a single deployment.
- **Real-Time Sync:** Live updates between the customer app, POS, and kitchen using WebSockets & Redis.
- **Dynamic Floor Maps:** Interactive and customizable seating arrangements.
- **Smart Promotions:** Highly customizable percent-based and fixed-amount voucher system.
- **Customer Loyalty:** Tiered memberships, reward points, and e-wallet features.
- **Order Management:** Support for dine-in, takeaway, and group orders.

## 🛠 Setup & Local Development

This project relies on Docker for streamlined local development. 

1. Ensure Docker Desktop is running.
2. Clone the repository.
3. Start the entire stack:
   ```bash
   docker compose up -d
   ```
4. **Access the services:**
   - Staff Dashboard: http://localhost:5173
   - Customer PWA: http://localhost:3001
   - Backend API: http://localhost:3000/api/v1
