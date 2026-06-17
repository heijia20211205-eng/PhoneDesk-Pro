# PhoneDesk Pro

**Enterprise Android Device Management Platform**

One PC. Control Every Phone.

PhoneDesk Pro is an enterprise-grade Android device management platform.
It enables users to mirror, control and automate multiple Android devices simultaneously from a single desktop.

---

## Key Features

- **Android Screen Mirroring** — Real-time device screen projection
- **Keyboard & Mouse Control** — Direct input to connected devices
- **Multi-device Management** — Simultaneous management of multiple Android devices
- **Multi-screen Workspace** — Organized multi-device grid layout
- **Batch Operations** — Install, record, screenshot across all devices at once
- **File Transfer** — Drag-and-drop file push/pull
- **APK Installation** — Bulk APK deployment
- **Screen Recording** — Per-device or batch recording
- **Screenshot** — Instant screen capture
- **AI Automation** *(Future)* — Intelligent automation workflows

---

## Project Structure

```
PhoneDeskPro/
├── docs/            # Documentation
├── third_party/     # Third-party dependencies
├── resources/       # Resources (icons, styles, etc.)
├── src/             # Source code
│   ├── app/         # Application entry
│   ├── ui/          # UI components
│   ├── core/        # Core abstractions
│   ├── common/      # Common utilities
│   ├── device/      # Device management
│   ├── adb/         # ADB integration
│   ├── screen/      # Screen mirroring
│   ├── control/     # Input control
│   ├── plugin/      # Plugin system
│   ├── config/      # Configuration
│   ├── database/    # Data persistence
│   ├── network/     # Networking
│   ├── ai/          # AI automation
│   ├── ocr/         # OCR engine
│   ├── util/        # Utilities
│   └── sdk/         # Public SDK
├── test/            # Tests
├── installer/       # Installer scripts
└── tools/           # Dev tools
```

---

## Tech Stack

| Category | Choice |
|----------|--------|
| UI Framework | Qt 6.8+ |
| Language | C++20 |
| Build System | CMake |
| Database | SQLite |
| Device Protocol | ADB |
| Screen Mirroring | scrcpy |
| Media | FFmpeg |
| Vision | OpenCV |
| Logging | spdlog |
| JSON | nlohmann/json |

---

## Architecture

```
Application
    └── MainWindow
            ├── DeviceManager
            ├── ADBManager
            ├── ScreenManager
            ├── ControlManager
            ├── PluginManager
            ├── ConfigManager
            └── LogManager
```

---

## UI Layout (V0.1)

```
┌──────────────────────────────────────────┐
│               Menu Bar                   │
├──────────────────────────────────────────┤
│               Toolbar                    │
├───────────────┬──────────────────────────┤
│  Device List  │                          │
│  ───────────  │                          │
│  Pixel 9      │    Device Display Area   │
│  Samsung      │                          │
│  Xiaomi       │                          │
│  OPPO         │                          │
│  Huawei       │                          │
│               │                          │
│               │                          │
│               │                          │
├───────────────┴──────────────────────────┤
│  Status Bar: CPU | FPS | Devices | USB   │
└──────────────────────────────────────────┘
```

---

## Git Workflow

- `main` — Stable releases
- `develop` — Integration branch
- `feature/*` — Feature branches (e.g. `feature/ui`, `feature/adb`, `feature/ai`)

---

## Getting Started

*Prerequisites: Qt 6.8+, CMake 3.20+, C++20 compiler*

```bash
git clone https://github.com/heijia20211205-eng/PhoneDesk-Pro.git
cd PhoneDesk-Pro
cmake -B build -DCMAKE_PREFIX_PATH=/path/to/Qt/6.8.x
cmake --build build
```

---

## License

MIT
