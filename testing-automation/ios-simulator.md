---
name: ios-simulator
description: "21 production-ready scripts for iOS app testing, building, and automation. Semantic UI navigation, build automation, accessibility testing, simulator management."
source: https://github.com/conorluddy/ios-simulator-skill
---

# iOS Simulator Skill

Build, test, and automate iOS applications using accessibility-driven navigation.

## Quick Start

```bash
# 1. Check environment
bash scripts/sim_health_check.sh

# 2. Launch app
python scripts/app_launcher.py --launch com.example.app

# 3. Map screen to see elements
python scripts/screen_mapper.py

# 4. Tap button
python scripts/navigator.py --find-text "Login" --tap

# 5. Enter text
python scripts/navigator.py --find-type TextField --enter-text "user@example.com"
```

## 21 Scripts by Category

### Build & Development

| Script | Purpose |
|--------|---------|
| `build_and_test.py` | Build Xcode projects, run tests, parse results |
| `log_monitor.py` | Real-time log monitoring with filtering |

### Navigation & Interaction

| Script | Purpose |
|--------|---------|
| `screen_mapper.py` | Analyze screen, list interactive elements |
| `navigator.py` | Find and interact with elements semantically |
| `gesture.py` | Swipes, scrolls, pinches, long press |
| `keyboard.py` | Text input, special keys, hardware buttons |
| `app_launcher.py` | Launch, terminate, install apps, deep links |

### Testing & Analysis

| Script | Purpose |
|--------|---------|
| `accessibility_audit.py` | Check WCAG compliance |
| `visual_diff.py` | Compare screenshots for changes |
| `test_recorder.py` | Document test execution with screenshots |
| `app_state_capture.py` | Create debugging snapshots |
| `sim_health_check.sh` | Verify environment setup |

### Permissions & Testing

| Script | Purpose |
|--------|---------|
| `clipboard.py` | Manage simulator clipboard |
| `status_bar.py` | Override status bar (time, battery, network) |
| `push_notification.py` | Send simulated push notifications |
| `privacy_manager.py` | Grant/revoke app permissions |

### Device Lifecycle

| Script | Purpose |
|--------|---------|
| `simctl_boot.py` | Boot simulators |
| `simctl_shutdown.py` | Shutdown simulators |
| `simctl_create.py` | Create simulators dynamically |
| `simctl_delete.py` | Delete simulators |
| `simctl_erase.py` | Factory reset without deletion |

## Common Patterns

### Navigation

```bash
# Find by text (fuzzy matching)
python scripts/navigator.py --find-text "Submit" --tap

# Find by element type
python scripts/navigator.py --find-type TextField --enter-text "hello"

# Find by accessibility ID
python scripts/navigator.py --find-id "login-button" --tap
```

### Gestures

```bash
# Swipe
python scripts/gesture.py --swipe up

# Scroll
python scripts/gesture.py --scroll down --count 3

# Pull to refresh
python scripts/gesture.py --refresh

# Long press
python scripts/gesture.py --long-press --x 100 --y 200
```

### App Lifecycle

```bash
# Launch
python scripts/app_launcher.py --launch com.example.app

# Terminate
python scripts/app_launcher.py --terminate com.example.app

# Deep link
python scripts/app_launcher.py --open-url "myapp://profile/123"

# List installed apps
python scripts/app_launcher.py --list
```

### Permissions

```bash
# Grant camera access
python scripts/privacy_manager.py --bundle-id com.example.app --grant camera

# Revoke all permissions
python scripts/privacy_manager.py --bundle-id com.example.app --reset

# Multiple permissions
python scripts/privacy_manager.py --bundle-id com.example.app --grant camera,microphone,photos
```

### Status Bar

```bash
# Clean screenshot mode (9:41, 100% battery)
python scripts/status_bar.py --preset clean

# Low battery test
python scripts/status_bar.py --preset low-battery

# Custom
python scripts/status_bar.py --time "14:30" --battery-level 75
```

## Typical Workflow

1. Verify environment: `bash scripts/sim_health_check.sh`
2. Launch app: `python scripts/app_launcher.py --launch com.example.app`
3. Analyze screen: `python scripts/screen_mapper.py`
4. Interact: `python scripts/navigator.py --find-text "Button" --tap`
5. Verify: `python scripts/accessibility_audit.py`
6. Debug: `python scripts/app_state_capture.py --app-bundle-id com.example.app`

## Requirements

- macOS 12+
- Xcode Command Line Tools
- Python 3
- IDB (optional, for interactive features)

## Key Design Principles

- **Semantic Navigation** - Find by meaning, not pixels
- **Token Efficiency** - Concise output (3-5 lines default)
- **Accessibility-First** - Built on standard accessibility APIs
- **Zero Configuration** - Works immediately with Xcode
- **Structured Data** - JSON output with `--json` flag
