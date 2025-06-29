```dataviewjs
const pages = dv.pages().where(p => p.tags);
let tagCounts = {};

// Count key tags
for (let page of pages) {
  const tags = Array.isArray(page.tags) ? page.tags : [page.tags];
  for (let tag of tags) {
if (['eventos_era_de_ouro', 'localidades_era_de_ouro', 'npc_era_de_ouro', 'npc', 'mayor', 'individual', 'widow', 'third', 'lore'].includes(tag)) {
      tagCounts[tag] = (tagCounts[tag] || 0) + 1;
    }
  }
}

// Data
const labels = Object.keys(tagCounts);
const counts = Object.values(tagCounts);

// 💀 Grunge palette
const colorMap = {
  rancher: '#c8ae5f', // antique gold
  wrecking_crew: '#9e9e9e',   // blood rust red
  loyalist: '#D66843',  // steel blue
  pirate: '#91a6ba',   // swamp green
  mayor: '#F3DB07', // some color
  individual: '#F56800', // orangey
  widow: '#ffccff', // widow white
  third: '#A15CA1',
  lore: '#b7bbbc', // widow white
  
};
const backgroundColors = labels.map(label => colorMap[label] || '#777');

// Chart config
const chartData = {
    type: 'bar',
    data: {
        labels: labels,
        datasets: [{
            label: 'Characters',
            data: counts,
            backgroundColor: backgroundColors,
            borderColor: '#222',
            borderWidth: 1
        }]
    },
    options: {
        plugins: {
            legend: {
                labels: {
                    color: '#CCC'
                }
            }
        },
        scales: {
            x: {
                ticks: { color: '#CCC' },
                grid: { color: '#444' }
            },
            y: {
                ticks: { color: '#CCC' },
                grid: { color: '#444' }
            }
        }
    }
};

window.renderChart(chartData, this.container);
```

