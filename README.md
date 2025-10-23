# 🌌 Beyond Item Shop Creator Guide

> [!IMPORTANT]
> **Find Beyond cosmetics:** [https://fortnite.gg/cosmetics](https://fortnite.gg/cosmetics?season=1,2,3,4,5,6,7,8,9,10,11,12))
>
> **Track shop updates:** [FNBR.co/History](https://fnbr.co/history)
>
> **Version supported:** Chapter 2 Season 2 – v12.41 and earlier only

 

---

 

## 🧭 Step 1: Know the Syntax

> [!WARNING]
> **Each cosmetic reference must include the correct type prefix and be wrapped in double quotes.**
>
> **Structure:** `"ItemType:CosmeticID"`

**Examples:**

```json
"AthenaCharacter:CID_132_Be_Commando_M_SciOps"
"AthenaPickaxe:Pickaxe_ID_081_Be_HammerSteel"
"AthenaDance:EID_WaveHello"
```

 

---

 

## ⚙️ Step 2: Item Type Reference

| Cosmetic         | Item Type           |
| ---------------- | ------------------- |
| Skins            | `AthenaCharacter`       |
| Back Accessories | `AthenaBackpack`        |
| Harvesting Tools | `AthenaPickaxe`         |
| Emotes           | `AthenaDance`           |
| Gliders          | `AthenaGlider`          |
| Wraps            | `AthenaItemWrap`        |
| Trails           | `AthenaSkyDiveContrail` |
| Loading Screens  | `AthenaLoadingScreen`   |

 

---

 

## 🛒 Step 3: Configure Your Shop

Your Beyond shop layout includes **8 slots total** (4 standard + 4 featured).

Each entry requires:

* `itemGrants`: list of one or more cosmetic IDs (with type)
* `price`: V-Bucks cost (no commas, numbers only)

**Template:**

```json
{
  "//": "Athena Item Shop Config v12.41",
  "daily1": {"itemGrants": [""], "price": 0},
  "daily2": {"itemGrants": [""], "price": 0},
  "daily3": {"itemGrants": [""], "price": 0},
  "daily4": {"itemGrants": [""], "price": 0},
  "daily5": {"itemGrants": [""], "price": 0},
  "daily6": {"itemGrants": [""], "price": 0},
  "featured1": {"itemGrants": [""], "price": 0},
  "featured2": {"itemGrants": [""], "price": 0}
}
```

 

---

 

## 🧩 Step 4: Complete Example

```json
{
  "//": "BE Item Shop Config v12.41",
  "daily1": {"itemGrants": ["AthenaCharacter:CID_132_Be_Commando_M_SciOps"], "price": 1200},
  "daily2": {"itemGrants": ["AthenaCharacter:CID_133_Be_Commando_F_SciOps"], "price": 1200},
  "daily3": {"itemGrants": ["AthenaPickaxe:Pickaxe_ID_081_Be_HammerSteel"], "price": 800},
  "daily4": {"itemGrants": ["AthenaItemWrap:Wrap_056_Be_TechnoCircuit"], "price": 500},
  "daily5": {"itemGrants": ["AthenaDance:EID_WaveHello"], "price": 200},
  "daily6": {"itemGrants": ["AthenaCharacter:CID_190_Be_Commando_M_QuantumKnight"], "price": 1500},
  "featured1": {"itemGrants": ["AthenaBackpack:BID_143_QuantumPack"], "price": 400},
  "featured2": {"itemGrants": ["AthenaGlider:Glider_ID_091_Be_TechFeather"], "price": 800}
}
```

 

---

 

## ⚠️ Common Errors to Avoid

### 🚫 Missing Type Prefix

**Incorrect:**

```json
"itemGrants": ["CID_132_Be_Commando_M_SciOps"]
```

**Correct:**

```json
"itemGrants": ["AthenaCharacter:CID_132_Be_Commando_M_SciOps"]
```

---

### 🚫 Missing Quotes

**Incorrect:**

```json
"itemGrants": [AthenaPickaxe:Pickaxe_ID_081_Be_HammerSteel]
```

**Correct:**

```json
"itemGrants": ["AthenaPickaxe:Pickaxe_ID_081_Be_HammerSteel"]
```

---

### 🚫 Commas in Prices

**Incorrect:**

```json
"price": 1,200
```

**Correct:**

```json
"price": 1200
```

---

### 🚫 Using Wrong Version

This format is **only valid for v12.41 and older.**
Later Fortnite Versions changed naming conventions and price formatting. if im not wrong

---

## ✅ Pro Tip

If you’re unsure of an item’s **Cosmetic ID**, use the **Fortnite.GG** link above, click an item, and copy its internal ID from the URL — just be sure to prepend the **correct type** from Step 2.
