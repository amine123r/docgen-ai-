# DocGen AI Extension - Tech Stack & Dependencies

## Core Technologies
- **Chrome Extension Manifest V3** - Latest Chrome extension framework
- **Vanilla JavaScript (ES6+)** - No frameworks, pure JS for performance
- **HTML5 & CSS3** - Standard web technologies
- **Chrome APIs** - Built-in browser capabilities

## External Libraries & Versions

### Code Analysis
- **@babel/parser v7.23.0** - Parse JavaScript/TypeScript code
- **acorn v8.11.0** - Lightweight JavaScript parser (fallback)
- **tree-sitter-web v0.20.8** - Universal code parsing (advanced features)

### AI Integration
- **Google Generative AI REST API** - Direct HTTP calls (no SDK needed)
- **Fetch API** - Native browser HTTP client

### File Processing
- **marked v9.1.6** - Markdown parsing and generation
- **jszip v3.10.1** - Handle ZIP files from GitHub
- **prettier v3.1.0** - Code formatting

### GitHub Integration
- **GitHub REST API v4** - Repository access via HTTP
- **No external SDK** - Direct API calls

### UI Components
- **Tailwind CSS v3.3.6** - Utility-first CSS (CDN)
- **Lucide Icons v0.294.0** - Icon library (CDN)

### Storage & Utilities
- **Chrome Storage API** - Built-in extension storage
- **Chrome Tabs API** - Built-in tab management
- **IndexedDB** - Native browser database

## Development Tools
- **No build process** - Direct file loading for prototype
- **Chrome DevTools** - Built-in debugging
- **VS Code** - Development environment

## API Dependencies
- **Gemini API** - Your existing key (AIzaSyA5E8sRx9x2Y4L4ZUk8nfXsOmG_QXUjHIE)
- **GitHub API** - Public repositories (no auth needed for public repos)

## File Structure
```
documate-extension/
├── manifest.json          # Extension configuration
├── popup.html            # Extension popup UI
├── popup.js              # Popup functionality
├── content.js            # GitHub page integration
├── background.js         # Background processes
├── styles.css            # Custom styles
├── icons/                # Extension icons
└── lib/                  # External libraries (if needed)
```

## Size Estimate
- **Total extension size**: ~2-3 MB
- **Core files**: ~500 KB
- **Libraries**: ~1.5-2 MB
- **Icons**: ~100 KB

## Browser Compatibility
- **Chrome 88+** (Manifest V3 support)
- **Edge 88+** (Chromium-based)
- **Opera 74+** (Chromium-based)

## Offline Capabilities
- **Code analysis**: Works offline
- **Documentation generation**: Requires internet (AI API)
- **File processing**: Works offline
- **GitHub integration**: Requires internet

## Security Considerations
- **API key storage**: Chrome storage (encrypted)
- **Permissions**: Minimal required permissions
- **Content Security Policy**: Strict CSP in manifest
- **No eval()**: Safe code execution only

## Performance Targets
- **Startup time**: <500ms
- **Code analysis**: <2s for typical repo
- **Documentation generation**: 5-15s (depends on AI API)
- **Memory usage**: <50MB

## Fallback Strategies
- **AI API failure**: Use cached templates
- **GitHub API limits**: Parse visible code only
- **Large repositories**: Process in chunks
- **Network issues**: Offline mode with basic features