# Copa do Brasil de Pickleball 2026 — site oficial

Página única do evento. Tudo (HTML, CSS, JavaScript e logos) está dentro do `index.html`.
Não precisa instalar nada, não tem build, não tem dependência externa além das fontes do Google Fonts.

- **Evento:** 11, 12 e 13 de dezembro de 2026
- **Local:** Pickleball Barra, no Clube de Aeronáutica — Barra da Tijuca, Rio de Janeiro
- **Realização:** APRJ · **Chancela:** CBP · **Mídia oficial:** PKB Brasil

---

## 1. Publicar no GitHub Pages (sem terminal, tudo pelo navegador)

**Passo 1 — Criar a conta**
Entre em github.com e crie uma conta. Use um e-mail institucional da APRJ, não um e-mail pessoal de alguém do comitê. É grátis.

**Passo 2 — Criar o repositório**
Clique em **New repository** (botão verde).
- Repository name: `copa-do-brasil-2026`
- Marque **Public** (o GitHub Pages grátis só funciona em repositório público)
- Marque **Add a README file**
- Clique em **Create repository**

**Passo 3 — Subir o arquivo**
Dentro do repositório, clique em **Add file → Upload files**.
Arraste o `index.html` para a área indicada.
Escreva em Commit changes uma descrição curta (ex.: "primeira versão do site") e clique em **Commit changes**.

**Passo 4 — Ligar o GitHub Pages**
Vá em **Settings** (engrenagem no topo do repositório) → menu lateral **Pages**.
- Em *Source*, escolha **Deploy from a branch**
- Em *Branch*, escolha **main** e a pasta **/ (root)**
- Clique em **Save**

**Passo 5 — Esperar e conferir**
Em 1 a 3 minutos a mesma tela mostra o endereço:
`https://SEU-USUARIO.github.io/copa-do-brasil-2026/`
Abra no celular e no computador antes de divulgar.

---

## 2. Usar um domínio próprio (opcional, recomendado)

**Passo 1 — Registrar**
Em registro.br, registre por volta de R$ 40/ano. Sugestão: `copadobrasilpickleball.com.br`.
Registre no **CNPJ da APRJ**, nunca no CPF de uma pessoa física. O domínio é ativo de legado para as próximas edições.

**Passo 2 — Apontar para o GitHub**
No painel do registro.br, na área de DNS, crie:

| Tipo | Nome | Valor |
|---|---|---|
| CNAME | www | SEU-USUARIO.github.io |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**Passo 3 — Informar o domínio no GitHub**
Em Settings → Pages → *Custom domain*, escreva o domínio e clique em **Save**.
Espere a verificação e marque **Enforce HTTPS**.
A propagação pode levar algumas horas — é normal.

---

## 3. Editar a página depois

Abra o repositório, clique em `index.html` e no ícone de lápis (**Edit this file**).
Altere o texto, clique em **Commit changes**. A página no ar atualiza em cerca de 1 minuto.

Dica: antes de mexer, baixe uma cópia do arquivo. Se algo quebrar, é só subir a cópia de novo.

### Preencher antes de divulgar

| O que | Onde procurar no arquivo | Situação |
|---|---|---|
| Link do torneio no Sistema Pickleball Integrado | `id="link-inscricao"` | falta |
| Valores de inscrição | seção Inscrições, selo "a confirmar" | valores de referência de 2025 |
| Prazos de inscrição e chaveamento | seção Inscrições | estimados |
| E-mails comercial@ e imprensa@ | seção Patrocínio e rodapé | placeholder |
| WhatsApp comercial | seção Patrocínio | placeholder `5521000000000` |
| Instagram APRJ, CBP e Pickleball Barra | rodapé | placeholder |
| Link do regulamento oficial | rodapé | falta |

### Trocar o logo do naming rights

No topo do arquivo, na seção HERO, existe um comentário `ESPAÇO RESERVADO AO NAMING RIGHTS`.
Quando a cota fechar, substitua o comentário pela linha indicada ali, com o logo do patrocinador em versão monocromática branca.

### Colocar logo de patrocinador

Na seção Patrocínio, troque cada `<div class="slot">Espaço disponível</div>` por:

```html
<div class="slot"><img src="logo-da-marca.png" alt="Nome da marca" style="max-height:52px"></div>
```

Suba o arquivo de imagem no mesmo repositório (Add file → Upload files) antes de referenciá-lo.

---

## 4. Rotina de atualização

Página desatualizada prejudica mais do que ajuda — patrocinador em negociação entra no site para decidir.
Defina **um responsável** e atualize em três momentos:

1. Abertura das inscrições (link e valores confirmados)
2. Cada patrocinador que fecha (logo na grade)
3. Publicação do chaveamento e da grade horária

---

## Padrões que não devem ser alterados

- Azul #061B46, dourado #FFC72C, verde CBP #009739 apenas no selo institucional
- Tipografia Archivo Black (títulos) e Archivo (texto)
- A sede é sempre **"Pickleball Barra, no Clube de Aeronáutica"** — o clube nunca é citado sozinho
- Host, sede e mídia oficial aparecem em tamanho institucional reduzido, nunca em tamanho de patrocinador (Cláusula 7.8 do Contrato de Cessão e nível 6 da hierarquia de marcas)
