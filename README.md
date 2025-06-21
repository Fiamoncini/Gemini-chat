# Gemini Chat

A clean, modern web-based chat interface for Google's Gemini AI model. This single-page application provides a responsive chat experience with a beautiful UI design.


![image](https://github.com/user-attachments/assets/c38ab4da-b39a-4d76-b6d4-f60f7be31bc7)


## Features

- 🤖 **Direct Gemini AI Integration** - Uses Google's Gemini 2.0 Flash model
- 💬 **Real-time Chat Interface** - Smooth messaging experience with typing indicators
- 📱 **Responsive Design** - Works perfectly on desktop and mobile devices
- ✨ **Modern UI** - Clean, professional design with smooth animations
- ⌨️ **Keyboard Shortcuts** - Send messages with Enter key
- 🎨 **Custom Styling** - Beautiful color scheme with green accents
- 📝 **Auto-resize Input** - Text area automatically adjusts to content

## Screenshots

The interface features:
- A centered chat container with rounded corners and shadow
- Green header with "Chat with Gemini" title
- User messages appear on the right in green bubbles
- AI responses appear on the left in gray bubbles
- Typing indicator with animated dots
- Responsive input area with send button

## Setup

### Prerequisites

- A Google AI API key for Gemini
- A web browser
- A web server (optional, for local development)

### Installation

1. **Get your API key**
   - Visit [Google AI Studio](https://aistudio.google.com/)
   - Create a new API key for Gemini

2. **Configure the application**
   - Open the HTML file in a text editor
   - Find the line: `const API_URL = \`https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=API_KEY\`;`
   - Replace `API_KEY` with your actual Google AI API key

3. **Run the application**
   - **Option A**: Open the HTML file directly in your browser
   - **Option B**: Serve it through a local web server:
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Using Node.js
     npx serve .
     
     # Using PHP
     php -S localhost:8000
     ```

## Usage

1. Open the application in your web browser
2. Type your message in the input field at the bottom
3. Press Enter or click the send button (➤)
4. Wait for Gemini's response
5. Continue the conversation!

### Keyboard Shortcuts

- **Enter**: Send message
- **Shift + Enter**: New line in message

## Customization

### Colors
The application uses a green color scheme. To customize:
- Primary green: `#036635`
- Light green for user messages: `#e6f4ea`
- Adjust these values in the CSS section

### Model Configuration
To use a different Gemini model, update the API URL:
```javascript
const API_URL = `https://generativelanguage.googleapis.com/v1beta/models/MODEL_NAME:generateContent?key=API_KEY`;
```

Available models:
- `gemini-2.0-flash` (default)
- `gemini-1.5-pro`
- `gemini-1.5-flash`

## Technical Details

### Architecture
- **Frontend**: Pure HTML, CSS, and JavaScript
- **API**: Google Generative Language API
- **Styling**: Custom CSS with modern design principles
- **Responsive**: Mobile-first design approach

### Browser Compatibility
- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+

### File Structure
```
gemini-chat/
├── index.html          # Main application file
└── README.md          # This file
```

## API Reference

The application uses Google's Generative Language API:

```javascript
// Request format
{
  "contents": [
    {
      "parts": [
        {
          "text": "Your message here"
        }
      ]
    }
  ]
}
```

## Troubleshooting

### Common Issues

**"Hello! Set up your Gemini API key to start chatting."**
- You need to replace `API_KEY` in the code with your actual API key

**"Oops! Something went wrong. Please try again."**
- Check your internet connection
- Verify your API key is correct and has proper permissions
- Check the browser console for detailed error messages

**CORS Errors**
- If running locally, use a web server instead of opening the file directly
- Some browsers block API requests from `file://` URLs

### API Limits
- Free tier has usage limits
- Monitor your usage in Google AI Studio
- Consider implementing rate limiting for production use

## Security Considerations

⚠️ **Important**: This implementation exposes your API key in the client-side code. For production use:

1. Implement a backend proxy to hide your API key
2. Add authentication and authorization
3. Implement rate limiting
4. Add input validation and sanitization

## Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.


## Acknowledgments

- Google for the Gemini AI API
- Inter font family for typography
- Modern CSS techniques for responsive design

---
