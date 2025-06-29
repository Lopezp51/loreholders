<%*
const nome = await tp.system.prompt("Nome da Criatura");
await tp.file.rename(nome);

const ameaca_num = await tp.system.prompt("Nível de Ameaça (1 a 5)");
const img = await tp.system.prompt("Nome da imagem (sem extensão)");


let ameaca = "💀".repeat(parseInt(ameaca_num));

let tag = "bestiario_era_de_ouro";

tR += `---
cssclasses:
  - npc-card
  - b-sides-script

tags:
  - ${tag}

img: "[[${img}.png]]"
conexao: [[Bestiário]]
ameaca: ${ameaca}
aparicao:
  - 
---

> [!NOTE|clean no-i right]+ ${nome}  
> ![[${img}.png|400]]  

## ** ${nome} **
**Descrição:**  
...

><h4>“...”</h4>

### **Primeira Aparição:** ...  
...

---

> [!groups_test]+ Aparições
>\`\`\`dataview
> list
> from ##tramas_era_de_ouro ALTERAR
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
