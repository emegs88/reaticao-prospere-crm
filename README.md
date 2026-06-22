# CRM Reativação — Grupo Prospere by Âncora

Mini-CRM em **um único arquivo** (`index.html`) para reaquecer leads de consórcio:
lista por temperatura, link de WhatsApp, roteiros prontos por segmento, controle de
status e exportação. Funciona no celular e no PC, sem instalar nada.

Identidade: preto, branco e vermelho · **Grupo Prospere by Âncora**.

---

## ⚠️ ATENÇÃO — LGPD (leia antes de publicar)

A base `leads.json` contém **nomes e telefones reais de clientes**. Por isso:

- O `.gitignore` **já bloqueia** `leads.json` — ele **não vai** para o GitHub.
- **Nunca** commite dados reais em um repositório **público**.
- Quem clonar/abrir o site público verá apenas a base de exemplo (`leads.sample.json`)
  e poderá carregar a própria base pelo botão **Trocar base**.

### Quero a base real no site hospedado
Use um repositório **privado** e remova a linha `leads.json` do `.gitignore`.
Aí o `index.html` carrega `leads.json` automaticamente.

---

## Como funciona o carregamento da base

Ao abrir, o app procura a base nesta ordem:
1. Base salva no navegador (de um carregamento anterior).
2. Arquivo `leads.json` ao lado do `index.html` (quando hospedado).
3. Se não achar, mostra a tela **Carregar base** — aceita o **`.csv`** exportado da
   ferramenta de leads **ou** um **`.json`**. Os dados ficam só no navegador.

---

## Rodar localmente

Abrir o `index.html` direto (file://) **não** carrega o `leads.json` sozinho — o
navegador bloqueia. Duas opções:

- **Mais fácil:** abra o `index.html` e use **Trocar base** para enviar o `.csv`/`.json`
  (depois fica salvo no navegador).
- **Servidor local** (carrega o `leads.json` automático):
  ```bash
  python -m http.server 8000
  # abra http://localhost:8000
  ```

---

## Publicar no GitHub

```bash
cd prospere-crm
git init
git add .
git commit -m "CRM Reativação Prospere - versão inicial"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/prospere-crm.git
git push -u origin main
```
> Crie antes o repositório vazio em github.com (recomendado: **Private**).

## Publicar o site (escolha um)

- **GitHub Pages:** repositório → Settings → Pages → Deploy from a branch → `main` / `/root`.
- **Vercel:** vercel.com → Add New → Project → importe o repositório → Deploy.

---

## Estrutura

```
prospere-crm/
├── index.html          # o CRM (código, sem dados)
├── leads.json          # base real (NÃO versionada — LGPD)
├── leads.sample.json   # base de exemplo (fictícia)
├── .gitignore
├── vercel.json
└── README.md
```

## Compliance (consórcio)
Nunca usar "investimento/rendimento". Sempre "planejamento / compra programada /
patrimônio". Nunca prometer data de contemplação — ela ocorre por sorteio ou lance.
