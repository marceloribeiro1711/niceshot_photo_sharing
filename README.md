# NiceShot

Tudo na raiz do repositório:

- `index.html`, `sw.js`, `manifest.webmanifest`, `icons/`, `.nojekyll` — app do participante, com o admin embutido (cinco toques na versão), publicados pelo GitHub Pages (Settings > Pages > Deploy from a branch > `main` / `(root)`).
- `worker.js`, `wrangler.jsonc` — API na Cloudflare (Workers & Pages > `niceshot-api` > Settings > Builds > Root directory: `/`).

Chaves (`GOOGLE_API_KEY`, `ADMIN_KEY`, `TOKEN_SECRET`, `MAC_KEY`) ficam só na Cloudflare, nunca neste repositório.

Para atualizar: edite o arquivo e faça commit na branch `main`. O Pages e a Cloudflare publicam sozinhos.

Busca por selfie (correio): o `wrangler.jsonc` já declara o `FILA`, que a Cloudflare cria no deploy. A senha `MAC_KEY` (Settings > Variables and Secrets) só é necessária quando o Photo Server do Mac entrar em uso.
