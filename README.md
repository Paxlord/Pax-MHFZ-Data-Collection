# Pax-MHFZ-Data-Collection
This repository is aiming to be a collection of data that I have mapped in this game. 
It's been pretty hard to find nicely-formatted accurate data about a lot of things related to this game. I hope this repo can help people that wants to create tools around MHFZ to find what they're looking for.

Data schemas will be refined over time as I mapped currently unknown values and I'll slowly push through my backlog and upload more data as I come across it in my different projects.

If you have any suggestions about data-formatting, feel free to raise an issue or shoot me a DM on Discord at @pax_777

## Melee 

### File format
- The json is an array of Weapon entries
- The in-game ID of a given weapon corresponds to the array index of this weapon
- Upgrade trees can be recursively processed through the "upgrades" part of the entry where each upgrade is pointing to a potential next weapon id
- I will provide an opinionated weapon tree structure at some point  

### Example entry
```json
{
    "name": "Iron Sword",
    "description": {
      "desc_1": "新米ハンターでも扱える大剣。",
      "desc_2": "多数のモンスターをなぎ払う",
      "desc_3": "ことが可能な武器。"
    },
    "stats": {
      "rarity": 1,
      "weapon_type": "GS",
      "price": 660,
      "raw": {
        "true_value": 60,
        "bloated_value": 288
      },
      "defense": 0,
      "affinity": 0,
      "element": {
        "type": "None",
        "true_value": 0,
        "bloated_value": 0
      },
      "ailment": {
        "type": "None",
        "value": 0
      },
      "slots": 0
    },
    "upgrades": {
      "next_1": 2,
      "next_2": 0,
      "next_3": 0,
      "next_4": 0
    }
  }
```

### Left to add 
- Upgrade recipes (mapped, need to extract)
- Sharpness (mapped, need to extract)
- GL shelling, HH songs, SA Phials (mapped, need to list them)
- Weapon Lengths (mapped)
- G Weapon Level upgrades (not mapped)
