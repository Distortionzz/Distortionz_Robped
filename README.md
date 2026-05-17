# Distortionz RobPed

> Premium civilian robbery script for Qbox/FiveM — rob ambient NPC peds for cash, dirty money, or items, with escalating police alerts and protected-ped filtering.

![FiveM](https://img.shields.io/badge/FiveM-cerulean-yellow?style=flat-square&labelColor=181b20)
![Qbox](https://img.shields.io/badge/Qbox-required-red?style=flat-square&labelColor=dfb317)
![License](https://img.shields.io/badge/License-MIT-brightgreen?style=flat-square)
![Version](https://img.shields.io/github/v/release/Distortionzz/Distortionz_RobPed?style=flat-square&color=d4aa62&label=version)

---

## Overview

Adds a "Rob Civilian" ox_target option to ambient NPC peds. Players threaten the ped, get a randomized loot drop, and risk a police alert. Script-spawned peds (contact peds, dealers, etc.) are auto-skipped via the `distortionz_protected_ped` state bag convention.

## Features

- ox_target "Rob Civilian" on ambient NPCs
- Randomized loot table (cash / dirty money / items)
- Per-tier loot weights
- Police alert chance with escalation
- Cooldown per ped (one-time-rob tracking)
- **Protected-ped filtering** — skips any ped flagged with:
  - `distortionz_protected_ped` (Distortionz convention)
  - `isShopKeeper` / `invincible` / `protected` (third-party)
- **Law-enforcement lockout** — police-type jobs can't rob peds (target hidden + server-enforced)
- Distortionz Notify support

## Dependencies

| Resource | Required | Purpose |
|---|---|---|
| `qbx_core` | yes | Player data, money |
| `ox_lib` | yes | Callbacks, progress bar |
| `ox_target` | yes | Ped interaction |
| `ox_inventory` | yes | Loot rewards |
| `distortionz_notify` | optional | Branded notifications |

## Installation

```cfg
ensure distortionz_robped
```

## Configuration

See [`config.lua`](config.lua) for loot table, police alert chance, cooldowns, and rob duration.

`Config.Police.blockPoliceFromRobbing` (default `true`) stops any job listed in `Config.Police.jobs` (`police`, `sheriff`, `state`) from robbing peds — applied whether on or off duty. Add jobs to that list to extend the lockout.

## Credits

- **Author:** Distortionz
- **Framework:** [Qbox Project](https://github.com/Qbox-project)

## License

MIT — see [LICENSE](LICENSE).
