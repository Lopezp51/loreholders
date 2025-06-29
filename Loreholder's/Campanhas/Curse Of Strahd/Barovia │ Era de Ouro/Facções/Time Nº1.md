---
cssclasses:
  - npc-card
  - b-sides-script
tags:
  - facção_era_de_ouro
img: "[[time_um.png]]"
status: Ativa
Afiliação: ???
Localização: ???
Status: Ativa
---
#  Time Nº1


> [!column-img|no-title]
>> [!NOTE|clean no-i right]+ Brasão  
>> ![[time_um.png|400]]
>
>> [!note|no-title] Place Name
>> ~~~meta-bind
>> INPUT[select(
>> option(1, ℹ️INFORMAÇÕES GERAIS),
>> option(2, 👥INTEGRANTES),
>> option(3, 📝HISTÓRIA),
>>  option(4, 🎒INVENTÁRIO),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box-maxh]
>>> >[!div-m|no-title]
>>> > ![[#INFORMAÇÕES GERAIS|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ```datacards
>>> > TABLE img, status FROM #pc_era_de_ouro
>>> > SORT file.name asc
>>> > 
>>> > // Settings 
>>> > preset: compact 
>>> > columns: 3
>>> > cardSpacing: 4
>>> > imageProperty: img
>>> > fontSize: small
>>> > ```
>>>
>>> > [!div-m|no-title]
>>> > ![[#HISTÓRIA|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#INVENTÁRIO|no-h clean]]
>>> 

> [!column|no-title]
>> [!note|no-title] Place Name
>>  ~~~meta-bind
>> INPUT[select(
>> option(1, 🤝ALIADOS),
>> option(2, ⚔️INIMIGOS),
>> option(3, 🔗CONEXÕES),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box-maxh]
>>> >[!div-m|no-title]
>>> > ![[#ALIADOS|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#INIMIGOS|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#CONEXÕES|no-h clean]]
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



# INFORMAÇÕES GERAIS

**Reputação Pública:** Indiferente  

**Status:** `INPUT[inlineSelect(option(Ativa),  option(Dissolvida), option(Destruída), option(Esquecida), option(Mítica)):Status]`    

**Sede Principal:** ???  




# HISTÓRIA
...

# INVENTÁRIO
...

# ALIADOS
...

# INIMIGOS
...

# CONEXÕES
[[Anna Wachter]]
[[Bel van der Voort]]
[[Cassandra Ashvire]]
[[Malkieer Montelli]]
[[Nikolai]]
[[Loreholder's/Campanhas/Curse Of Strahd/Barovia │ Era de Ouro/Facções/Facções|Facções]]



# RUMORES
...

# SEGREDOS
...
