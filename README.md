# Income Tax Calculator

A comprehensive web-based income tax calculator that helps users calculate their annual income tax liability based on current tax brackets and deductions. Built with vanilla JavaScript for fast, accurate tax calculations.

## 🚀 Live Demo

[Calculate Your Tax Now](https://your-username.github.io/income-tax-calculator)

## ✨ Features

- **Multiple Tax Year Support** - Calculate taxes for current and previous tax years
- **Progressive Tax Brackets** - Accurate calculations using official tax brackets
- **Standard & Itemized Deductions** - Support for both deduction types
- **Real-time Calculations** - Instant results as you input your information
- **Tax Summary Breakdown** - Detailed breakdown of tax calculations by bracket
- **Responsive Design** - Works on desktop, tablet, and mobile devices
- **Printable Results** - Generate PDF-ready tax summaries
- **Data Privacy** - All calculations performed locally, no data stored on servers

## 🛠️ Technologies Used

- **HTML5** - Semantic form structure and accessibility
- **CSS3** - Modern styling with responsive grid layout
- **JavaScript (ES6+)** - Tax calculation logic and DOM manipulation
- **Local Storage** - Save user preferences and recent calculations
- **Print CSS** - Optimized printing and PDF generation

## 📊 Supported Tax Calculations

### Income Types
- Salary/Wages (W-2 income)
- Self-employment income
- Investment income (dividends, capital gains)
- Rental income
- Other taxable income

### Deductions & Credits
- Standard deduction
- Itemized deductions (mortgage interest, charitable donations, etc.)
- Personal exemptions
- Child tax credit
- Earned income tax credit
- Educational credits

### Tax Brackets (2024)
- Single filers
- Married filing jointly
- Married filing separately
- Head of household

## 📦 Installation & Setup

### Quick Start
```bash
# Clone the repository
git clone https://github.com/your-username/income-tax-calculator.git

# Navigate to project directory
cd income-tax-calculator

# Open in browser
open index.html
```

### Local Development Server
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx http-server

# Access at http://localhost:8000
```

## 🎯 How to Use

### Step 1: Personal Information
1. Select your filing status (Single, Married Filing Jointly, etc.)
2. Choose the tax year
3. Enter your personal details

### Step 2: Income Entry
1. **W-2 Income**: Enter your salary and wages
2. **Self-Employment**: Add business income and expenses
3. **Investments**: Include dividends, interest, and capital gains
4. **Other Income**: Add any additional taxable income

### Step 3: Deductions
1. **Choose Deduction Type**: Standard or Itemized
2. **Standard**: Automatically calculated based on filing status
3. **Itemized**: Enter mortgage interest, charitable donations, state taxes, etc.

### Step 4: Credits & Results
1. Enter applicable tax credits
2. View real-time tax calculation
3. Review detailed breakdown by tax bracket
4. Print or save results

## 📁 Project Structure

```
income-tax-calculator/
├── index.html              # Main application page
├── styles/
│   ├── main.css           # Main stylesheet
│   ├── forms.css          # Form styling
│   ├── results.css        # Results display styling
│   └── print.css          # Print-optimized styles
├── scripts/
│   ├── app.js             # Main application logic
│   ├── taxCalculator.js   # Core tax calculation engine
│   ├── taxBrackets.js     # Tax bracket data
│   ├── deductions.js      # Deduction calculations
│   └── utils.js           # Utility functions
├── data/
│   ├── taxBrackets2024.js # 2024 tax brackets
│   ├── taxBrackets2023.js # 2023 tax brackets
│   └── standardDeductions.js # Standard deduction amounts
├── assets/
│   └── images/            # Icons and images
├── README.md              # This file
└── LICENSE                # MIT License
```

## 🧮 Calculation Engine

### Tax Bracket Calculation
```javascript
// Progressive tax calculation example
function calculateProgressiveTax(taxableIncome, brackets) {
    let totalTax = 0;
    let remainingIncome = taxableIncome;
    
    for (let bracket of brackets) {
        const taxableAtThisBracket = Math.min(remainingIncome, bracket.max - bracket.min);
        totalTax += taxableAtThisBracket * bracket.rate;
        remainingIncome -= taxableAtThisBracket;
        
        if (remainingIncome <= 0) break;
    }
    
    return totalTax;
}
```

## ⚠️ Important Disclaimers

- **Educational Purpose**: This calculator is for educational and estimation purposes only
- **Not Professional Advice**: Results should not be considered professional tax advice
- **Consult Professionals**: Always consult a qualified tax professional for official tax planning
- **Accuracy**: While calculations use official tax brackets, individual situations may vary
- **Updates**: Tax laws change frequently; verify current rates and rules

## 🔧 Configuration

### Updating Tax Brackets
To update tax brackets for new years:
1. Create new file in `/data/` directory
2. Follow the format in existing bracket files
3. Update the year selector in `app.js`

### Adding New Features
- Modify `taxCalculator.js` for calculation logic
- Update `index.html` for new form fields
- Add styling in appropriate CSS files

## 🧪 Testing

### Manual Testing Scenarios
- Test with various income levels
- Verify calculations against known tax scenarios
- Test edge cases (very high/low incomes)
- Validate all filing statuses
- Check responsive design on different devices

## 🤝 Contributing

Contributions welcome! Areas for improvement:
- Additional tax scenarios
- State tax calculations
- International tax support
- Enhanced accessibility features
- Mobile app version

1. Fork the repository
2. Create feature branch (`git checkout -b feature/state-taxes`)
3. Commit changes (`git commit -am 'Add state tax calculations'`)
4. Push to branch (`git push origin feature/state-taxes`)
5. Create Pull Request

## 📱 Browser Support

- Chrome 70+
- Firefox 65+
- Safari 12+
- Edge 79+
- Mobile browsers (iOS Safari 12+, Chrome Mobile 70+)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [IRS Tax Tables](https://www.irs.gov) - Official tax bracket data
- [Claude.ai](https://claude.ai) - Development assistance
- Open source community for inspiration and best practices

---

**⚠️ Remember: This is for estimation only. Consult a tax professional for official advice.**

⭐ **Star this repository if it helped with your tax calculations!**
