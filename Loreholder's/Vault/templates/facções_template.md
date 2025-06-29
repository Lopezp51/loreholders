<%*
const faccao = await tp.system.prompt("Nome da Facção");
await tp.file.rename(faccao);
const reputacao = await tp.system.prompt("Reputação Pública");
const tag = await tp.system.prompt("Nome da tag da facção. Ex: facção_era_de_ouro");
const integrantes = await tp.system.prompt("Nome da tag dos integrantes. EX: casa_van_der_voort");
const img = await tp.system.prompt("Nome da imagem");

tR += `---
cssclasses:
  - npc-card
  - b-sides-script
tags:
  - ${tag}

img: 
status: Ativa
Afiliação: ???
Localização: ???

---
# ${faccao}

> [!NOTE|clean no-i right]+ Símbolo  
> ![[${img}.png|400]]

> [!column] 📚
>> [!rustwater] Informações  
**Fundador:** ???  
**Reputação Pública:** ${reputacao}  
**Líder Atual:** ???  
**Status:** Ativa  
**Sede Principal:** ???  
>
>> [!rustwater] Aliados  
>> ...
>
>> [!rustwater] Inimigos  
>> ...
>
>> [!rustwater] Rumores e Segredos  
>> ...

---

> [!tramas]+ INTEGRANTES  
> \`\`\`datacards
> TABLE img, status FROM #${integrantes}
> SORT file.name asc
> 
> // Settings 
> preset: compact 
> columns: 5
> cardSpacing: 4
> imageProperty: img
> fontSize: small
> \`\`\`

---

## História

> <h4>“...”</h4>

---
`
%>
