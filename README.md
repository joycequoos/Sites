
# Criando um Site com Visual Studio Code

[← Voltar para Desenvolvimento Web](https://github.com/joycequoos/Development)

Passo a passo para estruturar um projeto web do zero — HTML, CSS e JavaScript — usando o Visual Studio Code e a extensão Live Server.

Vídeo de referência: https://www.youtube.com/watch?v=fmhz4nqGK4E

## Sumário

- [1. Criar a pasta do projeto](#1-criar-a-pasta-do-projeto)
- [2. Abrir a pasta no VS Code](#2-abrir-a-pasta-no-vs-code)
- [3. Criar o arquivo index.html](#3-criar-o-arquivo-indexhtml)
- [4. Gerar a estrutura básica do HTML](#4-gerar-a-estrutura-básica-do-html)
- [5. Construir o conteúdo do HTML](#5-construir-o-conteúdo-do-html)
- [6. Instalar a extensão Live Server](#6-instalar-a-extensão-live-server)
- [7. Visualizar a página com o Live Server](#7-visualizar-a-página-com-o-live-server)
- [8. Criar o arquivo CSS](#8-criar-o-arquivo-css)
- [9. Criar o arquivo JavaScript](#9-criar-o-arquivo-javascript)
- [10. Conectar CSS e JS ao HTML](#10-conectar-css-e-js-ao-html)
- [11. Testar o projeto completo](#11-testar-o-projeto-completo)

---

## 1. Criar a pasta do projeto

Antes de abrir o VS Code, crie uma pasta no computador para guardar todos os arquivos do projeto.

![Criar pasta do projeto](01_CriarPasta.GIF)

**Exemplo de caminho:** `C:\API_GITHUB\javascript\GITHUB`

---

## 2. Abrir a pasta no VS Code

Selecione essa pasta diretamente pelo Visual Studio Code (`File > Open Folder`), para que todos os arquivos do projeto fiquem organizados no explorador lateral.

![Selecionar a pasta no VS Code](02_Acessar_Pasta.GIF)

---

## 3. Criar o arquivo index.html

Dentro da pasta do projeto, crie o arquivo principal da página: `index.html`.

![Criar index.html](03_Index_HTML.GIF)

O arquivo aparece na estrutura de pastas do projeto:

![Arquivo criado na pasta](04_Arquivo_Pasta.GIF)

---

## 4. Gerar a estrutura básica do HTML

O VS Code (via extensão Emmet, nativa do editor) permite gerar automaticamente o esqueleto padrão de um documento HTML. Basta digitar `!` e pressionar **Enter** dentro do arquivo `index.html`.

![Gerando estrutura básica do HTML](05_Estrutura_BasicaHTML.GIF)

Isso cria automaticamente as tags `<!DOCTYPE html>`, `<html>`, `<head>` e `<body>`, prontas para receber o conteúdo da página.

---

## 5. Construir o conteúdo do HTML

Com a estrutura básica pronta, comece a adicionar o conteúdo da página dentro da tag `<body>` — títulos, parágrafos, imagens, links, listas etc.

![Começando a construção do HTML](06_Comecando_HTML.GIF)

---

## 6. Instalar a extensão Live Server

O **Live Server** é uma extensão do VS Code que atualiza a página no navegador automaticamente a cada alteração salva no código — essencial para acompanhar o resultado em tempo real.

![Buscar a extensão Live Server](07_Extensao.GIF)

![Instalando a extensão](08_Instalando.GIF)

---

## 7. Visualizar a página com o Live Server

Depois de instalada, clique com o botão direito no `index.html` e selecione **"Open with Live Server"**.

![Abrindo com Live Server](09_Open_LiveServer.GIF)

O navegador abre automaticamente exibindo a página HTML renderizada.

---

## 8. Criar o arquivo CSS

Para estilizar a página, crie um arquivo `.css` (ex: `style.css`) na mesma pasta do projeto — use `Ctrl + Click` sobre a pasta e depois **"New File"**.

![Criando o arquivo CSS](10_Criar_Arquivo.GIF)

---

## 9. Criar o arquivo JavaScript

Da mesma forma, crie o arquivo `scripts.js` para adicionar interatividade à página.

![Criando o arquivo JavaScript](11_Criar_ArquivoJS.GIF)

Use `Ctrl + Click` sobre a pasta e selecione **"Create File"** para confirmar a criação:

![Selecionar Create File](12_Selecionar_CreateFile.GIF)

---

## 10. Conectar CSS e JS ao HTML

Criar os arquivos `style.css` e `scripts.js` não é suficiente — é preciso vinculá-los ao `index.html` para que o navegador realmente os carregue.

**Vincular o CSS** — dentro da tag `<head>`:

```html
<head>
  <meta charset="UTF-8">
  <title>Meu Site</title>
  <link rel="stylesheet" href="style.css">
</head>
```

**Vincular o JavaScript** — antes do fechamento da tag `</body>` (garante que o HTML já foi carregado antes do script rodar):

```html
  <script src="scripts.js"></script>
</body>
</html>
```

Com isso, a estrutura final do projeto fica:

```
meu-projeto/
├── index.html
├── style.css
└── scripts.js
```

---

## 11. Testar o projeto completo

Com os três arquivos conectados, abra o `index.html` novamente com o **Live Server** e confirme que:

- O estilo do `style.css` está sendo aplicado na página
- Um `console.log()` de teste no `scripts.js` aparece no console do navegador (F12 → aba Console)
- Qualquer alteração salva em qualquer um dos três arquivos atualiza a página automaticamente

```javascript
// scripts.js — teste rápido de que o arquivo está conectado
console.log('JavaScript conectado com sucesso!');
```

Se a mensagem aparecer no console, o projeto está com a estrutura completa e pronto para receber o conteúdo, estilo e interatividade reais do site.

---

## Principais aprendizados

- Organização de um projeto web do zero: pasta, HTML, CSS e JavaScript separados
- Geração rápida de estrutura HTML com Emmet (`!` + Enter)
- Uso do Live Server para visualização em tempo real durante o desenvolvimento
- Vinculação correta de CSS (`<link>` no `<head>`) e JavaScript (`<script>` antes de `</body>`)
- Verificação de que os arquivos estão de fato conectados via console do navegador

**Próximos passos:** aprofundar em CSS (Flexbox, Grid, responsividade) e JavaScript (manipulação do DOM, eventos) para transformar essa estrutura básica em um site interativo completo.
