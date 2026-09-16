# IJ Som

Site institucional da IJ Som, empresa de estrutura para eventos (som, painéis de LED, iluminação, palco e equipe técnica).

Página única, sem build e sem dependência de servidor. Basta abrir o `index.html` no navegador.

## Arquivos

```
index.html      página inteira (HTML, CSS e JavaScript)
img/            logo e fotos usadas no site
```

## Formulário de orçamento

O formulário no fim da página não envia e não guarda nada. Ele monta uma mensagem formatada com as respostas e abre o WhatsApp da empresa já com o texto pronto, para o cliente apenas conferir e mandar.

O número fica em uma constante no topo do script, dentro do `index.html`:

```js
var WHATSAPP = '5531999777676';
```

Para trocar, mude essa linha e também os links `wa.me` espalhados no cabeçalho, no rodapé e no botão flutuante.

## Trocar ou acrescentar fotos

Coloque o arquivo em `img/` e aponte o `src` da imagem correspondente no `index.html`. As três fotos atuais ficam na seção de estrutura, marcadas por um comentário no código.

Vale comprimir as imagens antes de subir. As atuais têm entre 190 KB e 300 KB e dá para reduzir bastante sem perda visível.

## Publicar com GitHub Pages

1. No repositório, abra **Settings** e depois **Pages**.
2. Em *Source*, escolha **Deploy from a branch**.
3. Selecione a branch `main` e a pasta `/ (root)`. Salve.

Em poucos minutos o site fica no ar em `https://fern4ndinh0.github.io/ij-som/`.

## Pontos em aberto

- A faixa logo abaixo do título usa selos qualitativos no lugar de números. Quando houver dados reais de eventos realizados e tempo de mercado, dá para trocar. O local está marcado por um comentário no HTML.
- Não há seção de depoimentos. Ela só deve entrar com depoimentos verdadeiros e autorizados pelos clientes.
- O Tailwind vem por CDN, o que é prático mas gera um aviso no console do navegador. Para produção, o ideal é gerar o CSS compilado e embutir no arquivo.
