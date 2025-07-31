# Step Challenge App

A clean, GitHub-inspired step tracking application for 30-day challenges.

## 🎯 Features

- **GitHub-style contribution grid** - Visual step tracking with colored squares
- **Clean, minimal design** - Apple-inspired interface
- **Mobile responsive** - Works great on all devices
- **Real-time updates** - Colors change as you enter data
- **Admin controls** - Hidden participant management
- **Interactive tooltips** - Hover for detailed information
- **Daily winner tracking** - Automatically highlights top performers

## 🚀 Getting Started

1. Clone this repository or download the files
2. Open `index.html` in your web browser
3. Start tracking steps!

## 📱 Usage

### For Participants
- **Click any day square** to enter your step count
- **Hover over squares** to see details
- **Color meanings:**
  - Gray squares = no data
  - Orange squares = missed goal (<10,000 steps)  
  - Green squares = goal achieved (≥10,000 steps)
  - Blue squares = daily winner (highest steps that day)

### For Administrators
- **Click the gear icon (⚙️)** in bottom left
- **Add new participants** through the admin panel
- **Click the question mark (?)** for color legend

## 🎨 Color System

The app uses iOS-inspired colors:
- **Success**: `#30d158` (green) - Goal achieved
- **Warning**: `#ff9500` (orange) - Goal missed
- **Primary**: `#007aff` (blue) - Daily winner
- **Background**: `#f5f5f7` (light gray) - No data

## ⚙️ Customization

### Challenge Settings
- **Challenge Duration**: Change `DAYS_IN_CHALLENGE` constant (default: 30)
- **Step Goal**: Modify `STEP_GOAL` constant (default: 10,000)

### Visual Customization
- Colors can be modified in the CSS variables
- Grid spacing and square sizes are easily adjustable
- Typography uses system fonts for native feel

## 📊 Technical Details

- **Pure HTML/CSS/JavaScript** - No frameworks required
- **Local storage ready** - Easy to add data persistence
- **API ready** - Structure supports backend integration
- **Responsive design** - Mobile-first approach
- **Progressive enhancement** - Works without JavaScript for basic viewing

## 🔧 Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## 📈 Future Enhancements

- [ ] Data persistence (localStorage/backend)
- [ ] User authentication
- [ ] Push notifications
- [ ] Fitness tracker integration (Apple Health, Google Fit, Fitbit)
- [ ] Social features & comments
- [ ] Challenge history
- [ ] Export functionality (CSV, PDF)
- [ ] Team challenges
- [ ] Streak tracking
- [ ] Achievement badges
- [ ] Challenge templates
- [ ] Data visualization charts
- [ ] Weekly/monthly summaries

## 🛠️ Development

### Project Structure
```
step-challenge-app/
├── index.html          # Main application file
├── README.md           # This file
├── assets/             # Optional: separated assets
│   ├── css/
│   │   └── styles.css  # Separated styles
│   └── js/
│       └── app.js      # Separated JavaScript
├── docs/
│   └── screenshots/    # App screenshots
└── .gitignore
```

### Adding Data Persistence

To add localStorage support, add this to the JavaScript:

```javascript
// Save data
function saveToStorage() {
    localStorage.setItem('stepChallengeData', JSON.stringify({
        participants: participants,
        stepData: stepData
    }));
}

// Load data
function loadFromStorage() {
    const saved = localStorage.getItem('stepChallengeData');
    if (saved) {
        const data = JSON.parse(saved);
        participants = data.participants || participants;
        stepData = data.stepData || stepData;
    }
}
```

### Adding Backend Integration

The app structure supports easy backend integration:

```javascript
// Example API calls
async function saveStepsToAPI(participantId, day, steps) {
    await fetch('/api/steps', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ participantId, day, steps })
    });
}

async function loadChallengeData() {
    const response = await fetch('/api/challenge/current');
    return response.json();
}
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Test thoroughly
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

## 📝 License

MIT License - feel free to use this for your own step challenges!

## 💡 Inspiration

This app was inspired by:
- **GitHub's contribution graph** - Clean, visual progress tracking
- **Apple's design language** - Minimal, focused user interface
- **Family fitness challenges** - Making step tracking fun and social

## 👥 Credits

Created with ❤️ for family step challenges.

Special thanks to:
- GitHub for the contribution graph inspiration
- Apple for the design system inspiration
- The open source community for JavaScript patterns

---

**Happy stepping! 🚶‍♀️🚶‍♂️**