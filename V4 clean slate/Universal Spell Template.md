# Universal Spell Template for App Export

This document defines a standardized structure for all spells in the Exceed TTRPG magic system, designed for easy export to digital applications.

## Template Schema

```json
{
  "id": "string (unique_identifier)",
  "name": "string (display_name)",
  "shortDescription": "string (brief summary for lists and tooltips)",
  "longDescription": "string (complete mechanical and narrative description)",
  "attributeContribution": {
    "primary": "string (primary attribute this spell contributes to)",
    "secondary": "string (secondary attribute this spell contributes to)"
  },
  "tier": "integer (0-5, representing spell power level)",
  "apCost": "integer (action points required to cast)",
  "limitCost": {
    "basic": "string|integer (limit cost for basic version)",
    "advanced": "string|integer (limit cost for advanced version, if different)"
  },
  "damage": {
    "formula": "string (damage calculation if applicable)",
    "type": "string (damage type: physical, mental, elemental, etc.)",
    "scaling": "string (how damage scales with tier/attributes)"
  },
  "duration": "string (instant|concentration|turn|scene|permanent)",
  "versions": {
    "hasBasic": "boolean (true if basic version exists)",
    "hasAdvanced": "boolean (true if advanced version exists)",
    "basicCost": "integer (CP cost for basic version)",
    "advancedCost": "integer (CP cost for advanced version)"
  },
  "range": "string (self|touch|short|medium|long|sight)",
  "area": "string (single|line|cone|burst|aura)",
  "targeting": "string (self|ally|enemy|object|area)",
  "school": "string (elemental|mind|body|nature|divine|etc.)",
  "components": {
    "verbal": "boolean (requires speaking)",
    "somatic": "boolean (requires gestures)",
    "material": "boolean (requires materials)",
    "focus": "boolean (requires focus item)"
  },
  "effects": {
    "primary": "string (main mechanical effect)",
    "secondary": ["array of additional effects"],
    "conditions": ["array of conditions applied"],
    "saves": "string (resistance/save mechanics)"
  },
  "scaling": {
    "tier": "string (how spell improves with higher tiers)",
    "attribute": "string (how spell scales with caster attributes)",
    "limit": "string (effects of spending additional limit)"
  },
  "restrictions": ["array of casting limitations or requirements"],
  "prerequisites": {
    "spells": ["array of prerequisite spells"],
    "attributes": [
      {
        "name": "string (attribute name)",
        "level": "integer (minimum level required)"
      }
    ],
    "skills": [
      {
        "name": "string (skill name)",
        "level": "integer (minimum level required)"
      }
    ],
    "special": ["array of special requirements"]
  },
  "notes": "string (design notes or clarifications)",
  "status": "string (complete|wip|concept|deprecated)"
}
```

## Example Spells

### Tier 0 Utility Spell (Basic/Advanced Versions)
```json
{
  "id": "light",
  "name": "Light",
  "shortDescription": "Create torch-level illumination around yourself",
  "longDescription": "Create torch-level illumination around yourself. Advanced version can affect the entire team without consuming limit points.",
  "attributeContribution": {
    "primary": "Will",
    "secondary": null
  },
  "tier": 0,
  "apCost": 2,
  "limitCost": {
    "basic": "1 (self only)",
    "advanced": "1 (team-wide)"
  },
  "damage": {
    "formula": null,
    "type": null,
    "scaling": null
  },
  "duration": "persistent (or 10 minutes if cast as temporary spell)",
  "versions": {
    "hasBasic": true,
    "hasAdvanced": true,
    "basicCost": 1,
    "advancedCost": 3
  },
  "range": "self",
  "area": "aura",
  "targeting": "self/team",
  "school": "utility",
  "components": {
    "verbal": true,
    "somatic": true,
    "material": false,
    "focus": false
  },
  "effects": {
    "primary": "Bright light 10m radius",
    "secondary": ["Advanced: affects entire team", "Can be cast as temporary 10-minute effect"],
    "conditions": [],
    "saves": "none"
  },
  "scaling": {
    "tier": "N/A (tier 0)",
    "attribute": "None",
    "limit": "Advanced version more efficient for teams"
  },
  "restrictions": [],
  "prerequisites": {
    "spells": [],
    "attributes": [],
    "skills": [
      {"name": "Spellcraft", "level": 0}
    ],
    "special": ["Must have Mage perk"]
  },
  "notes": "Basic utility spell, demonstrates Basic/Advanced version mechanics",
  "status": "complete"
}
```

### Tier 1 Combat Spell
```json
{
  "id": "elemental_strike",
  "name": "Elemental Strike",
  "shortDescription": "Attack a target within 2m with Fire, Ice, Bludgeoning, Acid or Piercing",
  "longDescription": "Attack a target within 2m, with Fire, Ice, Bludgeoning, Acid or Piercing. Choose the element when casting.",
  "attributeContribution": {
    "primary": "Agility",
    "secondary": "Wit"
  },
  "tier": 1,
  "apCost": 2,
  "limitCost": {
    "basic": "none (instantaneous)",
    "advanced": "none (instantaneous)"
  },
  "damage": {
    "formula": "Spellcraft * 4d damage",
    "type": "chosen element (fire/ice/bludgeoning/acid/piercing)",
    "scaling": "Scales with Spellcraft level"
  },
  "duration": "instant",
  "versions": {
    "hasBasic": true,
    "hasAdvanced": false,
    "basicCost": 3,
    "advancedCost": null
  },
  "range": "short (2m)",
  "area": "single",
  "targeting": "enemy",
  "school": "elemental",
  "components": {
    "verbal": true,
    "somatic": true,
    "material": false,
    "focus": false
  },
  "effects": {
    "primary": "Elemental damage on successful hit",
    "secondary": ["Element chosen at casting", "Uses normal attack roll"],
    "conditions": [],
    "saves": "none"
  },
  "scaling": {
    "tier": "Higher tiers would increase damage",
    "attribute": "Damage scales with Spellcraft level",
    "limit": "N/A (instantaneous effect)"
  },
  "restrictions": ["Must be within 2m of target"],
  "prerequisites": {
    "spells": [],
    "attributes": [],
    "skills": [
      {"name": "Spellcraft", "level": 1}
    ],
    "special": ["Must have Mage perk"]
  },
  "notes": "Basic combat spell, demonstrates damage scaling mechanics",
  "status": "complete"
}
```

## Field Documentation

### Core Identity
- **id**: Unique identifier for database storage and cross-referencing
- **name**: Display name shown to players
- **shortDescription**: Brief summary perfect for spell lists and quick reference
- **longDescription**: Complete description combining mechanical effects with narrative flavor

### Casting Mechanics
- **attributeContribution**: Which attributes this spell contributes to when learned
- **tier**: Power level (0=cantrip, 5=legendary magic)
- **apCost**: Action points required to cast the spell
- **limitCost**: Limit points consumed for persistent effects (instantaneous spells cost no limit)

### Effects and Targeting
- **damage**: Damage formula, type, and scaling for combat spells
- **duration**: How long the spell's effects persist
- **versions**: Basic and Advanced versions with different CP costs and effects
- **range/area/targeting**: Spatial mechanics for spell application

### Magic System Integration
- **components**: What is required to cast (verbal, somatic, material, focus)
- **school**: Magical tradition or element for organization and specialization
- **scaling**: How the spell improves with Spellcraft level and tier progression

### Learning and Prerequisites
- **prerequisites**: Requirements to learn the spell (other spells, attributes, skills, special conditions)
- **restrictions**: Limitations on when or how the spell can be cast

This template captures the complexity of the Exceed Limit-based magic system, including Basic/Advanced spell versions, while remaining structured for digital implementation. Note that all spells are cast using Wit + Spellcraft regardless of the spell type.