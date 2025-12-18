# Instruções para Agentes AI — Site Gio (Portfólio Giovanna Marques)

**Resumo:** Site estático de portfólio de design gráfico. Não há build, testes ou dependências — alterações diretas em HTML/CSS.

## Estrutura Exigida do Projeto

```
Site Gio/
├── index.html              # HTML principal (estrutura semântica)
├── styles.css              # Estilos responsivos
├── imagens/                # Pasta com todas as imagens (obrigatória)
│   ├── group1.png          # Hero section (cabeçalho principal)
│   ├── foto1.png           # Foto ao lado de "Sobre mim"
│   ├── outdoor_kalista.png # Projeto Kalista Rose
│   ├── outdoor_milkshake_mix.png  # Projeto MilkShake Mix
│   ├── logo_astra.png      # Logo Astra
│   ├── etiqueta_astra.png  # Mockup 1 - Astra
│   ├── ecobag_astra.png    # Mockup 2 - Astra
│   ├── estrelas_esquerda.png # Decoração lado esquerdo
│   ├── estrelas_direita.png  # Decoração lado direito
│   ├── linkedin.png        # Ícone LinkedIn
│   └── whatsapp.png        # Ícone WhatsApp
└── .github/
    └── copilot-instructions.md
```

## Arquitetura Visual Fiel à Imagem group1.png

### Seções em Ordem
1. **Hero** — `group1.png` em fullwidth com `border-radius: 122px`
2. **Sobre mim** — `foto1.png` (esquerda) + texto (direita), layout flex
3. **Portfólio Acadêmico** — 3 projetos em estrutura vertical:
   - Kalista Rose com `outdoor_kalista.png`
   - MilkShake Mix com `outdoor_milkshake_mix.png`
   - Astra com `logo_astra.png` (esquerda) + texto (direita) + 2 mockups (`etiqueta_astra.png`, `ecobag_astra.png`) abaixo
4. **Obrigada por chegar até aqui** — `estrelas_esquerda.png` (esquerda) + texto (centro) + `estrelas_direita.png` (direita)
5. **Contato** — `linkedin.png` + link + `whatsapp.png` + link

### Tipografia
- **Títulos (h2, h3):** `Gloock` (importada via Google Fonts)
- **Corpo:** `Ibarra Real Nova` (importada via Google Fonts)
- **Cores:** Gradiente fundo `linear-gradient(180deg, rgba(27,17,17,0.99) 17.79%, #4A1515 54.81%, rgba(115,20,20,0.8) 83.18%)`

### Links Obrigatórios
- LinkedIn: `https://linkedin.com/in/marquesgio/`
- WhatsApp: `https://wa.me/5521988869947` (21 98886-9947)

## Padrões Detectados

- **Caminhos:** todas as imagens usam `imagens/` (pasta em português)
- **Nomes de classe:** `.hero`, `.about-section`, `.portfolio-section`, `.closing-section`, `.contact-section`
- **Layout flex:** seções About e Astra usam `display: flex` para lado-a-lado
- **Responsividade:** breakpoints 1024px, 768px, 480px
- **Fontes:** carregadas via CDN do Google Fonts (não desincluir `<link href="https://fonts.googleapis.com/...">`)

## Fluxos Comuns

**Adicionar imagem ao projeto:**
1. Coloque arquivo em `imagens/`
2. Atualize `src` em `index.html` com o caminho relativo (ex.: `imagens/nova_imagem.png`)

**Alterar texto:**
- Edite direto em `index.html` respeitando a estrutura HTML

**Ajustar estilos:**
- Edite `styles.css` respeitando gradiente, tipografia e responsive design

## O que NÃO fazer

- ❌ Não criar dependências npm/pip
- ❌ Não referenciar caminhos absolutos (ex.: `C:/Users/...`)
- ❌ Não remover imports de fontes Google
- ❌ Não alterar URLs de contato sem consultar
- ❌ Não quebrar estrutura flex das seções About, Astra e Closing

## Referências de Arquivo Chave

- **Hero:** `index.html` linhas ~14-16 (`.hero` com `img.hero-image`)
- **About:** `index.html` linhas ~19-35 (`.about-wrapper` flex layout)
- **Portfolio:** `index.html` linhas ~40-90 (3 `.project` articles)
- **Closing:** `index.html` linhas ~93-103 (`.closing-wrapper` com stars)
- **Contact:** `index.html` linhas ~106-118 (`.contact-wrapper` com icons + links)
- **CSS Base:** `styles.css` linhas 1-20 (reset, body, gradiente)
- **Responsive:** `styles.css` linhas ~200+ (media queries)

Se um usuário solicitar mudanças, verifique se a estrutura flex das seções está preservada e o responsivo funciona em mobile (768px/480px). A imagem `group1.png` é a "fonte da verdade" para o layout visual.
