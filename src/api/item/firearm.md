# Firearm

| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `type` | string | The type of the firearm, e.g. `primary`, `secondary` |
| `class` | string | The weapon class, e.g. `assaultCarbine`, `pistol`, ` smg` |
| `caliber` | string | The weapon caliber |
| `rof` | int | The rate of fire of the weapon |
| `burstRounds` | int | Number of rounds per burst, if available |
| `action` | string | The action type e.g. `gas`, `recoil`, `bolt` |
| `modes` | []string | The fire modes of the weapon |
| `velocity` | float | The muzzle velocity in meters per second |
| `effectiveDist` | float | The maximum effective range of the weapon |
| `ergonomics` | float | The base ergonomics of the firearm |
| `foldRectractable` | bool | Indicates if the butstock is fold or rectractable |
| `recoilVertical` | float | The base vertical recoil of the weapon |
| `recoilHorizontal` | float | The base horizontal recoil of the weapon |
| `slots` | [object](#slot) | A map of the modification slots |

## Slot
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `filter` | object | A map of compatible item IDs categorized by `kind` |
| `required` | bool | Indicates whether the slot is required for an operational state |

## Example
```JSON
{
  "_id": "574d967124597745970e7c94",
  "name": "Simonov Semi-Automatic Carbine SKS 7.62x39",
  "shortName": "SKS",
  "description": "Soviet semi-automatic carbine designed by Sergei Simonov for 7.62x39 cartridge and known abroad as SKS-45. Immensely popular both in CIS countries and in the West, this weapon is still in active service in some countries in form of various copies and modifications. This particular specimen comes from extended storage warehouses of Tula Arms Plant and haven't yet undergo the civilian weapon normalization procedure.",
  "price": 19331,
  "weight": 2.627,
  "maxStack": 1,
  "rarity": "rare",
  "grid": {
    "color": {
      "r": 0,
      "g": 0,
      "b": 0,
      "a": 1
    },
    "height": 1,
    "width": 4
  },
  "_modified": 1571536468,
  "_kind": "firearm",
  "type": "primary",
  "class": "assaultCarbine",
  "caliber": "7.62x39mm",
  "rof": 40,
  "action": "gas",
  "modes": [
    "single"
  ],
  "velocity": 0,
  "effectiveDist": 400,
  "ergonomics": 40,
  "foldRectractable": false,
  "recoilVertical": 182,
  "recoilHorizontal": 400,
  "slots": {
    "magazine": {
      "filter": {
        "magazine": [
          "5c5970672e221602b21d7855",
          "587df583245977373c4f1129",
          "587df3a12459772c28142567"
        ]
      },
      "required": false
    },
    "muzzle": {
      "filter": {
        "modificationMuzzle": [
          "593d490386f7745ee97a1555"
        ]
      },
      "required": false
    },
    "sightRear": {
      "filter": {
        "modificationSight": [
          "574db213245977459a2f3f5d"
        ]
      },
      "required": false
    },
    "stock": {
      "filter": {
        "modificationStock": [
          "587e0531245977466077a0f7",
          "5afd7ded5acfc40017541f5e",
          "574dad8024597745964bf05c"
        ]
      },
      "required": true
    }
  }
}
```
