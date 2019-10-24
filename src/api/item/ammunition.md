# Ammunition

| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `caliber` | string | The caliber of the ammunition |
| `type` | string | The type of the ammunition |
| `tracer` | bool | Indicates if it's tracer ammunition |
| `tracerColor` | string | The tracer color |
| `subsonic` | bool | Indicates if it's subsonic ammo |
| `ballisticCoef` | float | The ballistic coeficient of the ammo |
| `damage` | float | The flesh damage of the ammo |
| `penetration` | float | The penetration power of the ammo |
| `armorDamage` | float | The damage done to an armor |
| `fragmentation` | [object](#fragmentation) | The fragmentation properties of the ammo |
| `pellets` | int | The pellet count of the ammo if it's buckshot |

## Fragmentation
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `chance` | float | The penetration chance of the ammunition |
| `min` | int | The minimal fragment count |
| `max` | int | Indicates if it's tracer ammunition |

## Example
```JSON
{
  "_id": "560d5e524bdc2d25448b4571",
  "name": "12x70 Buckshot",
  "shortName": "12x70",
  "description": "12x70 Buckshot shell for 12ga shotguns",
  "price": 30,
  "weight": 0.05,
  "maxStack": 20,
  "rarity": "common",
  "grid": {
    "color": {
      "r": 104,
      "g": 102,
      "b": 40,
      "a": 255
    },
    "height": 1,
    "width": 1
  },
  "_modified": 1571536469,
  "_kind": "ammunition",
  "caliber": "12ga",
  "type": "buckshot",
  "tracer": false,
  "tracerColor": "red",
  "subsonic": true,
  "velocity": 320,
  "ballisticCoef": 1,
  "damage": 32,
  "penetration": 3,
  "armorDamage": 26,
  "fragmentation": {
    "chance": 0,
    "min": 1,
    "max": 1
  },
  "pellets": 8
}
```
