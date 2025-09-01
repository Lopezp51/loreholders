---
cssclasses:
  - b-sides-script
tags:
  - title
---

<div style="text-align: center;">
  <img src="loreholders_img.png">
</div>
<br>

<div class="homepage">
<hr>
</div>



> [!world]+ Campanhas
> ```datacards 
> TABLE cover, status, inicio as "Inicio", fim as "Fim" FROM #campanha
> SORT inicio ASC
> 
> // Settings 
> preset: square 
> columns: 5
> cardSpacing: 4
> imageProperty: cover
> ```

---
> [!infobox] 
>```calendarium
>```
> **ÚLTIMAS TRAMAS:**
>```datacards 
>TABLE cover, dateformat(file.ctime, "dd/MM/yyyy") as "Data"
>FROM #tramas
>SORT file.ctime desc
>limit 3
>
>// Settings 
>preset: compact 
>columns: 1 
>imageProperty: cover
>imageWidth: 50px
>```

> [!infobox] 
> [🗺️ Mapa de Faerûn](obsidian://open?vault=obsidian&file=Loreholder's%2FO%20Mundo%2FMapa%20de%20Faer%C3%BBn)
> [📜 Lore](obsidian://open?vault=obsidian&file=Loreholder's%2FO%20Mundo%2FLore)
> [⚔️ Party's](obsidian://open?vault=obsidian&file=Loreholder's%2FO%20Mundo%2FParty's)


> [!world]+ Últimos Personagens  Modificados
> ```dataview
> table 
>   status, 
>   aparicao,
>   "<span style='font-size: 0.85em; color: #bbb;'>" + date(file.mtime) + "</span>" as "TIME/DATE"
> from #npc
> sort file.mtime desc
> limit 5
> ```

---

> [!world]+ Últimas Modificações
>```dataview
> TABLE WITHOUT ID
>   link(file.path, file.folder + " / " + file.name) AS "Last Modified",
>   file.mtime AS "Date"
> FROM "/"
> WHERE file.mtime >= date(today) - dur(30 days)
> AND file.name != this.file.name
>     AND !contains(file.path, "z_Assets")
>    AND !contains(file.path, "Inline Scripts")
>     AND !contains(file.path, "z_Templates")
>     AND !contains(file.path, "daily notes")
>     AND !contains(file.path, "BRAT")
> SORT file.mtime DESC
> LIMIT 10
>```

2025, © **Loreholder's**
