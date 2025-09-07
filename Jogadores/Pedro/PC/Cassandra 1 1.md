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
lay_on_hands: 25
---


> [!note|no-title] Place Name
>  ~~~meta-bind
> INPUT[select(
> option(1, ℹ️Geral),
> option(2, 📜Habilidades),
> option(3, ⚙️ 1º nível),
> class(tabbed)
> )]
> ~~~
>>[!tabbed-box|10]
>> > [!div-m|no-title]
>> > ![[#Geral|no-h clean]]
>>
>> > [!div-m|no-title]
>> > ![[#Habilidades|no-h clean]]
>>
>> > [!div-m|no-title]
>> > ![[#1 nível|no-h clean]]




---

# Geral

```badges
items:
  - label: Level
    value: 5
  - label: Iniciativa
    value: + 4
  - label: Save DC
    value: 14
  - label: AC
    value: 18
dense: 0
```

```healthpoints
state_key: din_health
health: 49
hitdice:
  dice: d10
  value: 5

reset_on: ["short-rest", "long-rest"]
```
	            🧬 Features & Traits 
```consumable
items:
  - label: "🕊️ Divine Sense"
    state_key: divine_sense
    uses: 4
    reset_on: long-rest  
  - label: "🧠 Knowledge from a Past Life"
    state_key: past_life
    uses: 3
    reset_on: long-rest  
  - label: "🌌 Channel Divinity"
    state_key: channel_divinity
    uses: 1
    reset_on:
      - event: short-rest
        amount: 1  
      - event: long-rest  
```
 ✨ Lay on Hand  `INPUT[number:lay_on_hands]`     
 
					⚙️ Spell Slots 
```consumable
items:
  - label: "🔹1º nível"
    state_key: first_level
    uses: 4
    reset_on: long-rest  
  - label: "🔹2º nível"
    state_key: second_level
    uses: 2
    reset_on: long-rest  

```
---
```event-btns
items:
  - name: Short Rest
    value: short-rest
  - name: Long Rest
    value: long-rest
```
```badges
items:
  - label: 🔷 Platina
    value: 0
  - label: 🟡 Ouro
    value: 11
  - label: ⚪ Prata
    value: 7
  - label: 🟤 Cobre
    value: 0
dense: 0
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

bonuses:
  - name: ajuste
    target: wisdom
    value: 1
    modifies: saving_throw 
  - name: ajuste
    target: charisma
    value: 1
    modifies: saving_throw 
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


# Spell Book

# 1 nível

```datacards

TABLE Casting_Time, Range, Components, Duration, cover, txt

FROM #Paladin_Spell_List

SORT file.name ASC

  

// Settings

preset: dense

imageSize: small

imageProperty: cover

imagePosition: center

columns: 7

lazyLoad: true

fontSize: small

  

```
## Spell Slots




### teste



### Recursos



```stats
items:
  - label: SPELLCASTING ABILITY
    value: Charisma
  - label: SPELL ATTACK BONUS
    value: + 6
  - label: SAVING THROW DC
    value: 14
  - label: SPELLS TO PREPARE
    value: 5

grid:
  columns: 4
```


