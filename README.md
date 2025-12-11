# Kutti AI

A beautiful, voice-first personal finance assistant built with React, TypeScript, and modern web APIs. Quickly add expenses and income with natural voice commands or shorthand text parsing. Features a stunning light-wave UI, INR-formatted ledger, and seamless Excel export.

## Features

✅ **Voice Quick-Add**: Simply speak "add expense 250 lunch" or "income 50000 salary" ✅ **Text Parsing**: Use shortcuts like "-250 lunch" for quick entry ✅ **Light-Wave Avatar**: Animated avatar with ripple effect when listening ✅ **INR Formatting**: All currency values displayed in Indian Rupees (₹) ✅ **Ledger & Dashboard**: Track expenses by category, date, and account ✅ **Excel Export**: Download ledger as .xlsx with proper INR formatting ✅ **Keyboard Shortcuts**: Press Ctrl+K to open Quick-Add, Esc to cancel ✅ **Accessibility**: ARIA labels, keyboard navigation, high-contrast options

## Quick Start

### Prerequisites
- Node.js 16+ and npm

### Installation

```bash
# Clone the repository
git clone https://github.com/ashibabu999-hub/kutti-ai.git
cd kutti-ai

# Install dependencies
npm install

# Start the development server
npm start
```

The app will open at `http://localhost:3000`

## Project Structure

```
kutti-ai/
├── src/
│   ├── components/
│   │   ├── TopBar.tsx
│   │   ├── QuickAdd.tsx
│   │   ├── VoiceModal.tsx
│   │   ├── Ledger.tsx
│   │   ├── Dashboard.tsx
│   │   ├── Avatar.tsx
│   │   └── PermissionModal.tsx
│   ├── hooks/
│   │   ├── useVoiceRecognition.ts
│   │   ├── useLedger.ts
│   │   └── useParser.ts
│   ├── utils/
│   │   ├── parser.ts
│   │   ├── excelExport.ts
│   │   └── formatters.ts
│   ├── types/
│   │   └── index.ts
│   ├── App.tsx
│   ├── App.css
│   └── index.tsx
├── public/
├── package.json
├── tsconfig.json
└── README.md
```

## Architecture

### State Management
Uses React hooks (useState, useContext) for ledger data, voice state, and UI modals.

### Voice Recognition
Integrates Web Speech API for real-time transcription with fallback to text input.

### Data Persistence
LocalStorage for ledger data with optional OneDrive sync using Microsoft Graph API.

## Usage Examples

### Voice Commands
```
"Add expense 250 lunch"
"Income 50000 salary"
"Add expense 1500 fuel to cash account"
"Delete last entry"
```

### Text Shortcuts
```
-250 lunch
+50000 salary
expense 1500 fuel
income 2000 freelance
```

## Building & Deployment

### Build for production
```bash
npm run build
```

### Deploy to Netlify
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Deploy
netlify deploy --prod --dir=build
```

Or connect your GitHub repo to Netlify for automatic deployments.

## Browser Support
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+

**Note**: Voice recognition requires HTTPS in production.

## Roadmap

- [ ] OneDrive sync for ledger backups
- [ ] Receipt image attachment & OCR
- [ ] Multi-account support with reconciliation
- [ ] Monthly budget tracking and alerts
- [ ] CSV import/export
- [ ] Mobile app (React Native)
- [ ] Dark/Light theme toggle
- [ ] Multi-language support

## Contributing

Pull requests welcome! Please fork the repo and create a branch for your feature.

## License

MIT License - feel free to use this project for personal or commercial purposes.

## Contact

Built with ❤️ by [ashibabu999-hub](https://github.com/ashibabu999-hub)
