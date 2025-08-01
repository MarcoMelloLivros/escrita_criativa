Para estruturar a escrita de um livro no Obsidian, você pode ==usar uma combinação de pastas, notas e links para organizar suas ideias, capítulos e conteúdo==. Utilize a estrutura de pastas para separar o livro em capítulos, e cada capítulo em notas menores, facilitando a organização e a revisão. Use links para conectar ideias, personagens e eventos, criando um mapa mental do seu livro. 

Estrutura:

1. **1.** **Pastas:**
    
    Crie pastas para organizar seu livro por categorias como:
    
    - **Livro:** Pasta principal para o projeto do livro.
    - **Capítulos:** Pasta contendo as notas de cada capítulo.
    - **Personagens:** Pasta para notas sobre personagens.
    - **Cenários:** Pasta para notas sobre os cenários.
    - **Pesquisa:** Pasta para notas de pesquisa.
    - **Rascunhos:** Pasta para rascunhos e ideias iniciais.
    - **Esboços:** Pasta para esboços de capítulos e da história.
    - **Notas Diversas:** Pasta para notas não categorizadas.
    
2. **2.** **Notas:**
    
    Crie notas para cada capítulo, seção, personagem, cenário ou ideia relevante.
    
    - **Capítulo 1:** Uma nota para cada capítulo, com um título descritivo.
    - **Personagem A:** Uma nota para cada personagem, com descrição, características e informações relevantes.
    - **Cenário X:** Uma nota para cada cenário importante, com descrição detalhada.
    - **Ideia Y:** Uma nota para cada ideia importante que surgir.
    
3. **3.** **Links:**
    
    Utilize os links para conectar as notas e criar relações entre os elementos do seu livro.
    
    - **[[Personagem A]]**: Referencie personagens em notas de capítulos.
    - **[[Cenário X]]**: Referencie cenários em notas de capítulos.
    - **[[Ideia Y]]**: Referencie ideias em notas de personagens ou cenários.
    - **[[Capítulo 2]]**: Crie links entre capítulos para facilitar a navegação. 
    

Dicas adicionais:

- **Templates:** Utilize templates para criar notas com estrutura consistente.
- **Tags:** Utilize tags para organizar e filtrar suas notas.
- **Gráfico:** Explore o gráfico do Obsidian para visualizar a estrutura do seu livro.
- **Plugins:** Utilize plugins como o "Longform" para auxiliar na escrita de livros.
- **Revisão:** Revise e refine suas notas regularmente para manter a organização. 

Ao seguir essa estrutura, você poderá organizar seu livro de forma eficaz no Obsidian, facilitando a escrita, revisão e desenvolvimento da sua história.


---

## Entendendo o Arquivo `index.md` do Longform

O arquivo `index.md` que o Longform cria é, de fato, o **orientador central** para o plugin compilar e gerenciar o seu projeto. Ele funciona como o "cérebro" do seu livro dentro do Longform.

Vamos detalhar as propriedades que você encontrou no seu `index.md`:

YAML

```
longform:
  format: scenes
  title: Meu Destino
  sceneFolder: /
  scenes: []
  ignoredFiles: []
```

- **`longform:`**: Isso é apenas um cabeçalho que indica que as configurações abaixo são para o plugin Longform.
    
- **`format: scenes`**: Esta linha define como o Longform deve tratar os seus componentes de escrita. Basicamente, ele está esperando que você adicione "cenas" (que podem ser seus capítulos ou seções menores dentro dos capítulos) para serem compiladas. Você raramente precisará mudar isso, a menos que esteja fazendo algo muito específico com o plugin.
    
- **`title: Meu Destino`**: Esta é a propriedade mais simples: o **título do seu livro** dentro do projeto Longform. Você pode e deve mudar isso para o título real do seu livro.
    
- **`sceneFolder: /`**: Esta propriedade indica a **pasta onde o Longform buscará as suas "cenas"** (capítulos/seções).
    
    - Quando ele está como `/`, significa que ele está buscando na **raiz da pasta do seu projeto Longform**.
        
    - **Para a sua estrutura**, eu sugiro que você altere isso para `sceneFolder: Capítulos/`. Dessa forma, o Longform saberá que todas as suas notas para compilação estão dentro da pasta `Capítulos`.
        
- **`scenes: []`**: Este é o **coração da organização do seu livro** no Longform. É uma lista vazia porque você acabou de criar o projeto. Conforme você arrastar e soltar suas notas de capítulo (ou seções menores) para o painel do Longform, ou as adicionar manualmente, o Longform preencherá esta lista com os caminhos para essas notas.
    
    - **Exemplo:** Se você adicionar "01 - Introdução.md" e "02 - O Despertar.md", essa linha pode se parecer com:
        
        YAML
        
        ```
        scenes:
          - Capítulos/01 - Introdução.md
          - Capítulos/02 - O Despertar.md
        ```
        
- **`ignoredFiles: []`**: Esta lista é para **arquivos que você não quer que o Longform considere** ao compilar seu livro. Por exemplo, rascunhos antigos, notas de teste, etc. Você pode adicionar os caminhos desses arquivos aqui se eles estiverem na sua `sceneFolder` mas você não quiser que façam parte da compilação final.
    

---

### Você tem que escrever como ele entende?

Não exatamente "como ele entende" em termos de formatação de conteúdo dentro das notas. Você escreve o **conteúdo do seu livro em Markdown normal** dentro de cada nota de capítulo (`.md`). O que o Longform "entende" é a **estrutura de onde essas notas estão** e **quais delas devem ser incluídas na compilação**, baseado nas configurações do `index.md` e na ordem que você define no painel do Longform.

Pense nisso assim:

1. **Suas notas de capítulo (ex: `01 - Introdução.md`)**: Contêm o _texto bruto_ do seu livro em Markdown.
    
2. **O arquivo `index.md`**: Diz ao Longform _quais arquivos_ são seus capítulos e _onde encontrá-los_.
    
3. **O painel do Longform no Obsidian**: Permite que você _visualize e reorganize_ esses capítulos de forma fácil, sem mexer nos arquivos diretamente.
    

---

### Ação Sugerida

1. **Altere o `title`** no seu `index.md` para o título do seu livro.
    
2. **Altere o `sceneFolder`** no seu `index.md` para `Capítulos/` (se essa for a pasta onde você guarda seus arquivos de capítulo).
    
3. **Comece a adicionar suas notas de capítulo** (os arquivos `.md` dentro da pasta `Capítulos`) ao projeto Longform através do painel lateral. Conforme você faz isso, a propriedade `scenes: []` no `index.md` será automaticamente preenchida pelo Longform.
    

Com essa configuração, você terá uma base sólida para começar a escrever e gerenciar seu livro com o Longform!


---

### Organizando "Scenes" (Cenas) dentro de Capítulos no Longform

Você já tem a ideia de que o Longform usa a ordem dos arquivos na sua pasta `Capítulos` (ou a ordem que você define no painel do Longform) para compilar o livro. Agora, vamos detalhar como as "scenes" se encaixam nisso para dar uma granularidade ainda maior à sua escrita.

Pense em "scenes" como **subseções ou partes menores dentro de um capítulo maior**. Imagine que um capítulo é uma sala, e as cenas são diferentes cantos dessa sala, ou até mesmo pequenas cenas individuais que compõem a narrativa daquele capítulo.

#### Como funciona na Prática:

1. **Crie a Pasta do Capítulo:** Primeiro, para organizar as cenas, o ideal é criar uma **pasta para cada capítulo** dentro da sua pasta principal `Capítulos`. Isso ajuda a manter a estrutura visual limpa.
    
    **Exemplo da Estrutura de Pastas:**
    
    ```
    Livro/
    └── Capítulos/
        ├── 01 - Introdução/         <-- Nova pasta para o Capítulo 1
        │   ├── 01.1 - A Chegada.md   <-- Cena 1.1
        │   ├── 01.2 - O Primeiro Encontro.md <-- Cena 1.2
        │   └── 01.3 - Revelações Iniciais.md <-- Cena 1.3
        ├── 02 - O Despertar/        <-- Nova pasta para o Capítulo 2
        │   ├── 02.1 - O Sonho.md
        │   └── 02.2 - A Busca.md
        └── 03 - A Primeira Missão.md  <-- Este pode ser um capítulo sem sub-cenas, se preferir
    ```
    
    Nesse exemplo, `01 - Introdução` é a **pasta que representa seu Capítulo 1**. Dentro dela, você tem arquivos `.md` menores que são as suas **cenas**. A numeração (ex: `01.1`) ajuda a manter a ordem visualmente dentro da pasta.
    
2. **Adicionando ao Longform:**
    
    - No painel do Longform, em vez de arrastar o arquivo `01 - Introdução.md` (que não existe mais), você vai arrastar a **pasta `01 - Introdução/`**.
        
    - Quando você arrasta uma pasta para o Longform, ele reconhece que essa pasta deve ser tratada como um **"chapter" (capítulo)**, e todos os arquivos `.md` dentro dela (as suas cenas) serão automaticamente listados como **"scenes" (cenas)** sob esse capítulo.
        
    - O Longform, por padrão, organizará essas cenas na ordem alfabética ou numérica (se você usar `01.1`, `01.2`, etc.).
        
    
    **Visualização no Painel do Longform:**
    
    Você verá algo assim no painel do Longform:
    
    - **01 - Introdução** (isso representa a pasta do capítulo)
        
        - 01.1 - A Chegada
            
        - 01.2 - O Primeiro Encontro
            
        - 01.3 - Revelações Iniciais
            
    - **02 - O Despertar**
        
        - 02.1 - O Sonho
            
        - 02.2 - A Busca
            
    - 03 - A Primeira Missão (se este for um arquivo único, ele aparece como um "chapter" simples)
        
3. **Benefícios dessa Estrutura:**
    
    - **Foco na Cena:** Você pode trabalhar em uma cena por vez, sem se sentir sobrecarregado pelo capítulo inteiro.
        
    - **Reorganização Fácil:** Dentro do painel do Longform, você pode arrastar e soltar as cenas para mudar a ordem dentro de um capítulo, ou até mesmo arrastar cenas entre capítulos, tudo sem precisar mover os arquivos manualmente no explorador de arquivos do Obsidian.
        
    - **Compilação Contínua:** Quando você compilar seu livro, o Longform pegará todas essas cenas na ordem que você definiu no painel e as unirá em um texto contínuo.
        

---

### Exemplo de Uso e Edição

Se você estiver escrevendo o Capítulo 1 e perceber que precisa de uma cena extra entre "A Chegada" e "O Primeiro Encontro":

1. Crie um novo arquivo `.md` dentro da pasta `Livro/Capítulos/01 - Introdução/`, por exemplo, `01.1.5 - Um Novo Personagem.md`.
    
2. Automaticamente (ou após uma atualização do painel do Longform, se necessário), essa nova cena aparecerá na lista sob o capítulo "01 - Introdução".
    
3. Você pode então arrastá-la para a posição exata que desejar entre as outras cenas.
    

Essa abordagem oferece flexibilidade para grandes projetos, permitindo que você trabalhe em partes menores e as monte como peças de Lego para formar capítulos completos.

---
     

No Obsidian, as informações entre os `---` (traços) no início de uma nota são chamadas de **Frontmatter** (ou YAML Frontmatter). Esse é o local padrão para metadados como `tags`, `title`, `date`, `lastmod`, etc. A boa notícia é que **o plugin Longform, assim como a maioria dos exportadores de Markdown, _ignora automaticamente o Frontmatter_ durante a compilação**.

Isso significa que você pode manter seus metadados no template sem se preocupar que eles apareçam no seu livro final. Eles são usados pelo Obsidian e por outros plugins para organização e filtragem, mas não são considerados "conteúdo do texto" para leitura.

---

## Template para Longform: Sugestões e Adaptações

Com isso em mente, você pode adaptar seu template atual para ser super útil para seus capítulos e cenas do livro.

### 1. Template Básico para Capítulos/Cenas

Este template é uma excelente base para suas notas de capítulo ou cena.

Markdown

```
---
tags:
  - 📚/capitulo # ou 📚/cena, dependendo da sua granularidade
title: "{{date:YYYY-MM-DD}} - Título do Capítulo/Cena" # Título sugerido com data para facilitar identificação
date: "{{date:YYYY-MM-DD}}"
lastmod: "{{date:YYYY-MM-DD}}"
status: rascunho # Ou "em progresso", "revisado", "finalizado"
wordcount: 0 # Para controle de palavras, se você usar plugins que atualizem isso
personagens: [] # Liste personagens principais na cena/capítulo
cenarios: [] # Liste cenários principais na cena/capítulo
mood: # Ex: "tensão", "alegria", "mistério"
---

# Título do Capítulo ou Cena

## Objetivo do Capítulo/Cena

* Qual o propósito desta seção?
* O que precisa acontecer aqui?

---

## Rascunho / Conteúdo

Comece a escrever aqui.

---

## Notas e Ideias (Apagar antes da versão final)

* Lembrar de incluir a descrição de [[Personagem A]].
* Checar a cronologia da [[Linha do Tempo]].
* Pesquisar mais sobre [assunto].

```

### Explicação dos Campos Sugeridos:

- **`tags: - 📚/capitulo`**: Use tags para categorizar se a nota é um capítulo completo ou uma cena. Isso ajuda na busca e organização dentro do Obsidian.
    
- **`title: "{{date:YYYY-MM-DD}} - Título do Capítulo/Cena"`**: Eu adicionei `{{date:YYYY-MM-DD}}` para que o Obsidian preencha automaticamente a data de criação. Você pode remover se preferir apenas o título. É útil para manter a numeração sequencial dos capítulos (ex: `01 - Introdução`).
    
- **`status: rascunho`**: Um campo excelente para controle de progresso. Você pode usar tags para isso também (`#status/rascunho`, `#status/revisado`).
    
- **`wordcount: 0`**: Se você usa um plugin como "Better Word Count" ou similar, este campo pode ser atualizado automaticamente, dando uma ideia do tamanho da sua seção.
    
- **`personagens: []` e `cenarios: []`**: Listar os personagens e cenários diretamente no Frontmatter pode ser útil para um rápido vislumbre do que está naquela seção. Você pode preencher manualmente ou usar auto-completar se tiver plugins específicos.
    
- **`mood:`**: Um campo mais criativo para você definir o tom ou a emoção principal daquela cena/capítulo.
    
- **`# Título do Capítulo ou Cena`**: Este é o título que _aparecerá_ no seu texto compilado. É importante que ele seja igual (ou muito parecido) ao `title` no Frontmatter para consistência, mas o Longform só se importa com o conteúdo abaixo do segundo `---`.
    
- **`## Objetivo do Capítulo/Cena` e `## Rascunho / Conteúdo`**: Estas são seções de cabeçalho dentro da sua nota. Elas são ótimas para pré-planejamento e para estruturar sua escrita.
    
- **`## Notas e Ideias (Apagar antes da versão final)`**: Uma seção útil para anotações rápidas, lembretes ou ideias que você não quer esquecer, mas que _devem ser removidas_ antes da compilação final.
    

---

### Como Usar Templates no Obsidian:

1. **Crie a Pasta de Templates:** Se você ainda não tem, crie uma pasta para seus templates (ex: `Templates/`).
    
2. **Crie o Arquivo do Template:** Dentro dessa pasta, crie um novo arquivo `.md` e cole o conteúdo do template sugerido acima (ex: `Template - Capítulo Livro.md`).
    
3. **Configure o Plugin Templates:** Vá em **Configurações > Opções de Plugins > Templates**.
    
    - Defina o "Local da pasta de templates" para a pasta que você criou (ex: `Templates/`).
        
4. **Usando o Template:**
    
    - Quando for criar um novo capítulo ou cena, abra a paleta de comandos (`Ctrl/Cmd + P`) e pesquise por "Inserir template".
        
    - Selecione o seu template de livro. O Obsidian preencherá a nota com a estrutura definida, e você pode começar a escrever.
        

Ao usar este template, você garante consistência, tem campos úteis para organização e metadados que serão ignorados na compilação final pelo Longform.

---

Existem alguns plugins no Obsidian que podem te ajudar a **formatar e compilar** seu livro para exportação. É importante entender que o Obsidian por si só é um editor de Markdown e não um software de layout ou diagramação (como o InDesign, por exemplo). Os plugins que veremos aqui focam em pegar seu conteúdo em Markdown e convertê-lo para formatos mais adequados para livros (como DOCX, EPUB, PDF).

Aqui estão os principais plugins e ferramentas:

---

## 1. Longform (Seu Melhor Aliado)

Você já está usando o **Longform**, e ele é, sem dúvida, o plugin mais importante para a "formatação" do seu livro no sentido de **compilação e organização**.

- **O que ele faz:**
    
    - **Compilação de Manuscritos:** O principal recurso do Longform é pegar todas as suas notas de cena/capítulo (que você organiza no painel do plugin) e uni-las em um único arquivo Markdown. Isso é essencial para ter seu livro completo em um só lugar.
        
    - **Fluxos de Trabalho Personalizáveis:** Dentro das configurações de "Compile" (Compilar) do Longform, você pode criar "workflows" (fluxos de trabalho). Esses fluxos podem incluir passos como:
        
        - **`Prepend Title` (Preceder Título):** Adicionar automaticamente o título de cada cena/capítulo no início do texto compilado (ex: `# Capítulo 1 - Introdução`).
            
        - **`Insert Separator` (Inserir Separador):** Adicionar um separador (como `---` ou `***` ou até um quebra de página se o formato de saída suportar) entre as cenas ou capítulos.
            
        - **Scripts Personalizados:** Para usuários mais avançados, o Longform permite escrever scripts em JavaScript para fazer transformações complexas no texto antes da compilação.
            
    - **Exportação Básica:** O Longform geralmente exporta o livro compilado para um único arquivo Markdown (`.md`).
        
- **Limitação:** O Longform **não exporta diretamente para DOCX, EPUB ou PDF** com formatação complexa. Ele gera um arquivo Markdown limpo, que é então o ponto de partida para a próxima etapa.
    

---

## 2. Plugins de Exportação (Para Formatos Finais)

Para converter o arquivo Markdown compilado pelo Longform em formatos de livro, você precisará de plugins que usem ferramentas externas (principalmente **Pandoc**).

### a) **Obsidian Enhancing Export**

- **O que faz:** Este é um dos plugins mais robustos para exportação. Ele serve como uma interface para o **Pandoc**, uma ferramenta de linha de comando universal para conversão de documentos.
    
    - Permite exportar seus arquivos Markdown para uma vasta gama de formatos, incluindo **DOCX, PDF, EPUB, HTML** e outros.
        
    - Você pode configurar comandos personalizados do Pandoc, o que dá um controle enorme sobre a formatação da saída.
        
- **Como usar:**
    
    1. **Instale o Pandoc:** Você precisará baixar e instalar o Pandoc no seu computador separadamente, pois este plugin usa o Pandoc por trás dos panos. Visite [pandoc.org](https://pandoc.org/) para baixá-lo.
        
    2. **Instale e Habilite o Plugin:** No Obsidian, vá em **Configurações > Plugins da Comunidade > Navegar**, procure por "Obsidian Enhancing Export", instale e habilite.
        
    3. **Configure no Plugin:** Nas configurações do plugin, você pode definir modelos de exportação (templates) e parâmetros para o Pandoc.
        
    4. **Execute a Exportação:** Abra o arquivo Markdown compilado pelo Longform, use a paleta de comandos (`Ctrl/Cmd + P`), procure por "Export" (ou algo similar configurado pelo plugin) e escolha o formato desejado.
        

### b) **Pandoc Plugin (do Oliver Balfour)**

- **O que faz:** Similar ao Enhancing Export, este plugin também serve como uma interface para o Pandoc. É mais simples em alguns aspectos, mas igualmente eficaz para conversões diretas.
    
- **Como usar:** O processo é muito parecido com o Enhancing Export: instale o Pandoc, instale e habilite o plugin, configure e exporte.
    

---

## 3. Considerações de Formatação para Livros

- **Markdown é para Conteúdo, Não Layout:** Lembre-se que o Markdown é sobre a _estrutura_ do seu conteúdo (títulos, parágrafos, listas) e não sobre a _aparência visual_ (fontes específicas, margens, espaçamento de linha, etc.).
    
- **Controle de Estilo com Pandoc (e CSS):**
    
    - Ao exportar para **DOCX** com Pandoc, você pode usar um **arquivo de referência DOCX** (um documento Word com os estilos que você deseja) para que o Pandoc aplique esses estilos ao seu texto. Isso é poderoso para ter controle sobre a fonte, tamanho, espaçamento de parágrafos, etc.
        
    - Ao exportar para **EPUB ou HTML**, você pode usar um **arquivo CSS** personalizado para definir o estilo visual do seu livro (fontes, cores, espaçamento).
        
- **Revisão Externa:** Mesmo com plugins, é quase certo que você precisará de um programa externo (Microsoft Word, Google Docs, um editor de EPUB como o Calibre) para fazer os ajustes finos e a formatação final do seu livro antes da publicação.
    

---

### Fluxo de Trabalho Recomendado:

1. **Escreva seu livro** em notas Markdown no Obsidian, usando a estrutura de pastas e o plugin Longform para organização e gerenciamento de cenas/capítulos.
    
2. Use o **Longform para compilar** todas as suas notas de capítulo em um **único arquivo `.md`**.
    
3. Use o plugin **Obsidian Enhancing Export** (ou Pandoc Plugin) em conjunto com o **Pandoc** (instalado separadamente) para converter o arquivo `.md` compilado para o formato final desejado (DOCX para revisão profissional, EPUB para e-readers, PDF para impressão, etc.).
    
4. Realize os **ajustes finos de formatação** e diagramação no software de destino (Word, Calibre, etc.).
    

Com esses plugins, você tem um fluxo de trabalho poderoso que começa no ambiente flexível do Obsidian e termina com um manuscrito bem formatado.

Qual formato final (DOCX, EPUB, PDF) você planeja usar para o seu livro? 

---


Ótimo! Como preencher as notas de apoio como `[[Linha do Tempo]]` e `[assunto]`.

Essas notas servem como **bases de dados ou referências** para o seu livro. Elas não são parte do manuscrito compilado, mas são cruciais para manter a consistência, a organização e a profundidade da sua história.

---

## Conteúdo do Arquivo `[[Linha do Tempo]]`

A nota `Linha do Tempo.md` é vital para organizar os eventos do seu livro cronologicamente. Isso ajuda a evitar inconsistências na sequência dos acontecimentos e a manter o controle sobre o ritmo da história.

### Sugestões de Conteúdo para `[[Linha do Tempo]]`

Você pode estruturar a linha do tempo de várias maneiras, dependendo da complexidade da sua história. Aqui estão algumas opções:

#### Opção 1: Linha do Tempo Simples (Texto e Marcadores)

Para histórias mais lineares ou com poucos eventos simultâneos.

Markdown

```
# Linha do Tempo do Livro: [Título do Livro]

## Era Antes do Início (Opcional, para histórico do mundo)
* [Ano/Evento]: Breve descrição.
* [Ano/Evento]: Breve descrição.

---

## Eventos Principais (Ordem Cronológica)

* **Dia 1 / Semana 1 / Mês 1 - [Data específica se houver]:**
    * **Manhã:** [[Personagem A]] acorda e decide viajar para [[Cenário X]].
    * **Tarde:** Encontro com [[Personagem B]] na cidade de [Cidade].
    * **Noite:** Ocorre o evento [Evento Chave]. (Link para o capítulo se for o caso: [[01 - Introdução]])

* **Dia 2 / Semana 2:**
    * [[Personagem B]] revela o segredo sobre [informação]. (Relacionado ao [[Plot Twist]])
    * Primeiro ataque dos [Antagonistas]. (Ligado à [[Batalha na Floresta]])

* **Dia 7 / Semana 3:**
    * Chegada em [[Cenário Y]].
    * Descoberta de [Artefato Mágico].

---

## Eventos Paralelos (Se houver múltiplas subtramas)
* **[Personagem Secundário] - Dia 3:** Investigação em [Local].
* **[Grupo Antagonista] - Semana 1:** Preparativos para [Plano].

---

## Notas da Linha do Tempo
* Verificar se a idade dos personagens faz sentido com os eventos.
* A "queda do Império" aconteceu 200 anos antes do início da história principal.
* [[Personagem C]] é introduzido no Capítulo 5.
```

#### Opção 2: Linha do Tempo com Tabelas (Para mais detalhes ou Dataview)

Se você quiser uma estrutura mais organizada ou planeja usar o plugin **Dataview** para consultar sua linha do tempo, tabelas são excelentes.

Markdown

```
# Linha do Tempo do Livro: [Título do Livro]

## Eventos Principais

| Data/Período | Evento                                      | Personagens Envolvidos | Locais Envolvidos | Notas                                      |
| :----------- | :------------------------------------------ | :--------------------- | :---------------- | :----------------------------------------- |
| Dia 1        | [[Personagem A]] chega a [[Cenário X]]     | [[Personagem A]]       | [[Cenário X]]     | Início da jornada.                         |
| Dia 1, Noite | Revelação do [[Plot Twist]]                 | [[Personagem A]], [[Personagem B]] | [Local Secreto]   | Ponto de virada da trama.                  |
| Dia 2        | Início da [[Batalha na Floresta]]           | [[Personagem A]], [[Personagem B]], [Antagonistas] | Floresta Negra    | Conflito inicial com os inimigos.          |
| Dia 7        | Descoberta do [Artefato Mágico]             | [[Personagem A]], [[Personagem C]] | Ruínas Antigas    | Chave para o próximo estágio da missão.    |
| Dia 10       | Conclusão do Capítulo 3                     | Todos                  | [Cidade Principal] | Fim do primeiro arco.                      |

---

## Eventos Pretéritos (História do Mundo)

| Ano | Evento Histórico           | Relevância para a Trama         |
| :-- | :------------------------- | :------------------------------ |
| -500 | Fundação do Reino de X     | Origem de [[Cenário X]]         |
| -100 | Guerra dos Cem Anos        | Causa da inimizade entre facções |
```

**Dica:** Se você usa o Dataview, pode até criar queries para listar cenas por data, facilitando a visualização da linha do tempo.

---

## Conteúdo do Arquivo `[assunto]` (Notas de Pesquisa/Temas)

A nota `[assunto]` (ou, idealmente, algo mais específico como `Magia e Encantamentos.md`, `História da Cultura X.md`, `Mitologia Local.md`) é onde você compila informações sobre temas, pesquisas, conceitos ou quaisquer detalhes que fundamentam seu livro.

### Sugestões de Conteúdo para `[assunto]`

#### Exemplo: `Magia e Encantamentos.md`

Markdown

```
# Magia e Encantamentos

## Tipos de Magia
* **Magia Elemental:** Controla os quatro elementos (Terra, Água, Fogo, Ar).
    * Fontes: Conexão direta com a natureza.
    * Limitações: Requer proximidade com o elemento, cansaço físico.
    * Usuários conhecidos: [[Ordem dos Magos Elementais]].

* **Magia Arcana:** Magia baseada em runas e feitiços complexos.
    * Fontes: Estudo e conhecimento de textos antigos.
    * Limitações: Requer foco mental intenso, pode levar à exaustão.
    * Usuários conhecidos: [[Personagem A]] (aprendiz), [[Grande Mago Z]].

* **Magia Negra:** Manipulação de energias sombrias.
    * Fontes: Sacrifícios, pactos.
    * Limitações: Corrói a alma do usuário, consequências imprevistas.
    * Usuários conhecidos: [[Antagonista Principal]].

---

## Feitiços Conhecidos (Exemplos)
* **Feitiço de Iluminação:** Cria uma pequena luz na palma da mão.
    * Custo: Pouca energia.
    * Usado em: Capítulo 1, cena da caverna.

* **Encantamento de Proteção:** Cria um escudo temporário contra ataques.
    * Custo: Moderado.
    * Usado por: [[Personagem B]] no Capítulo 3.

---

## Regras da Magia
* A magia é finita no mundo; seu uso excessivo pode esgotar o ambiente.
* Nem todos nascem com a capacidade de usar magia; é um dom raro.
* Objetos encantados retêm parte da magia do criador.

---

## Notas de Pesquisa
* Inspirar-se em sistemas de magia de [livro/série].
* Como a magia afeta a sociedade e a tecnologia? (Impacto social)
```

#### Exemplo: `Historia da Civilizacao Antiga.md`

Markdown

```
# História da Civilização Antiga: O Povo das Sombras

## Origens
* Fundado há 3000 anos, antes do Grande Cataclismo.
* Acreditavam na dualidade entre luz e escuridão.

## Auge da Civilização
* Construíram cidades subterrâneas e templos ocultos.
* Conhecimento avançado em [Ciência/Magia específica].
* Governados por uma linhagem de Sacerdotes-Reis.

## A Queda
* Causas: [Motivo 1], [Motivo 2].
* Evento chave: O Grande Cataclismo (detalhes em [[O Grande Cataclismo]]).
* Consequências: Dispersão do povo, perda de conhecimento.

---

## Artefatos e Ruínas
* [[Amuleto da Escuridão]] (artefato principal da trama).
* Ruínas de [Cidade Esquecida] (cenário de um capítulo).

---

## Mitos e Lendas Associados
* A Lenda do Retorno das Sombras.
* Os Guardiões dos Segredos Antigos.
```

---

### Dicas Adicionais para Notas de Referência:

- **Links, Links, Links:** Use muitos **links internos** `[[ ]]` para conectar essas notas de referência entre si e com suas notas de capítulo/cena. Isso cria uma verdadeira rede de conhecimento.
    
- **Tags:** Use tags (`#personagem`, `#local`, `#magia`) para categorizar suas notas de referência e facilitar a busca.
    
- **Propriedades/Frontmatter:** Use o Frontmatter para adicionar metadados específicos a essas notas (ex: `tipo: personagem`, `status: vivo/morto`, `poderes: []`).
    
- **Gráfico do Obsidian:** Explore o gráfico! Com todas essas notas interligadas, o gráfico se tornará um mapa visual da sua história, mostrando as conexões entre personagens, locais, eventos e temas.
    

Essas notas de apoio são o "motor" por trás da sua história. Quanto mais detalhadas e interconectadas elas estiverem, mais rica e consistente será a sua narrativa.

Você planeja ter muitas notas de pesquisa e referência, ou seu livro é mais focado em poucos elementos principais?


---

A nota do **"Personagem A"** é um lugar perfeito para usar metadados (no YAML Frontmatter) para controlar e organizar as informações mais importantes sobre seus personagens. Isso é super útil para manter a consistência, desenvolver a profundidade e até mesmo para criar consultas com plugins como o Dataview, se você for para esse nível de organização.

---

## Metadados Essenciais para uma Nota de Personagem

Aqui está um exemplo de como seria o Frontmatter de uma nota de personagem, com sugestões de metadados:

Markdown

```
---
tags:
  - 👥/personagem # Ou 👥/protagonista, 👥/antagonista
title: "Nome Completo do Personagem A"
apelido: "Apelido, se houver"
status: "vivo" # ou "morto", "desaparecido", "desconhecido"
genero: "feminino" # ou "masculino", "não binário", etc.
idade: 25 # Ou uma faixa etária: "jovem adulto", "criança"
ocupacao: "Mago Elementar"
filiacao: "Ordem dos Magos" # A que grupo, família ou organização pertence
local_atual: "Cidade X" # Onde ele está na maior parte da história
objetivo: "Encontrar o artefato perdido" # O que ele busca na trama
medo_principal: "Falhar em sua missão"
motivacao: "Vingança pela família"
arc_de_personagem: "De cético a herói" # Como ele se desenvolve ao longo da história
primeira_aparencia: "Capítulo 1" # Onde ele aparece pela primeira vez
aparencia_fisica: "Cabelos ruivos, olhos verdes, cicatriz na bochecha" # Resumo da aparência
personalidade: "Reservado, leal, sarcástico"
---

# Nome Completo do Personagem A

## Visão Geral
[Um parágrafo resumindo o personagem e seu papel na história.]

---

## História/Background
* Infância: [detalhes importantes]
* Eventos Marcantes: [eventos que moldaram o personagem, como [[Tragédia Familiar]]]
* Treinamento: [suas habilidades, como ele as adquiriu]

---

## Relacionamentos
* [[Personagem B]]: Amigo de infância, leal.
* [[Antagonista Principal]]: Inimigo jurado.
* [[Mentor X]]: Professor e figura paterna.

---

## Habilidades e Fraquezas
* **Habilidades:** Magia de Fogo, Combate Corpo a Corpo, Conhecimento de línguas antigas.
* **Fraquezas:** Impulsivo, confia demais nos outros, tem medo de altura.

---

## Notas Adicionais
* Ideias para diálogos: "Nunca subestime um inimigo pequeno."
* Cenários importantes para ele: [[Floresta Sombria]], [[Torre Antiga]].
* Pontos a desenvolver no capítulo X.

```

---

### Por que esses metadados são úteis?

1. **Consistência:** Garante que detalhes como idade, ocupação ou filiação do personagem permaneçam os mesmos em todo o livro.
    
2. **Visão Rápida:** Ao abrir a nota do personagem, você tem um resumo essencial no Frontmatter sem ter que ler o texto inteiro.
    
3. **Filtragem e Busca:** Você pode facilmente buscar todos os personagens com `status: "vivo"` ou que sejam da `ocupacao: "Mago Elementar"`.
    
4. **Desenvolvimento:** Ter `objetivo`, `medo_principal` e `arc_de_personagem` ajuda a manter o foco no desenvolvimento do personagem durante a escrita e revisão.
    
5. **Plugins (ex: Dataview):** Com o Dataview, você pode criar tabelas dinâmicas listando todos os seus personagens, seus status, idades, etc., o que é incrivelmente útil para uma visão geral do elenco.
    
    _Exemplo de consulta Dataview (em outra nota):_
    
    ````
    ```dataview
    TABLE status, genero, idade, ocupacao, objetivo
    FROM #👥/personagem
    SORT file.name ASC
    ````
    

Ao preencher esses metadados para cada personagem, você constrói uma base de dados rica e organizada que apoiará sua escrita e garantirá a profundidade e consistência do seu universo.

---

A nota de cenários é tão importante quanto a de personagens para dar vida e consistência ao seu mundo. Assim como nas notas de personagem, podemos usar **metadados (YAML Frontmatter)** para as informações essenciais e o corpo da nota para os detalhes mais ricos.

---

## Estruturando o Arquivo de Cenário

Vamos montar uma estrutura para sua nota de cenário, usando a pasta `Cenários` que você já planejou.

### Metadados Essenciais para uma Nota de Cenário

Aqui está um exemplo de como seria o Frontmatter de uma nota de cenário:

Markdown

```
---
tags:
  - 🗺️/cenario # Ou 🗺️/cidade, 🗺️/floresta, 🗺️/reino, etc.
title: "Nome do Cenário"
tipo: "cidade" # Ou "floresta", "montanha", "reino", "planeta", "edificio"
localizacao_geral: "Continente X" # Ou "País Y", "Galáxia Z"
populacao_estimada: "100.000" # Se aplicável
clima: "temperado" # Ou "frio", "desértico", "tropical"
caracteristicas_chave:
  - "arquitetura antiga"
  - "porto movimentado"
  - "governo corrupto"
atmosfera: "mistério e decadência" # O sentimento geral do lugar
eventos_historicos: # Eventos importantes que aconteceram ou estão acontecendo aqui
  - "Fundação há 500 anos"
  - "Cerco de 200 anos atrás"
personagens_associados: # Personagens que têm forte ligação com este local
  - "[[Personagem A]]"
  - "[[Líder da Cidade]]"
---

# Nome do Cenário

## Visão Geral
[Um parágrafo resumindo o cenário e sua importância para a história.]

---

## Geografia e Características Físicas
* **Topografia:** Montanhoso, plano, costeiro, subterrâneo.
* **Flora e Fauna:** Vegetação predominante, animais característicos (inclusive se há criaturas mágicas).
* **Marcos/Pontos de Interesse:** Construções notáveis, formações naturais, pontos turísticos importantes na sua história.
    * [[Torre do Mago]]
    * [[Mercado Central]]

---

## Cultura e Sociedade (Se aplicável a cidades, reinos, etc.)
* **Governo:** Monarquia, república, teocracia, conselho.
* **Leis e Costumes:** Regras importantes, tradições locais, festivais.
* **Economia:** Comércio, agricultura, mineração, tecnologia.
* **Grupos/Facções:** Guildas, clãs, organizações criminosas que operam aqui.

---

## História
* **Origem:** Como o cenário surgiu/foi fundado.
* **Eventos Chave:** Guerras, desastres, momentos de prosperidade.
* **Lendas/Mitos:** Histórias que o povo local conta sobre o lugar.

---

## Importância para a Trama
* Quais eventos cruciais ocorrem aqui?
* Como este cenário influencia os personagens?
* Que segredos este lugar guarda?

---

## Notas Adicionais
* Detalhes sensoriais: Como cheira? Que sons tem? Qual a sensação tátil?
* Pontos de conflito ou mistério a explorar.
* Inspirado em: [Local real ou fictício].
```

---

### Por que esses metadados são úteis para cenários?

1. **Consistência e Detalhe:** Garante que você mantenha os detalhes geográficos, climáticos e culturais do seu cenário consistentes ao longo do livro.
    
2. **Imersão:** Ter informações sobre a atmosfera e as características-chave ajuda a construir um ambiente vívido e imersivo para o leitor.
    
3. **Localização Rápida:** Ao abrir a nota, você tem um resumo rápido dos aspectos mais importantes do cenário.
    
4. **Conexões:** `personagens_associados` e `eventos_historicos` ajudam a linkar o cenário a outros elementos da sua história.
    
5. **Filtragem e Organização:** Com o **Dataview**, por exemplo, você pode listar todos os cenários por `tipo` (cidade, floresta) ou `localizacao_geral`, o que é excelente para ter uma visão geral do seu mundo.
    
    _Exemplo de consulta Dataview (em outra nota):_
    
    ````
    ```dataview
    TABLE tipo, localizacao_geral, clima, atmosfera
    FROM #🗺️/cenario
    SORT file.name ASC
    ````
    

Ao preencher essas informações detalhadas para cada cenário, você construirá um mundo rico e coeso para sua história.

Você está criando um mundo totalmente original ou adaptando elementos de cenários existentes?

