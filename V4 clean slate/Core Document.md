# Exceed TTRPG

## Game Overview

*A tabletop role-playing game*

### Core Concept
[Describe the central theme, setting, or unique mechanics of your game]

### Target Audience
[Who is this game designed for? New players, experienced gamers, specific age groups?]

## Core Rules

### Basic Mechanics
[Core dice mechanics, resolution system, basic gameplay loop]

### Character Creation

**Step 1:** Select a name and concept for your character.

**Step 2:** GM awards starting Character Points (CP) in two categories:

**CP Categories:**
- **Combat XP:** HP (Tough perk), combat skills, combat-related perks
- **Social XP:** Social, knowledge, crafting, wilderness skills, and related perks

**Step 3:** Spend CP on skills and perks. Each purchase shows (Attribute1) or (Attribute1/Attribute2) indicating which attributes benefit. CP spent creates attribute points that you allocate between the listed attributes. When attributes reach tier thresholds (10/30/60/100/150), you gain +1 to that attribute.

**Step 4:** Calculate bonus actions:
- **Mental Actions:** Every 5 total Mental attributes (Perception + Will + Charisma + Wit) = +1 Mental Action
- **Physical Actions:** Every 5 total Physical attributes (Might + Endurance + Agility + Dexterity) = +1 Physical Action

**Step 5:** Select starting gear and calculate final statistics:
- **HP:** Max Toughness × (5 + Armor) + Extra HP
- **Initiative:** 2d10 + Perception
- **Movement and damage based on equipment and attributes** 

#### Attributes
[Core character stats/attributes]

#### Skills/Abilities
[Character skills, powers, or special abilities]

### Gameplay

#### Turn Structure
[How turns/rounds work during play]

#### Conflict Resolution
[How challenges, combat, or other conflicts are resolved]

## Setting

### World/Universe
[The game world, its history, geography, cultures]

### Important Locations
[Key places in your setting]

### NPCs & Factions
[Important non-player characters and organizations]

## Game Master Section

### Running the Game
[Guidance for GMs]

### Adventure Hooks
[Story seeds and plot ideas]

### Enemies/Challenges
[Antagonists, obstacles, stat blocks]

## Equipment & Resources

### Gear
[Weapons, armor, tools, etc.]

### Magic/Technology
[Special items, spells, tech if applicable]

## Optional Rules

### Advanced Mechanics
[Complex or optional rules for experienced players]

### Variants
[Alternative ways to play]

## Designer Notes

### Development Log
[Track changes and design decisions as you develop]

### Playtesting Notes
[Record feedback and observations from testing]

# Design Decisions & Logic

### Unique Selling Proposition (USP)

**The Limit System** - The core innovation of Exceed is the "Limit" stat, which governs the maximum number of persistent magical and non-magical effects a character can sustain simultaneously.

#### Problem Solved
Traditional systems suffer from "pre-buff" issues where players stack numerous temporary bonuses before encounters, and "magic item bloat" where characters accumulate dozens of persistent magical effects. D&D 5e attempts to address this with concentration, time limits, and attunement slots, while PF2E uses 10 attunement slots but still allows hundreds of different buffs to stack.

#### Solution: Limit
The Limit stat creates a hard cap on the total number of active persistent effects, forcing meaningful tactical choices:
- Players must prioritize which effects to maintain
- No endless stacking of buffs
- Clear, trackable resource management
- Scales with character power (Limit increases as characters advance)
- Applies to all persistent effects: spells, permanent magic items, class abilities, etc.

This system eliminates bookkeeping nightmares while maintaining strategic depth through meaningful choice constraints.

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



---

*Last Updated: [Date]*
*Version: 0.1*
...

### Core Resolution System

**Formula:** 2d10 + Skill + Attribute + Bonuses vs. Difficulty

**Skill Application:**
- **Direct skill use:** Full skill bonus (e.g., Dancing to dance)
- **Raw attribute:** Attribute only, no skill bonus (e.g., Agility only to dance gracefully)
- **Related skill:** GM assigns -1 to -3 penalty based on how related (e.g., Fast-talk at -2 to cover bad dancing)
- **Creative alternatives:** GM discretion on penalty for innovative approaches

**Key Features:**
- Skills and attributes capped at 5 for bounded accuracy
- Positive feedback loop: Higher skills → higher attributes → better performance with related skills
- Players choose which attribute to increase when raising skills
- GM determines appropriate skill/attribute combinations and penalties situationally




## Skills System

### Social Skills

**1. Dancing** (Agility/Charisma) - Formal and social dancing, grace in movement, social positioning through performance

**2. Negotiating** (Charisma/Wit) - Making deals, bargaining, diplomatic solutions, finding win-win outcomes

**3. Manipulation** (Charisma/Will) - Subtle influence, psychological pressure, making people think your ideas are theirs

**4. Leadership** (Charisma/Will) - Inspiring groups, command presence, rallying others in crisis situations

**5. Fast-talk** (Charisma/Agility) - Quick convincing, rapid lies and truths, overwhelming with words, time-pressure persuasion

**6. Singing** (Endurance/Charisma) - Vocal performance, crowd entertainment, emotional resonance through music

**7. Gossip** (Charisma/Perception) - Information gathering, rumor trading, social intelligence, reputation management

### Athletic/Acrobatic Skills

**1. Running** (Agility/Endurance) - Speed and endurance movement; choose Agility for sprinting/quick bursts or Endurance for long-distance running

**2. Climbing** (Might/Agility) - Scaling walls, cliffs, buildings; vertical movement and grip strength

**3. Swimming** (Endurance/Might) - Aquatic movement, underwater endurance, water rescue

**4. Jumping** (Might/Agility) - Explosive leg power, long jumps, high jumps, parkour leaps

**5. Acrobatics** (Agility/Dexterity) - Tumbling, flips, balance, contortion, graceful movement, fall mitigation, tightrope walking, escaping bonds, squeezing through spaces

**6. Lifting** (Might/Endurance) - Raw strength application, moving heavy objects, feats of strength

**7. Breaking** (Might/Wit) - Destructive force application, knowing weak points, demolition work

### Crafting Skills

**1. Smithing** (Might/Dexterity) - Metalwork, jewelry, weapons, armor, tools

**2. Woodworking** (Dexterity/Wit) - Carpentry, furniture, bows, wooden tools, construction

**3. Textilework** (Dexterity/Perception) - Leatherworking, tailoring, rope-making, fabric crafts

### Natural Sciences

**1. Biology** (Wit/Perception) - Living organisms, anatomy, plant identification, natural remedies, organic poisons

**2. Chemistry** (Wit/Dexterity) - Chemical processes, explosives, acids, synthetic compounds, material properties

**3. Medicine** (Wit/Dexterity) - Healing, surgery, anatomy, practical medical treatment

### Stealth/Criminal Skills

**1. Stealth** (Agility/Perception) - Moving unseen, hiding, avoiding detection

**2. Lockpicking** (Dexterity/Perception) - Bypassing mechanical security, opening locked containers

**3. Sleight of Hand** (Dexterity/Agility) - Pickpocketing, palming objects, manual dexterity tricks

### Wilderness Skills

**1. Survival** (Endurance/Perception) - Wilderness living, foraging, finding shelter and water

**2. Tracking** (Perception/Wit) - Following trails, reading signs, hunting quarry

**3. Navigation** (Perception/Wit) - Finding your way, reading maps, celestial navigation

### Knowledge Skills

**1. Arcane Lore** (Wit/Will) - Magic theory, spell identification, understanding magical phenomena

**2. History** (Wit/Will) - Past events, cultures, legends, political knowledge

**3. Theology** (Will/Charisma) - Divine knowledge, rituals, religious traditions

**4. Street Wisdom** (Charisma/Perception) - Criminal underworld knowledge, black market connections
<!--  -->
### Skill Progression
- Skills range from 1-5, providing flat bonuses to related rolls
- Separate perk system provides special abilities with skill prerequisites
- Players choose which attribute to increase when raising skills
- Potions are created through spellcrafting (liquid spells) rather than mundane skills

## Hit Points and Wounds System

### Base Health
All human characters start with:
- **2 Mex Wounds**  
- **5 HP per Wound** (spieces dependent, will be 5 for the time being)
- **Total Starting HP: 10**

### HP Calculation
**Total HP = Max Wounds × (5 + Armor Bonus+Endurance)+ExtraHP**
  - Stamina HP: First half (recovers quickly)
  - Health HP: Second half (real damage)
On stamina HP deplition roll on [Minor conditions table] according to the table rules.
On health HP deplition roll on [Major conditions table] accoring to the table rules, fall unconcious and mark off 1 wound. If you exceed Max Wounds - you die.


### Increasing Hit Points

#### Perk: Tough (Endurance/Will)
- **Cost:** MaxWounds * XP per HP
- **Consolidation:** Every 5 HP (change with race HP in later interations) purchased becomes +1 Wound.  The new wound gains full armor bonus like existing wounds
- **Example:** Character with +2 Armor has 4 extra HP
  - Current: 2 wounds × 7 HP + 4 HP = 18 total HP  
  - After buying 1 more HP: 3 wounds × 7 HP = 21 total HP

### Progression Examples
- **Starting:** 2 wounds × 5 HP = 10 total HP (12 with armor 1)
- **+1 Wound (10 XP):** 3 wounds × 5 HP = 15 total HP (21 with armor 2)
- **+2 Wounds (20 XP):** 4 wounds × 5 HP = 20 total HP (32 with armor 3)

## Combat Resolution
## Action Economy

**Base Actions:** 5 actions per turn for all characters

**Specialization Bonuses:**
- **Mental Actions:** Every 5 total points in Mental attributes (Perception + Will + Charisma + Wit) grants +1 Mental Action
- **Physical Actions:** Every 5 total points in Physical attributes (Might + Endurance + Agility + Dexterity) grants +1 Physical Action

**Action Restrictions:**
- Mental Actions can only be used for mental tasks: spells, social interactions, knowledge checks, perception, concentration
- Physical Actions can only be used for physical tasks: movement, attacks, athletics, manual tasks
- Base 5 actions can be used for either type

**Design Benefits:**
- Specialists get more actions in their domain of expertise
- Generalists maintain flexibility with unrestricted base actions
- Prevents "agility dominance" by spreading bonuses across multiple attributes
- Creates meaningful choice between specialization and versatility


### Determining Initiative

- **Standard Encounters:** Initiative = 2d10 + Perception attribute. This reflects awareness, reaction time, and mental preparedness when combat begins unexpectedly.
- **Ambushes or Prepared Battles:** When initiating an ambush, relevant skills can provide modifiers to the initiative roll.
- **Ties:** Players go first in case of ties.
- **Modifiers:** Spells, abilities, and circumstances provide bonuses to initiative rolls.
- **Delaying:** Done before the beginning of your turn to a predetermined point, only once per round. All beginning/end of turn effects are delayed with your action.

### Surprise Rounds

- **Ambush Coordination:** Ambushing side rolls initiative as one group using their leader's roll, representing coordinated surprise attacks.
- **Stunned Targets:** Ambushed combatants who roll 5 or lower than the ambush leader become Stunned 3 (lose first 3 actions, cannot use reactions) as they process the situation.
- **Ambush Sites:** Favorable ambush locations can provide bonuses to the ambush initiative roll.

## Attacking and Defending
### Defensive Options
There are 3 main defensive options in the game.
Parry - WeaponsSkill + Agility/Dexterity (based on weapon type)
Dodge - Agility+Perception 
Block - ShieldSkill+Agility/Endurance (based on shield type)
Shields provide Defensive bonus that adds to all three abilities if raised.
Magic can provide other defensive options, according to the spells used.
### Offensive Options
All melee weapons use Agility as the main stat for offensive maneuvers.
Heavy - Allowing using might (generally heavy, blunt weapons)
Finesse - Allowing using Dexterity (generally piercing/slashing weapons).

Ranged weapons use Dexterity or Perception based on weapon type.

Certain perks allow to change the Attached attribute.

### Offensive Abilities
Offensive abilities can be normal - allowing all 3 defenses  have traits of:
AOE - can't parry without a perk or gear
Ranged - can't parry without a perk or gear
Unblockable - can't be blocked without a perk or gear


### Rolling for Damage 
When the attack hits roll for damage. 
Damage = WeaponDice+Attribute+Bonuses
Weapon skill determines the number of damage dice.
  - Skill 1-2: 1 dice
  - Skill 3-4: 2 dice
  - Skill 5+: 3 dice
Magic weapons can have an attribute and limit requirnment. They will provide the basic bonus to attacks, but won't provide other benefits like an increased die size, extra damage type, magical effects etc.
Light weapons generally have 1d4-1d6 WeaponDice, Normal - d6-d8, Heavy D8-D12.

  

## Actions in Combat
### Basic Strike
Each weapon takes 2-4 (maybe 1-3) action points to attack normaly, stepping 1 square forward as a part of the action. Light weapons - 2 action points, Normal (without a light or heavy trait) take 3 actions and heavy take 4 actions.
The action cost can be modified, combined or compressed with appropriate combat perks.

