# Álbum de Fotografias Minimalista e Responsivo

Veja a demonstração deste Album: https://profedney.github.io/foto2/
Este é um projeto simples de um álbum de fotografias minimalista e responsivo, utilizando HTML e CSS com Flexbox. O álbum é estilizado para apresentar duas colunas de imagens em dispositivos de tela maior, como desktops, e uma coluna em dispositivos móveis.

## Características

- **Design responsivo**: O layout do álbum se adapta a diferentes tamanhos de tela. Em dispositivos grandes, as fotos são exibidas em duas colunas; em telas menores, como smartphones, as fotos ocupam uma coluna.
- **Estilização minimalista**: O projeto usa uma paleta de cores suave e fontes simples para manter o foco nas fotografias.
- **Flexbox**: Utilizado para organizar e alinhar as imagens, garantindo flexibilidade e facilidade de manutenção do layout.

## Layout

- **Desktop**: As fotos são exibidas em duas colunas, ocupando até 45% da largura do contêiner.
- **Mobile**: Quando a tela for menor que 768px, as fotos são reorganizadas para ocupar 100% da largura da tela, sendo exibidas em uma única coluna.
- **Mudança de cor de fundo**: A cor de fundo muda de rosa (para telas maiores) para azul claro (para telas menores), proporcionando uma leve diferenciação de estilo entre os dispositivos.

## Tecnologias Utilizadas

- **HTML**: Estrutura básica do álbum de fotos.
- **CSS com Flexbox**: Responsável pelo layout flexível e responsivo.
  
## Exemplo de Código

```css
body {
    background-color: pink;
    font-family: Arial, sans-serif;
    padding: 20px;
    text-align: center;
}

h1 {
    margin-bottom: 20px;
    color: #333;
}

.album {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
}

.foto {
    flex: 1 1 45%;
    max-width: 45%;
}

.foto img {
    width: 100%;
    height: auto;
    display: block;
}

@media only screen and (max-width: 768px) {
    body {
        background-color: lightblue;
    }
    .foto {
        flex: 1 1 100%;
        max-width: 100%;
    }
}
```

## Como Funciona

- O layout é controlado pela classe `.album`, que utiliza o Flexbox para criar um grid de imagens.
- A classe `.foto` define que cada imagem deve ocupar até 45% da largura do contêiner em telas grandes.
- Quando a tela tem largura menor que 768px, as fotos passam a ocupar 100% da largura, facilitando a visualização em dispositivos móveis.
- A cor de fundo muda de rosa para azul claro, quando a largura da tela é reduzida, oferecendo uma pequena distinção visual entre os modos desktop e mobile.

## Como Utilizar

1. Clone o repositório ou copie o código acima.
2. Adicione suas imagens dentro do contêiner `.album` seguindo a estrutura de HTML abaixo:

```html
<div class="album">
    <div class="foto">
        <img src="foto1.jpg" alt="Foto 1">
    </div>
    <div class="foto">
        <img src="foto2.jpg" alt="Foto 2">
    </div>
    <!-- Adicione mais imagens conforme necessário -->
</div>
```

3. Abra o arquivo HTML em um navegador para visualizar o álbum de fotografias em diferentes dispositivos.

## Licença

Este projeto é de uso livre e pode ser modificado e distribuído conforme a necessidade.
