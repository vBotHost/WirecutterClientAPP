# WireCutter - SCUM Server Management Bot

<div align="center">
  <img src="/assets/images/logo/wire_cutter_logo_V.png" alt="WireCutter Logo" width="200"/>

  [![Version](https://img.shields.io/badge/version-1.5.0-blue.svg)]
  [![Flutter](https://img.shields.io/badge/Flutter-3.0+-02569B.svg?logo=flutter)](https://flutter.dev)
  [![License](https://img.shields.io/badge/license-Proprietary-red.svg)](LICENSE)
  [![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Android%20%7C%20iOS%20%7C%20macOS-lightgrey.svg)]
</div>

## 📋 Overview

WireCutter is a comprehensive server management application designed for SCUM game servers. It provides real-time monitoring, player management, automated tasks, and advanced administrative features through an intuitive cross-platform interface.

## ✨ Key Features

### 🎮 Server Management
- **Real-time Server Monitoring** - Track server status, player count, and performance metrics
- **Multi-Server Support** - Manage multiple SCUM servers from a single interface
- **Server Configuration** - Adjust server settings and parameters remotely
- **Automated Restart Scheduling** - Schedule server restarts and maintenance windows

### 👥 Player Management
- **Player Information Dashboard** - View detailed player statistics and activity
- **Squad Management** - Create, manage, and monitor player squads
- **Player Permissions** - Granular control over player permissions and roles
- **Ban/Kick Management** - Administrative actions with logging and history

### 📦 Item & Economy Management
- **Item Pack System** - Create and distribute custom item packs to players
- **Market System** - In-game economy management with trading capabilities
- **Stock Management** - Monitor and control item availability and distribution
- **Vehicle Management** - Track and manage in-game vehicles

### 🔐 Security Features
- **Bunker Lock Management** - Control access to bunkers and secure areas
- **Region-based Permissions** - Set area-specific rules and restrictions
- **Secure Authentication** - Steam OpenID integration for secure login
- **Encrypted Communications** - All server communications are encrypted

### 📊 Administrative Tools
- **Real-time Event Stream** - Monitor server events and player actions in real-time
- **Scheduled Tasks** - Automate routine server tasks and maintenance
- **IGC (In-Game Currency) Control** - Manage server economy and currency
- **Advanced Analytics** - Detailed charts and statistics for server performance

### 🌐 Cross-Platform Support
- **Windows Desktop** - Native Windows application with full feature set
- **Android Mobile** - Monitor and manage servers on the go
- **iOS Mobile** - Full-featured iOS application
- **macOS Desktop** - Native macOS support

## 🚀 Getting Started

### Prerequisites

- Flutter SDK 3.0 or higher
- Dart SDK
- For Windows: Visual Studio with C++ development tools
- For mobile: Android Studio / Xcode
- SCUM game server with administrative access

### Installation

#### For End Users (Pre-built Release)

1. Download the latest release for your platform from the [Releases](https://github.com/yourusername/wirecutter/releases) page
2. **Windows**: Run the `.msix` installer
3. **Android**: Install the `.apk` file
4. **iOS**: Install via TestFlight or App Store
5. **macOS**: Open the `.dmg` file and drag to Applications

#### For Developers (Building from Source)

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/wirecutter.git
cd wirecutter_client
```

2. **Install dependencies**
```bash
flutter pub get
```

3. **Set up environment variables**
Create a `.env` file in the root directory with your configuration:
```env
API_BASE_URL=your_server_api_url
STEAM_API_KEY=your_steam_api_key
CERT_PASSWORD=your_certificate_password
```

4. **Generate code (for Hive adapters)**
```bash
flutter pub run build_runner build
```

5. **Run the application**
```bash
# For development
flutter run

# For specific platform
flutter run -d windows
flutter run -d chrome
flutter run -d android
```

### Building for Production

#### Windows
```bash
# Build MSIX package for Windows Store
dart run msix:create --store

# Build standard MSIX package
dart run msix:create
```

#### Android
```bash
flutter build apk --release
# or for App Bundle
flutter build appbundle --release
```

#### iOS
```bash
flutter build ios --release
# Then open in Xcode for signing
open ios/Runner.xcworkspace
```

#### macOS
```bash
flutter build macos --release
# Sign the app (replace with your certificate hash)
codesign --deep --force --verbose --sign "YOUR_CERT_HASH" build/macos/Build/Products/Release/wirecutter.app
```

## 📱 Features in Detail

### Dashboard
The main dashboard provides an at-a-glance view of:
- Server status and health
- Active player count
- Recent events and alerts
- Quick access to common tasks

### Admin Stream
Real-time event monitoring system that displays:
- Player connections/disconnections
- In-game events and actions
- System notifications
- Administrative action logs

### Player Management
Comprehensive player management interface:
- Search and filter players
- View detailed player profiles
- Manage player permissions
- Track player activity history

### Pack Service
Item distribution system allowing:
- Creation of custom item packs
- Category-based organization
- Scheduled distribution
- Player-specific allocations

### Market System
In-game economy management:
- Item pricing controls
- Supply and demand tracking
- Trade history and analytics
- Market manipulation prevention

## 🔧 Configuration

### Server Connection
1. Launch WireCutter
2. Navigate to Settings
3. Enter your server details:
   - Server IP/Domain
   - API Port
   - Authentication credentials
4. Test connection
5. Save configuration

### Permissions Setup
WireCutter uses a role-based permission system:
- **Super Admin**: Full system access
- **Server Admin**: Server-specific management
- **Moderator**: Limited administrative functions
- **Player**: Basic viewing permissions

## 🛡️ Security

WireCutter implements multiple security layers:
- **End-to-end encryption** for all communications
- **Steam OpenID** authentication
- **JWT token-based** session management
- **Rate limiting** on API endpoints
- **Audit logging** for all administrative actions

## 📊 System Requirements

### Minimum Requirements
- **OS**: Windows 10 / Android 6.0 / iOS 12.0 / macOS 10.14
- **RAM**: 2GB
- **Storage**: 200MB
- **Network**: Stable internet connection

### Recommended Requirements
- **OS**: Windows 11 / Android 10+ / iOS 15+ / macOS 12+
- **RAM**: 4GB+
- **Storage**: 500MB
- **Network**: Broadband connection

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is proprietary software. All rights reserved by Codenfast.

## 🆘 Support

For support, please:
- Check the [Wiki](https://github.com/yourusername/wirecutter/wiki) for documentation
- Search existing [Issues](https://github.com/yourusername/wirecutter/issues)
- Join our [Discord Server](https://discord.gg/yourserver)
- Contact support at support@codenfast.com

## 🙏 Acknowledgments

- SCUM game developers for providing server management APIs
- Flutter team for the excellent cross-platform framework
- All contributors and beta testers
- The SCUM server admin community

## 📸 Screenshots

<div align="center">
  <img src="docs/screenshots/dashboard.png" alt="Dashboard" width="400"/>
  <img src="docs/screenshots/player_management.png" alt="Player Management" width="400"/>
  <img src="docs/screenshots/admin_stream.png" alt="Admin Stream" width="400"/>
  <img src="docs/screenshots/pack_service.png" alt="Pack Service" width="400"/>
</div>

## 🗺️ Roadmap

- [ ] Linux desktop support
- [ ] Web-based admin panel
- [ ] Advanced automation scripting
- [ ] Machine learning-based player behavior analysis
- [ ] Multi-language support expansion
- [ ] Plugin system for custom extensions
- [ ] Advanced backup and restore functionality
- [ ] Integration with Discord bots

## ⚡ Performance

WireCutter is optimized for performance:
- **Efficient data caching** reduces API calls
- **Lazy loading** for improved startup time
- **Background task processing** keeps UI responsive
- **WebSocket connections** for real-time updates
- **Compressed data transfer** minimizes bandwidth usage

---

<div align="center">
  Made with ❤️ by Codenfast Team

  [Website](https://codenfast.com) • [Documentation](https://docs.codenfast.com/wirecutter) • [Support](https://support.codenfast.com)
</div>