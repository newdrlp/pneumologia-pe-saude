# Roteiro de migracao - piloto saude

Este roteiro documenta a sequencia usada no piloto `saude` para repetir depois nas demais clinicas.

## Modelo recomendado

Use um repositorio separado por clinica quando houver subdominio proprio em GitHub Pages.

Motivo: GitHub Pages aceita um unico `CNAME` por site, localizado na raiz da fonte publicada. Um unico repositorio com varias pastas nao consegue ter um `CNAME` diferente por pasta.

## Passos do piloto

1. Copiar a landing da clinica para a raiz do novo repositorio.
2. Criar `CNAME` na raiz com o subdominio final.
3. Remover arquivos especificos do Netlify, como `_redirects` e `_headers`.
4. Criar rota real para `/pre-atendimento/` quando for necessario manter URL bonita no dominio da clinica.
5. Publicar GitHub Pages em `main` a partir da raiz `/`.
6. No Wix, alterar o CNAME do subdominio para `newdrlp.github.io`.
7. Aguardar DNS e SSL do GitHub Pages.
8. Testar:
   - pagina inicial carrega com status 200;
   - logo e botoes aparecem;
   - WhatsApp abre corretamente;
   - `/pre-atendimento/` preserva `clinica=saude`;
   - envio ao Apps Script continua gravando na planilha.

## DNS no Wix para este piloto

| Subdominio | Tipo | Valor |
| --- | --- | --- |
| saude | CNAME | newdrlp.github.io |

## Depois de validar

Repita o mesmo padrao criando um repositorio por clinica, com o `CNAME` correspondente na raiz.