# Página de Planos e Preços

Página estática com três planos de assinatura (Basic, Pro e Premium), feita com HTML, CSS e JavaScript puro. Cada card mostra preço, lista de benefícios incluídos e excluídos, e um botão de escolha. Os cards têm confetes animados em canvas e um layout responsivo.

## Demonstração rápida

- Três cards lado a lado em telas grandes.
- Em celular, os cards ficam um embaixo do outro, em largura total.
- Confetes caem dentro de cada card, sem sair da borda.

## Como executar

Não há dependências nem build. Basta abrir o arquivo `index.html` no navegador.

```bash
git clone <url-do-repositorio>
cd <pasta-do-projeto>
# abra index.html no navegador
```

Para testar o responsivo, use o DevTools (F12) com o modo de celular (Ctrl + Shift + M).

## Estrutura do projeto

```
.
├── index.html    # estrutura da página e script dos confetes
├── styles.css    # layout, cores, responsivo e efeitos
└── README.md     # documentação do projeto
```