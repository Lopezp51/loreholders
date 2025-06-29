---
cssclasses:
  - b-sides-script
conexao: [[Localidades]]
tags: 
 - localidades_era_de_ouro
img: "[[Castelo Ravenloft.png]]"
descricao: Castelo Ravenloft ergue-se como vigia solitário sobre toda Barovia, um bastião de pedra gótica que há sessenta e seis anos serve de trono ao Rei Strahd. Suas torres rasgam as névoas eternas, lançando sombras que alcançam cada aldeia e estrada abaixo. Dentro de seus corredores, segredos antigos ainda respiram atrás de portas trancadas, enquanto o eco de passos perdidos testemunha conspirações que jamais viram a luz do dia. Entre muralhas adornadas por gárgulas e tapeçarias de histórias esquecidas, repousa o coração de um reino que aprende, geração após geração, a temer o próprio silêncio.
---

<h2>Castelo Raveloft</h2>




> [!column-img|no-title]
>> [!NOTE|clean no-i right]+ Castelo 
>> ![[Castelo Ravenloft.png|400]]  
>> [🗺️ Mapa do Castelo Ravenloft](obsidian://open?vault=DisgracelandOnline&file=Loreholder's%2FCampanhas%2FCurse%20Of%20Strahd%2FBarovia%20%E2%94%82%20Era%20de%20Ouro%2FLocalidades%2FCastelo%20Ravenloft%2FCastelo%20Ravenloft.canvas)
>
>> [!note|no-title] Town Name
>> ~~~meta-bind
>> INPUT[select(
>> option(1, 📜DESCRIÇÃO),
>> option(2, 👤RESIDENTES),
>> class(tabbed)
>> )]
>> ~~~
>>>[!tabbed-box-maxh]
>>> >[!div-m|no-title]
>>> > ![[#Descrição|no-h clean]]
>>>
>>> >[!div-m|no-title]
>>> > ![[#Residentes do Castelo Ravenloft|no-h clean]]
>>>



# Descrição
**Castelo Ravenloft** ergue-se como vigia solitário sobre toda Barovia, um bastião de pedra gótica que há sessenta e seis anos serve de trono ao Rei Strahd. Suas torres rasgam as névoas eternas, lançando sombras que alcançam cada aldeia e estrada abaixo. Dentro de seus corredores, segredos antigos ainda respiram atrás de portas trancadas, enquanto o eco de passos perdidos testemunha conspirações que jamais viram a luz do dia. Entre muralhas adornadas por gárgulas e tapeçarias de histórias esquecidas, repousa o coração de um reino que aprende, geração após geração, a temer o próprio silêncio.




# Residentes do Castelo Ravenloft

```datacards
table img, status, dateformat(file.mtime, "dd/MM/yyyy") as "Última Edição"
from #npc_era_de_ouro
where contains(string(Localização), "Castelo Ravenloft")
sort file.mtime desc

// Settings
preset: compact
imageSize: small
fontSize: small
imageProperty: img
imagePosition: center
columns: 3
lazyLoad: true

```
