```dataviewjs
const propertyMap = new Map();

for (let page of dv.pages()) {
  if (!page.file.frontmatter) continue;

  for (let key of Object.keys(page.file.frontmatter)) {
    if (!propertyMap.has(key)) {
      propertyMap.set(key, []);
    }
    propertyMap.get(key).push(page);
  }
}

const sortedKeys = Array.from(propertyMap.entries())
  .sort((a, b) => b[1].length - a[1].length);

for (let [key, pages] of sortedKeys) {
  dv.header(3, `${key} (${pages.length})`);
  dv.table(["File", "Value"], 
    pages.map(p => [
      p.file.link, 
      p[key] ?? "*No Value*"
    ])
  );
}
```
