# Armor

| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `type` | string | The type of the armor e.g. `body, helmet` |
| `armor` | [object](#armor-properties) | The armor properties |
| `penalties` | [object](#penalties) | The penalties of the armor |
| `blocking` | array | Blocked zones e.g. `earpiece, eyewear` |
| `slots` | object | Modification slots of the armor |
| `compatibility` | object | If it's an attachment to which it's compatible |

## Armor properties
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `class` | int | The armor class |
| `durability` | float | The max durability of the armor |
| `material` | [object](#material-properties) | Material properties of the armor |
| `bluntThroughput` | float | The damage done to the target when the armor is not penetrated |
| `zones` | array | The zones protected by the armor |

## Material properties
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `name` | string | Name of the material |
| `destructibility` | float | The destructibility of the material |

## Penalties
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `mouse` | float | Mouse speed penalty |
| `speed` | float | Movement speed penalty |
| `ergonomics` | int | Ergonomics deduction |
| `deafness` | string | Strength of hearing reduction e.g. `low, medium, high` |


## Example
```JSON
{
  "_id": "5b44d0de86f774503d30cba8",
  "name": "IOTV Gen4 armor (high mobility kit)",
  "shortName": "Gen4 HMK",
  "description": "The Improved Outer Tactical Vest (IOTV) Gen IV is designed to permit maximum freedom of movement required to assume correct firing positions with the agility to execute and maneuver tasks. Optimal design characteristics ensure the best possible weight distribution of both the ballistic body armor system as well as additional load bearing equipment, thus providing enhanced comfort, wear duration, and mobility. Increased mobility and comfort kit.",
  "price": 118774,
  "weight": 10,
  "maxStack": 1,
  "rarity": "superrare",
  "grid": {
    "color": {
      "r": 28,
      "g": 65,
      "b": 86,
      "a": 255
    },
    "height": 4,
    "width": 3
  },
  "_modified": 1571536471,
  "_kind": "armor",
  "type": "body",
  "armor": {
    "class": 5,
    "durability": 62,
    "material": {
      "name": "titanium",
      "destructibility": 0.45
    },
    "bluntThroughput": 0.22,
    "zones": [
      "chest",
      "stomach"
    ]
  },
  "penalties": {
    "mouse": -15,
    "speed": -11,
    "ergonomics": -11,
    "deafness": "none"
  },
  "blocking": [],
  "slots": {},
  "compatibility": {}
}
```
