---

tags: 📝/anotação
creation: 2025-07-29 18:21
lastmod: 2025-07-29 18:21

---Pode parecer intimidador mas te garanto que se seguir o passo a passo que preparei vai conseguir tranquilo
E lembra, só precisa fazer esses passos uma vez e vai estar seguro contra imprevistos com seu computador.

## 🚶‍➡️Passos a seguir
- Criar conta no [github](https://github.com/)
- Criar repositório privado no github
- Pegar link gerado e guardar
- Instale o [git](https://git-scm.com/downloads)
- Abra o terminal
- [[#✉️Configure o name e email]]
	- Email tem que ser o mesmo do github
- Instalar a extensão no obsidian
- Vai dizer que ainda tem que configurar
- Abra seu terminal novamente
- Vá até onde está seu cofre
- [[#💻Iniciar repositório local e enviar para o remoto]]
- Voltar para o obsidian e entrar nas configurações da extensão
- Colocar name e email e tempo de intervalo de envio.
- Se quiser posso mandar manualmente através da próprio extensão que fica na sidebar direita.
- Posso baixar o vault direto pelo github quando quiser usar ele em outro computador.

#### ✉️Configure o name e email
```bash
git config --global user.name "Seu nome"
git config --global user.email seuemail-da-conta-do-github
git config --list 👉para ver se está configurado certo
```
#### 💻Iniciar repositório local e enviar para o remoto
```bash
git init 👉 Inicia repositório local
git remote add origin git@github.com:aleduca/obsidian.git 👉 liga co repositório local com o remoto - foi gerado pelo github ao criar o repositório remoto.
git add . 👉 Prepara para enviar com as modificações
git commit -m "Primeiro commit" 👉 Mensagem que vai aparecer no github
git push origin master 👉 Envia para o repositório remoto
```

### **Quick setup** — if you’ve done this kind of thing before

Get started by [creating a new file](https://github.com/MarcoMelloLivros/escrita_criativa/new/main) or [uploading an existing file](https://github.com/MarcoMelloLivros/escrita_criativa/upload). We recommend every repository include a [README](https://github.com/MarcoMelloLivros/escrita_criativa/new/main?readme=1), [LICENSE](https://github.com/MarcoMelloLivros/escrita_criativa/new/main?filename=LICENSE.md), and [.gitignore](https://github.com/MarcoMelloLivros/escrita_criativa/new/main?filename=.gitignore).

### …or create a new repository on the command line

echo "# escrita_criativa" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:MarcoMelloLivros/escrita_criativa.git
git push -u origin main

### …or push an existing repository from the command line

git remote add origin git@github.com:MarcoMelloLivros/escrita_criativa.git
git branch -M main
git push -u origin main