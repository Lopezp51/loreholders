---
cssclasses:
  - b-sides-script
conexao: [[Localidades]]
tags: 
 - localidades_era_de_ouro
img: "[[vila_barovia_full.png]]"
descricao: A Vila de Barovia aninha-se no vale como um suspiro de pedra e madeira, perpetuamente enredada nas brumas que o próprio castelo exala. Diferente de outras terras que aprenderam a erguer muralhas de esperança contra o medo, Barovia permanece estagnada, seus telhados inclinados sob o peso de invernos intermináveis e preces que raramente encontram resposta. Sem burgomestre, é o capitão da guarda quem tenta impor ordem a um povo acostumado a sobreviver mais do que a viver.
---

<h2>Vila de Barovia</h2>

> [!column-img|no-i no-t]
>> [!info|no-title] Map
>> ```leaflet  
>> id: vila_de_barovia
>> image: media/strahd/Localidades/vila_de_barovia.png
>> bounds: [[0,0], [5000, 4025]] ### Size of the map in px Height_y, Width_x. Ignore 0,0  
>> height: 500px ### Size of the leaflet embed in px on your screen  
>> width: 95% ### Size of the leaflet embed in your note  
>> lat: 2500 ### To center the map, make this half of the map height.  
>> long: 2012.5 ### To center the map, make this half of the map width.  
>> minZoom: -3 ### Controls how far away from the map you can zoom out. Hover over the target icon to see the current level.  
>> maxZoom: 1 ### Controls how far towards the map you can zoom in. Hover over the target icon to see the current level.  
>> defaultZoom: -3 ### Sets the default zoom level when the map loads. Hover over the target icon to see the current level.  
>> zoomDelta: 0.5 ### Adjust how much the zoom changes when you zoom in or out.  
>> unit: mi ### The value displayed when measuring so you know what type of unit is being measure.  
>> scale: 0.09328358208955223 ### Real units/px (resolution) of your map  
>> recenter: false  
>> darkmode: false ### marker
>> ```
>
>> [!note|no-title] Town Name
>> ~~~meta-bind
>> INPUT[select(
>> option(1, 📜DESCRIÇÃO),
>> option(2, 👤RESIDENTES),
>> option(3, 🗺️LOCAIS),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box-maxh]
>>> >[!div-m|no-title]
>>> > ![[#Descrição|no-h clean]]
>>>
>>> >[!div-m|no-title]
>>> > ![[#Residentes da Vila de Barovia|no-h clean]]
>>>
>>> > [!div-m|no-title]
>>> > ![[#Locais|no-h clean]]
>>> 



# Descrição
A Vila de Barovia aninha-se no vale como um suspiro de pedra e madeira, perpetuamente enredada nas brumas que o próprio castelo exala. Diferente de outras terras que aprenderam a erguer muralhas de esperança contra o medo, Barovia permanece estagnada, seus telhados inclinados sob o peso de invernos intermináveis e preces que raramente encontram resposta.

Sem burgomestre , é o capitão da guarda quem tenta impor ordem a um povo acostumado a sobreviver mais do que a viver. Ruas lamacentas serpenteiam entre casas fechadas a pregos e olhares desconfiados, enquanto velhas lamparinas oscilam na ventania, prometendo uma luz que mal afasta as sombras. Nesta aldeia solitária, até o silêncio parece guardar rancor — lembrando, a cada passo, que em Barovia o passado nunca se rende, e o futuro raramente chega.

De todas as [[Cidades]], é a pior cidade para se viver atualmente.




# Residentes da Vila de Barovia

```datacards
table img, status, dateformat(file.mtime, "dd/MM/yyyy") as "Última Edição"
from #npc_era_de_ouro
where contains(string(Localização), "Vila de Barovia")
sort file.mtime desc

// Settings
preset: compact
imageSize: small
fontSize: small
imageProperty: img
imagePosition: center
columns: 4
lazyLoad: true

```

# Locais

[🛖 Casa da Party](obsidian://open?vault=DisgracelandOnline&file=Loreholder's%2FCampanhas%2FCurse%20Of%20Strahd%2FBarovia%20%E2%94%82%20Era%20de%20Ouro%2FLocalidades%2FCidades%2FVila%20de%20Barovia%2FCasa%20Leste%20da%20Party.canvas): Casa atual do Time Nº1

[⛪ Igreja do Sol](obsidian://open?vault=DisgracelandOnline&file=Loreholder's%2FCampanhas%2FCurse%20Of%20Strahd%2FBarovia%20%E2%94%82%20Era%20de%20Ouro%2FLocalidades%2FCidades%2FVila%20de%20Barovia%2FIgreja%20Vila%20de%20Barovia%20do%20Sol.canvas)

🍺Sangue no Vinho

🛖Fazenda do Velho Ernest

🛖Açougue Porco Feliz

🛖Mercantil de Bildrath

🛖Correios

🛖Casa da vó Wensencia