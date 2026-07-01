![BlowVPN](https://img.shields.io/badge/BlowVPN-VPN%20Client-blue?style=flat-square)
![Flutter](https://img.shields.io/badge/Flutter-3.0+-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

# BlowVPN - Modern VPN Client

A sleek, minimalist VPN client application built with Flutter, supporting V2Ray, VLESS, and Shadowsocks protocols.

## 🎨 Features

### Core Features
- ✅ **Modern UI** - Dark theme with neon blue/purple accents
- ✅ **One-Tap Connection** - Large animated power button for quick VPN toggle
- ✅ **Multi-Protocol Support** - V2Ray, VLESS, Shadowsocks compatibility
- ✅ **Subscription Management** - Secure storage of VPN subscriptions
- ✅ **Server Monitoring** - Real-time ping checking and server status
- ✅ **Connection Timer** - Track your VPN uptime with live counter
- ✅ **Pull-to-Refresh** - Easy server list refresh with latency updates
- ✅ **Secure Storage** - Encrypted credential storage on device

### UI Components
- Animated power button with pulsing halo effect
- Real-time connection status indicator
- Server list with ping information
- Subscription management interface
- Payment gateway integration (Telegram bot)

## 🚀 Getting Started

### Prerequisites
- Flutter SDK 3.0 or higher
- Dart SDK 3.0 or higher
- Android 8.0+ or iOS 12.0+

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/moovmovvik-dotcom/Blowvpn.git
cd Blowvpn
```

2. **Install dependencies:**
```bash
flutter pub get
```

3. **Run the app:**
```bash
flutter run
```

## 📱 Usage

### Adding a Subscription
1. Tap the **+** tab at the bottom
2. Paste your subscription URL (V2Ray, VLESS, or Shadowsocks format)
3. Tap **Save Subscription**
4. Your servers will be automatically parsed and saved securely

### Connecting to VPN
1. On the home screen, tap the large **power button**
2. The button will animate and the connection status will update
3. The uptime timer will begin counting
4. Your connection status is displayed above the button

### Checking Server Status
1. Tap the **🔄** tab to view all available servers
2. Pull down to refresh ping times
3. Servers show real-time latency information

### Managing Subscription
1. Tap the **🔤** tab (Payment)
2. Tap **Open Payment Bot** to manage your subscription in Telegram

## 🛠️ Project Structure

```
lib/
├── main.dart                      # App entry point
├── theme/
│   └── app_theme.dart             # Design system & colors
├── models/
│   ├── vpn_server.dart            # Server data model
│   └── vpn_connection.dart        # Connection status model
├── providers/
│   ├── vpn_provider.dart          # VPN state management
│   └── server_provider.dart       # Server & subscription management
├── services/
│   ├── subscription_parser.dart   # Parse V2Ray/VLESS/SS configs
│   └── ping_service.dart          # Server latency checking
├── screens/
│   ├── home_screen.dart           # Main home screen
│   ├── add_key_screen.dart        # Subscription input
│   ├── servers_screen.dart        # Server list view
│   └── payment_screen.dart        # Subscription management
└── widgets/
    ├── power_button.dart          # Animated power button
    ├── vpn_status_widget.dart     # Connection status badge
    └── server_list_tile.dart      # Server list item
```

## 🔐 Security Features

- **Secure Storage**: All VPN subscriptions are encrypted using platform-specific secure storage
  - iOS: Keychain
  - Android: EncryptedSharedPreferences
- **No Logging**: Connection data is never logged to disk
- **Certificate Pinning**: Ready for implementation with custom certificate handling

## 🎨 Design

### Color Palette
- **Primary Black**: #0A0E27
- **Dark Navy**: #1A1F3A
- **Neon Blue**: #00D9FF
- **Neon Purple**: #9D4EDD
- **Success Green**: #06D6A0
- **Error Red**: #FF006E

### Animations
- Smooth power button state transitions (300ms)
- Pulsing halo effect on active connection
- Animated connection status badge
- Gradient overlays for visual depth

## 📦 Dependencies

### Core
- `flutter`: UI framework
- `provider`: State management

### Networking & Parsing
- `dio`: HTTP client
- `http`: HTTP requests
- `url_launcher`: Open external URLs

### Security & Storage
- `flutter_secure_storage`: Encrypted credential storage
- `shared_preferences`: App preferences

### UI & Animation
- `flutter_animate`: Animation utilities
- `lottie`: Lottie animation support

### Utilities
- `uuid`: Generate unique identifiers
- `connectivity_plus`: Check network connectivity
- `intl`: Internationalization support

## 🔌 Protocol Support

### VLESS (v2ray)
Format: `vless://uuid@host:port?encryption=none&security=tls#name`

### VMESS (v2ray)
Format: `vmess://base64-encoded-json`

### Shadowsocks
Format: `ss://method:password@host:port#name`

## 🚧 Roadmap

- [ ] V2Ray core integration for actual VPN connection
- [ ] OpenVPN protocol support
- [ ] WireGuard protocol support
- [ ] Advanced server filtering and sorting
- [ ] Connection speed testing
- [ ] Split tunneling support
- [ ] Kill switch feature
- [ ] Auto-connect on app launch
- [ ] Dark/Light theme toggle
- [ ] Multi-language support

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs and feature requests.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

This VPN client is provided "as is" for educational and privacy purposes. Users are responsible for ensuring their use complies with local laws and regulations. The developers are not responsible for misuse of this software.

## 📧 Contact

- **GitHub**: [@moovmovvik-dotcom](https://github.com/moovmovvik-dotcom)
- **Support**: Check GitHub Issues for support

---

Built with ❤️ using Flutter
