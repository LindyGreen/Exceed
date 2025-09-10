# Universal Spell Template for App Export

This document defines a standardized structure for all spells in the Exceed TTRPG magic system, designed for easy export to digital applications.

## Template Schema

```json
{
  "id": "string (unique_identifier)",
  "name": "string (display_name)",
  "shortDescription": "string (brief summary for lists and tooltips)",
  "longDescription": "string (complete mechanical and narrative description)",
  "attributes": {
    "primary": "string (primary attribute used)",
    "secondary": "string (secondary attribute used)",
    "formula": "string (how attributes combine for spellcraft)"
  },
  "tier": "integer (0-5, representing spell power level)",
  "apCost": "integer (action points required to cast)",
  "limit": "integer (limit points consumed when cast)",
  "damage": {
    "formula": "string (damage calculation if applicable)",
    "type": "string (damage type: physical, mental, elemental, etc.)",
    "scaling": "string (how damage scales with tier/attributes)"
  },
  "duration": "string (instant|concentration|turn|scene|permanent)",
  "complexity": "string (basic|advanced)",
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

### Basic Damage Spell
```json
{
  "id": "force_bolt",
  "name": "Force Bolt",
  "shortDescription": "Launch a bolt of pure magical force",
  "longDescription": "You gather magical energy and launch it as a concentrated bolt of force that strikes with unerring accuracy. The bolt manifests as a shimmering projectile of raw magical energy.",
  "attributes": {
    "primary": "Will",
    "secondary": "Perception", 
    "formula": "Will/Perception + Spellcraft"
  },
  "tier": 1,
  "apCost": 3,
  "limit": 1,
  "damage": {
    "formula": "1d6 + Will modifier",
    "type": "force",
    "scaling": "+1d6 per tier above 1st"
  },
  "duration": "instant",
  "complexity": "basic",
  "range": "medium",
  "area": "single",
  "targeting": "enemy",
  "school": "force",
  "components": {
    "verbal": true,
    "somatic": true,
    "material": false,
    "focus": false
  },
  "effects": {
    "primary": "Deals force damage with automatic hit",
    "secondary": [],
    "conditions": [],
    "saves": "none"
  },
  "scaling": {
    "tier": "Damage increases by 1d6 per tier",
    "attribute": "Damage bonus from Will modifier",
    "limit": "Spend +1 limit for +1d6 damage"
  },
  "restrictions": ["Requires line of sight to target"],
  "prerequisites": {
    "spells": [],
    "attributes": [
      {"name": "Will", "level": 2}
    ],
    "skills": [
      {"name": "Spellcraft", "level": 1}
    ],
    "special": []
  },
  "notes": "Classic starter damage spell, reliable and straightforward",
  "status": "complete"
}
```

### Advanced Utility Spell
```json
{
  "id": "teleportation_circle",
  "name": "Teleportation Circle",
  "shortDescription": "Create a portal linking two distant locations",
  "longDescription": "You inscribe a complex magical circle that opens a dimensional gateway, allowing instantaneous travel between two points. The circle requires precise geometric patterns and significant magical energy to maintain stability.",
  "attributes": {
    "primary": "Will",
    "secondary": "Intelligence",
    "formula": "Will/Intelligence + Spellcraft"
  },
  "tier": 4,
  "apCost": 8,
  "limit": 4,
  "damage": {
    "formula": null,
    "type": null,
    "scaling": null
  },
  "duration": "concentration",
  "complexity": "advanced",
  "range": "touch",
  "area": "portal",
  "targeting": "location",
  "school": "spatial",
  "components": {
    "verbal": true,
    "somatic": true,
    "material": true,
    "focus": true
  },
  "effects": {
    "primary": "Creates bidirectional portal between two known locations",
    "secondary": ["Portal can transport multiple creatures", "Requires 10 minutes to inscribe"],
    "conditions": [],
    "saves": "none"
  },
  "scaling": {
    "tier": "Range increases, casting time decreases",
    "attribute": "Portal stability and duration improve",
    "limit": "Spend +2 limit to make portal permanent until dispelled"
  },
  "restrictions": [
    "Must have visited destination before",
    "Requires expensive material components",
    "Cannot cross planar boundaries"
  ],
  "prerequisites": {
    "spells": ["dimensional_step", "arcane_sight"],
    "attributes": [
      {"name": "Will", "level": 4},
      {"name": "Intelligence", "level": 3}
    ],
    "skills": [
      {"name": "Spellcraft", "level": 4}
    ],
    "special": ["Must have Mage perk"]
  },
  "notes": "High-level transportation magic requiring significant investment",
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
- **attributes**: Which attributes are used for spellcraft rolls and how they combine
- **tier**: Power level (0=cantrip, 5=legendary magic)
- **apCost**: Action points required to cast the spell
- **limit**: Limit points consumed (core magic system resource)

### Effects and Targeting
- **damage**: Damage formula, type, and scaling for combat spells
- **duration**: How long the spell's effects persist
- **complexity**: Whether this is a basic or advanced spell for learning requirements
- **range/area/targeting**: Spatial mechanics for spell application

### Magic System Integration
- **components**: What is required to cast (verbal, somatic, material, focus)
- **school**: Magical tradition or element for organization and specialization
- **scaling**: How the spell improves with higher tiers, attributes, or limit investment

### Learning and Prerequisites
- **prerequisites**: Requirements to learn the spell (other spells, attributes, skills, special conditions)
- **restrictions**: Limitations on when or how the spell can be cast

This template captures the complexity of the Exceed magic system while remaining structured for digital implementation.