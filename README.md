# Stardew Valley: "Marina", my own character in-game

**Author:** Marina Simion  
**High School:** Colegiul Național “Sfântul Sava”  
**Supervisor:** Prof. Talaat‑Hamid Anca  
**School Year:** 2022–2023  

---

## Project Overview

This project is a SMAPI Content Patcher mod for **Stardew Valley** that adds “Marina” (my in‑game avatar) as a fully realized NPC. Rather than patching the game’s DLLs, it leverages JSON‑driven content packs to inject:

- **Custom visuals:** sprite sheets for movement & portraits for dialogue  
- **Dynamic dialogue:** season‑ and event‑driven lines with branching heart‑level variations  
- **Daily schedule:** context‑aware routines depending on season or weather  
- **Gift preferences:** unique responses to “loved,” “liked,” “neutral,” “disliked,” and “hated” gifts    

All configuration is stored in human‑readable JSON files, and all art assets were hand‑drawn in GIMP. It demonstrates how you can extend an existing game without altering its core code, by designing structured data definitions and assets that a mod loader (SMAPI + Content Patcher) interprets at runtime.

---

## Requirements

- **Stardew Valley** (latest version)  
- **SMAPI** mod loader  
- **Content Patcher** (by Pathoschild)  

---

## Installation

1. **Install SMAPI** (see [SMAPI installation guide](https://smapi.io/)).  
2. Subscribe to **Content Patcher** via the in‑game mod browser or place its DLL in your `Mods` folder.  
3. Download or clone this repo into your `Stardew Valley/Mods/` folder, keeping the root folder name as `[CP] Marina`.  
4. Launch the game via SMAPI; the console should show `Content Patcher: Loading “AddingMyself”`.

---

## File Structure

```text
[CP] Marina/
├── manifest.json            # Metadata & Content Patcher settings
├── content.json             # Asset-loading & data-edit directives
└── assets/
    ├── portraits.png        # Emotion portraits (64×64 px)
    ├── sprites.png          # Walk-cycle frames (16×32 px)
    ├── dialogue.json        # All dialogue lines keyed by trigger
    └── schedule.json        # NPC daily routines (time → location)
