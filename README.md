<div align="center">

# 🧾 razorpay-billing-saas

### Full-Stack SaaS Billing Starter with Razorpay Integration

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-brightgreen)](https://nodejs.org)
[![React](https://img.shields.io/badge/React-18-blue)](https://reactjs.org)
[![MongoDB](https://img.shields.io/badge/MongoDB-6%2B-green)](https://mongodb.com)
[![Razorpay](https://img.shields.io/badge/Razorpay-Integrated-072654)](https://razorpay.com)
[![Made in India](https://img.shields.io/badge/Made%20in-India%20🇮🇳-orange)](#)
[![Stars](https://img.shields.io/github/stars/gajendrachary/razorpay-billing-saas?style=social)](https://github.com/gajendrachary/razorpay-billing-saas/stargazers)

**A production-ready SaaS billing boilerplate built specifically for Indian startups and developers.**
Skip months of setup. Start collecting payments from Day 1.

[🚀 Features](#-features) • [📦 Installation](#-installation) • [🔧 Configuration](#-configuration) • [📸 Screenshots](#-screenshots) • [🤝 Contributing](#-contributing)

</div>

---

## 🎯 Why This Project?

Building a SaaS product in India comes with unique challenges:
- Integrating **Razorpay** (UPI, cards, net banking, wallets)
- Managing **GST-compliant invoices**
- Handling **subscription plans** and **payment webhooks**
- Building a clean **admin dashboard** to track revenue

This starter solves all of that — out of the box.

---

## ✨ Features

### 💳 Payments & Billing
- ✅ Razorpay Payment Gateway (UPI, Cards, Net Banking, Wallets)
- ✅ Subscription plans (monthly / yearly)
- ✅ Webhook handling for payment success/failure
- ✅ Automatic invoice generation (PDF)
- ✅ GST-ready invoice templates
- ✅ Refund management

### 👤 Auth & Users
- ✅ JWT-based authentication
- ✅ Role-based access (Admin / Customer)
- ✅ Email verification & password reset
- ✅ Google OAuth (optional)

### 📊 Dashboard
- ✅ Revenue analytics
- ✅ Active subscriptions overview
- ✅ Transaction history
- ✅ Customer management

### 🛠️ Developer Experience
- ✅ Clean REST API with Express.js
- ✅ React frontend with Tailwind CSS
- ✅ MongoDB with Mongoose ODM
- ✅ Environment-based config
- ✅ Docker-ready
- ✅ Fully documented API

---

## 🧱 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 18, Tailwind CSS, Axios |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Payments | Razorpay SDK |
| Auth | JWT, bcrypt |
| Email | Nodemailer |
| Deployment | Docker, GitHub Actions |

---

## 📦 Installation

### Prerequisites
- Node.js v18+
- MongoDB (local or Atlas)
- Razorpay account ([Sign up free](https://razorpay.com))

### Clone & Setup

```bash
# Clone the repo
git clone https://github.com/gajendrachary/razorpay-billing-saas.git
cd razorpay-billing-saas

# Install backend dependencies
cd server && npm install

# Install frontend dependencies
cd ../client && npm install
```

---

## 🔧 Configuration

Create a `.env` file in the `/server` directory:

```env
# Server
PORT=5000
NODE_ENV=development

# MongoDB
MONGODB_URI=mongodb://localhost:27017/saas_billing

# JWT
JWT_SECRET=your_super_secret_key
JWT_EXPIRES_IN=7d

# Razorpay
RAZORPAY_KEY_ID=rzp_test_xxxxxxxxxxxx
RAZORPAY_KEY_SECRET=your_razorpay_secret
RAZORPAY_WEBHOOK_SECRET=your_webhook_secret

# Email
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your@email.com
SMTP_PASS=your_app_password
```

---

## 🚀 Running the App

```bash
# Run backend (from /server)
npm run dev

# Run frontend (from /client)
npm start
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 📁 Project Structure

```
razorpay-billing-saas/
├── client/                  # React frontend
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/           # Dashboard, Billing, Auth pages
│   │   ├── hooks/           # Custom React hooks
│   │   └── utils/           # Helpers & API calls
├── server/                  # Node.js backend
│   ├── controllers/         # Route controllers
│   ├── models/              # Mongoose models
│   ├── routes/              # API routes
│   ├── middlewares/         # Auth, error handling
│   ├── services/            # Razorpay, email services
│   └── webhooks/            # Razorpay webhook handler
├── .github/
│   └── workflows/           # CI/CD pipelines
├── docker-compose.yml
└── README.md
```

---

## 🔗 API Endpoints

### Auth
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | Login |
| POST | `/api/auth/forgot-password` | Forgot password |

### Billing
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/plans` | Get all plans |
| POST | `/api/orders/create` | Create Razorpay order |
| POST | `/api/orders/verify` | Verify payment |
| GET | `/api/invoices` | Get user invoices |
| GET | `/api/invoices/:id/pdf` | Download invoice PDF |

### Webhooks
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/webhook/razorpay` | Handle Razorpay events |

---

## 🤝 Contributing

Contributions are welcome! Whether it's bug fixes, new features, or documentation improvements.

```bash
# Fork the repo, then:
git checkout -b feature/your-feature
git commit -m 'Add your feature'
git push origin feature/your-feature
# Open a Pull Request
```

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

## 👨‍💻 Author

**Gajendrachary**  
Founder & Full-Stack Developer at [DevHorizon Technologies](https://devhorizontech.com)  
Bengaluru, Karnataka, India 🇮🇳

[![GitHub](https://img.shields.io/badge/GitHub-@gajendrachary-black?logo=github)](https://github.com/gajendrachary)  

---

<div align="center">

**If this project helped you, please ⭐ star it — it means a lot!**

</div>
