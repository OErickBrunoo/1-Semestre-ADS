## 📄 Template Parallax com Materialize

**Um template web moderno e responsivo, implementando o efeito *parallax* para criar uma experiência visual dinâmica, construído sobre o framework Materialize CSS.**

-----

## 📝 Descrição Geral

Este projeto consiste em um template básico de página inicial (landing page) que demonstra a utilização do framework **Materialize CSS**. O foco principal é explorar o efeito *parallax* nativo do framework, combinado com uma estrutura limpa e os componentes de design Material.

O objetivo é fornecer uma base sólida e visualmente atraente que pode ser adaptada para diversos fins, como sites corporativos, portfólios ou páginas de eventos.

O projeto utiliza:

  * **Materialize CSS:** O framework completo para estilização, layout e componentes.
  * **Efeito Parallax:** Implementado em três seções distintas para profundidade visual.
  * **Design Responsivo:** Navegação adaptável com *Sidenav* e layout de colunas fluído.
  * **Ícones Material Design:** Utilização da biblioteca de ícones do Google.
  * **JQuery:** Requerido pelo Materialize para inicialização de componentes.

-----

## 💡 Principais Funcionalidades

### Estrutura de Layout

  * **Navbar Fixa:** Barra de navegação branca com links, que se torna um *Sidenav* (`sidenav-trigger`) em dispositivos móveis.
  * **Herói (Banner Inicial):** Uma seção *parallax* destacada com um título central, descrição e um botão de chamada para ação (`btn-large`).
  * **Seções de Destaque:** Três blocos de ícones (`icon-block`) para apresentar recursos ou serviços de forma concisa.
  * **Seções Intermediárias:** Duas seções adicionais com efeito *parallax* e texto centralizado, servindo como divisores de conteúdo.
  * **Rodapé Completo:** Estrutura de rodapé em cor `teal` com colunas para "O que Fazemos?", "Trabalhos" e "Blog", além da seção de direitos autorais.

### Componentes Materialize

  * **Classes de Layout:** Uso de containers, `row`s e `col`s (sistema de grid `s12 m4`).
  * **Efeito Parallax:** As classes `parallax-container` e `parallax` são o foco do template, usando as imagens `imagen01.jpg`, `imagen02.jpg` e `imagen03.jpg`.
  * **Tipografia:** Classes como `header center`, `teal-text text-lighten-2`, e `light` para estilos de texto.
  * **Botões:** `btn-large waves-effect waves-light` para botões com efeito *ripple* (ondas).

-----

## 📁 Estrutura do Projeto

```
template-materialize-parallax
├── css/
│   ├── materialize.min.css   # Arquivo CSS do framework Materialize.
│   └── estilos.css           # Estilos CSS customizados do projeto.
├── js/
│   ├── materialize.min.js    # Arquivo JS do framework Materialize.
│   └── configuracoes.js      # Script para inicialização dos componentes (e.g., parallax, sidenav).
├── imagens/
│   ├── imagen01.jpg          # Imagem de fundo para o primeiro Parallax.
│   ├── imagen02.jpg          # Imagem de fundo para o segundo Parallax.
│   └── imagen03.jpg          # Imagem de fundo para o terceiro Parallax.
└── index.html                # Página principal do template.
```

-----

## ⚙️ Tecnologias e Dependências

| Categoria | Tecnologia | Uso |
| :--- | :--- | :--- |
| **Framework** | Materialize CSS | Estilo e componentes de UI/UX. |
| **Scripts** | JQuery 2.1.1 | Dependência primária do Materialize. |
| **Scripts** | Materialize.js | Lógica para componentes dinâmicos (sidenav, parallax). |
| **Ícones** | Google Material Icons | Ícones do menu móvel e seções de destaque. |

-----

## 🚀 Como Executar o Projeto

### 1\. Requisitos

O projeto requer que você tenha os arquivos do Materialize e JQuery nas pastas `css/` e `js/` conforme referenciado no `index.html`.

### 2\. Abrir no Navegador

1.  Baixe ou clone os arquivos do repositório.
2.  Garanta que o arquivo `js/configuracoes.js` contenha o código de inicialização do Materialize (ex: `M.AutoInit()` ou inicialização específica para Parallax e Sidenav).
3.  Abra o arquivo `index.html` diretamente no seu navegador.

### ⚠️ Observação

O efeito *Parallax* e o *Sidenav* dependem da inicialização via JavaScript. Certifique-se de que seu arquivo `js/configuracoes.js` ou equivalente contenha o seguinte código básico (após o carregamento do jQuery e Materialize.js):

```javascript
document.addEventListener('DOMContentLoaded', function() {
    var elems = document.querySelectorAll('.parallax');
    M.Parallax.init(elems);
    
    var sidenav = document.querySelectorAll('.sidenav');
    M.Sidenav.init(sidenav);
});
```
