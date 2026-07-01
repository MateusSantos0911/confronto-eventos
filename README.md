# Confronto eSocial × ERGON — versão web (compartilhável)

Ferramenta interna (PGE-RJ) que roda **100% no navegador**, offline, sem backend.
Nenhum dado do usuário sai do computador dele: a base de servidores e as planilhas
carregadas ficam apenas no `localStorage`/memória do próprio navegador.

Este repositório contém **apenas** a versão pública (`index.html`), que **não embute
nenhum dado pessoal**. A versão de uso pessoal (com base embutida) e os arquivos de
dados (`.csv`, `.xlsx`) estão no `.gitignore` e **nunca** devem ser versionados.

## Publicar / atualizar

O site é um único arquivo estático (`index.html`). Para atualizar:

1. Gere a nova versão compartilhável a partir do `tpl.html`.
2. Copie-a para cá como `index.html`.
3. `git add index.html && git commit -m "atualiza app" && git push`.

O deploy é automático (GitHub Pages / Cloudflare Pages).

## Privacidade

- A página em si é pública (qualquer um com o link a abre), mas **os dados nunca são
  enviados a servidor algum** — ficam só no navegador de quem usa.
- Para exigir **login** ao abrir a página, use Cloudflare Access na frente do site
  (ver instruções que acompanham o deploy).
