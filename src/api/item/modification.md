# Modification

| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `ergonomics` | int | The ergonomics modifier of the modification |
| `raidModdable` | int | Indicates if the modification is moddable in Raid. `0` = **no**, `1` = **yes**, `2` = **only with a tool** |
| `gridModifier` | [object](#grid-modifier) | The modifiers that influence the grid properties of the parent |
| `slots` | [object](#slot) | A map of the modification slots |
| `compatibility` | object | A map of compatible item IDs (reverse) categorized by `kind` |
| `conflicts` | object | A map of item IDs to conflict with, categorized by `kind` |

## Grid Modifier
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `height` | int | The grid height modifier |
| `width` | int | The grid width modifier |

## Slot
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `filter` | object | A map with compatible item IDs categorized by `kind` |
| `required` | bool | Indicates whether the slot is required for an operational state |

## Example
```JSON
{
  "_id": "5c90c3622e221601da359851",
  "name": "B-13V rail platform above reciever \"Classic\"",
  "shortName": "B-13V",
  "description": "The B-13 rail platform above receiver mounts on the standard Dovetail joint located on the PP-19-01 \"Vityaz\". Provides a platform for sighting devices.",
  "price": 7600,
  "weight": 0.158,
  "maxStack": 1,
  "rarity": "none",
  "grid": {
    "color": {
      "r": 28,
      "g": 65,
      "b": 86,
      "a": 1
    },
    "height": 1,
    "width": 1
  },
  "_modified": 1571536473,
  "_kind": "modificationMount",
  "ergonomics": 0,
  "raidModdable": 1,
  "gridModifier": {
    "height": 0,
    "width": 0
  },
  "slots": {
    "scope_00": {
      "filter": {
        "modificationMount": [
          "58d39d3d86f77445bb794ae7",
          "5c7d55f52e221644f31bff6a",
          "5b3b6dc75acfc47a8773fb1e",
          "5b2389515acfc4771e1be0c0",
          "577d128124597739d65d0e56",
          "5c86592b2e2216000e69e77c",
          "5a37ca54c4a282000d72296a",
          "58d2664f86f7747fec5834f6",
          "57c69dd424597774c03b7bbc",
          "5b3b99265acfc4704b4a1afb",
          "5aa66a9be5b5b0214e506e89",
          "5aa66c72e5b5b00016327c93",
          "5c1cdd302e221602b3137250",
          "5b31163c5acfc400153b71cb",
          "5a33b652c4a28232996e407c",
          "5a33b2c9c4a282000c5a9511",
          "59db7eed86f77461f8380365",
          "5a1ead28fcdbcb001912fa9f"
        ],
        "modificationSight": [
          "57ac965c24597706be5f975c",
          "57aca93d2459771f2c7e26db",
          "544a3a774bdc2d3a388b4567",
          "57adff4f24597737f373b6e6",
          "5c0517910db83400232ffee5",
          "591c4efa86f7741030027726",
          "570fd79bd2720bc7458b4583",
          "570fd6c2d2720bc6458b457f",
          "558022b54bdc2dac148b458d",
          "5c07dd120db834001c39092d",
          "5c0a2cec0db834001b7ce47d",
          "58491f3324597764bc48fa02",
          "584924ec24597768f12ae244",
          "5b30b0dc5acfc400153b7124",
          "5c0505e00db834001b735073",
          "584984812459776a704a82a6",
          "59f9d81586f7744c7506ee62",
          "570fd721d2720bc5458b4596",
          "57ae0171245977343c27bfcf"
        ]
      },
      "required": false
    }
  },
  "compatibility": {
    "firearm": [
      "57838ad32459774a17445cd2",
      "576165642459773c7a400233",
      "5c46fbd72e2216398b5a8c9c",
      "5839a40f24597726f856b511",
      "5ac66cb05acfc40198510a10",
      "5c501a4d2e221602b412b540",
      "57c44b372459772d2b39b8ce",
      "5a0ec13bfcdbcb00165aa685",
      "5ac4cd105acfc40016339859",
      "5ac66d725acfc43b321d4b60",
      "5ab8e9fcd8ce870019439434",
      "5644bd2b4bdc2d3b4c8b4572",
      "59984ab886f7743e98271174",
      "5ac66d2e5acfc43b321d4b53",
      "583990e32459771419544dd2",
      "5ac66d9b5acfc4001633997a",
      "5abcbc27d8ce8700182eceeb",
      "5ac66d015acfc400180ae6e4"
    ]
  },
  "conflicts": {
    "modificationMount": [
      "5648b6ff4bdc2d3d1c8b4581"
    ],
    "modificationReceiver": [
      "59985a6c86f77414ec448d17"
    ],
    "modificationSight": [
      "5c82342f2e221644f31c060e",
      "576fd4ec2459777f0b518431",
      "5c82343a2e221644f31c0611"
    ]
  }
}
```
