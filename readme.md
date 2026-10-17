# Website Tracker — Chrome Extension

<p align="center">
  <img src="https://img.shields.io/badge/Chrome-Extension-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Chrome Extension">
  <img src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/Analytics-Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white" alt="Chart.js">
  <img src="https://img.shields.io/badge/Storage-Chrome%20Local-34A853?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Chrome Storage">
</p>

<p align="center">
  <strong>Track your browsing habits. Understand your screen time. Take control of your productivity.</strong>
</p>

<p align="center">
  A Chrome extension that monitors time spent on websites and visualizes browsing activity through interactive charts, daily and monthly analytics, and customizable website restrictions.
</p>

---

## Overview

**Website Tracker** helps you understand how you spend your time online. It tracks active website usage, records browsing statistics, and presents your activity through visual analytics.

Whether you want to reduce distractions, improve productivity, or understand your internet usage, Website Tracker helps you make informed decisions about your browsing habits.

### Key Highlights

- Automatic website usage tracking
- Interactive analytics dashboard
- Daily and monthly browsing reports
- Website usage limits and blocking controls
- Pie charts and graphical usage summaries
- Local data persistence using Chrome Storage

---

## Preview

### Extension Popup

<p align="center">
  <img src="assets/video/popup.gif" alt="Website Tracker extension popup showing website usage" width="650">
</p>

### Browsing Analytics

<p align="center">
  <img src="assets/video/graph.gif" alt="Website Tracker analytics graphs and charts" width="650">
</p>

> If the GIFs do not appear on GitHub, verify that the files exist at `assets/video/popup.gif` and `assets/video/graph.gif`. GitHub filenames and paths are case-sensitive.

---

## Features

### 1. Real-Time Website Tracking

- Tracks time spent on websites while browsing.
- Displays website usage through the extension popup.
- Helps identify frequently visited websites.
- Provides insights into browsing habits and time allocation.

### 2. Interactive Analytics Dashboard

Visualize browsing activity using charts and graphs.

- **Daily Analytics:** Review website usage during the day.
- **Monthly Analytics:** Understand longer-term browsing trends.
- **Pie Chart:** Compare the distribution of time spent across websites.
- **Usage Comparisons:** Identify websites that consume the most time.

### 3. Website Usage Management

Customize how individual websites are tracked and accessed.

| Mode | Description |
|---|---|
| **None** | No special restriction is applied. |
| **Ignore** | Excludes selected websites from tracking, if supported by the implementation. |
| **Time Limit** | Sets a daily usage allowance for a selected website. |
| **Block** | Restricts access to selected websites, subject to extension permissions and implementation. |

When a configured time limit is reached, the extension can restrict access for the remainder of the day if this functionality is implemented and enabled.

### 4. Persistent Local Storage

- Uses `chrome.storage.local` to store browsing statistics and settings.
- Retains saved information across browser sessions.
- Stores extension data in the browser's local extension storage.

### 5. Lightweight Chrome Integration

- Accessible directly from the Chrome toolbar.
- Built using standard web technologies.
- Uses Chrome extension APIs for browser integration.
- Supports data visualization through Chart.js.

---

## Technology Stack

| Technology | Purpose |
|---|---|
| **JavaScript** | Tracking logic, data processing, and interactions |
| **HTML5** | Popup and dashboard structure |
| **CSS3** | Layout, styling, and responsive presentation |
| **Bootstrap** | UI components and layout utilities |
| **Chart.js** | Interactive charts and data visualization |
| **Chrome Extension APIs** | Browser integration and extension functionality |
| **Chrome Storage API** | Persistent local storage of tracking data and settings |

---

## Installation

Install Website Tracker locally using Chrome Developer Mode.

### Prerequisites

- Google Chrome or a compatible Chromium-based browser
- Git, or a downloaded copy of the repository

### Step 1: Clone the Repository

Open a terminal and run:

```bash
git clone https://github.com/ankitjha2603/website-tracker.git
```

### Step 2: Open Chrome Extensions

Navigate to:

```text
chrome://extensions/
```

### Step 3: Enable Developer Mode

Enable **Developer mode** using the toggle in the upper-right corner of the Extensions page.

### Step 4: Load the Extension

1. Click **Load unpacked**.
2. Navigate to the folder containing `manifest.json`.
3. Select that folder.
4. Confirm that Website Tracker appears in your extensions list.

### Step 5: Start Tracking

Pin the extension to the Chrome toolbar, browse a website, and click the Website Tracker icon to access its popup.

> Select the directory containing `manifest.json`, not its parent directory. Actual behavior depends on the extension's manifest version, permissions, and source code.

---

## Usage Guide

### View Website Usage

1. Open Chrome and browse normally.
2. Click the Website Tracker icon.
3. Review the usage information displayed in the popup.

### Analyze Browsing Habits

1. Open the extension's analytics interface.
2. Select the daily or monthly view, where available.
3. Examine the charts to compare website usage.
4. Use the results to identify browsing patterns and potential distractions.

### Configure Website Restrictions

1. Open the website management or settings interface.
2. Select the website you want to manage.
3. Choose an available mode: None, Ignore, Time Limit, or Block.
4. Configure the daily limit or blocking settings, where applicable.
5. Save your changes and verify the behavior.

*Available controls and their exact behavior depend on the implementation included in the repository.*

---

## Project Structure

The following is an example structure for a Chrome extension of this type. Your repository may use different filenames or directories.

```text
website-tracker/
│
├── manifest.json
├── popup.html
├── popup.css
├── popup.js
│
├── background.js
├── dashboard.html
├── dashboard.css
├── dashboard.js
│
├── assets/
│   ├── icons/
│   └── video/
│       ├── popup.gif
│       └── graph.gif
│
└── README.md
```

**Note:** Files such as `background.js` and `dashboard.html` are illustrative. Keep the filenames and directories that actually exist in your project.

---

## Privacy

Website Tracker helps users understand their browsing activity.

- Tracking data can be stored locally using `chrome.storage.local`.
- The extension requires appropriate Chrome permissions to access information needed for tracking.
- Review `manifest.json` and the source code to understand exactly what information is collected and how it is handled.
- Local storage does not automatically guarantee that all data stays local. Verify whether the implementation uses external services or network requests.

Use the extension responsibly and review its permissions before installation.

---

## Troubleshooting

### The Extension Does Not Load

- Open `chrome://extensions/`.
- Check for errors displayed on the extension card.
- Verify that `manifest.json` is valid.
- Ensure you selected the correct project directory.

### The Popup Does Not Display Usage Data

- Visit a website and allow the extension time to record activity.
- Check the extension's permissions.
- Inspect the popup and background service worker for errors.
- Verify that the tracking logic and storage operations are working correctly.

### The Charts Are Not Displayed

- Confirm that Chart.js is available and loaded correctly.
- Verify that the chart container exists.
- Check the browser console for JavaScript errors.
- Ensure that the analytics code receives valid data.

### Screenshots or GIFs Are Missing

Confirm that these files exist in the repository:

```text
assets/video/popup.gif
assets/video/graph.gif
```

If you have added or updated the GIFs, commit and push the changes:

```bash
git add README.md assets/video/
git commit -m "Improve README documentation and previews"
git push
```

---

## Contributing

Contributions, bug reports, and suggestions are welcome.

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature/your-feature
   ```

3. Make your changes and test the extension.
4. Commit your changes:

   ```bash
   git commit -m "Add your feature"
   ```

5. Push your branch:

   ```bash
   git push origin feature/your-feature
   ```

6. Open a Pull Request describing your changes.

Please ensure that the extension continues to load correctly and that existing tracking and analytics functionality is preserved.

---

## License

Check the repository for an existing `LICENSE` file to determine the applicable license. If no license is present, add one before explicitly licensing the project for redistribution or modification.

---

<p align="center">
  <strong>Browse smarter. Understand your habits. Make your time online count.</strong>
</p>
