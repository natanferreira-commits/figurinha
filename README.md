# Pacote Premiado

Landing page promocional do **Pacote Premiado** — campanha de captação de CPA do Dupla Aposta com mecânica gamificada de figurinhas (formato Panini).

## 🎯 Sobre

Edição **Pré-Copa do Mundo 2026**. O usuário cadastra dados, abre um pacote virtual, descobre seus prêmios (R$ 50 de banca + Acesso VIP por 30 dias) e resgata cadastrando em uma casa parceira.

## 🏗️ Stack

- HTML, CSS, JS puro (sem build)
- Single-file (auto-contido)
- Mobile-first (max-width 480px)
- Animações: CSS keyframes + Framer-style transições
- SVG inline pra ilustrações

## 🚀 Deploy

Pronto pra deployar na Vercel:

```bash
vercel --prod
```

Ou conecta o repo direto no dashboard da Vercel — detecta automaticamente como static site.

## 📁 Estrutura

```
.
├── index.html        # Landing completa (single-file)
├── bg-copa.jpg       # Background da Copa (adicionar)
└── README.md
```

## 🎨 Customizações

Toda lógica do fluxo está no `<script>` no fim do `index.html`:

- `goToStep(stepId)` — navegação entre telas
- `submitForm(e)` — captura lead
- `spawnConfetti()` — anima confete
- `renderSticker(idx)` — renderiza figurinha
- `selectCasa(el, name)` — seleciona casa parceira

## 🔌 Integrações pendentes (TODOs no código)

1. `submitForm()` → POST pro backend (`/api/leads`)
2. `selectCasa()` → redirecionar pro link de afiliação real da casa
3. Validação de print de cadastro pra liberar prêmios

## 🎁 Fluxo

```
Hero → Intro (pacote pra clicar) → Form →
Opening (animação) → Reveal (3 figurinhas) → Claim (resgate)
```

## ⚠️ Compliance

A landing está alinhada com a Lei 14.790/2023 e as diretrizes da SPA:
- Idade +18 visível
- Aviso de jogo responsável
- Telefone de apoio (0800 026 1818)
- Sem promessa de "ganho garantido"
- Foco em "presente" / "boas-vindas"

---

© 2026 Dupla Aposta · CNPJ 36.213.131/0001-02
