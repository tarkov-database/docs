# Ammunition

| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `caliber` | string | The caliber of the ammunition |
| `type` | string | The type of the ammunition |
| `tracer` | bool | Indicates if it's tracer ammunition |
| `tracerColor` | string | The tracer color |
| `subsonic` | bool | Indicates if it's subsonic ammo |
| `velocity` | float | Velocity of the projectile(s) in meters per second |
| `ballisticCoef` | float | The ballistic coeficient of the ammo |
| `damage` | float | The flesh damage of the ammo |
| `penetration` | float | The penetration power of the ammo |
| `armorDamage` | float | The damage done to an armor |
| `fragmentation` | [object](#fragmentation) | The fragmentation properties of the ammo |
| `effects` | [object](#effects) | Various effects of the ammo |
| `pellets` | int | **DEPRCATED** The pellet count of the ammo if it's buckshot |
| `projectiles` | int | The projectile count, relevant to e.g. buckshot or flechette rounds |
| `weaponModifier` | [object](#weapon-modifier) | The fragmentation properties of the ammo |

## Fragmentation
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `chance` | float | The penetration chance of the ammunition |
| `min` | int | The minimal fragment count |
| `max` | int | Indicates if it's tracer ammunition |

## Effects
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `lightBleedingChance` | float | Percentage value increases or decreases the chance of light bleeding |
| `heavyBleedingChance` | float | Percentage value increases or decreases the chance of heavy bleeding |

## Weapon Modifier
| Name  | Type   | Description          |
| ----- | ------ | -------------------- |
| `accuracy` | float | Modifier for weapon accuracy (percent) |
| `recoil` | float | Modifier for weapon recoil (percent) |

## Example
```JSON
{
  "_id": "56d59d3ad2720bdb418b4577",
  "name": "9x19 mm Pst gzh",
  "shortName": "Pst gzh",
  "description": "9x19 mm Pst gzh round. Steel core bullet. Developed by TSNIITOCHMASH in the early 90s. Bullet weight — 5,4 g, muzzle velocity — 445—470 m/s. It outperforms the commercially available 9×19 mm Parabellum ordnance and corresponds to the more powerful 9×19 mm NATO army rounds (9×19 +P). The bullet hits through 4 mm plate of St.3 steel at distance of 55 m.",
  "price": 42,
  "weight": 0.005,
  "maxStack": 50,
  "rarity": "none",
  "grid": {
    "color": {
      "r": 104,
      "g": 102,
      "b": 40,
      "a": 1
    },
    "height": 1,
    "width": 1
  },
  "_modified": 1571536468,
  "_kind": "ammunition",
  "caliber": "9x19mm Parabellum",
  "type": "bullet",
  "tracer": false,
  "tracerColor": "red",
  "subsonic": false,
  "velocity": 457,
  "ballisticCoef": 1,
  "damage": 56,
  "penetration": 18,
  "armorDamage": 33,
  "fragmentation": {
    "chance": 0.15,
    "min": 1,
    "max": 3
  },
  "projectiles": 0,
  "weaponModifier": {
    "accuracy": 0,
    "recoil": 0
  }
}
```
