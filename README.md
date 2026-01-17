# AniList Minimal

A lightweight, single-page web application for managing your AniList anime collection. This minimalist frontend provides a clean and fast interface to view, search, add, and update your anime list entries.

## ✨ Features

- **Simple Authentication**: Log in with your AniList access token
- **List Management**: View and organize your anime across different statuses
  - Currently Watching (including Rewatching)
  - Completed
  - Planning
  - On Hold
  - Dropped
- **Search & Add**: Quickly search and add new anime to your list
- **Progress Tracking**: Increment episode progress with a single click
- **Detailed Editing**: Update status, progress, score, rewatches, and dates
- **Smart Caching**: Local caching for fast load times (4-hour cache expiration)
- **Optimistic UI Updates**: Instant feedback with background API synchronization
- **Responsive Design**: Mobile-friendly interface with adaptive layouts
- **Dark Theme**: Easy on the eyes with a modern dark color scheme

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- An AniList account
- An AniList API access token

### Getting Your Access Token

1. Go to [AniList Settings - Developer](https://anilist.co/settings/developer)
2. Create a new API Client if you haven't already
3. Click on your client to view details
4. Copy your Access Token

### Installation

This is a static single-page application. You can run it in several ways:

#### Option 1: Open Directly
Simply open `index.html` in your web browser.

#### Option 2: Local Server (Recommended)
Using Python:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000`

Using Node.js (npx):
```bash
npx serve
```

#### Option 3: Deploy to Static Hosting
Deploy the `index.html` file to any static hosting service:
- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages

### Usage

1. **Login**: Paste your AniList access token on the login screen
2. **Browse**: View your anime list organized by status tabs
3. **Quick Update**: Click the `+` button next to any anime to increment progress
4. **Edit Details**: Click on any anime entry to open the detailed editor
5. **Add Anime**: Click the `+ Add` button to search and add new anime
6. **Refresh**: Click the sync button to refresh your list from AniList

## 🛠️ Technical Details

### Technologies Used

- **Pure HTML/CSS/JavaScript**: No build process or dependencies required
- **Tailwind CSS**: Loaded via CDN for styling
- **AniList GraphQL API**: For all data operations
- **LocalStorage**: For caching and token storage

### Architecture

- Single HTML file with embedded CSS and JavaScript
- Client-side only - no backend required
- GraphQL queries for efficient data fetching
- Optimistic UI updates for instant feedback
- Smart caching strategy with 4-hour expiration

### API Integration

The app integrates with the AniList GraphQL API (`https://graphql.anilist.co`) to:
- Fetch user's anime list
- Search for anime
- Add anime to list
- Update anime entries (progress, status, score, dates)
- Delete anime from list

### Caching Strategy

- Full anime list is cached locally for 4 hours (240 minutes)
- Cache is versioned (`cache_v4_full_list`)
- Manual refresh available via sync button
- Optimistic updates for immediate UI feedback

## 📱 Mobile Support

The interface is fully responsive with mobile-specific optimizations:
- Tab icons-only view on small screens to prevent horizontal scrolling
- Adaptive modal layouts for smaller screens
- Touch-friendly buttons and controls

## 🎨 Customization

The app uses CSS custom properties and can be easily customized by modifying the `<style>` section in `index.html`:

- **Colors**: Change `background-color` and color values
- **Fonts**: Update the Google Fonts import and `font-family`
- **Animations**: Adjust animation timings and effects
- **Layout**: Modify Tailwind classes for different layouts

## 🔒 Privacy & Security

- Your access token is stored locally in your browser's LocalStorage
- No data is sent to any third-party servers (except AniList API)
- All communication is done directly between your browser and AniList
- Click "Logout" to clear all stored data including your token

## 📄 License

This project is provided as-is for personal use.

## 🙏 Acknowledgments

- [AniList](https://anilist.co/) for providing the excellent GraphQL API
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS framework
- [Feather Icons](https://feathericons.com/) for the SVG icons (embedded)

## 🤝 Contributing

This is a minimal project, but contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests

## 📞 Support

If you encounter any issues:
1. Check that your AniList access token is valid
2. Ensure you have a stable internet connection
3. Try clearing your browser's cache and localStorage
4. Check the browser console for error messages

---

Made with ❤️ for the AniList community
