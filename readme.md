# Mapa com Pontos de Interesse

Este é um projeto de mapa interativo que permite aos usuários adicionar, editar, excluir e visualizar pontos de interesse categorizados. Os dados são salvos localmente no `localStorage` do navegador, permitindo que os pontos persistam entre as sessões.

## Funcionalidades

* **Adicionar Pontos:** Clique no botão "Adicionar ponto" e, em seguida, clique em qualquer lugar do mapa para abrir um formulário e adicionar um novo marcador.
* **Categorias:** Cada ponto pode ser classificado em uma das quatro categorias:
    * Ocorrência (Vermelho)
    * Vigilância (Verde)
    * Apreensão (Azul)
    * Outro (Amarelo)
* **Editar e Excluir:** Ao clicar em um ponto existente, um pop-up é exibido com os botões "Editar" e "Apagar".
* **Persistência de Dados:** Todos os pontos criados são salvos no `localStorage` do navegador e recarregados automaticamente ao abrir a página.
* **Pesquisa de Endereço:** Uma barra de pesquisa no canto superior direito (utilizando *Leaflet Control Geocoder*) permite ao usuário pesquisar e voar para endereços específicos.
* **Pesquisa de Pontos:** Uma segunda barra de pesquisa (utilizando *Leaflet Search*) permite pesquisar os pontos de interesse já adicionados pelo nome ou descrição.
* **Localização do Usuário:** Um botão de localização (utilizando *Leaflet Locate Control*) centraliza o mapa na localização atual do usuário. Um modal de confirmação é exibido antes de ativar o recurso, alertando sobre a possível imprecisão em computadores.

## Tecnologias Utilizadas

* **HTML5**
* **CSS3**
* **JavaScript (ES6+)**
* **Leaflet.js v1.9.4:** A biblioteca principal para o mapa interativo.
* **Plugins do Leaflet:**
    * `leaflet-control-geocoder`: Para a funcionalidade de pesquisa de endereços.
    * `leaflet.locatecontrol`: Para a funcionalidade de "mostrar minha localização".
    * `leaflet-search`: Para a funcionalidade de pesquisa de marcadores.

## Como Executar

Este é um projeto puramente front-end e não requer um back-end.

1.  Clone ou baixe este repositório.
2.  Certifique-se de que os arquivos `index.html` e `styles.css` estejam no mesmo diretório.
3.  Abra o arquivo `index.html` em qualquer navegador web moderno.

**Nota:** Para que a funcionalidade de geolocalização (localização do usuário) funcione corretamente, pode ser necessário servir os arquivos a partir de um servidor web local (por exemplo, usando a extensão "Live Server" no VS Code ou um simples comando `npx serve`) em vez de abrir o `index.html` diretamente do sistema de arquivos (`file:///...`), devido às políticas de segurança do navegador.