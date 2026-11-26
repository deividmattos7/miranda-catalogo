# Miranda Móveis — Catálogo digital (primeira versão)

Site responsivo em português, com catálogo público e página administrativa separada.

## Arquivos
- `index.html` — site público do catálogo, sem link para administração.
- `admin.html` — página administrativa separada (não é ligada pelo catálogo público).
- `assets/logo-miranda.png` — logo fornecida pelo usuário.
- `css/style.css` — estilo responsivo.
- `js/catalog.js` — busca, categorias, seleção de itens e WhatsApp.
- `js/admin.js` — cadastro, edição, exclusão, publicação/ocultação, upload de fotos e configurações.

## Aviso importante sobre esta versão
Esta é uma versão front-end para protótipo/testes. Produtos, configurações e imagens são guardados no `localStorage` do navegador. Isso significa:
- o catálogo e o painel, quando abertos no **mesmo navegador e dispositivo**, podem compartilhar as alterações locais;
- os visitantes em outros aparelhos não recebem atualizações feitas pelo administrador;
- não há autenticação real, banco de dados, proteção de acesso nem sincronização.

**Não use o painel para dados sensíveis e não considere a página admin protegida.** Para produção, a recomendação é conectar autenticação administrativa, banco de dados e armazenamento de imagens (por exemplo, Supabase), e deixar o catálogo público somente leitura.

## Rodar localmente
1. Extraia a pasta.
2. Abra `index.html` no navegador para ver o catálogo.
3. Abra `admin.html` separadamente para experimentar o painel.
4. Para WhatsApp, no painel > WhatsApp e configurações, informe o telefone no formato internacional, só números, por exemplo `55DDDNUMERO`.

## Publicar gratuitamente pelo GitHub Pages
1. Entre no GitHub e crie um repositório, por exemplo `miranda-catalogo`.
2. Envie (upload) **todos os arquivos e pastas desta extração** para a raiz do repositório. Confirme que `index.html` está na raiz, e não dentro de outra subpasta.
3. No repositório, vá em **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione branch `main` e folder `/ (root)`, depois Save.
6. Aguarde o GitHub Pages publicar. O link será parecido com `https://SEU-USUARIO.github.io/miranda-catalogo/`.
7. A página administrativa, nesta versão, terá URL separada: `https://SEU-USUARIO.github.io/miranda-catalogo/admin.html`. O catálogo não exibe link para ela, mas a URL não é protegida por login — não confunda separação de página com segurança.

## Próxima etapa recomendada para produção
- Implementar autenticação com conta admin e autorização no backend.
- Banco de dados compartilhado para produtos e categorias.
- Storage para fotos.
- Configurar vendedores/WhatsApp e regras de direcionamento.
- Testar publicação e catálogo nos celulares e computadores.
