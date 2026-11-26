<h1 align="center">🎬 MovieBrowser for Enigma2</h1>

<p align="center">
  <a href="https://github.com/Belfagor2005/MovieBrowser">
    <img src="https://img.shields.io/badge/Version-4.4-blue.svg" alt="Version">
  </a>

  <a href="https://www.enigma2.net">
    <img src="https://img.shields.io/badge/Enigma2-Plugin-ff6600.svg" alt="Enigma2">
  </a>

  <a href="https://www.python.org">
    <img src="https://img.shields.io/badge/Python-3-blue.svg" alt="Python">
  </a>

  <a href="https://github.com/Belfagor2005/MovieBrowser/actions/workflows/pylint.yml">
    <img src="https://github.com/Belfagor2005/MovieBrowser/actions/workflows/pylint.yml/badge.svg" alt="Python package">
  </a>

</p>

<p align="center">
  <a href="https://github.com/Belfagor2005">
    <img src="https://komarev.com/ghpvc/?username=Belfagor2005&label=Repository%20Views&color=blueviolet" alt="Visitors">
  </a>
</p>

<p align="center">
  <a href="https://ko-fi.com/lululla">
    <img src="https://img.shields.io/badge/_-Donate-red.svg?logo=githubsponsors&labelColor=555555&style=for-the-badge" alt="Ko-fi">
  </a>

  <a href="https://paypal.me/belfagor2005">
    <img src="https://img.shields.io/badge/_-Donate-green.svg?logo=githubsponsors&labelColor=555555&style=for-the-badge" alt="PayPal">
  </a>
</p>

**Advanced movie and series management plugin for Enigma2-based set-top boxes**  
*Forked from @kashmir's original work, completely rewritten for modern APIs*

---

## 📺 Screenshots

<table>
  <tr>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Belfagor2005/MovieBrowser/main/screenshot/screenmovie1.png" height="220">
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Belfagor2005/MovieBrowser/main/screenshot/screenmovie2.png" height="220">
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Belfagor2005/MovieBrowser/main/screenshot/screenmovie3.png" height="220">
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Belfagor2005/MovieBrowser/main/screenshot/screenmovie4.png" height="220">
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Belfagor2005/MovieBrowser/main/screenshot/screenmovie5.png" height="220">
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Belfagor2005/MovieBrowser/main/screenshot/screenmovie6.png" height="220">
    </td>
  </tr>
</table>


---


## 📋 Table of Contents
- [✨ Features](#-features)
- [📦 Installation](#-installation)
- [⚙️ Configuration](#️-configuration)
- [🎨 Skins & Layouts](#-skins--layouts)
- [🔧 API Integration](#-api-integration)
- [🐛 Troubleshooting](#-troubleshooting)
- [📁 Project Structure](#-project-structure)
- [🔑 API Keys Setup](#-api-keys-setup)
- [📜 Changelog v4.3](#-changelog-v43)
- [📜 Changelog v4.2](#-changelog-v42)
- [📜 Development History](#-development-history)
- [🤝 Contributing](#-contributing)

---

## ✨ Features

### 🗄️ **Database Management**
- **SQLite database** with optimized queries and indexes
- **Automatic metadata scraping** from TMDb (movies and series)
- **Multi-filter system** (genre, actor, director, folder)
- **Watch status tracking** and blacklist management

### 🖼️ **Visual Experience**
- **Dual skin support**: HD (1280x720) and FHD (1920x1080)
- **Dynamic poster display** with 4-panel preview
- **Horizontal banner support** for TV series
- **Rating bars** with visual progress indicators
- **Multi-language UI** (Italian, German, Dutch, Chinese included)

### 🔄 **Media Integration**
- **TMDb API v3** integration for movie and series metadata and covers
- **TMDb-only metadata** for movies and TV series; TheTVDb integration has been removed
- **Smart image caching** system
- **Automatic backdrop and poster downloading**

### ⌨️ **Keyboard Shortcuts**

| Key | Function | Description |
|-----|----------|-------------|
| **Info** | Toggle Info | Show/hide detailed information |
| **Video** | Update DB | Refresh database from sources |
| **Text** | Edit DB | Open database editor |
| **Stop** | Mark Seen | Mark movie as watched |
| **Radio** | Delete | Remove/blacklist movie |
| **← →** | First Letter | Jump to alphabetical section |
| **1** | Cut Editor | Open CutListEditor/MovieCut |
| **2** | TMDb Update | Refresh metadata from TMDb |
| **3** | Reserved | No function assigned |
| **4** | Hide Seen | Toggle watched movies visibility |
| **5** | View Toggle | Switch Movies/Series view |
| **6** | Folder Select | Movie folder selection |
| **7** | Director Select | Filter by director |
| **8** | Actor Select | Filter by actor |
| **9** | Genre Select | Filter by genre |
| **0** | End of List | Jump to last item |

---

## 📦 Installation

### **Method 1: IPK Package (Recommended)**
```bash
# Download latest release
wget -q --no-check-certificate https://raw.githubusercontent.com/Belfagor2005/MovieBrowser/main/installer.sh -O - | /bin/sh

# Install on Enigma2
opkg enigma2-plugin-extensions-moviebrowser

# Restart GUI
init 4 && init 3
```

### **Method 2: Manual Installation**
```bash
# Clone repository
git clone https://github.com/Belfagor2005/MovieBrowser.git

# Copy to plugins directory
cp -r MovieBrowser /usr/lib/enigma2/python/Plugins/Extensions/

# Set permissions
chmod 755 /usr/lib/enigma2/python/Plugins/Extensions/MovieBrowser/plugin.py

# Restart Enigma2
reboot
```

### **Method 3: Plugin Browser**
1. Navigate to: **Menu → Plugins → Download Plugins**
2. Search for "MovieBrowser"
3. Select and install
4. Restart your receiver

---

## ⚙️ Configuration

### **First Run Setup**
1. Access plugin via: **Plugins → MovieBrowser**
2. Configure your movie directories in settings
3. Set up API keys for full functionality (optional)

### **Directory Structure**
The plugin automatically scans these default directories:
```
/movie/                   # Primary movie location
/media/hdd/movie/         # HDD storage
/media/usb/movie/         # USB drives
```

---

## 🎨 Skins & Layouts

### **HD Skin (1280x720)**
- **Location**: `/usr/lib/enigma2/python/Plugins/Extensions/MovieBrowser/skin/hd/`
- **Layout**: Optimized for standard HD displays
- **Features**: Compact view, smaller icons, efficient space usage

### **FHD Skin (1920x1080)**
- **Location**: `/usr/lib/enigma2/python/Plugins/Extensions/MovieBrowser/skin/fhd/`
- **Layout**: Full HD with larger posters and banners
- **Features**: Enhanced visuals, better spacing, modern look

### **Custom Skins**
Create your own skin by duplicating an existing one and modifying:
- XML layout files in `skin/[resolution]/default/`
- Images in `skin/[resolution]/pic/`

---

## 🔧 API Integration

### **TMDb Integration**
MovieBrowser uses TMDb for movie and TV series metadata, including:
- Movie and series details
- Posters, backdrops and banners
- Search and Discover results

TheTVDb integration and its leftover code have been removed. Configure your TMDb API key in the plugin's settings or in the relevant configuration location used by your installation.

---


## 🐛 Troubleshooting

### **Common Issues & Solutions**

#### **1. Banners Not Displaying**
```log
# Check logs for:
tail -f /tmp/enigma2.log | grep -i banner

# Solutions:
# 1. Verify API keys in library.py
# 2. Check internet connectivity
# 3. Clear cache: rm -rf /tmp/moviebrowser*.jpg
```

#### **2. Database Errors**
```bash
# Recreate database:
rm ~/.moviebrowser/moviebrowser.db
# Restart plugin
```

#### **3. Missing Fonts Error**
```log
[eListboxPythonMultiContent] specified font XX was not found!
```
**Fix**: Edit `plugin.py` and change font IDs to `font=0` (default font)

#### **4. Slow Performance**
```bash
# Optimize database:
sqlite3 ~/.moviebrowser/moviebrowser.db "VACUUM; REINDEX;"
```

---

## 📁 Project Structure

```
MovieBrowser/
├── plugin.py              # Main plugin entry point
├── library.py             # TMDb API integration
├── movie_config.py        # Configuration handling
├── __init__.py            # Package initialization
│
├── db/                    # Database files
│   ├── cache/             # Image cache (backdrops, posters)
│   │   ├── default_backdrop.m1v
│   │   ├── default_backdrop.png
│   │   └── ...
│   ├── filter             # Saved filters
│   └── last               # Last session data
│
├── locale/                # Internationalization
│   ├── it/LC_MESSAGES/    # Italian translations
│   ├── de/LC_MESSAGES/    # German translations
│   └── cn/LC_MESSAGES/    # Chinese translations
│
├── log/                   # Log files
│   ├── cleanup.log
│   ├── timer.log
│   └── update.log
│
└── skin/                  # UI Skins
    ├── fhd/               # Full HD (1920x1080)
    │   ├── default/       # XML layout files
    │   └── pic/           # Images and icons
    └── hd/                # HD (1280x720)
        ├── default/
        └── pic/
```

---

## 🔑 API Keys Setup

### **1. Get Your TMDb API Key**
- **TMDb:** https://www.themoviedb.org/settings/api

### **2. Configure the API Key**
Follow the plugin configuration and enter your TMDb API key where requested. Do not publish your personal API key in screenshots, logs or public commits.

### **3. Test API Connectivity**
```bash
curl "https://api.themoviedb.org/3/movie/550?api_key=YOUR_TMDB_API_KEY"
```

---

## 📜 Changelog v4.4

### **Fixed**
- Development and fix alignment


## 📜 Changelog v4.3

### **Added**
- Added TMDb Discover integration for movies and TV series.
- Added automatic update functionality.
- Added additional language support.
- Added optional background overlay for Discover screens:
  - Off
  - Light
  - Medium
  - Dark

### **Improved**
- Improved visual text presentation.
- Cleaned up the codebase and removed remaining TheTVDb references.

### **Fixed**
- Fixed database reset functionality.

---

## 📜 Changelog v4.2

### **Fixes (November 2026)**
- **Series metadata:** series information and covers are now retrieved from TMDb; TheTVDb API integration has been removed.
- **Library scan:** fixed filename recognition to prevent movies from being added as duplicates on every scan.
- **TMDb search:** fixed title filtering that truncated movie names after the first word.
- **Media and blacklist:** fixed background/default poster loading and blacklist reading errors.
- **Series information:** fixed missing information in series views.
- **Movie player:** the player can now also be closed with the EXIT button.

### **UI and Translations**
- Added a new `plugin.png` logo.
- Added a new movie selection frame.
- Updated German (DE), Italian (IT) and Dutch (NL) translations.

---

## 📜 Changelog v4.0

### **Major Improvements**
- Reworked the screen layouts and interface.
- Reworked the database implementation.
- Updated source code and API URLs.
- Separated libraries into dedicated modules.
- Introduced the new API v4 integration.
- Removed unused and unnecessary code.

### **UI/UX**
- Fixed the MovieList banner display.

---

## 📜 Development History

### **2025-12-02 — Lululla**
- Completely recoded MovieBrowser.
- Reworked screen layouts and source code.
- Updated API URLs.
- Separated libraries into dedicated modules.
- Rewrote the database code.
- Removed unused code.
- Introduced the new API v4.

### **2025-05-16 — Lululla**
- Refactored all classes.
- Removed unnecessary code throughout the plugin.

### **2024-09-20 — Lululla**
- Recoded and cleaned up the plugin.
- Removed unnecessary code.

### **2022-12-22 — Lululla**
- Major code rewrite and fixes.

### **2022-12-08 — Lululla**
- Added `callInThread`.
- Added `getMountDefault`.

### **2022-12-04 — Lululla**
- Added language support.
- Improved configuration.
- Applied major fixes.

### **2022-10-04 — Kiddac**
- Added Python 3 support.
- Applied additional code improvements.

---

## 🤝 Contributing

### **Development Setup**
```bash
# 1. Fork the repository
# 2. Clone your fork
git clone https://github.com/Belfagor2005/MovieBrowser.git

# 3. Create feature branch
git checkout -b feature/amazing-feature

# 4. Test changes on Enigma2
# 5. Commit and push
git commit -m "Add amazing feature"
git push origin feature/amazing-feature

# 6. Create Pull Request
```

### **Coding Standards**
- Follow existing Python style (PEP 8 inspired)
- Maintain compatibility with the Python version supported by the target Enigma2 image
- Add comments for complex logic
- Update documentation for new features

### **Testing**
- Test on both HD and FHD resolutions
- Verify with and without API keys
- Check database migration scenarios

---

## 📞 Support

- **GitHub Issues**: [Report Bugs](https://github.com/Belfagor2005/MovieBrowser/issues)
- **Documentation**: [Wiki](https://github.com/Belfagor2005/MovieBrowser/wiki)
- **Releases**: [Download Latest](https://github.com/Belfagor2005/MovieBrowser/releases)

---

## 📄 License

This project is licensed under the **GNU General Public License v3.0** - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Original plugin by **@kashmir**
- Last mod rewrite from Lululla
- TMDb for their excellent API
- Open Source community for continuous support

---

**⭐ Star this repository if you find it useful!**  
**🐛 Found a bug? Please open an issue!**  
**💡 Have a suggestion? We'd love to hear it!**

---

*Last Updated: November 2026 | Version: 4.3*
