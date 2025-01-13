# Projeto Frontend

## Descrição

Este projeto é uma página web responsiva com um layout moderno e limpo. Ele utiliza **HTML** e **CSS** para criar uma interface flexível e visualmente atraente. A página inclui um cabeçalho, uma seção principal com uma imagem com conteúdo, e um rodapé com links para redes sociais. O design garante alinhamento e funcionalidade adequados em diferentes tamanhos de tela, desde desktops até dispositivos móveis.

## Funcionalidades

- **Design Responsivo**: Adapta-se perfeitamente a diferentes tamanhos de tela, garantindo uma ótima experiência do usuário em desktops, tablets e smartphones.
- **Seção foto**: Inclui uma imagem e conteúdo adjacente, organizados lado a lado utilizando CSS Grid.
- **Rodapé**: Links para redes sociais alinhados à direita para desktops e tornando o posicionamento centralizados ao redimensionar a tela.
- **Estilo Personalizado**: Inclui efeitos de hover e redimensionamento dinâmico para melhor interatividade.

## Tecnologias Utilizadas

- **HTML5**
- **CSS3**
  - CSS Grid
  - CSS Flex
  - Media Queries

## Estrutura de Arquivos

```
pasta-do-projeto/

|-- index.html

|-- src/
    |-- reset.css
    |-- responsivo.css
    |-- style.css

|-- images/
    |-- bg-desktop.svg
    |-- bg-mobile.svg
    |-- illustration-mockups.svg
    |-- favicon-32x32.png
    |-- logo.png

```

## Como Executar

1. Clone o repositório ou faça o download dos arquivos do projeto.
2. Abra o arquivo `index.html` em qualquer navegador moderno.
3. Ajuste o tamanho da janela do navegador para visualizar o design responsivo em ação.

## Media Queries

Os seguintes pontos de quebra foram usados para garantir a responsividade:

- **740px e abaixo**: Ajusta o layout do grid para uma única coluna, melhorando a legibilidade em tablets.
- **570px e abaixo**: Ajusta ainda mais os tamanhos de fonte, dimensões das imagens e o padding dos botões para dispositivos móveis.Otimiza espaçamentos e alinhamentos para telas pequenas.

## Principais Conceitos de CSS

### CSS Grid

O container `.main` utiliza CSS Grid para estruturar a seção foto:

```css
.main {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto;
  gap: 20px;
}
```

### Ajustes Responsivos

Com media queries, os elementos são estilizados para telas menores. Exemplo:

```css
@media (max-width: 570px) {
 .main {
      grid-template-columns: 1fr;
      padding: 10px;
    }
    .header img {
      max-width: 200px;
      align-self: flex-start;
    }
    .foto{
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .foto-image {
      max-width: 300px;
      align-self: center; 
    }
}
```

### Alinhamento do Rodapé no desktop

Os links das redes sociais no rodapé mantêm o alinhamento utilizando `flexbox`:

```css
.footer {
  display: flex;
  justify-content: flex-end;
  gap: 20px;
}
```

### Alinhamento do Rodapé em telas menores

Os links das redes sociais no rodapé fazem o alinhamento utilizando `flexbox`:

```css
.footer {
  justify-content: center;
  gap: 10px;
}
```


## Créditos

Criado por Lucas Manhães De Almeida Lourenço.

Desafio do Frontend Mentor-Huddle landing page with single introductory section.