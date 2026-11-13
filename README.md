# Planos e PreÃ§os

PÃ¡gina de planos e preÃ§os com trÃªs cards responsivos, construÃ­da com HTML, CSS e JavaScript puro, sem frameworks e sem dependÃªncias externas. Os cards usam flexbox para manter o mesmo alinhamento em qualquer largura de tela, e um efeito de confetes desenhado em canvas adiciona um toque visual sem atrapalhar a leitura.

> ðŸ”— **Demo:** adicione aqui o link do GitHub Pages, se publicar.

---

## âœ¨ Funcionalidades

- **TrÃªs planos lado a lado** (Basic, Pro e Premium), com recursos incluÃ­dos e excluÃ­dos marcados por Ã­cones.
- **Alinhamento consistente:** os cards tÃªm a mesma altura na linha, e o botÃ£o de cada plano fica sempre na base, mesmo com listas de tamanhos diferentes.
- **Layout responsivo:** os cards quebram para a linha de baixo em telas menores e ocupam a largura total no celular.
- **Confetes animados em canvas:** cada card tem sua prÃ³pria animaÃ§Ã£o, que se ajusta ao tamanho do card ao redimensionar a janela.
- **Hover com elevaÃ§Ã£o** em dispositivos com mouse, respeitando a preferÃªncia de movimento reduzido do sistema.
- **Foco visÃ­vel** nos botÃµes, para navegaÃ§Ã£o pelo teclado.

## ðŸ› ï¸ Tecnologias

| Tecnologia | Uso |
| --- | --- |
| HTML5 semÃ¢ntico | Estrutura da pÃ¡gina, com `canvas` marcado como decorativo (`aria-hidden`) |
| CSS3 | Flexbox, variÃ¡veis CSS, media queries e seletores com escopo por classe |
| JavaScript (ES6+) | AnimaÃ§Ã£o dos confetes com `requestAnimationFrame` e `getContext('2d')` |

## ðŸ“ Estrutura do projeto

```
PreÃ§o de Planos/
â”œâ”€â”€ index.html    # Estrutura da pÃ¡gina e script dos confetes
â”œâ”€â”€ styles.css    # Estilos, variÃ¡veis, layout e responsividade
â”œâ”€â”€ assets/
â”‚   â””â”€â”€ fundo-cafe.jpg   # Imagem de fundo do container
â””â”€â”€ README.md
```

## ðŸš€ Como executar

NÃ£o hÃ¡ dependÃªncias. Basta:

```bash
# 1. Clone o repositÃ³rio
git clone https://github.com/LuisMano/pricing-plans.git

# 2. Entre na pasta
cd pricing-plans

# 3. Abra o index.html no navegador
```

Ou use um servidor local, como a extensÃ£o **Live Server** do VS Code.

> Confira se a pasta `assets/` existe e contÃ©m `fundo-cafe.jpg`. Sem ela, o fundo da pÃ¡gina aparece sem imagem.

## ðŸ§  DecisÃµes tÃ©cnicas

- **Flexbox no container e no card:** o container usa `flex-wrap` e `justify-content: center`, e o card usa `flex-direction: column`. Com isso, o botÃ£o pode ser empurrado para a base com `margin-top: auto`, sem depender de alturas fixas.
- **`min-width: 0` no card:** evita que um texto longo estoure o layout.
- **Seletores com classe:** todos os estilos usam classes, como `.titulo-plano` e `.recursos`, para nÃ£o afetar outras partes de um site maior.
- **VariÃ¡veis CSS:** cores e fontes ficam em `:root`, entÃ£o um ajuste de tema exige mudar apenas uma linha.
- **Ãcones com flexbox:** o âœ” e o âœ— sÃ£o pseudo-elementos com largura fixa, alinhados ao texto pelo prÃ³prio layout, sem `top` negativo.
- **Imagem local:** o fundo vem da pasta `assets/`, e nÃ£o de um link externo que poderia sair do ar.
- **Confetes decorativos:** o canvas fica atrÃ¡s do conteÃºdo, com `pointer-events: none`, para nÃ£o bloquear cliques nos botÃµes.

## â™¿ Acessibilidade

- Contraste de texto acima de 4,5:1 sobre o fundo branco dos cards.
- Canvas decorativo oculto de leitores de tela com `aria-hidden="true"`.
- BotÃµes com contorno visÃ­vel ao receber foco pelo teclado.

## ðŸ—ºï¸ PrÃ³ximos passos

- [ ] Respeitar `prefers-reduced-motion` no script dos confetes, pausando a animaÃ§Ã£o
- [ ] Mover o script para um arquivo separado, `script.js`
- [ ] Tornar os botÃµes funcionais, levando a uma pÃ¡gina de checkout ou de cadastro

## ðŸ‘¤ Autor

**LuisMnao**, desenvolvedor em formaÃ§Ã£o com foco em JavaScript e Node.js.

## ðŸ“„ LicenÃ§a

Projeto aberto para estudo e portfÃ³lio. Sinta-se Ã  vontade para usar como referÃªncia.

