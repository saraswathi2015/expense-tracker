# 💰 ExpenseFlow - Smart Expense Tracker PWA

A comprehensive Progressive Web App for tracking personal expenses with AI-powered bill scanning, SMS/email parsing, budget management, and advanced analytics.

## ✨ Features

### Core Functionality
- **📸 AI Bill Scanning**: Upload photos of receipts/bills - AI extracts merchant, amount, date, and items automatically using OCR
- **💬 SMS/Email Parser**: Paste transaction messages to automatically extract expense details
- **💰 Manual Entry**: Quick manual expense entry with intuitive form
- **🏷️ Smart Categorization**: Auto-categorizes expenses (Food, Transport, Shopping, Bills, Entertainment, Health, Other)

### Budget Management
- **🎯 Category Budgets**: Set monthly budgets for each category
- **📊 Real-time Tracking**: Visual progress bars showing budget utilization
- **⚠️ Smart Alerts**: Get warnings when approaching budget limits (80%, 100%)
- **💡 Budget Insights**: Track remaining budget and overspending

### Analytics & Insights
- **📈 Spending Trends**: 30-day trend chart showing daily spending patterns
- **🥧 Category Breakdown**: Visual pie chart of spending by category
- **💡 AI Insights**: Smart insights about spending habits
  - Month-over-month comparisons
  - Most active spending days
  - Average expense calculations
  - Top spending categories

### Data Management
- **💾 Local Storage**: All data stored on your device (complete privacy)
- **📤 Export/Import**: Backup and restore data as JSON files
- **🔄 Cross-Device Sync**: Manually transfer data between phone and laptop
- **🗑️ Data Control**: Clear all data option

### User Experience
- **📱 Responsive Design**: Works perfectly on phone and laptop
- **🌙 Dark Theme**: Eye-friendly dark interface with financial data focus
- **⚡ Offline Support**: Works completely offline (PWA)
- **🏠 Installable**: Add to home screen on phone or desktop
- **🔔 Real-time Notifications**: Success, warning, and error alerts

## 🚀 Getting Started

### Installation Options

#### Option 1: Deploy to Web Server (Recommended)
1. Upload all files to your web server
2. Access via browser on phone/laptop
3. Click "Add to Home Screen" to install as app

#### Option 2: Local Development Server
```bash
# Using Python
cd expense-tracker
python -m http.server 8000

# Using Node.js
npx serve

# Using PHP
php -S localhost:8000
```

Then open: `http://localhost:8000`

#### Option 3: GitHub Pages (Free Hosting)
1. Create a GitHub repository
2. Upload all files
3. Enable GitHub Pages in repository settings
4. Access via `https://yourusername.github.io/repo-name`

### First-Time Setup

1. **Access the App**: Open in your web browser
2. **Install (Optional)**: 
   - **Phone**: Tap browser menu → "Add to Home Screen"
   - **Desktop**: Click install icon in address bar
3. **Set Budgets**: Go to Budget tab → "Set Monthly Budget"
4. **Configure Settings**: Adjust currency and default category

## 📖 Usage Guide

### Adding Expenses

#### Method 1: Manual Entry
1. Click "Add Expense" on dashboard
2. Fill in amount, merchant, category, date
3. Click "Add Expense"

#### Method 2: Scan Bill (Recommended)
1. Click "Scan Bill" on dashboard
2. Take photo or upload image of receipt
3. AI extracts details automatically
4. Review and confirm
5. Click "Save Expense"

**Supported Bill Formats:**
- Restaurant bills
- Shopping receipts
- Utility bills
- Any printed receipt with clear text

#### Method 3: Parse SMS/Email
1. Click "Parse SMS/Email"
2. Copy transaction message from SMS/email
3. Paste into text box
4. Click "Parse Message"
5. Review extracted details
6. Click "Save Expense"

**Example SMS Formats:**
```
Rs.450 debited from A/c XX1234 on 15-Feb for SWIGGY transaction

Your ICICI Bank A/c XX7890 is debited with INR 1,200 on 14-Feb-25 at UBER

Payment of Rs.299 made to NETFLIX via UPI
```

### Budget Management

1. Navigate to "Budget" tab
2. Click "Set Monthly Budget"
3. Enter budget amounts for each category
4. Click "Save Budgets"

**Budget Alerts:**
- **Green**: Under 80% of budget
- **Amber**: 80-100% of budget (warning)
- **Red**: Over budget (alert)

### Viewing Analytics

Navigate to "Analytics" tab to see:
- **Category Chart**: Pie chart of spending distribution
- **Trend Chart**: 30-day line graph of daily expenses
- **AI Insights**: Spending patterns and recommendations

### Data Management

#### Export Data
1. Go to Settings → "Export Data (JSON)"
2. Save the JSON file to your device
3. Keep this file safe as backup

#### Import Data
1. Go to Settings → "Import Data"
2. Select previously exported JSON file
3. Confirm replacement of current data

#### Sync Between Devices
1. Export data from Device A
2. Transfer JSON file (email, cloud, USB)
3. Import data on Device B

## 🎨 Features in Detail

### Smart Categorization

The app automatically detects expense categories from:
- Merchant names (Swiggy → Food, Uber → Transport)
- Keywords in bills/messages
- Common patterns

Categories:
- 🍔 **Food & Dining**: Restaurants, food delivery, groceries
- 🚗 **Transport**: Uber, Ola, fuel, parking
- 🛍️ **Shopping**: Amazon, Flipkart, retail
- 💡 **Bills & Utilities**: Electricity, water, internet, subscriptions
- 🎬 **Entertainment**: Movies, Netflix, Spotify, games
- 💊 **Health & Fitness**: Pharmacy, gym, medical
- 📦 **Other**: Everything else

### OCR Technology

Bill scanning uses **Tesseract.js** for optical character recognition:
- Extracts merchant names
- Identifies amounts (₹, Rs., INR formats)
- Detects dates in multiple formats
- Reads line items

**Tips for Best Results:**
- Good lighting when taking photos
- Flat, unwrinkled receipts
- Clear, in-focus images
- Complete bill visible in frame

### Privacy & Security

- **100% Local Storage**: All data stored in browser localStorage
- **No Cloud Sync**: Zero data transmission to external servers
- **No Tracking**: No analytics or tracking code
- **No Accounts**: No login required, no personal info collected
- **Full Control**: Export, import, or delete data anytime

## 📱 PWA Features

### Offline Support
- Works without internet connection
- Caches essential resources
- Data always accessible

### Installability
**Phone:**
- Appears on home screen like native app
- No browser UI (fullscreen)
- Fast startup

**Desktop:**
- Installable from browser
- Standalone window
- Easy access from taskbar

## 🛠️ Technical Stack

- **Frontend**: Pure HTML5, CSS3, JavaScript (no frameworks)
- **Charts**: Chart.js for analytics visualization
- **OCR**: Tesseract.js for bill scanning
- **Storage**: localStorage API (browser-based)
- **PWA**: Service Workers for offline functionality
- **Responsive**: Mobile-first CSS Grid/Flexbox design

## 📊 Browser Compatibility

- ✅ Chrome/Edge (Desktop & Mobile) - Recommended
- ✅ Safari (iOS 11.3+)
- ✅ Firefox (Desktop & Mobile)
- ✅ Samsung Internet
- ⚠️ OCR may be slower on older devices

## 🔧 Customization

### Change Currency
1. Go to Settings
2. Select your currency from dropdown
3. All amounts will update automatically

### Modify Categories
Edit the `categoryIcons` object in `index.html` to add/remove categories:

```javascript
const categoryIcons = {
    'Food': '🍔',
    'Transport': '🚗',
    'YourCategory': '🏷️',  // Add custom category
    // ...
};
```

### Adjust Theme Colors
Modify CSS variables in `index.html`:

```css
:root {
    --bg-primary: #0F172A;      /* Main background */
    --accent-green: #10B981;    /* Primary accent */
    /* ... more colors */
}
```

## 💡 Tips & Best Practices

1. **Regular Backups**: Export data monthly for safety
2. **Set Realistic Budgets**: Start conservative, adjust as needed
3. **Daily Tracking**: Add expenses daily for accuracy
4. **Use Bill Scanning**: Faster and more accurate than manual entry
5. **Review Analytics**: Check insights weekly to improve spending habits
6. **Clear Old Data**: Archive and clear data yearly to maintain performance

## 🐛 Troubleshooting

### OCR Not Working
- Ensure good lighting and clear image
- Try rotating or cropping the image
- Fallback to manual entry if needed

### Data Not Syncing Between Devices
- PWA uses local storage (no auto-sync)
- Use export/import feature to manually transfer data

### App Not Installing
- Use supported browser (Chrome, Safari, Edge)
- Check if already installed
- Try clearing browser cache

### Charts Not Displaying
- Check if Chart.js loaded (network required first time)
- Refresh page
- Ensure JavaScript is enabled

## 📄 File Structure

```
expense-tracker/
├── index.html          # Main app file (all-in-one)
├── manifest.json       # PWA manifest
├── sw.js              # Service worker (offline support)
└── README.md          # This file
```

## 🔐 Privacy Policy

This app:
- Stores ALL data locally on your device
- Does NOT transmit data to any server
- Does NOT use cookies or tracking
- Does NOT collect personal information
- Does NOT require internet after initial load

Your data is YOURS. Period.

## 📝 Version History

**v1.0** (Current)
- AI-powered bill scanning
- SMS/Email parsing
- Budget tracking with alerts
- Category-wise analytics
- Spending trend charts
- Export/Import functionality
- PWA support with offline mode
- Dark theme interface

## 🤝 Contributing

This is a personal expense tracker. Feel free to:
- Fork and customize for your needs
- Suggest improvements
- Report bugs

## 📧 Support

For issues or questions:
1. Check this README
2. Review browser console for errors
3. Try clearing app data and reloading

## ⚖️ License

Free to use for personal expense tracking. All rights reserved.

---

**Made with ❤️ for better financial tracking**

Start tracking your expenses smarter, not harder! 💰📊
