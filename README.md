# 30-day-step-challenge
# Step Challenge App

A clean, GitHub-inspired step tracking application for 30-day challenges.

## Project Structure

```
step-challenge-app/
├── index.html          # Main application file
├── README.md           # This file
├── assets/
│   ├── css/
│   │   └── styles.css  # Separated styles (optional)
│   └── js/
│       └── app.js      # Separated JavaScript (optional)
├── docs/
│   └── screenshots/    # App screenshots
└── .gitignore
```

## Features

- **GitHub-style contribution grid** - Visual step tracking with colored squares
- **Clean, minimal design** - Apple-inspired interface
- **Mobile responsive** - Works great on all devices
- **Real-time updates** - Colors change as you enter data
- **Admin controls** - Hidden participant management
- **Interactive tooltips** - Hover for detailed information
- **Daily winner tracking** - Automatically highlights top performers

## Getting Started

1. Clone this repository
2. Open `index.html` in your browser
3. Start tracking steps!

## Usage

### For Participants
- Click any day square to enter your step count
- Hover over squares to see details
- Gray squares = no data
- Orange squares = missed goal (<10,000 steps)  
- Green squares = goal achieved (≥10,000 steps)
- Blue squares = daily winner (highest steps that day)

### For Administrators
- Click the gear icon (⚙️) in bottom left
- Add new participants through the admin panel
- Click the question mark (?) for color legend

## Technical Details

- **Pure HTML/CSS/JavaScript** - No frameworks required
- **Local storage ready** - Easy to add data persistence
- **API ready** - Structure supports backend integration
- **Responsive design** - Mobile-first approach

## Customization

### Colors
The app uses iOS-inspired colors that can be customized in the CSS:
- Success: `#30d158` (green)
- Warning: `#ff9500` (orange) 
- Primary: `#007aff` (blue)
- Background: `#f5f5f7` (light gray)

### Challenge Duration
Change `DAYS_IN_CHALLENGE` constant to modify the challenge length.

### Step Goal
Modify `STEP_GOAL` constant to change the daily target.

## Future Enhancements

- [ ] Data persistence (localStorage/backend)
- [ ] User authentication
- [ ] Push notifications
- [ ] Fitness tracker integration
- [ ] Social features & comments
- [ ] Challenge history
- [ ] Export functionality
- [ ] Team challenges
- [ ] Streak tracking
- [ ] Achievement badges

## Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License - feel free to use this for your own step challenges!

## Credits

Inspired by GitHub's contribution graph and Apple's design language.
Created for family step challenges with love ❤️
