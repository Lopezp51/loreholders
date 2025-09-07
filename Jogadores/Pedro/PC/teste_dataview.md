```datacards

TABLE Casting_Time, Range, Components, Duration, cover, status

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
booleanDisplayMode: "checkbox"

  

```





```dataview
TABLE WITHOUT ID
  file.link as "Feitiço",
  done as "✅ Preparado?"
from #Paladin_Spell_List
sort file.name asc

```



```dataview
list from #Paladin_Spell_List
sort file.name asc
```



```dataviewjs
const pages = dv.pages("#Paladin_Spell_List").sort(p => p.file.name, 'asc');

const rows = pages.map(p => {
  const pathNoMd = p.file.path.replace(/\.md$/,'');

  // Toggle editável (done)
  const doneBlock =
`~~~meta-bind
INPUT[toggle:${pathNoMd}#done]
~~~`;

  // Valores fixos (com fallback para "Casting Time" ou "Casting_Time")
  const casting = p["Casting_Time"] ?? p["Casting Time"] ?? "";
  const range = p.Range ?? "";
  const components = Array.isArray(p.Components) ? p.Components.join(", ") : (p.Components ?? "");
  const duration = p.Duration ?? "";
  const txt = p.txt ?? "";

  return [p.file.link, doneBlock, casting, range, components, duration, txt];
});

dv.table(["Spells", "✅ Preparado?", "Casting Time", "Range", "Components", "Duration", "Description"], rows);
```

