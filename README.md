# Interview FAQ Chat Assistant

A modern, responsive chat interface powered by n8n workflow automation and RAG (Retrieval-Augmented Generation) AI technology.

## Features

- 🤖 AI-powered interview question answering
- 💬 Real-time chat interface
- 📱 Responsive design for all devices
- ⚡ Fast webhook-based communication
- 🎨 Modern gradient UI design
- 💾 Session persistence
- ⚡ Fast and lightweight
- 🔄 Auto-retry on network failures
- 💾 Session management

## Setup

1. **Fork this repository** to your GitHub account

2. **Update the webhook URL** in `script.js`:
   ```javascript
   const CONFIG = {
       WEBHOOK_URL: 'https://your-n8n-instance.com/webhook/your-webhook-id/chat',
       // ... other config
   };
   ```

3. **Enable GitHub Pages**:
   - Go to your repository settings
   - Scroll down to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

4. **Your chat will be available at**: `https://yourusername.github.io/your-repo-name`

## n8n Webhook Setup

Your n8n webhook should:

1. **Accept POST requests** with JSON payload:
   ```json
   {
     "message": "User's message",
     "timestamp": "2024-01-01T00:00:00.000Z",
     "sessionId": "session_12345"
   }
   ```

2. **Return JSON response** in one of these formats:
   ```json
   { "response": "AI response text" }
   ```
   or
   ```json
   { "message": "AI response text" }
   ```
   or just a plain string

## Customization

### Styling
Edit `styles.css` to customize:
- Colors and gradients
- Fonts and typography
- Layout and spacing
- Animations

### Functionality
Edit `script.js` to customize:
- Webhook URL and payload format
- Response handling
- Error messages
- Retry logic

### Content
Edit `index.html` to customize:
- Page title and meta tags
- Header content
- Initial bot message

## File Structure

```
.
├── index.html          # Main HTML structure
├── styles.css          # Styling and responsive design
├── script.js           # Chat functionality and n8n integration
├── sw.js              # Service worker for offline support
└── README.md          # This file
```

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License - feel free to use this for your projects!

## Support

If you encounter any issues:
1. Check the browser console for errors
2. Verify your n8n webhook is working
3. Test the webhook URL directly
4. Check CORS settings on your n8n instance
