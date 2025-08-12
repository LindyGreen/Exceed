## 1. Skill Levels & Dice Progression 

Skill levels determine what dice you roll for checks. Higher skill = better dice and higher averages, with progression designed for smooth scaling.

| Skill Level | Dice Formula      | Max Roll | Average |
| ----------- | ----------------- | -------- | ------- |
| 1           | 1d4               | 4        | 2.5     |
| 2           | 1d4 + 1           | 5        | 3.5     |
| 3           | 1d4 + 2           | 6        | 4.5     |
| 4           | 2d4               | 8        | 5.0     |
| 5           | 1d4 + 1d6         | 10       | 6.0     |
| n (even)    | 2dN               | 2n       | n + 1   |
| n (odd)     | 1d(N-1) + 1d(N+1) | 2n       | n + 1   |


**Design Notes:**

- Average roll increases steadily from 2 to 20.
    
- At higher skill levels, raw attributes have less relative impact (skill outweighs stat).
    
- The system supports levels above 6 using the same progression pattern (eventually moving into d12s).
    
- For skill levels **4+**, average success is roughly `Skill Level + 1` versus DCs.

## 2. Contested vs. Uncontested Checks

### **Contested Checks** (Opposed Rolls)

Used when two characters are directly opposed — combat, arm-wrestling, sneaking past a guard, etc.

**Process:**

1. Both participants roll their **skill dice**.
    
2. Add the relevant **attribute modifier** and any situational bonuses.
    
3. Compare totals. **Higher total wins**.
    
4. If tied, **attacker wins**.
    

**Example:**

- **Attacker**: Skill 5 → 1d4 + 1d6, Attribute +2 (Control) → Range 4–14
    
- **Defender**: Skill 4 → 2d4, Attribute +0 → Range 2–8
    
- If the attacker’s roll minus defender’s roll ≥ 0, the attacker succeeds.
    

**Competitive Balance:**

- Equal skill: Attacker wins ~37–44% of the time (attacker’s tie-break advantage included).
    
- +1 skill advantage: 50–63% win rate.
    
- +2 skill advantage: 65–81% win rate.
    

---

### **Critical Results** (Optional, TBD)

For extreme successes/failures in opposed rolls:

- **Critical Defender**: Defender’s total ≤ attacker’s smallest die roll.
    
- **Critical Attacker**: Attacker’s total ≥ defender’s smallest die roll.
    
- Adjust effect severity accordingly.
    

---

### **Uncontested Checks**

Used when the outcome is against an objective difficulty, not another character.

**Process:**

1. Roll **skill dice**.
    
2. Add the relevant **attribute modifier** and bonuses.
    
3. Compare total against the **Difficulty Class (DC)**.
    
4. If needed, the **margin of success** (total – DC) can be used for tiered effects.
    

**Notes:**

- No critical results for uncontested checks by default.
    
- Can add degrees of success/failure if the system calls for it.