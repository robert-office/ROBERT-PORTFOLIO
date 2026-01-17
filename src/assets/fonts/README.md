# Fontes do Projeto

Esta pasta deve conter os arquivos de fonte **Aeonik** e **Input**.

## Arquivos necessários:

### Aeonik
- `Aeonik-Regular.woff2`
- `Aeonik-Regular.woff`
- `Aeonik-Bold.woff2`
- `Aeonik-Bold.woff`

### Input
- `Input-Regular.woff2`
- `Input-Regular.woff`
- `Input-Bold.woff2`
- `Input-Bold.woff`

## Como adicionar as fontes:

1. Coloque os arquivos de fonte nesta pasta (`src/assets/fonts/`)
2. As fontes já estão configuradas no `main.css` e `tailwind.config.js`

## Como usar no código:

### Com Tailwind CSS:
```vue
<h1 class="font-aeonik">Texto com Aeonik</h1>
<p class="font-input">Texto com Input</p>
```

### Com CSS inline:
```vue
<h1 style="font-family: Aeonik, sans-serif">Texto com Aeonik</h1>
<p style="font-family: Input, Arial, sans-serif">Texto com Input</p>
```

## Onde obter as fontes:

- **Aeonik**: https://www.fontshare.com/fonts/aeonik (versão gratuita disponível)
- **Input**: https://input.djr.com/ (fonte comercial, requer licença)
