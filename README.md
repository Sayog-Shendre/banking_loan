# 🏦 Bank Lending System

A comprehensive loan management and tracking solution built with vanilla HTML, CSS, and JavaScript. This system provides a complete interface for creating loans, processing payments, and tracking loan histories with a modern, responsive design.

## 🌟 Features

### Core Functionality
- **📝 Loan Creation**: Generate new loans with automatic interest and EMI calculations  
- **💰 Payment Processing**: Record EMI and lump sum payments with real-time balance updates  
- **📊 Loan Ledger**: Complete transaction history and loan status tracking  
- **👤 Customer Overview**: Comprehensive summary of all customer loans  
- **📈 Progress Tracking**: Visual progress bars showing payment completion status  

### Technical Features
- **🎨 Modern UI/UX**: Gradient backgrounds, animations, and interactive elements  
- **📱 Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices  
- **⚡ Real-time Calculations**: Instant loan calculations using simple interest formula  
- **🔄 Mock API**: Simulates backend operations with realistic response delays  
- **💾 In-Memory Storage**: Data persistence during session (resets on page refresh)  
- **🎯 Error Handling**: Comprehensive error messages and validation  


### Sample Data for Testing
- **Customer IDs**: `CUST001` (John Doe), `CUST002` (Jane Smith)  
- **Test Loan Amount**: ₹100,000  
- **Test Period**: 5 years  
- **Test Interest Rate**: 12.5% per annum  

## 📋 Table of Contents
- [Installation](#-installation)
- [Usage](#-usage)
- [API Documentation](#-api-documentation)
- [Calculations](#-calculations)
- [Project Structure](#-project-structure)
- [Technologies Used](#-technologies-used)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [License](#-license)

## 🔧 Installation

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No additional dependencies required!

### Quick Start
```bash
git clone https://github.com/Sayog-Shendre/banking_loan.git
cd banking_loan

# Option 1: Open directly
open index.html

# Option 2: Use local server
python -m http.server 8000
# or
npx serve .
```

## 📖 Usage

### 1. Creating a New Loan
```text
Go to "Create Loan" tab → Fill customer ID, amount, period, interest rate → Click "Create Loan"
```

### 2. Making Payments
```text
Go to "Make Payment" tab → Enter Loan ID and amount → Select EMI or Lump Sum → Click "Record Payment"
```

### 3. Viewing Loan Ledger
```text
Go to "View Ledger" tab → Enter Loan ID → Click "Get Ledger"
```

### 4. Customer Overview
```text
Go to "Customer Overview" tab → Enter Customer ID → View all active loans
```

## 🔌 API Documentation

### Create Loan
```js
POST /loans
{
  customer_id: "string",
  loan_amount: "number",
  loan_period_years: "number",
  interest_rate_yearly: "number"
}
```

### Make Payment
```js
POST /loans/{loan_id}/payments
{
  amount: "number",
  payment_type: "EMI" | "LUMP_SUM"
}
```

### Get Ledger
```js
GET /loans/{loan_id}/ledger
```

### Customer Overview
```js
GET /customers/{customer_id}/overview
```

## 🧮 Calculations

### Simple Interest Formula
```
Interest = Principal × Rate × Time / 100
Total = Principal + Interest
Monthly EMI = Total / (Years × 12)
```

### Example
```
Principal = ₹100,000, Rate = 12.5%, Time = 5 years
Interest = ₹62,500
Total = ₹162,500
Monthly EMI = ₹2,708.33
```

## 📁 Project Structure

```
banking_loan/
├── ht.html
├── README.md
└── assets/
    ├── screenshots/
    └── docs/
```

## 🛠️ Technologies Used

| Technology | Purpose | Version |
|------------|---------|---------|
| HTML5      | Markup  | Latest  |
| CSS3       | Styling | Latest  |
| JavaScript (ES6+) | Logic | ES2018+ |

## 🎨 Design System

### Color Palette
```css
Primary: linear-gradient(135deg, #667eea, #764ba2)
Secondary: linear-gradient(135deg, #74b9ff, #0984e3)
Success: #00b894, Warning: #fdcb6e, Error: #e17055
```

### Typography
```css
Font: 'Segoe UI', Tahoma, sans-serif
Headers: 2.5rem bold
Body: 1rem regular
```

## 📱 Browser Compatibility

| Browser | Supported |
|---------|-----------|
| Chrome  | ✅        |
| Firefox | ✅        |
| Safari  | ✅        |
| Edge    | ✅        |
| IE 11   | ⚠️ Limited |



## 🧪 Testing

### Manual Test Cases
- ✅ Valid/Invalid Loan Creation  
- ✅ Payment Recording (EMI / Lump Sum)  
- ✅ Ledger Accuracy  
- ✅ Responsive Layout  
- ✅ Validation & Error Handling  

### Sample Test Data
```js
const testLoan = {
  customer_id: "CUST001",
  loan_amount: 100000,
  loan_period_years: 5,
  interest_rate_yearly: 12.5
};
const testPayment = {
  amount: 5000,
  payment_type: "EMI"
};
```

## 🚀 Deployment

### GitHub Pages
- Enable GitHub Pages in repo settings (branch: `main`)

### Netlify
- Connect → Set build command: none → Publish directory: `/`

### Local Dev
```bash
python -m http.server 8000
# or
npx serve .
```

## 🤝 Contributing

1. Fork → Branch → Commit → Push → PR  
2. Follow existing style  
3. Test all changes  
4. Keep responsive design intact

## 📄 License

This project is licensed under the MIT License  
See the [LICENSE](LICENSE) file for more details.

## 👨‍💻 Author

**Sayog Shendre**  
- GitHub: [@Sayog-Shendre](https://github.com/Sayog-Shendre)  
- LinkedIn: [Sayog Shendre](https://linkedin.com/in/sayog-shendre)  
- Email: sayogshendre6838@gmail.com

## 🔮 Future Enhancements

- [ ] Backend API Integration  
- [ ] Persistent DB (IndexedDB/LocalStorage)  
- [ ] User Authentication  
- [ ] Export Reports (PDF/CSV)  
- [ ] Compound Interest Support  
- [ ] Notifications & Alerts  
- [ ] Dark Mode & Accessibility  
- [ ] Multi-language Support  
- [ ] Chart.js Analytics  
- [ ] React Native Mobile App
