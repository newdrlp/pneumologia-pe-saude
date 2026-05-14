# Pneumologia PE - Vida e Saude

Landing page piloto para migracao gradual do Netlify para GitHub Pages.

Dominio previsto: https://saude.pneumologia-pe.com.br

## Estrutura

- `index.html`: landing da clinica Vida e Saude / Clinica dos Feirantes.
- `CNAME`: dominio customizado do GitHub Pages.
- `pre-atendimento/index.html`: rota publica alinhada ao dominio, redirecionando para a ficha central com `clinica=saude`.
- `preatendimento/index.html`: compatibilidade com links antigos sem hifen.

## Publicacao

GitHub Pages deve publicar a branch `main` a partir da raiz `/`.