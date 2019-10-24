# Backpack

| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `grids` | [array](#grid) | Grids of the backpack |
| `penalties` | [object](armor.md#penalties) | The penalties of the backpack |

## Grid
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `id` | string | Identifier of the grid |
| `height` | int | The grid height |
| `width` | int | The grid width |
| `maxWeight` | float | The maximum weight of the grid |
| `filter` | object | Compatible items that fit into the grid (whitelist). No restriction when empty |

## Example
```JSON
{
  "_id": "5b44c6ae86f7742d1627baea",
  "name": "Ana tactical Beta 2 battle backpack",
  "shortName": "Beta2",
  "description": "An lightweight and capacious backpack from Ana Tactical. Specially designed for use in dynamic conditions and on rough terrain.",
  "price": 50686,
  "weight": 1.1,
  "maxStack": 1,
  "rarity": "none",
  "grid": {
    "color": {
      "r": 76,
      "g": 42,
      "b": 85,
      "a": 1
    },
    "height": 5,
    "width": 5
  },
  "_modified": 1571536460,
  "_kind": "backpack",
  "grids": [
    {
      "id": "main",
      "height": 6,
      "width": 5,
      "maxWeight": 0,
      "filter": {}
    }
  ],
  "penalties": {
    "speed": -3
  }
}
```
