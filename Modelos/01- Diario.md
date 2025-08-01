
---
<%*
const inputFileName = await tp.system.prompt("Digite um nome para a nota");
if (inputFileName) {
  const now = tp.date.now("YYYY-MM-DD HH-mm"); // Formata a data e hora
  const newFileName = `${now} - ${inputFileName}`; // Concatena
  await tp.file.rename(newFileName);
} else {
  // Opcional: lida com o caso em que o usuário não digita nada
  new Notice("Nome da nota não fornecido. Mantendo o nome original.", 3000);
}
%>
tags: 📝/diario
creation: <% tp.file.creation_date() %>
lastmod: <% tp.file.last_modified_date("YYYY-MM-DD HH:mm") %>

---

Observações planejamentos, apague esta frase e escreva o que queira
