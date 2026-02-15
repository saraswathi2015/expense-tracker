# 💰 Expense Tracker

A comprehensive personal expense tracking app with smart budgeting, insurance deductible tracking, and automated recurring transactions. Track your finances efficiently with rollover budgets, insurance optimization, and hands-free bill management.

---

## ✨ Features

### 📊 Dashboard
- Real-time overview of income vs expenses
- Net balance calculation
- Category-wise spending visualization
- Budget progress bars with color-coded alerts

### 💸 Expense Tracking
- Quick expense entry with categories
- Date-based organization
- Link expenses to insurance deductibles
- Mark recurring expenses
- Categories: Food, Transport, Shopping, Bills, Entertainment, Health, Other

### 🎯 Smart Budgeting with Rollover
- Set monthly budgets per category
- **Rollover budgets**: Carry unused budget to next month
- Enable/disable rollover per category
- Visual progress tracking
- Color-coded alerts (green/yellow/red)
- Real-time budget vs actual spending
- Rewards disciplined spending

**Rollover Example:**
```
February Food Budget: $600
Spent: $400
Saved: $200

March Food Budget: $600 + $200 (rollover) = $800 total available
```

### 🔄 Recurring Transactions
- **Auto-create monthly bills** on specific days
- Set up once, creates automatically every month
- Works for both expenses AND income
- Choose specific day of month (1-28)
- Toggle active/paused status
- Prevents duplicate entries with smart tracking

**Perfect for:**
- Rent/Mortgage payments
- Subscriptions (Netflix, Spotify, etc.)
- Monthly salary income
- Insurance premiums
- Utility bills

### 🛡️ Insurance Deductible Tracking
- Track multiple insurance deductibles (Health, Auto, Home, etc.)
- Visual progress bars showing deductible completion
- Automatically apply medical expenses to deductibles
- Alerts when close to meeting deductible
- Strategic planning for maximum insurance benefits

**Use Cases:**
- Know when you've met your annual health insurance deductible
- Plan expensive medical procedures after deductible is met
- Track auto insurance deductible progress after accidents
- Maximize benefits in the same calendar year

### 💰 Income Tracking
- Track multiple income sources
- Salary, freelance, gifts, and more
- Monthly income summaries

---

## 🛠️ Installation & Setup

### Option 1: Direct Browser Use
1. Download `index.html`
2. Open in any modern web browser
3. Start tracking! (Data saves automatically)

### Option 2: Install as PWA (Progressive Web App)
1. Open the app in Chrome/Edge/Safari
2. Click the install icon in the address bar
3. App installs on your device
4. Works offline after installation

### Option 3: Deploy to GitHub Pages
1. Create a new GitHub repository
2. Upload these files:
   - `index.html`
   - `manifest.json`
   - `sw.js`
3. Enable GitHub Pages in repository settings
4. Access from anywhere!

---

## 📱 How to Use

### Adding Your First Expense
1. Click **"Expenses"** tab
2. Click **"+ Add Expense"**
3. Fill in:
   - Amount
   - Category
   - Description
   - Date
4. Optional: Apply to insurance deductible
5. Click **"Add Expense"**

### Setting Up Budgets with Rollover
1. Click **"Budgets"** tab
2. Click **"+ Set Budget"**
3. Choose category
4. Enter monthly amount
5. ✅ Check **"Enable Rollover"** to carry unused budget forward
6. Click **"Set Budget"**

### Creating Recurring Transactions
1. Click **"Recurring"** tab
2. Click **"+ Add Recurring"**
3. Set up:
   - Type (Expense or Income)
   - Amount
   - Category
   - Description (e.g., "Rent", "Netflix", "Salary")
   - Day of month (1-28)
4. Click **"Add Recurring Transaction"**

**The app will automatically create this transaction on the specified day each month!**

### Tracking Insurance Deductibles
1. Click **"Insurance"** tab
2. Click **"+ Add Deductible"**
3. Enter:
   - Insurance name (e.g., "Health Insurance 2026")
   - Total deductible amount
   - Year
4. When adding medical expenses:
   - ✅ Check "Apply to insurance deductible"
   - Select which deductible
   - Amount automatically counts toward deductible

---

## 💡 Pro Tips

### Rollover Budgets
- **Enable for irregular categories**: Shopping, Entertainment, Gifts
- **Disable for fixed costs**: Rent, Bills, Insurance
- Build up a buffer for big purchases over 2-3 months

### Insurance Deductibles
- Track all medical expenses through the app
- Watch for the alert when you're close to meeting deductible
- Schedule elective procedures after deductible is met
- Maximize benefits in the same calendar year

### Recurring Transactions
- Set up ALL your regular bills upfront
- Review the "Recurring" tab monthly
- Pause subscriptions you're not using
- Use day 1-5 for most bills to stay organized

### Budget Strategy
```
Category          Budget    Rollover?   Why
────────────────────────────────────────────────
Rent              $1,650    ❌          Fixed cost
Food              $600      ✅          Flexible, can save
Transport         $200      ✅          Varies monthly
Shopping          $300      ✅          Save for big purchase
Bills             $150      ❌          Fixed utilities
Entertainment     $200      ✅          Splurge some months
Health            $100      ✅          Varies with needs
```

---

## 🔒 Privacy & Data

### Local Storage
- **All data stored in your browser only**
- Nothing sent to any server
- Completely private
- No account required

### Data Persistence
- Data saves automatically after each action
- Survives browser restarts
- Cleared only if you clear browser data

### Backup Your Data
To backup manually:
1. Open browser console (F12)
2. Go to "Application" tab
3. Click "Local Storage"
4. Copy the data
5. Save to a text file

To restore:
1. Open console
2. Paste data back into Local Storage
3. Refresh page

---

## 🎯 Use Cases

### For Students
- Track allowance/income
- Budget for textbooks and supplies
- Manage part-time job earnings
- Control dining and entertainment

### For Working Professionals
- Salary tracking with tax withholdings
- Rollover budgets for vacation savings
- Insurance deductible optimization
- Automate recurring bills

### For Freelancers
- Multiple income streams
- Variable monthly expenses
- Tax-deductible expense tracking
- Project-based budgeting

### For Families
- Combined household budgeting
- Track medical expenses against deductibles
- Plan for large purchases with rollover
- Monitor subscription costs

---

## 📊 Example Workflow

### Monthly Routine (5 minutes)
1. **Start of Month:**
   - Check Dashboard for rollover amounts
   - Review Budget tab for available funds
   - Verify Recurring transactions processed

2. **During Month:**
   - Add expenses as they happen
   - Check budget progress weekly
   - Update insurance deductibles for medical expenses

3. **End of Month:**
   - Review Dashboard for spending patterns
   - Check which budgets had rollover
   - Adjust next month's budgets if needed

## 🔧 Technical Details

### Technologies Used
- **React 18** - UI framework
- **Tailwind CSS** - Styling
- **LocalStorage API** - Data persistence
- **Service Worker** - Offline support (PWA)
- **Vanilla JavaScript** - No build tools needed

### Browser Compatibility
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

### File Structure
```
expense-tracker/
├── index.html          # Main app file (complete React app)
├── manifest.json       # PWA manifest for installable app
├── sw.js              # Service worker for offline support
└── README.md          # Documentation (this file)
```

---

## 🚨 Important Notes

### Recurring Transactions
- Only processes on the specified day of month
- Checks once per day (won't create duplicates)
- Day 29-31 not supported (use day 28 for end of month)
- Can pause temporarily without deleting

### Rollover Budgets
- Calculated at the start of each new month
- Only carries forward if budget > spending
- Doesn't roll backwards (can't go negative)
- Each category independent

### Insurance Deductibles
- Manual expense linking required
- Progress doesn't auto-reset yearly
- Create new deductible entry each year
- Multiple deductibles can be active

---

## 📈 Potential Future Enhancements
(Ideas for possible additions)

- 📊 Advanced charts and analytics
- 💱 Multi-currency support
- 📤 Export to CSV/Excel
- 🏷️ Custom tags for expenses
- 🎯 Savings goals tracker
- 📸 Receipt photo storage
- 🔔 Budget alerts via notifications
- 👥 Shared budgets (family mode)

---

## ❓ FAQ

**Q: Is my data secure?**
A: Yes! All data is stored locally in your browser only. Nothing is sent to any server.

**Q: How do I enable rollover for existing budgets?**
A: Go to Budgets → Click "+ Set Budget" → Select the same category → Enable rollover → Save

**Q: Can I have both rollover and non-rollover categories?**
A: Yes! Each category can have rollover enabled or disabled independently.

**Q: What happens if I delete a recurring transaction?**
A: It stops creating future entries. Past entries remain in your expense/income history.

**Q: Can I edit past expenses that were auto-created?**
A: Not directly in this version. You'll need to delete and re-add manually.

**Q: How do I reset my insurance deductible for a new year?**
A: Create a new deductible entry with the new year. The old one remains for historical tracking.

**Q: Does this work offline?**
A: Yes! If installed as PWA. The app and all your data work completely offline.

**Q: Can I use this on multiple devices?**
A: Each device stores data separately. For multi-device sync, deploy to GitHub Pages and use the same URL.

---

## 🐛 Troubleshooting

### Data not saving
1. Check browser privacy settings
2. Ensure LocalStorage is enabled
3. Try a different browser
4. Clear cache and reload

### Recurring transactions not creating
1. Check the day of month setting
2. Verify transaction is "Active"
3. Wait until the specified day
4. Check browser console for errors

### Rollover not calculating
1. Wait for month to change
2. Ensure rollover is enabled for category
3. Check that previous month had unused budget
4. Refresh the page

---

## 📄 License

MIT License - Free to use, modify, and distribute.

---

## 🙏 About

Built for comprehensive personal finance management with focus on:
- Smart budgeting with rollover support
- Tax withholding tracking (per paycheck, not quarterly)
- Debt management (0% APR tracking)
- Insurance deductible optimization
- Automation through recurring transactions
- Complete privacy with local-only data storage

**Last Updated:** February 2026  
**Compatibility:** All modern browsers

---

## 📞 Support

Having issues or questions?
- Check the FAQ above
- Review the "How to Use" section
- Inspect browser console for errors (F12)
- Try clearing browser cache

---

**Happy tracking! 💰📊**
