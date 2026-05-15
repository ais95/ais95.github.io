# Tab Activity Monitor - Chrome Extension

A simple, lightweight Chrome extension that monitors and tracks active time spent on each browser tab.

## Features

✨ **Real-time Tracking** - Automatically tracks time spent on each tab
📊 **Statistics** - View total tabs and total time spent
🔍 **Search & Filter** - Quickly find tabs by name or URL
📈 **Sorting** - Sort by time spent, name, or recency
💾 **Local Storage** - All data is stored locally on your device
🗑️ **Clear Data** - Easy reset of all tracking data
🎨 **Clean UI** - Modern, intuitive interface

## Installation

### Method 1: Manual Installation

1. **Download the extension files**
   - Clone or download this repository
   - Ensure you have: `manifest.json`, `background.js`, `popup.html`, `popup.css`, `popup.js`

2. **Open Chrome Extensions Page**
   - Go to `chrome://extensions/`
   - Enable **"Developer mode"** (toggle in top right)

3. **Load the Extension**
   - Click **"Load unpacked"**
   - Select the folder containing the extension files
   - The extension icon should appear in your Chrome toolbar

### Method 2: Package as CRX (for distribution)

1. Go to `chrome://extensions/`
2. Click the menu icon ⋮ next to the extension
3. Click **"Pack extension"**
4. Select the extension folder
5. A `.crx` file will be generated for distribution

## How to Use

1. **Open the Popup**
   - Click the extension icon in your Chrome toolbar
   - The popup shows all tracked tabs with their active time

2. **Search Tabs**
   - Use the search box to filter tabs by title or URL
   - Results update in real-time

3. **Sort Results**
   - **By Time** - Shows most-used tabs first
   - **By Name** - Alphabetical order
   - **By Recent** - Recently opened tabs first

4. **View Statistics**
   - **Total Tabs** - Number of unique tabs tracked
   - **Total Time** - Combined active time across all tabs

5. **Clear Data**
   - Click the trash icon (🗑️) in the top right
   - Confirm to reset all tracking data

## How It Works

- **Background Service Worker** (`background.js`) runs continuously and:
  - Tracks tab switches and active time
  - Monitors window focus changes
  - Saves data to Chrome's local storage
  - Updates when tabs are opened/closed/refreshed

- **Popup Interface** (`popup.html/css/js`) displays:
  - All tracked tabs with icons and URLs
  - Time spent on each tab
  - Search and filtering capabilities
  - Real-time statistics

## Storage

- Data is stored locally using `chrome.storage.local`
- No data is sent to external servers
- Data persists across browser sessions
- Clearing browser data will clear extension data

## Privacy

✅ **Your data is private**
- No tracking, no analytics
- No connection to external services
- All data stored locally on your device
- You have full control to clear data anytime

## Permissions

- **tabs** - Read tab information (title, URL, status)
- **storage** - Store tracking data locally
- **scripting** - Execute scripts in tabs (prepared for future features)

## Troubleshooting

### Extension not showing time for some tabs
- Reload the tab (Ctrl+R / Cmd+R)
- Switch to another tab and back
- Check if the extension has proper permissions

### Data not persisting
- Check if you're using Incognito/Private mode (data not saved there)
- Verify extension storage permissions
- Try clearing and resetting the extension

### Popup not updating
- Click the extension icon to refresh
- The popup auto-updates every 2 seconds

## Future Enhancements

Potential features for future versions:
- 📈 Daily/weekly/monthly statistics charts
- 🎯 Tab activity goals and alerts
- 📊 Export data as CSV
- 🌙 Dark mode
- ⏰ Idle time detection
- 📱 Sync across devices
- 🔔 Notifications for inactive tabs

## Development

### File Structure
```
chrome-tab-monitor/
├── manifest.json      # Extension configuration
├── background.js      # Service worker - tracking logic
├── popup.html         # Popup interface
├── popup.css          # Popup styling
├── popup.js           # Popup logic
└── README.md         # This file
```

### Making Changes

1. Modify the source files
2. Go to `chrome://extensions/`
3. Click the refresh icon for the extension
4. Changes take effect immediately

### Testing

- Use different tabs to test tracking
- Close and reopen Chrome to verify data persistence
- Test search and sorting functionality
- Check window focus behavior with multiple windows

## License

MIT License - Feel free to use, modify, and distribute

## Support

For issues or suggestions:
1. Check the troubleshooting section
2. Verify all files are present and properly installed
3. Try reloading the extension
4. Clear extension data and restart

---

**Enjoy tracking your browsing habits!** 🚀
