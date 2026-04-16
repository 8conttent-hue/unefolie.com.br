# CLAUDE.md — UNEFOLIE

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** UNEFOLIE
**Nicho:** Gastronomia
**Keywords:** Augusto Bittencourt Meu pai e padrinho seguiram o caminho da cozinha a
**Paleta de cores:** gold | **Fonte:** outfit

Augusto Bittencourt Meu pai e padrinho seguiram o caminho da cozinha, a convivência e admiração fez com que esse amor pela gastronomia me contaminasse também. Hoje sou grato por ter feito as escolhas que fiz... A criação da Une Folie Hoje temos um site, sistema de entrega, equipe de atendimento...mas essa jornada começou em 2015. Foi muito desejo e coragem no inicio, 5 anos depois de muitas parcerias e vitorias abrimos nossa presença no mercado de revenda e eventos. Hoje estamos consolidados no estado do Paraná, mais ainda buscamos crescer para vizinhos.



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-E |
| Hero | Hero-H |
| Features | Features-B |
| About Section | About-G |
| Posts | Posts-E |
| Footer | Footer-C |
| Página Sobre | Sobre-D |
| Página Contato | Contato-B |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
