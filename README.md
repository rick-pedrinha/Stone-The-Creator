# Stone The Creator — Estudo de HTML/CSS/JS

Site estático com estética psicodélica para o projeto **Stone The Creator**.  
Foco em **layout responsivo**, **tipografia futurista**, **player de áudio** e **integração com YouTube** — tudo com **HTML + CSS + JS** puro, ideal para estudo e portfólio.

![Preview do site](img/preview.png)

---

## 🔗 Demo
- **GitHub Pages**: https://SEU-USUARIO.github.io/stone-the-creator/  
  > Troque `SEU-USUARIO` após publicar nas *Pages*.

---

## ✨ Destaques
- **Design responsivo** (Grid/Flex), espaçamentos confortáveis
- Identidade visual: título com **Orbitron** + paleta “verde Monster”
- **Hero** com avatar
- **Galeria** e **Lançamentos**
- **Player de áudio** com playlist (WAV/MP3) e capa dinâmica
- **Vídeos do YouTube** (nocookie) em grade responsiva
- **Formulário** semântico e acessível (labels, inputs, textarea)
- Sem frameworks — fácil de entender, manter e publicar

---

## 🧱 Estrutura
/
├─ index.html
├─ img/
│ ├─ preview.png
│ ├─ WhatsApp Image 2025-10-14 at 17.32.07.jpeg
│ └─ ...
├─ musicas/
│ ├─ ATLANTIS Stone The Creator,Marsaw - Track1 V2 (Mastered).wav
│ └─ (opcional) stone_atlantis.mp3
├─ README.md
├─ LICENSE
└─ .gitignore

markdown
Copiar código
> **GitHub Pages é case-sensitive**: nomes/caminhos devem bater exatamente. Para nomes com espaços/acentos, use URL codificada no `src` (`%20`, `%28`, `%29`).

---

## ▶️ Rodar localmente
- Abra `index.html` no navegador (duplo clique).  
- Para testar melhor mídias, use a extensão **Live Server** (VS Code) ou qualquer servidor local.

---

## 🚀 Deploy (GitHub Pages, sem terminal)
1. Crie um repositório **público** (ex.: `stone-the-creator`).
2. **Add file → Upload files**: envie **todos** os arquivos e pastas.
3. **Settings → Pages**  
   - **Build and deployment → Source**: *Deploy from a branch*  
   - **Branch**: `main` | **Folder**: `/` (root) → **Save**
4. Aguarde 1–2 minutos e abra o link das Pages:  
   `https://SEU-USUARIO.github.io/stone-the-creator/`

**Soluções rápidas**  
- 404 geral → confira `main / root` nas Pages.  
- 404 em mídia → abra F12 → Network → verifique nome/caminho exatos.  
- WAV > 100 MB → GitHub bloqueia. Adicione também **MP3** e use duas `<source>`.

---

## 🎵 Player — adicionar MP3
```html
<audio controls>
  <source src="musicas/stone_atlantis.mp3" type="audio/mpeg">
  <source src="musicas/ATLANTIS%20Stone%20The%20Creator%2CMarsaw%20-%20Track1%20V2%20%28Mastered%29.wav" type="audio/wav">
</audio>
Na playlist, duplique um <li class="track"> e ajuste data-src, data-title, data-cover.

🎬 Vídeos — adicionar/remover
html
Copiar código
<div class="yt-wrap">
  <iframe
    src="https://www.youtube-nocookie.com/embed/ID_DO_VIDEO?start=0&rel=0"
    title="Stone The Creator - Vídeo X"
    loading="lazy"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen>
  </iframe>
</div>
IDs usados: tObxHPsB1LI, 6jvpaf6UgfU, _oTfk5aukQc (com start=167 quando necessário).

♿ Acessibilidade
HTML semântico (header, nav, section, figure, footer)

label ligado a input/textarea

alt nas imagens essenciais

bom contraste

controles com aria-label nos botões extra do player

🔍 SEO básico (opcional)
Coloque no <head>:

html
Copiar código
<meta name="description" content="Stone The Creator — site estático com estética psicodélica, player de áudio e vídeos.">
<meta property="og:title" content="Stone The Creator" />
<meta property="og:description" content="Estudo de HTML/CSS/JS: site psicodélico, responsivo e com player." />
<meta property="og:image" content="https://SEU-USUARIO.github.io/stone-the-creator/img/preview.png" />
<meta property="og:type" content="website" />
<meta property="og:url" content="https://SEU-USUARIO.github.io/stone-the-creator/" />
<meta name="twitter:card" content="summary_large_image" />
⚡ Performance (dicas)
Prefira MP3 para streaming; deixe WAV como opção secundária

Otimize imagens (ex.: 1280px de largura para o preview)

Use loading="lazy" onde couber

Reduza famílias/pesos de fontes se quiser mais leveza

🧩 Personalização
Título: troque Orbitron por Audiowide/Monoton etc.

Cores: edite variáveis no :root (--bg, --surface, --ink…)

Avatar: troque a imagem da classe .avatar

❓ FAQ
Não toca automaticamente → navegadores bloqueiam autoplay; clique em Play.
404 em mídia → verifique case e caminhos (F12 → Network → Status 200).
WAV grande não sobe → limite do GitHub é 100 MB por arquivo; use MP3 também.

🗺️ Roadmap
Botão flutuante de WhatsApp

Tema claro/escuro

PWA (instalável)

Animações suaves no título

🤝 Contribuição
Sugestões? Abra Issues e PRs. Para trabalhos/collabs, use o formulário do site.

📝 Licença
MIT — veja LICENSE.

👤 Autor
Henrique Pedrinha (Stone The Creator) — Brasília/DF
