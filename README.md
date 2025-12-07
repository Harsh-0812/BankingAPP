<div align="center">
  <br />
  
  <div>
    <img src="https://img.shields.io/badge/-Next_JS-black?style=for-the-badge&logoColor=white&logo=nextdotjs&color=000000" alt="nextdotjs" />
    <img src="https://img.shields.io/badge/-TypeScript-black?style=for-the-badge&logoColor=white&logo=typescript&color=3178C6" alt="typescript" />
    <img src="https://img.shields.io/badge/-Tailwind_CSS-black?style=for-the-badge&logoColor=white&logo=tailwindcss&color=06B6D4" alt="tailwindcss" />
    <img src="https://img.shields.io/badge/-Appwrite-black?style=for-the-badge&logoColor=white&logo=appwrite&color=FD366E" alt="appwrite" />
  </div>

  <h3 align="center">Banking App – Modern Fintech Dashboard</h3>
</div>

## 📋 Table of Contents

1. 🤖 [Introduction](#introduction)
2. ⚙️ [Tech Stack](#tech-stack)
3. 🔋 [Features](#features)
4. 🤸 [Quick Start](#quick-start)
5. 🕸️ [Code Snippets to Copy](#snippets)
6. 🔗 [Assets](#links)
7. 🚀 [More](#more)

## 🤖 Introduction

**Banking App** is a modern fintech web application built with **Next.js** and **TypeScript** that simulates a real-world banking dashboard.

The application allows users to:

- Securely sign up and sign in using **Appwrite** authentication  
- Connect multiple bank accounts using **Plaid**  
- View a unified overview of balances, recent transactions, and spending categories  
- Transfer funds between users using **Dwolla** as a payment rail  
- Track financial activity in a clean, responsive dashboard UI  

The goal of this project is to practice and demonstrate **full-stack skills**: integrating multiple third-party APIs (Appwrite, Plaid, Dwolla), handling real-world data flows (accounts, transactions, transfers), and building a scalable UI with reusable components (ShadCN, Radix UI, TailwindCSS).

This project is ideal for learning:

- How to structure a Next.js app using the **App Router**
- How to implement **SSR-friendly authentication** and sessions
- How to connect external fintech services safely with environment variables
- How to build a production-style dashboard with reusable UI patterns

## ⚙️ Tech Stack

- **Framework:** Next.js (App Router)
- **Language:** TypeScript
- **Styling:** TailwindCSS, TailwindCSS Animate
- **UI Components:** ShadCN, Radix UI (Tabs, Progress, Select, etc.)
- **Backend / Auth / DB:** Appwrite (users, banks, transactions collections)
- **Bank Integrations:** Plaid (accounts, transactions, link token, processor token)
- **Payments:** Dwolla (customers, funding sources, transfers)
- **Forms & Validation:** React Hook Form, Zod
- **Data Visualization:** Chart.js
- **Other utilities:** Custom hooks and helper functions (`utils`, `actions`, etc.)

## 🔋 Features

- **Authentication with Appwrite**  
  - Email/password signup and login  
  - Secure session handling using HTTP-only cookies  
  - Server-side user fetching with `createSessionClient` and `createAdminClient`

- **Multi-bank integration with Plaid**  
  - Connect multiple bank accounts from the sandbox environment  
  - Exchange Plaid public token for access token and item ID  
  - Fetch account details (balance, mask, subtype, institution)  
  - Store bank metadata in Appwrite collections

- **Real-time account overview dashboard**  
  - Total balance across all connected banks  
  - List of connected accounts with current/available balance  
  - Top spending categories using progress bars  
  - Recent transactions list with debit/credit indication

- **Transaction history and pagination**  
  - Fetch and combine Plaid transactions and internal transfer records  
  - Sort by date to show most recent activity first  
  - Paginated transaction list with previous/next navigation

- **Funds transfer with Dwolla**  
  - Create Dwolla customers linked to Appwrite users  
  - Create funding sources using Plaid processor tokens  
  - Transfer money between users’ funding sources  
  - Store transfer metadata as transactions in Appwrite

- **Sharable account ID for transfers**  
  - Generate encrypted sharable IDs for accounts  
  - Allow transfers using a public sharable ID instead of raw account ID  
  - Decrypt sharable ID safely on the server

- **Reusable UI components**  
  - `BankInfo`, `BankTabItem`, `BankDropdown` for account selection  
  - `Category` cards with Radix progress bars  
  - `PaymentTransferForm` with validation and loading states  
  - `Pagination`, `Copy` button, and various ShadCN form components

- **Responsive layout**  
  - Works smoothly on desktop, tablet, and mobile  
  - Uses a modern dashboard layout with sidebar, header, and content sections

## 🤸 Quick Start

Follow these steps to set up the project locally.

### Prerequisites

Make sure you have installed:

- [Git](https://git-scm.com)
- [Node.js](https://nodejs.org/en) (v18+ recommended)
- [npm](https://www.npmjs.com/) (or yarn/pnpm if you prefer)

### Clone the Repository

```bash
git clone https://github.com/<Harsh-0812>/banking-app.git
cd banking-app
