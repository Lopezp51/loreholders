---
cssclasses:
  - b-sides-script
Player: Cassandra
Role: Player
level: 5
hp: 49
max_hp: 
ac: 18
modifier: 3
pasperc: 9
PlayerKnownLanguages:
  - Celestial
  - Common
  - Dwarvish
char_status: Alive
---

> [!column-img|no-title]
>> [!NOTE|clean no-i right]+ Cassandra  
>> ![[Cassandra_1.png|620]]
>
>> [!note|no-title] Place Name
>>  ~~~meta-bind
>> INPUT[select(
>> option(1, ℹ️Geral),
>> option(2, 📜Habilidades),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box|10]
>>> > [!div-m|no-title]
>>> > ![[#Geral|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#Habilidades|no-h clean]]
>
>> [!note|no-title] Place Name
>>  ~~~meta-bind
>> INPUT[select(
>> option(1, 🗣️RUMORES),
>> option(2, 🔒SEGREDOS),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box-maxh]
>>> > [!div-m|no-title]
>>> > ![[#RUMORES|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#SEGREDOS|no-h clean]]
>>









---

# Geral

```dataviewjs
const lvl = dv.current().level;
const ac = dv.current().ac;
const mod = dv.current().modifier;

// Initiative string with plus sign if positive
const initStr = (typeof mod === "number" && mod > 0) ? `+${mod}` : `${mod}`;


// build badges array
const badges = [
  { label: "Level",           value: lvl        },
  { label: "Initiative",      value: initStr    },
  { label: "Spell Save",      value: 14         },
  { label: "AC",              value: ac         }
];

// serialize to a ```badges block
let out = "```badges\nitems:\n";
for (let b of badges) {
  const v = typeof b.value === "number" ? b.value : `'${b.value}'`;
  out += `  - label: ${b.label}\n    value: ${v}\n`;
}
out += "```";

// render it
dv.paragraph(out);
```

```dataviewjs
// grab your hp value
const hp = dv.current().hp;

// (optional) if you want hitdice dynamic, you could pull them similarly:
// const dice = dv.current().hitdice?.dice || "d6";
// const diceValue = dv.current().hitdice?.value || 3;
// here we'll hard-code them as in your example:
const dice = "d10";
const diceValue = 5;

// build the healthpoints YAML block
let out = "```healthpoints\n";
out += `state_key: din_health\n`;
out += `health: ${hp}\n`;
out += `hitdice:\n`;
out += `  dice: ${dice}\n`;
out += `  value: ${diceValue}\n`;
out += "```";

// render it into your note
dv.paragraph(out);
```


# Habilidades 

```ability
abilities:
  strength: 8
  dexterity: 18
  constitution: 16
  intelligence: 8
  wisdom: 8
  charisma: 16

proficiencies:
  - charisma
  - wisdom
```

<br>

```skills
proficiencies:
  - Acrobatics
  - Deception
  - Intimidation
  - Persuasion
  - Sleight of Hand
  - Stealth

bonuses:
  - name: fix
    target: Acrobatics
    value: 1
  - name: fix
    target: Deception
    value: 1
  - name: fix
    target: Intimidation
    value: 1
  - name: fix
    target: Persuasion
    value: 1
  - name: fix
    target: Sleight of Hand
    value: 1
  - name: fix
    target: Stealth
    value: 1

```

# Description

...

# Configure

| Stat     | Value                        |
| -------- | ---------------------------- |
| Status   | `INPUT[inlineSelect(option(Alive), option(Dead)):char_status]`                             |
| Race     |   `INPUT[template-Race][:char_race]`                            |
| Class    | `INPUT[inlineSelect(option(Infant), option(Child), option(Teenager), option(Young Adult), option(Adult), option(Elder)):char_class]`                              |
| Level    | `INPUT[number:level]`        |
| Gender   | `INPUT[inlineSelect(option(Male), option(Female), option(Other)):char_gender]`                              |
| Age      | `INPUT[inlineSelect(option(Infant), option(Child), option(Teenager), option(Young Adult), option(Adult), option(Elder)):char_age]`                              |
| HP       | `INPUT[number:hp]`           |
| Max HP   | `INPUT[number:player_maxhp]` |
| AC       | `INPUT[number:ac]`           |
| Modifier | `INPUT[number:modifier]`     |


# GM Notes

Make notes of what you need to track in the town here. 

# Skillsssss



```ability
abilities:
  strength: 8
  dexterity: 18
  constitution: 16
  intelligence: 8
  wisdom: 8
  charisma: 16

proficiencies:
  - charisma
  - wisdom
```

<br>

```skills
proficiencies:
  - Acrobatics
  - Deception
  - Intimidation
  - Persuasion
  - Sleight of Hand
  - Stealth

bonuses:
  - name: fix
    target: Acrobatics
    value: 1
  - name: fix
    target: Deception
    value: 1
  - name: fix
    target: Intimidation
    value: 1
  - name: fix
    target: Persuasion
    value: 1
  - name: fix
    target: Sleight of Hand
    value: 1
  - name: fix
    target: Stealth
    value: 1

```


# Traits

### Luck Points
```consumable
label: ""
state_key: din_luck_points
uses: 3
```

You have inexplicable luck that seems to kick in at just the right moment.

**You have 3 luck points.** Whenever you make an attack roll, an ability check, or a saving throw, you can spend one luck point to roll an additional d20. You can choose to spend one of your luck points **after you roll the die, but before the outcome is determined**. You choose which of the d20s is used for the attack roll, ability check, or saving throw.

You can also spend one luck point when an **attack roll** is made against you. Roll a d20 and then choose whether the attack uses the attacker's roll or yours.

If more than one creature spends a luck point to influence the outcome of a roll, the points cancel each other out; no additional dice are rolled.

You regain your expended luck points when you finish a long rest.

### Arcane Recovery
```consumable
label: ""
state_key: din_arcane_recovery
uses: 1
```

You have learned to regain some of your magical energy by studying your spell book. Once per day when you finish a **short rest**, you can choose expended spell slots to recover. The spell slots can have a combined level that is equal to or **less than half your wizard level** (rounded up), and none of the slots can be 6th level or higher.

For example, if you're a 4th-level wizard, you can recover up to two levels worth of spell slots. You can recover either a 2nd-level spell slot or two 1st-level spell slots.

### Researcher

When you attempt to learn or recall a piece of lore, **if you do not know that information, you often know where and from whom you can obtain it**.

Usually, this information comes from a library, scriptorium, university, or a sage or other learned person or creature.

Your DM might rule that the knowledge you seek is secreted away in an almost inaccessible place, or that it simply cannot be found. Unearthing the deepest secrets of the multiverse can require an adventure or even a whole campaign.

# Spell Book

## Spell Slots

```consumable
items:
  - label: "Level 1"
    state_key: din_spells_1
    uses: 4
  - label: "Level 2"
    state_key: din_spell_2
    uses: 2
```

### Fey Touched

```consumable
items:
  - label: "Misty Step"
    state_key: din_fey_touched_misty_step
    uses: 1
  - label: "Silvery Barbs"
    state_key: din_fey_touched_silvery_barbs
    uses: 1
```

> [!NOTE]- Prepared
> List Spells Here

> [!NOTE]+ Known
> List Spells Here

# Inventory

The following items belong to `= this.file.name`.

Items: `INPUT[inlineListSuggester(optionQuery(#Category/Quest)):char_items]`

#### Ring of Investigation
```consumable
label: ""
state_key: din_items__ring_of_investigation
uses: 3
```

_May the ability to see also provide you with a clear vision" Grants +1 to Investigation Roles_


```ability
abilities:
  strength: 8
  dexterity: 18
  constitution: 16
  intelligence: 8
  wisdom: 8
  charisma: 16

proficiencies:
  - charisma
  - wisdom
```

<br>

```skills
proficiencies:
  - Acrobatics
  - Deception
  - Intimidation
  - Persuasion
  - Sleight of Hand
  - Stealth

bonuses:
  - name: fix
    target: Acrobatics
    value: 1
  - name: fix
    target: Deception
    value: 1
  - name: fix
    target: Intimidation
    value: 1
  - name: fix
    target: Persuasion
    value: 1
  - name: fix
    target: Sleight of Hand
    value: 1
  - name: fix
    target: Stealth
    value: 1

```

