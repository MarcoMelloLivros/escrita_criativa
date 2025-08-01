**NÃO FICÇÃO GERAL**  
Sobre este modelo

Quando compilado ( **File \> Compile …** ), este projeto irá gerar um documento no formato de manuscrito padrão usado para muitos tipos de não-ficção. As configurações também são fornecidas para facilitar a compilação em um PDF no estilo brochura para autopublicação ou um ePub ou ebook Kindle.

Como usar este modelo

* Dentro da pasta “Manuscrito”, crie uma nova pasta para cada capítulo e intitule cada pasta com o nome do capítulo. (Você não precisa \- e de fato não deve \- intitular as pastas como "Capítulo Um" e assim por diante, porque a numeração dos capítulos será feita automaticamente durante o processo de compilação.) A pasta do primeiro capítulo foi criada para você com o título de espaço reservado “Capítulo”.

  * *⁠ **Nota:*** A pasta “Manuscript” é o que chamamos na documentação de “Pasta Rascunho”. Acabou de ser renomeado como “Manuscrito” neste modelo.

* Crie um novo documento de texto para cada seção dentro das pastas dos capítulos. (Na exportação, as seções serão separadas com o caractere “\#” para formato de manuscrito padrão ou com uma linha em branco para outros formatos.)

* Se você não precisar de um prefácio, mova o documento “Prefácio” para a pasta Lixeira. Como alternativa, renomeie-o como “Prefácio” ou “Introdução”, se preferir.

* As pastas “Notas” e “Ideias” foram fornecidas para sua conveniência, embora você possa substituí-las ou criar diferentes pastas de nível superior para seus materiais de pesquisa, se necessário (essas são apenas pastas comuns que tiveram ícones personalizados atribuídos a elas usando a guia **Documentos \> Alterar** recurso de ícone).

Tabelas e Figuras

Se precisar usar tabelas ou figuras em seu manuscrito, você pode rotulá-las usando as seguintes tags, substituindo “KEYWORD” por uma palavra única que identifique sua tabela ou figura.

\!fig(PALAVRA-CHAVE)

\!tabela(PALAVRA-CHAVE)

Essas tags serão substituídas por números no documento compilado, com o fluxo de numeração para figuras sendo separado do fluxo de numeração para tabelas.

Você pode se referir a essas tags da seguinte maneira:

\#fig(PALAVRA-CHAVE)

\#tabela(PALAVRA-CHAVE)

Aqui está um exemplo:

Tabela \!table(vendas): Vendas 2011

Table \!table(dates): Datas de envio

Figura \!fig(esqueleto): O esqueleto do gnu.

Figure \!fig(malcolmreynolds): O segundo personagem mais legal de *Firefly* .

… (Para números de vendas, consulte a tabela \#table(sales))… Para datas de embarque, consulte a tabela \#table(dates)… onde ele descobriu o esqueleto de um gnu nodoso (consulte a figura \#fig(esqueleto))… Crônicas fornecendo uma *descrição* semelhante papel, embora sem o ator *Castle* (ver figura \#fig(malcolmreynolds)).

No documento compilado, o texto acima ficaria assim:

Tabela 1: Vendas 2011

Tabela 2: Datas de embarque

Figura 1: O esqueleto do gnu.

Figura 2: O segundo personagem mais legal de *Firefly* .

… (Para números de vendas, veja a tabela 1)… Para datas de embarque, veja a tabela 2… onde ele descobriu o esqueleto de um gnu retorcido (veja a figura 1)… Crônicas com um papel similar, embora sem o ator do Castelo (veja *a* figura 2 *)* .

Compilando

As páginas de título e o front matter são todos fornecidos na pasta “Front Matter”. Diferentes matérias iniciais são usadas para diferentes formatos.

Uma pasta “Back Matter” também é fornecida. Aqui você pode adicionar qualquer material de fundo específico para cada formato de compilação. Atualmente, ele contém apenas documentos para armazenar notas finais (veja abaixo).

***Dica:*** você pode abrir este documento em uma janela de referência rápida e abri-lo ao lado da caixa de diálogo de compilação, se precisar consultar essas instruções durante a compilação.

**Para compilar para o formato de manuscrito padrão:**

1. Edite o documento “Title Page” dentro da pasta Front Matter/Manuscript Format para garantir que ele contenha as informações corretas (por padrão, ele usará as informações do autor fornecidas em **Arquivo \> Opções …** ).

   2. Para criar seu sumário:

      1. Mantendo pressionada a tecla Ctrl, selecione todos os documentos que deseja incluir na listagem de conteúdo. (Normalmente, será "Prólogo" e todas as pastas de capítulos, mas *não* as seções individuais dentro das pastas de capítulos. Se você tiver notas de rodapé e desejar que elas sejam adicionadas ao final do manuscrito como notas finais, você também deve incluir o documento "Notas finais " dentro de “Back Matter”.)

      2. Vá para **Editar \> Copiar Especial \> Copiar Documentos como ToC** .

      3. Cole no documento “Conteúdo” na pasta inicial “Formato do manuscrito”. ( ***Dica:*** Use **Formatar \> Fonte \> Sublinhado** para alterar ou remover o sublinhado pontilhado entre os nomes dos capítulos e os números das páginas. Você também pode ajustar o recuo, o alinhamento e a posição da tabulação conforme necessário. Com as margens padrão de 1" do projeto em compilar, a marca de 6,5" na régua no editor será a borda interna direita da página compilada.) 

         O texto vinculado resultante e as tags de número de página serão substituídos pelos nomes dos capítulos finais e números de página no documento compilado. 

         Observe que você não precisa fazer isso toda vez que compilar, apenas quando os capítulos forem adicionados, excluídos, renomeados ou movidos. ( *Observação para usuários do Microsoft Word:* se você exportar para o Word, pode ser necessário gerar uma visualização de impressão no Word para forçar a exibição correta dos números das páginas \- eles podem aparecer como pontos de interrogação antes de fazê-lo.) Você não precisa fazer 

         isso . a propósito, use “Copiar documentos como ToC” para criar um sumário. Você também pode construir um usando links de documentos e espaços reservados \- consulte “Lista de todos os espaços reservados…” no menu **Ajuda** para obter mais informações sobre o último.

   3. Vá em **Arquivo \> Compilar …**

   4. Ao lado de “Compilar para”, selecione “Imprimir”, “PDF” ou um dos formatos de arquivo rich text, como RTF, Word ou OpenOffice.

   5. Selecione “Manuscrito de não ficção (Courier)” ou “Manuscrito de não ficção (Times )” na lista de formatos à esquerda.

   6. Certifique-se de que o botão “Adicionar matéria inicial” esteja marcado na lista de conteúdo à direita e que a pasta “Formato do manuscrito” esteja selecionada no menu suspenso próximo a ela. (Isso já foi configurado para você.)

   7. Se você tiver notas de rodapé em seu texto, elas podem ser incluídas no final de cada página (o padrão) ou como notas finais. Para incluí-los como notas finais:

   1. Abaixo da lista de documentos no lado direito da caixa de diálogo de compilação, marque “Adicionar material posterior” e selecione a pasta Formato de material posterior/manuscrito para que seu documento “Notas finais” seja adicionado à lista de compilação.

   2. Clique no ícone de engrenagem na barra de cabeçalho mais à direita na compilação.

   3. Marque “Exportar notas de rodapé do inspetor como notas finais” e “Exportar notas de rodapé embutidas como notas finais”.

   4. Se você estiver compilando para um formato de arquivo rich text para uso com um processador de texto que suporte notas de rodapé verdadeiras, as notas finais serão colocadas no final do texto completo em vez de seguir o cabeçalho “Notas”. Você pode editar sua colocação no processador de texto ou pode convertê-los em texto normal durante o processo de compilação para que sejam impressos no local correto. Para fazer isso, clique duas vezes no formato de compilação escolhido para editá-lo e clique em “Compatibilidade” na parte inferior da lista na barra lateral esquerda. (Se isso não estiver visível, clique no menu suspenso na parte superior da barra lateral e escolha RTF.) Desmarque “Achatar notas de rodapé e comentários em texto normal” e clique em Salvar.

   8. Clique em “Compilar”.

   **Para compilar para o formato PDF de brochura:**

   1. Edite as páginas de capa contidas na pasta Front Matter/Paperback.

   2. Siga as instruções em compilação para formato de manuscrito padrão para criar um índice, mas desta vez cole a lista de conteúdo no documento Front Matter/Paperback/Contents.

   3. Vá em **Arquivo \> Compilar …**

   4. Ao lado de “Compilar para”, selecione “PDF”.

   5. Selecione “Paperback (5,06” x 7,81”)” na lista de formatos à esquerda.

   6. Certifique-se de que o botão “Adicionar matéria inicial” esteja marcado na lista de conteúdo à direita e que a pasta “Paperback” esteja selecionada no menu suspenso ao lado dela. (Isso já foi configurado para você.)

   7. Se você tiver notas de rodapé em seu texto, elas podem ser incluídas no final de cada página ou como notas finais. Consulte as instruções em compilação para formato de manuscrito padrão para obter informações sobre como incluir notas de rodapé como notas de fim (neste caso, no entanto, selecione a pasta de contracapa “Paperback” no menu suspenso depois de marcar “Add Back Matter”).

   8. Clique em “Compilar”.

   **Para compilar para o formato ebook:**

   1. Edite ou remova a página de dedicatória contida na pasta Front Matter/Ebook. Sinta-se à vontade para adicionar quaisquer outros documentos iniciais, conforme necessário.

   2. Importe uma imagem de capa (de preferência no formato JPG ou PNG).

      * Você pode armazená-lo em qualquer lugar, mas faz sentido colocá-lo na pasta de front-mate “Ebook”. Uma imagem de capa de espaço reservado já foi fornecida \- você desejará excluí-la depois de importar a sua.

      * Certifique-se de verificar online os tamanhos de imagem recomendados, porque as recomendações estão em constante mudança. A amostra de imagem de capa fornecida é de 2.500 x 1.563 pixels, com base no tamanho e nas proporções recomendados pela Amazon para uma capa do Kindle no momento em que este modelo foi criado.

   3. Vá em **Arquivo \> Compilar …**

   4. No menu “Compilar para”, selecione um dos formatos de e-book.

   5. Selecione “Ebook” na lista de formatos à esquerda.

   6. Se você tiver outros documentos frontais além da imagem da capa, certifique-se de que o botão “Adicionar material frontal” esteja marcado na lista de conteúdo à direita e que a pasta “Ebook” esteja selecionada no menu suspenso próximo a ela. Se você não tiver nenhum documento de rosto, você pode desmarcar “Adicionar arquivo de rosto”. (Desmarcar isso não afeta a imagem da capa.)

   7. Acima da lista de conteúdo na barra de cabeçalho mais à direita estão seis botões. Clique em cada um deles para percorrer as várias configurações disponíveis, alterando o que você precisa. Em particular:

      * Preencha os metadados, como nome do autor e título do livro.

      * Certifique-se de que sua imagem de capa esteja selecionada e exibida.

   8. Clique em “Compilar”.

Adicionando subtítulos

Se você deseja que seus capítulos sejam divididos em seções, cada uma com seus próprios subtítulos, basta usar grupos de arquivos em branco para cada título, com cada seção sob esse título um subdocumento do grupo de arquivos, como este:

![][image1]

Personalizando o Índice do Ebook

Ao exportar para o formato ebook, o Scrivener gera automaticamente um sumário. Se você deseja personalizar o que aparece no conteúdo, siga estas instruções:

1. Crie um documento para o sumário dentro da pasta Front Matter/Ebook.

2. Nomeie o documento como "Conteúdo".

3. Com o documento “Conteúdo” aberto no editor, selecione **Navegar \> Editor \> Bloquear no local** . O cabeçalho do editor ficará rosa para indicar o bloqueio e você poderá trabalhar no fichário sem afetar o editor.

4. No fichário, selecione os documentos que deseja que apareçam no sumário (mantenha pressionada a tecla **Ctrl** para selecionar mais de um documento).

5. Para uma lista plana simples, arraste os documentos selecionados para o editor e solte-os no documento “Conteúdo” vazio. Como alternativa, se você quiser que o índice seja recuado para corresponder à estrutura do fichário, selecione **Editar \> Copiar especial \> Copiar documentos como lista de links estruturados** e, em seguida, clique no texto do documento “Conteúdo” e pressione **Ctrl+V** ou use **Editar \> Colar** . Os documentos que você deseja que apareçam no índice agora aparecerão como uma lista de links.

6. Se desejar centralizar o sumário, selecione o texto e centralize-o.

7. No Inspetor, altere o “Tipo de seção” do documento “Conteúdo” para “Página de conteúdo”.

8. Remova o bloqueio do editor alternando **Navegar \> Editor \> Bloquear no local** ou desmarcando a opção no menu que aparece ao clicar com o botão direito do mouse no ícone do documento no cabeçalho do editor. 

   Agora, quando você compilar, seu documento “Conteúdo” personalizado será usado em vez do gerado automaticamente. Os títulos nos links do documento “Conteúdo” serão atualizados automaticamente para corresponder aos do ebook final compilado.

Exemplo de Documento

Veja o arquivo PDF “Sample MS” na pasta Research para um exemplo de um documento que foi criado usando este modelo.

Nota Final

Os modelos de projeto do Scrivener são flexíveis e não se destinam a restringir você a um fluxo de trabalho específico. Você pode alterar, excluir ou mover os arquivos e pastas contidos no modelo para se adequar à sua forma de trabalhar.

Como todos os modelos no Scrivener, este projeto foi originalmente criado a partir do modelo “Blank”. Simplesmente adicionamos algumas pastas e configuramos tudo de maneira que seja útil para autores de não-ficção. Tudo o que você pode fazer com este projeto, você também pode fazer criando um projeto “em branco” e configurando-o você mesmo.

Você pode criar seus próprios modelos configurando um projeto esquelético com os arquivos, pastas e configurações que gostaria de usar para novos projetos e usando **Arquivo \> Salvar como modelo …**

[image1]: <data:image/png;base64,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>