# Sumz - AI Article Summarizer

A modern web application that summarizes articles and blogs in seconds using OpenAI's GPT-4 API.

## 🎯 Features

- **Instant Summarization**: Paste any article URL and get a concise AI-powered summary
- **Search History**: Keep track of all previously summarized articles
- **Copy to Clipboard**: Easily copy URLs from your history with one click
- **Remove from History**: Delete individual articles from your history with the × button
- **Clear All**: Remove your entire search history at once
- **Clean UI**: Minimal, distraction-free interface with a white background
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## 🚀 Tech Stack

- **Frontend Framework**: React 18
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **API Integration**: OpenAI GPT-4
- **State Management**: Redux Toolkit
- **HTTP Client**: RTK Query

## 📋 Prerequisites

Before you begin, ensure you have:
- Node.js (v14 or higher)
- npm or yarn
- An OpenAI API key

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd ai_summarizer
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create environment configuration**
   Create a `.env.local` file in the root directory:
   ```bash
   VITE_RAPID_API_KEY=your_openai_api_key_here
   VITE_RAPID_API_HOST=your_api_host_here
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```
   The app will open at `http://localhost:5173`

## 📦 Project Structure

```
ai_summarizer/
├── src/
│   ├── components/
│   │   ├── Demo.jsx          # Main article input and history display
│   │   └── Hero.jsx          # Hero section with title and description
│   ├── services/
│   │   ├── article.js        # RTK Query API configuration
│   │   └── store.js          # Redux store setup
│   ├── assets/
│   │   └── index.js          # Asset imports (icons, images)
│   ├── App.jsx               # Main app component
│   ├── App.css               # App styling
│   ├── main.jsx              # React entry point
│   └── index.css             # Global styles
├── public/                   # Static files
├── package.json              # Dependencies and scripts
├── vite.config.js            # Vite configuration
├── tailwind.config.js        # Tailwind CSS configuration
└── eslint.config.js          # ESLint configuration
```

## 🎨 Features Breakdown

### Article Input
- Enter any valid URL in the search field
- Click the submit button (↵) or press Enter to summarize
- Loading spinner appears while fetching the summary

### Search History
- All summarized articles are stored in browser's localStorage
- History persists across browser sessions
- Each history item shows the article URL

### History Actions
- **Copy Icon**: Click to copy the URL to your clipboard
- **× Button**: Click to remove a single article from history
- **Clear History Button**: Click to remove all articles from history

### Summary Display
- Shows the AI-generated summary with the heading "Article Summary"
- Clear and readable formatting
- Error handling with user-friendly messages

## 🔑 Environment Variables

- `VITE_RAPID_API_KEY`: Your RapidAPI key for OpenAI access
- `VITE_RAPID_API_HOST`: The RapidAPI host endpoint

## 🚦 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint

## 📱 How to Use

1. **Summarize an Article**
   - Paste the article URL in the input field
   - Press Enter or click the submit button
   - Wait for the AI to process the article
   - View the summary below

2. **Manage History**
   - Click the copy icon to copy a URL
   - Click the × button to remove an article
   - Click "Clear History" to remove all articles

3. **View Summary**
   - The summary appears below the input field
   - Read and understand the key points instantly

## 🔒 Privacy & Data

- Your search history is stored in your browser's localStorage
- No data is sent to external servers except for the article summarization
- Clear your history anytime with the "Clear History" button

## ⚠️ Error Handling

- Invalid URLs are rejected by the form validation
- API errors are displayed with helpful messages
- Failed requests won't be added to history

## 🎨 Customization

### Styling
- Tailwind CSS classes are used throughout
- Modify `tailwind.config.js` for global color and style changes
- Edit `src/App.css` for component-specific styles

### Colors
- Primary accent: Blue gradient (`blue_gradient` class)
- Background: White
- Text: Various shades of gray and black

## 🐛 Troubleshooting

**Summaries not loading?**
- Check your OpenAI API key is valid
- Verify the article URL is accessible
- Check browser console for error messages

**History not persisting?**
- Check if localStorage is enabled in your browser
- Clear browser cache and try again

**Styling issues?**
- Clear browser cache
- Restart the development server

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

For issues and questions, please open an issue in the repository.

---

**Built with ❤️ using React and OpenAI GPT-4**
