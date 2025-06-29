<%*
const nome = await tp.system.prompt("Nome do Personagem");
await tp.file.rename(nome);

const status = await tp.system.prompt("Status (Ex: Vivo, Morto, Desaparecido)");
const img = await tp.system.prompt("Nome da imagem principal (sem extensão)");

tR += `---
cssclasses:
  - npc-card
  - b-sides-script
tags: 
  - npc
  - npc_era_de_ouro

img: "[[${img}.png]]"
status: ${status}
Afiliação: ???
Localização: ???
aparicao:
  - 
---

> [!NOTE|clean no-i right]+ ${nome}  
> ![[${img}.png|500]]  

# ** ${nome} **

**Descrição:**  
...

### **Segredos ou Boatos:**  
...

### **Citação Marcante:**  
> "..."

### **Primeira Aparição:** ??? 
...

---

> [!groups_test]+ Aparições  
> \`\`\`dataview
> list
> from ## tramas_era_de_ouro ALTERAR
> where contains(this.aparicao, file.name)
> sort file.name asc
> \`\`\`

---

### 🖼️ **Galeria de Imagens Alternativas**

<div class="npc-gallery">
    <img src="${img}.png" alt="${nome}" />
</div>
`
%>
