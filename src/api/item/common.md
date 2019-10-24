# Common

| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `_id` | string | The ID of the item |
| `name` | string | The name of the item |
| `shortName` | string | The short name of the item |
| `description` | string | The description of the item |
| `price` | int | The base price in rubles of the item |
| `weight` | float | The weight of the item |
| `maxStack` | int | The maximum stack size of the item |
| `rarity` | string | The rarity of the item |
| `grid` | [object](#grid) | The grid properties of the item |
| `_modified` | int | The modified date as Unix timestamp |
| `_kind` | string | The entity type of the item |

## Grid
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `color` | [object](#color) | The grid background color in RGBA |
| `height` | int | The grid height |
| `width` | int | The grid width |

## Color
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `r` | int | Red channel |
| `g` | int | Green channel |
| `b` | int | Blue channel |
| `a` | int | Alpha channel |

## Example
```JSON
{
  "_id": "590c392f86f77444754deb29",
  "name": "SSD drive",
  "shortName": "SSD",
  "description": "Solid state drive. Used to store data, with enhanced read and write performance.",
  "price": 250000,
  "weight": 0.4,
  "maxStack": 1,
  "rarity": "rare",
  "grid": {
    "color": {
      "r": 28,
      "g": 65,
      "b": 86,
      "a": 255
    },
    "height": 1,
    "width": 1
  },
  "_modified": 1571536468,
  "_kind": "common"
}
```
