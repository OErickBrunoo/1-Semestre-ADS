## 🍹 Bebidas Imaginárias Diferentes

**Um catálogo de bebidas fictícias, utilizando uma estrutura moderna e responsiva baseada em HTML, CSS (Bootstrap) e um mapa interativo com Leaflet.**

-----

## 📝 Descrição Geral

Este projeto é uma *landing page* e um pequeno catálogo para uma loja fictícia de bebidas, a **Bebidas Imaginárias Diferentes**. O objetivo é apresentar os produtos em um formato atraente e profissional, utilizando as melhores práticas de desenvolvimento web front-end.

O site foi construído com foco em:

  * **Design Responsivo:** Utilização do *framework* **Bootstrap 5** para garantir que o layout se adapte perfeitamente a qualquer dispositivo.
  * **Navegação Dinâmica:** Um menu de navegação que se transforma em "menu hambúrguer" em telas menores e apresenta um *dropdown* para "Poções Especiais".
  * **Visualização Geográfica:** Integração da biblioteca **Leaflet** para exibir um mapa interativo da localização da loja na "Cidade Imaginária".
  * **Estrutura Modular:** Separação clara de arquivos HTML para cada produto e uso de links para bibliotecas externas (Font Awesome, Leaflet, Bootstrap).
  * **Estilo Moderno:** Rodapé com gradiente colorido e ícones de redes sociais.

-----

## 💡 Principais Funcionalidades

### Catálogo de Produtos

O site apresenta três bebidas principais, cada uma com sua própria página de detalhes e descrição dos ingredientes:

  * **Chá Verde Cooler:** Combina chá verde, folhas de camomila e gengibre, sendo rico em vitaminas e minerais.
  * **Framboesa Geladinha:** Uma mistura de suco de framboesa, capim-limão, raspas de gelo e fruto da roseira-brava, para clarear e revigorar a mente.
  * **Elixir da Felicidade:** Essência de vacínio e cereja misturadas a uma base de chá de ervas da flor do sabugueiro, proporcionando um estado relaxado de felicidade.

### Navegação (Navbar)

  * **Bootstrap Navbar:** Menu fixo no topo com logomarca e links de navegação.
  * **Dropdown:** Seção "Poções Especiais" com itens de menu fictícios (Sérum da Serenidade, Filtro da Fortuna, Licor do Luar Místico).
  * **Estilização:** Links de navegação coloridos por categoria (`text-primary`, `text-success`, `text-danger`, `text-purple`).

### Mapa Interativo (Leaflet)

A página inicial (`index.html`) exibe um mapa da "Cidade Imaginária", permitindo aos usuários a visualização de "Como Chegar" até a loja, localizada na "Rua Sem Número".

-----

## ⚙️ Tecnologias e Dependências

| Categoria | Tecnologia | Uso |
| :--- | :--- | :--- |
| **Estrutura** | HTML5 | Conteúdo principal e semântica. |
| **Estilo** | Bootstrap 5 | Layout responsivo, componentes de navegação e *utility classes*. |
| **Estilo Extra** | CSS3 (em `css/estilos.css`) | Estilos customizados e complementares. |
| **Mapa** | Leaflet | Biblioteca para renderização do mapa interativo. |
| **Ícones** | Font Awesome | Ícones de redes sociais no rodapé. |
| **Ícones** | Bootstrap Icons | Ícones adicionais. |

-----

## 📁 Estrutura do Projeto

```
bebidas-imaginarias
├── css/
│   ├── bootstrap.min.css    # Arquivos CSS do Bootstrap.
│   └── estilos.css          # Estilos CSS customizados do projeto.
├── js/
│   ├── bootstrap.bundle.min.js # Arquivos JS do Bootstrap (para menu, dropdown).
│   └── configuracoes.js     # Lógica JavaScript para o mapa (não fornecido, mas referenciado no HTML).
├── imagens/                 # Diretório para imagens (logo.png, drinks.png, chaverde.png, etc.).
├── index.html               # Página inicial (landing page) com o mapa.
├── chaverdecooler.html      # Página de detalhes do Chá Verde Cooler.
├── framboesageladinha.html  # Página de detalhes da Framboesa Geladinha.
├── elixirdafelicidade.html  # Página de detalhes do Elixir da Felicidade.
└── README.md                # Documentação do projeto.
```

-----

## 🚀 Como Visualizar o Projeto

### 1\. Clonar o Repositório

```bash
git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
```

### 2\. Abrir no Navegador

1.  Navegue até o diretório clonado.
2.  Clique duas vezes no arquivo `index.html` ou abra-o em qualquer navegador web.

Como o projeto utiliza bibliotecas CDN para Leaflet e Font Awesome, e os arquivos de terceiros (Bootstrap) estão referenciados em pastas locais, ele pode ser executado diretamente do seu sistema de arquivos local.

