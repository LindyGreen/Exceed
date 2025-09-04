### Attribute System - Final Design

**Bottom-Up Skill-Driven System**
- Cannot directly buy attributes - only skills and abilities
- Skills increase related attributes as secondary benefits
- Progressive costs based on total stat increases provided

**Final Attribute Structure:**
```
Mental Attributes:
- Perception, Will, Charisma, Wit

Physical Attributes:
- Might, Endurance, Agility, Dexterity
```

**Examples of Skill → Attribute Growth:**
- Archery skill → increases Dexterity + Perception
- Medicine → increases Wit + Dexterity  
- Running → increases Might + Agility
- Limit training → increases Will + Charisma

**Design Decision:** Removed the hierarchical attribute structure (Body/Mind → 4 main → 8 sub) as it created unnecessary complexity with the bottom-up system. Skills naturally create relationships between the 8 core attributes.

