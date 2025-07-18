# 🕒 Universal Auto-Off Blueprint for Home Assistant

Automatically turn off any `switch`, `light`, `input_boolean`, or `climate` entity in Home Assistant after it has been active for a specified duration — with optional pre-shutoff notifications.

[![hass-blueprint](https://img.shields.io/badge/Home%20Assistant-Blueprint-41BDF5?logo=home-assistant&logoColor=white)](https://www.home-assistant.io/blueprints/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## 🚀 Features

- ✅ Works with `switch`, `light`, `input_boolean`, and `climate` domains
- ✅ Automatically turns the entity off after a set time
- ✅ Sends a **notification 5 minutes before shutoff** (optional)
- ✅ No `configuration.yaml` changes required
- ✅ Fully UI-friendly — no YAML editing needed after import

---

## 📦 Import This Blueprint

Paste this URL into Home Assistant when importing a blueprint:
https://github.com/barrycarrjr/universal-auto-off-blueprint/blob/main/blueprints/automation/barry/universal_auto_turn_off_with_notification.yaml

Or download and place it manually in:
config/blueprints/automation/barry/universal_auto_turn_off_with_notification.yaml


Then reload blueprints under **Settings → Automations & Scenes → ⋮ → Reload Blueprints**.

---

## 🛠️ How to Use

1. Go to **Settings → Automations & Scenes → Create Automation → From Blueprint**
2. Select **Universal Auto Turn Off (Switch, Light, Boolean, Climate)**
3. Fill out:
   - The target entity to monitor (e.g., `switch.pool_pump`, `climate.living_room`)
   - The maximum time it should stay active
   - Whether to send a notification 5 minutes before shutoff
   - The notification service (e.g., `notify.mobile_app_pixel_8`)
   - The custom notification message (optional)

---

## 💡 Example Use Cases

| Entity Type      | Use Case Example                             | Max On Duration |
|------------------|----------------------------------------------|------------------|
| `switch`         | Turn off pool heater after 2 hours           | `02:00:00`       |
| `light`          | Turn off patio lights after 45 minutes       | `00:45:00`       |
| `input_boolean`  | Auto-disable “guest mode” after 30 minutes   | `00:30:00`       |
| `climate`        | Turn off guest room thermostat after 6 hours | `06:00:00`       |

---

## 📋 Blueprint YAML Location

```text
blueprints/
└── automation/
    └── barry/
        └── universal_auto_turn_off_with_notification.yaml
