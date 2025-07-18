# 🕒 Universal Auto-Off Blueprint for Home Assistant (Reboot-Safe)

Automatically turn off any `switch`, `light`, `input_boolean`, or `climate` entity in Home Assistant after it has remained active for a specified duration — even across reboots.

This blueprint is **reboot-safe**, using `for:` logic to ensure the countdown resumes correctly after Home Assistant restarts.

[![hass-blueprint](https://img.shields.io/badge/Home%20Assistant-Blueprint-41BDF5?logo=home-assistant&logoColor=white)](https://www.home-assistant.io/docs/blueprint/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## 🚀 Features

- ✅ Works with `switch`, `light`, `input_boolean`, and `climate` domains
- ✅ Automatically turns the entity off after it remains active for a set time
- ✅ Fully reboot-safe using `for:` logic
- ✅ No helper entities, timers, or YAML edits required
- ✅ Clean, simple, UI-driven setup

---

## 📦 Import This Blueprint

Click below to import directly into Home Assistant:

[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/barrycarrjr/universal-auto-off-blueprint/main/blueprints/automation/barrycarrjr/universal_auto_turn_off_with_notification.yaml)

---

Or install manually:

- Save the file to:
  config/blueprints/automation/barrycarrjr/universal_auto_turn_off_with_notification.yaml
- Reload blueprints:
  **Settings → Automations & Scenes → ⋮ Menu → Reload Blueprints**

---

## 🛠️ How to Use

1. Go to **Settings → Automations & Scenes → Create Automation → From Blueprint**
2. Select **Universal Auto Turn Off (Switch, Light, Boolean, Climate)**
3. Fill out:
- The entity to monitor (e.g., `switch.fireplace_blower`)
- The duration it should be allowed to stay on (e.g., `03:00:00`)

Once the entity has remained in an active state (`on`, `heat`, etc.) for that long, it will be turned off — even if Home Assistant is restarted during the countdown.

---

## 💡 Example Use Cases

| Entity Type      | Use Case Example                             | Max On Duration |
|------------------|----------------------------------------------|------------------|
| `switch`         | Turn off fireplace blower after 3 hours      | `03:00:00`       |
| `light`          | Auto-shutoff attic light after 30 minutes    | `00:30:00`       |
| `input_boolean`  | Disable "Vacation Mode" after 12 hours       | `12:00:00`       |
| `climate`        | Turn off guest room thermostat after 6 hours | `06:00:00`       |

---

## 📋 Blueprint YAML Location

```text
blueprints/
└── automation/
  └── barrycarrjr/
      └── universal_auto_turn_off_with_notification.yaml