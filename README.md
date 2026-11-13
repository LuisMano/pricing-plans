# Planos e Preços

Página de planos e preços com três cards responsivos, construída com HTML, CSS e JavaScript puro, sem frameworks e sem dependências externas. Os cards usam flexbox para manter o mesmo alinhamento em qualquer largura de tela, e um efeito de confetes desenhado em canvas adiciona um toque visual sem atrapalhar a leitura.

> 🔗 **Demo:** https://luismano.github.io/pricing-plans/

---

## ✨ Funcionalidades

- **Três planos lado a lado** (Basic, Pro e Premium), com recursos incluídos e excluídos marcados por ícones.
- **Alinhamento consistente:** os cards têm a mesma altura na linha, e o botão de cada plano fica sempre na base, mesmo com listas de tamanhos diferentes.
- **Layout responsivo:** os cards quebram para a linha de baixo em telas menores e ocupam a largura total no celular.
- **Confetes animados em canvas:** cada card tem sua própria animação, que se ajusta ao tamanho do card ao redimensionar a janela.
- **Hover com elevação** em dispositivos com mouse, respeitando a preferência de movimento reduzido do sistema.
- **Foco visível** nos botões, para navegação pelo teclado.

## 🛠️ Tecnologias

| Tecnologia | Uso |
| --- | --- |
| HTML5 semântico | Estrutura da página, com `canvas` marcado como decorativo (`aria-hidden`) |
| CSS3 | Flexbox, variáveis CSS, media queries e seletores com escopo por classe |
| JavaScript (ES6+) | Animação dos confetes com `requestAnimationFrame` e `getContext('2d')` |

## 📁 Estrutura do projeto

```
Preço de Planos/
├── index.html    # Estrutura da página e script dos confetes
├── styles.css    # Estilos, variáveis, layout e responsividade
├── assets/
│   └── fundo-cafe.jpg   # Imagem de fundo do container
└── README.md
```

## 🚀 Como executar

Não há dependências. Basta:

```bash
# 1. Clone o repositório
git clone https://github.com/LuisMano/pricing-plans.git

# 2. Entre na pasta
cd pricing-plans

# 3. Abra o index.html no navegador
```

Ou use um servidor local, como a extensão **Live Server** do VS Code.

> Confira se a pasta `assets/` existe e contém `fundo-cafe.jpg`. Sem ela, o fundo da página aparece sem imagem.

## 🧠 Decisões técnicas

- **Flexbox no container e no card:** o container usa `flex-wrap` e `justify-content: center`, e o card usa `flex-direction: column`. Com isso, o botão pode ser empurrado para a base com `margin-top: auto`, sem depender de alturas fixas.
- **`min-width: 0` no card:** evita que um texto longo estoure o layout.
- **Seletores com classe:** todos os estilos usam classes, como `.titulo-plano` e `.recursos`, para não afetar outras partes de um site maior.
- **Variáveis CSS:** cores e fontes ficam em `:root`, então um ajuste de tema exige mudar apenas uma linha.
- **Ícones com flexbox:** o ✔ e o ✗ são pseudo-elementos com largura fixa, alinhados ao texto pelo próprio layout, sem `top` negativo.
- **Imagem local:** o fundo vem da pasta `assets/`, e não de um link externo que poderia sair do ar.
- **Confetes decorativos:** o canvas fica atrás do conteúdo, com `pointer-events: none`, para não bloquear cliques nos botões.

## ♿ Acessibilidade

- Contraste de texto acima de 4,5:1 sobre o fundo branco dos cards.
- Canvas decorativo oculto de leitores de tela com `aria-hidden="true"`.
- Botões com contorno visível ao receber foco pelo teclado.

## 🗺️ Próximos passos

- [ ] Respeitar `prefers-reduced-motion` no script dos confetes, pausando a animação
- [ ] Mover o script para um arquivo separado, `script.js`
- [ ] Tornar os botões funcionais, levando a uma página de checkout ou de cadastro

## 👤 Autor

**LuisMano**, desenvolvedor em formação com foco em JavaScript e Node.js.

## 📄 Licença

Projeto aberto para estudo e portfólio. Sinta-se à vontade para usar como referência.


