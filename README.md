# ✦ Grimório D&D 2024 — PWA

App mobile com todas as 327 magias do Player's Handbook 2024.
Funciona offline após a primeira visita.

---

## Como instalar no celular (via Netlify)

### Passo 1 — Criar conta gratuita
1. Acesse **https://netlify.com**
2. Clique em **Sign up** → entre com Google ou GitHub (gratuito)

### Passo 2 — Fazer o deploy
1. No painel do Netlify, clique em **"Add new site"** → **"Deploy manually"**
2. Arraste a **pasta inteira** `dnd-spells-pwa` para a área indicada
3. Aguarde alguns segundos — o Netlify gera uma URL tipo `https://grimorio-abc123.netlify.app`

### Passo 3 — Instalar no celular

**Android (Chrome):**
1. Abra a URL no Chrome
2. Toque no menu ⋮ → **"Adicionar à tela inicial"**
3. Confirme — o app aparece na tela inicial como qualquer outro app

**iPhone (Safari):**
1. Abra a URL no Safari (obrigatório — não funciona no Chrome do iOS)
2. Toque no botão de compartilhar (retângulo com seta pra cima)
3. Role e toque em **"Adicionar à Tela de Início"**
4. Confirme

---

## Arquivos do projeto

```
dnd-spells-pwa/
├── index.html      → App completo (interface + lógica)
├── spells.json     → 327 magias do PHB 2024 (PT-BR)
├── manifest.json   → Configuração do PWA
├── sw.js           → Service worker (cache offline)
├── icon-192.svg    → Ícone do app (tela inicial)
└── icon-512.svg    → Ícone do app (splash screen)
```

---

## Funcionalidades

- 🔍 Busca por nome ou escola
- 🎨 Filtro por escola de magia (chips coloridos)
- 📋 Toque numa magia para ver todos os detalhes
- 📴 Funciona 100% offline após a primeira visita
- 📱 Instalável na tela inicial (Android e iPhone)

---

## Alternativa sem internet (arquivo local)

Se quiser usar sem deploy, você pode abrir `index.html` direto no celular,
mas precisará de um servidor local. A forma mais simples:

```bash
# Com Python instalado no computador:
cd dnd-spells-pwa
python3 -m http.server 8000

# Acesse no celular (mesma rede Wi-Fi):
# http://SEU-IP-LOCAL:8000
```
