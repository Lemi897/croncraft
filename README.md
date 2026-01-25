# CronCraft ⏰

> Build cron schedules visually. No more syntax headaches.

A beautiful, modern web tool for creating and managing cron jobs without memorizing the syntax. Perfect for developers, system administrators, and anyone who works with scheduled tasks on Linux.

**[Live Demo →](https://lemi897.github.io/croncraft/)**

![Status](https://img.shields.io/badge/status-active-success.svg)
![Made with Love](https://img.shields.io/badge/made%20with-%E2%9D%A4-red.svg)

## ✨ Features

- **Visual Builder** - Input fields for each cron component with helpful hints
- **Quick Presets** - Common schedules (hourly, daily, weekly, weekdays only)
- **Import Existing** - Paste your cron job and auto-fill all fields
- **Next Run Times** - See exactly when your job will run next (5 upcoming runs)
- **Input Validation** - Red borders show invalid values instantly
- **Dark/Light Mode** - Toggle between themes, preference saved
- **Save & Manage** - Store multiple jobs in your browser
- **One-Click Copy** - Copy to clipboard ready for crontab
- **Download** - Export as .txt file
- **Human Readable** - Plain English description of your schedule
- **Mobile Responsive** - Works on all devices

## 🚀 Quick Start

Just open the website and start building! No installation needed.

**Or run locally:**
```bash
git clone https://github.com/lemii897/croncraft.git
cd croncraft
open index.html  # Or just double-click the file
```

## 📖 Usage

### Building a Cron Job

1. **Use Quick Presets** or fill in the time fields manually
2. **Add your command** (script path or command)
3. **Copy or download** your cron job
4. **Add to crontab:**
   ```bash
   crontab -e
   # Paste your cron job
   ```

### Importing Existing Jobs

Got an existing cron job? Paste it in the "Import Existing" box and hit Import. All fields auto-fill.

### Saving Jobs

Click "Save Job" to store it in your browser. Load it anytime from the "Saved Jobs" section.

## 💡 Examples

```bash
# Backup every day at 2 AM
0 2 * * * /usr/bin/backup.sh

# Check disk space every 15 minutes
*/15 * * * * /usr/bin/check_disk.sh

# Weekly report every Monday at midnight
0 0 * * 1 /usr/bin/weekly_report.sh

# Weekday reminder at 9 AM
0 9 * * 1-5 /usr/bin/reminder.sh
```

## 🎯 Cron Syntax Reference

```
┌───────────── minute (0-59)
│ ┌─────────── hour (0-23)
│ │ ┌───────── day of month (1-31)
│ │ │ ┌─────── month (1-12)
│ │ │ │ ┌───── day of week (0-7, 0/7 = Sunday)
│ │ │ │ │
* * * * * command to execute
```

**Special Characters:**
- `*` - Every unit (every minute, every hour, etc.)
- `*/N` - Every N units (*/5 = every 5 minutes)
- `N-M` - Range (1-5 = Monday through Friday)
- `N,M` - List (1,3,5 = Monday, Wednesday, Friday)

## 🛠️ Tech Stack

- Pure HTML/CSS/JavaScript
- No frameworks, no dependencies
- localStorage for saving jobs
- Responsive design with CSS Grid

## 🤝 Contributing

Contributions welcome! Here are some ideas:

**v2.0 Ideas:**
- [ ] Timezone support
- [ ] Email cron jobs to yourself
- [ ] Multi-job manager/editor
- [ ] Export to different formats (systemd timers, etc.)
- [ ] Cron job templates library
- [ ] Share jobs via URL

**To contribute:**
1. Fork the repo
2. Create a feature branch (`git checkout -b feature/cool-feature`)
3. Commit changes (`git commit -m 'Add cool feature'`)
4. Push to branch (`git push origin feature/cool-feature`)
5. Open a Pull Request

## 📝 License

MIT License - feel free to use this project however you want!

## 🌟 Support

If this tool saved you time, give it a star! ⭐

Found a bug or have a suggestion? [Open an issue](https://github.com/lemii897/croncraft/issues)

## 📬 Contact

Made with ❤️ for the Linux community

---

**Tip:** Bookmark this tool for quick access whenever you need to create a cron job!
