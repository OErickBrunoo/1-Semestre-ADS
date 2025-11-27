## Site Helicópteros de Luxo

**Um site responsivo e moderno para apresentar as aeronaves mais luxuosas do mercado.**

Este projeto é uma landing page e catálogo digital construído com **HTML5**, **CSS3** (utilizando design responsivo) e **JavaScript**, com integração de um mapa interativo usando a biblioteca **Leaflet**.

### ✨ Principais Recursos

  * **Design Responsivo:** A navegação e o conteúdo se adaptam perfeitamente a dispositivos móveis (o menu `navbar` se transforma em um "menu hambúrguer" em telas pequenas).
  * **Catálogo de Produtos:** Páginas dedicadas para helicópteros de alto luxo:
      * **Eurocopter EC130 T2**
      * **Bell 525 Relentless**
      * **EC 145 Mercedes-Benz Style** (colaboração entre Airbus Helicopters e Mercedes-Benz).
  * **Mapa Interativo:** O site principal (`index.html`) apresenta a localização da loja ("Cidade Aeroviária") usando a biblioteca [Leaflet](https://leafletjs.com/), facilitando a visualização de "Como Chegar".
  * **Estrutura Limpa:** Código bem organizado, separando estilos (`estilos.css`) e lógica principal (diretamente nos arquivos HTML para funções simples de navegação e mapa).

### 🛠️ Tecnologias Utilizadas

| Tecnologia | Descrição |
| :--- | :--- |
| **HTML5** | Estrutura de todas as páginas e conteúdo. |
| **CSS3** | Estilização completa e media queries para responsividade. |
| **JavaScript** | Controle de navegação do menu e funcionalidades do mapa. |
| **Leaflet** | Biblioteca JS de código aberto para mapas interativos. |

### 📂 Estrutura do Projeto

O projeto está organizado na seguinte estrutura de arquivos:

```
.
├── index.html            # Página inicial com o mapa e informações da loja.
├── Bell.html             # Página de detalhes do helicóptero Bell 525 Relentless.
├── Eurocopter.html       # Página de detalhes do helicóptero Eurocopter EC130 T2.
├── Mercedes.html         # Página de detalhes do helicóptero EC 145 Mercedes-Benz Style.
├── estilos.css           # Arquivo principal de estilos CSS (inclui media queries).
├── configuracoes.js      # (Arquivos não utilizados no HTML principal, mas presente no projeto.)
└── imagens/              # Diretório para todas as imagens do projeto (logo, modelos, etc.).
```

### 🗺️ Configuração do Mapa

O mapa interativo na página `index.html` utiliza a biblioteca Leaflet e está configurado para mostrar a localização na **Cidade Aeroviária**.

  * **Coordenadas:** As coordenadas centrais são `[-15.87198, -47.91970]`.
  * **Tile Layer:** Utiliza o provedor de mapas OpenStreetMap.

<!-- end list -->

```html
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script>
    const cidadeAeroviaria = [-15.87198, -47.91970];
    const map = L.map('map').setView(cidadeAeroviaria, 14);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: 'Mapa da Cidade Aeroviária © OpenStreetMap contributors'
    }).addTo(map);

    // ... código do marker ...
</script>
```

### 🔗 Como Visualizar o Projeto

Para visualizar o projeto, siga estas etapas simples:

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
    ```
2.  **Navegue até o diretório:**
    ```bash
    cd NOME_DO_REPOSITORIO
    ```
3.  **Abra o arquivo:**
    Simplesmente clique duas vezes no arquivo `index.html` no seu explorador de arquivos ou arraste-o para o seu navegador.

