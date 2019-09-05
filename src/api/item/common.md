# Common

| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `_id` | string | The ID of the item |
| `name` | string | The name of the item |
| `shortName` | string | The short name of the item |
| `description` | string | The description of the item |
| `price` | int | The base price of the item |
| `weight` | float | The weight of the item |
| `maxStack` | int | The maximum stack size of the item |
| `rarity` | string | The rarity of the item |
| `grid` | object | The grid properties of the item |
| `_modified` | int | The modified date as Unix timestamp |
| `_kind` | string | The entity type of the item |



## Example
```JSON
{
  "_id": "590dde5786f77405e71908b2",
  "name": "Bank case",
  "shortName": "Case",
  "description": "Armored bank case. It clearly hides something valuable, and thus survived many attempts of breaking it open.",
  "price": 0,
  "weight": 7,
  "maxStack": 1,
  "rarity": "none",
  "grid": {
    "color": {
      "r": 104,
      "g": 102,
      "b": 40,
      "a": 1
    },
    "height": 4,
    "width": 4
  },
  "_kind": "common"
}
```
