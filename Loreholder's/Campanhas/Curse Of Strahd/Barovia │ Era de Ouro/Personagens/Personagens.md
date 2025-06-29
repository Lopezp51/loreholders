---
cssclasses:
  - b-sides-script
cover: [[Loreholder's/media/strahd/paginas/char_img.png]]
conexao: [[Barovia │ Era de Ouro]]
descricao: Heróis, traidores, santos e monstros disfarçados de gente.
tags:
  - barovia_era_de_ouro
---
# PERSONAGENS

```datacards
TABLE img, status, Afiliação, Localização
FROM #npc_era_de_ouro
SORT Localização ASC 

// Settings
preset: cover
imageSize: xlarge
imageProperty: img
imagePosition: center
columns: 7
lazyLoad: true

```