# Spotify Media Player Classic 🎵

> A nostalgic Windows Media Player-inspired desktop application for Spotify, bringing back the classic aesthetic of the early 2000s with modern functionality.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://github.com/username/spotify-2000/workflows/CI/badge.svg)](https://github.com/username/spotify-2000/actions)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)](https://github.com/username/spotify-2000/releases)

## ✨ Features

- 🎨 **Authentic Retro Interface** - Pixel-perfect recreation of Windows Media Player's classic UI
- 🎵 **Full Spotify Integration** - Complete Spotify Web API and Playback SDK integration
- 🎚️ **Classic Controls** - Nostalgic transport controls with authentic styling
- 📊 **Vintage Visualizations** - Oscilloscope, spectrum analyzer, and classic WMP visualizations
- 🎯 **Multiple Themes** - Blue, Silver, Charcoal themes with custom theme support
- ⚡ **High Performance** - Built with Rust and Tauri for minimal resource usage
- 🖥️ **Cross-Platform** - Native support for Windows, macOS, and Linux
- 🔒 **Privacy-First** - Local data storage with optional telemetry

## 🖼️ Screenshots

*Coming soon - authentic Windows Media Player experience awaits!*

## 🛠️ Tech Stack

- **Framework**: [Tauri](https://tauri.app/) (Rust backend + React frontend)
- **Backend**: Rust 1.70+ with async/await
- **Frontend**: React 18+ with TypeScript
- **State Management**: Zustand
- **Styling**: CSS Modules with SCSS
- **Audio**: Web Audio API + Rust audio libraries (rodio, cpal)
- **API**: Spotify Web API with OAuth 2.0 PKCE

## 🚀 Quick Start

### Prerequisites

- [Rust](https://rustup.rs/) 1.70+
- [Node.js](https://nodejs.org/) 18+
- [Spotify Premium Account](https://spotify.com/premium) (required for playback)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/username/spotify-2000.git
   cd spotify-2000
   ```

2. **Install dependencies**
   ```bash
   # Install frontend dependencies
   npm install
   
   # Rust dependencies will be installed automatically
   ```

3. **Set up Spotify API credentials**
   ```bash
   # Copy environment template
   cp .env.example .env
   
   # Edit .env with your Spotify app credentials
   # Get them from: https://developer.spotify.com/dashboard
   ```

4. **Run in development mode**
   ```bash
   npm run tauri dev
   ```

## 🏗️ Development

### Project Structure

```
spotify-2000/
├── src/                    # Frontend source code
│   ├── components/         # React components
│   ├── stores/            # Zustand state management
│   ├── styles/            # SCSS stylesheets
│   └── types/             # TypeScript definitions
├── src-tauri/             # Rust backend source
│   ├── src/               # Rust source code
│   ├── Cargo.toml         # Rust dependencies
│   └── tauri.conf.json    # Tauri configuration
├── public/                # Static assets
└── docs/                  # Documentation
```

### Development Scripts

```bash
# Start development server
npm run tauri dev

# Build for production
npm run tauri build

# Run frontend only (for UI development)
npm run dev

# Run tests
npm test                   # Frontend tests
cargo test                 # Backend tests

# Linting and formatting
npm run lint              # ESLint + Prettier
cargo clippy              # Rust linting
cargo fmt                 # Rust formatting
```

### Setting Up Spotify Development

1. Create a Spotify app at [developer.spotify.com](https://developer.spotify.com/dashboard)
2. Add `http://localhost:8888/callback` as a redirect URI
3. Copy your Client ID to `.env`:
   ```env
   VITE_SPOTIFY_CLIENT_ID=your_client_id_here
   ```

## 📱 Usage

1. **Launch the application**
2. **Login with Spotify** - OAuth 2.0 secure authentication
3. **Choose your theme** - Blue (default), Silver, or Charcoal
4. **Start playing music** - Search, browse playlists, or use Spotify Connect
5. **Customize visualizations** - Choose from classic WMP visualizations
6. **Enjoy the nostalgia** - Experience the early 2000s with modern convenience

## 🎨 Themes & Customization

The application includes authentic Windows Media Player themes:

- **Blue Theme** (Default) - Classic WMP blue gradient
- **Silver Theme** - Windows XP silver styling  
- **Charcoal Theme** - Dark theme with green accents
- **Media Center** - Windows Media Center inspired

Custom themes can be created using JSON configuration files.

## 🧪 Testing

We maintain a comprehensive testing strategy:

- **70% Unit Tests** - Individual component and function testing
- **20% Integration Tests** - Cross-component functionality
- **10% End-to-End Tests** - Complete user workflows

```bash
# Run all tests
npm run test:all

# Run specific test suites
npm test                  # Frontend unit tests
cargo test               # Backend unit tests  
npm run test:e2e         # End-to-end tests
npm run test:performance # Performance benchmarks
```

## 📦 Building & Distribution

### Build for Release

```bash
# Build optimized version for your platform
npm run tauri build

# Cross-platform builds (requires setup)
npm run build:windows
npm run build:macos  
npm run build:linux
```

Binaries will be available in `src-tauri/target/release/bundle/`

### System Requirements

**Minimum:**
- OS: Windows 10, macOS 11, Ubuntu 20.04
- RAM: 512MB available
- Storage: 50MB free space
- Network: Internet connection for Spotify

**Recommended:**
- RAM: 1GB+ available  
- Storage: 500MB free space (for cache)
- Audio: Dedicated audio hardware

## 🤝 Contributing

We welcome contributions! This project is designed to be educational and community-driven.

### Getting Started

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Read the [TDD.md](./TDD.md)** for comprehensive technical details
4. **Follow our coding standards** (detailed in `.cursor/rules/`)
5. **Add tests** for your changes
6. **Update documentation** as needed
7. **Submit a pull request**

### Development Guidelines

- **Rust Code**: Follow the learning-focused standards in our rules
- **React Components**: Use TypeScript strictly with proper interfaces
- **Testing**: Maintain test coverage above 80%
- **Documentation**: Update TDD.md with significant changes
- **Performance**: Keep memory usage under 150MB

### Areas for Contribution

- 🎨 New visualizations and themes
- 🌐 Localization and i18n
- 🚀 Performance optimizations
- 📱 Mobile companion app
- 🔌 Plugin system development
- 📚 Documentation improvements

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Microsoft** - For the original Windows Media Player that inspired this project
- **Spotify** - For their excellent Web API and Playback SDK
- **Tauri Team** - For creating an amazing framework for desktop apps
- **Rust Community** - For building incredible tools and libraries
- **Contributors** - Everyone who helps make this project better

## 📞 Support & Community

- 🐛 **Bug Reports**: [GitHub Issues](https://github.com/username/spotify-2000/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/username/spotify-2000/discussions)
- 📖 **Documentation**: [Project Wiki](https://github.com/username/spotify-2000/wiki)
- 📧 **Contact**: [Email](mailto:contact@example.com)

## 🗺️ Roadmap

### Phase 1: Foundation (Months 1-3) ✅
- [x] Core infrastructure and Tauri setup
- [x] Basic Spotify integration
- [x] Classic UI recreation
- [ ] Audio visualization system
- [ ] Theme system implementation

### Phase 2: Enhancement (Months 4-6)
- [ ] Advanced search and discovery
- [ ] Plugin system architecture  
- [ ] Performance optimizations
- [ ] Cross-platform compatibility

### Phase 3: Community (Months 7+)
- [ ] Mobile companion app
- [ ] Theme marketplace
- [ ] Community features
- [ ] Enterprise features

See [TDD.md](./TDD.md) for detailed technical specifications and implementation timeline.

---

<div align="center">
  
**Bringing back the magic of early 2000s computing** ✨

*Made with ❤️ by the open source community*

</div>