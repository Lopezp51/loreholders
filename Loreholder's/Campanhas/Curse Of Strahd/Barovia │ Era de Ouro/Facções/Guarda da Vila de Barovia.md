---
cssclasses:
  - npc-card
  - b-sides-script
tags:
  - facção_era_de_ouro
img: "[[guardas da vila de barovia.png]]"
status: Ativa
Afiliação: ???
Localização: ???
Status: Ativa
---



# Guarda da Vila de Barovia


> [!column-img|no-title]
>> [!NOTE|clean no-i right]+ Imagem da Guarda  
>> ![[guardas da vila de barovia.png|400]]
>
>> [!note|no-title] Place Name
>> ~~~meta-bind
>> INPUT[select(
>> option(1, ℹ️INFORMAÇÕES GERAIS),
>> option(2, 👥INTEGRANTES),
>> option(3, 📝HISTÓRIA),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box-maxh]
>>> >[!div-m|no-title]
>>> > ![[#INFORMAÇÕES GERAIS|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ```datacards
>>> > TABLE img, status FROM #facçao_guarda_vila_barovia
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

> [!column|no-title]
>> [!note|no-title] Place Name
>>  ~~~meta-bind
>> INPUT[select(
>> option(1, 🤝ALIADOS),
>> option(2, ⚔️INIMIGOS),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box-maxh]
>>> >[!div-m|no-title]
>>> > ![[#ALIADOS|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#INIMIGOS|no-h clean]]
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

**Fundador:** ???
**Reputação Pública:** 
**Líder Atual:**  [[Vadrik]]
**Status:**  `INPUT[inlineSelect(option(Ativa),  option(Dissolvida), option(Destruída), option(Esquecida), option(Mítica)):Status]`  
**Sede Principal:** [[Vila de Barovia]]


# HISTÓRIA
...


# ALIADOS
...


# INIMIGOS
...


# RUMORES
...


# SEGREDOS
...