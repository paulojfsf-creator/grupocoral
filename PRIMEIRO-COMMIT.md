# 📤 Como Subir para o GitHub

Guia passo-a-passo para fazer o primeiro upload.

---

## 🎯 Opção 1: Via GitHub Desktop (Mais Fácil)

### Passo 1: Instalar GitHub Desktop
- Download: https://desktop.github.com/
- Instala e faz login com a tua conta GitHub

### Passo 2: Criar Repositório
1. Abre GitHub Desktop
2. File → New Repository
3. Preenche:
   - **Name:** gestao-liturgica
   - **Description:** Aplicação web para gestão litúrgica do coro paroquial
   - **Local Path:** Escolhe onde guardar
   - **Initialize with README:** ❌ Não marcar (já temos)
   - **Git ignore:** None (já temos .gitignore)
   - **License:** MIT (já temos)
4. Clica **Create Repository**

### Passo 3: Adicionar Ficheiros
1. Copia todos os ficheiros deste projeto para a pasta criada
2. Volta ao GitHub Desktop
3. Verás todos os ficheiros listados
4. Escreve a mensagem do commit: `✨ Initial commit - v15.0`
5. Clica **Commit to main**

### Passo 4: Publicar
1. Clica **Publish repository**
2. Confirma:
   - ✅ Keep this code private (ou desmarcar se quiseres público)
3. Clica **Publish repository**

**✅ Pronto! Está no GitHub.**

### Passo 5: Ativar GitHub Pages
1. Vai a https://github.com/[teu-username]/gestao-liturgica
2. Settings → Pages
3. Source: Deploy from a branch
4. Branch: main / (root)
5. Save

**⏱️ Aguarda 2 minutos.**

Acede a: `https://[teu-username].github.io/gestao-liturgica/`

---

## 💻 Opção 2: Via Linha de Comandos

### Passo 1: Criar Repositório no GitHub
1. Vai a https://github.com/new
2. Preenche:
   - **Repository name:** gestao-liturgica
   - **Description:** Aplicação web para gestão litúrgica do coro paroquial
   - **Public** ou Private
   - ❌ Não adicionar README, .gitignore ou license (já temos)
3. Clica **Create repository**

### Passo 2: Inicializar Git Local
```bash
# Vai para a pasta do projeto
cd /caminho/para/grupocoral-github

# Inicializa git
git init

# Adiciona todos os ficheiros
git add .

# Primeiro commit
git commit -m "✨ Initial commit - v15.0"

# Adiciona remote (substitui [username] pelo teu)
git remote add origin https://github.com/[username]/gestao-liturgica.git

# Define branch principal
git branch -M main

# Push para o GitHub
git push -u origin main
```

### Passo 3: Ativar GitHub Pages
```bash
# Ou via interface web (mais fácil):
# Settings → Pages → Source: main / (root) → Save
```

**✅ Pronto! Está online.**

---

## 🌐 Opção 3: Upload via Web (Sem Git)

### Passo 1: Criar Repositório
1. Vai a https://github.com/new
2. Cria repositório vazio (gestao-liturgica)

### Passo 2: Upload de Ficheiros
1. Clica em **uploading an existing file**
2. Arrasta TODOS os ficheiros do projeto
3. Escreve commit message: `✨ Initial commit - v15.0`
4. Clica **Commit changes**

### Passo 3: Ativar Pages
1. Settings → Pages
2. Source: main / (root)
3. Save

**✅ Online em 2 minutos.**

---

## 📋 Checklist de Ficheiros

Antes de fazer upload, confirma que tens:

```
grupocoral-github/
├── index.html                  ✅
├── scripts/
│   └── scripts.js              ✅
├── .github/
│   └── workflows/
│       └── deploy.yml          ✅
├── README.md                   ✅
├── CHANGELOG.md                ✅
├── CONTRIBUTING.md             ✅
├── INSTALL.md                  ✅
├── LICENSE                     ✅
├── .gitignore                  ✅
└── PRIMEIRO-COMMIT.md          ✅ (este ficheiro)
```

---

## 🔐 Configurações Recomendadas

Depois do upload, configura:

### 1. Descrição do Repositório
- Settings → (topo da página)
- **About** → Edit
- Description: `Aplicação web para gestão litúrgica do coro paroquial`
- Website: `https://[username].github.io/gestao-liturgica/`
- Topics: `liturgia`, `coral`, `web-app`, `javascript`, `gestão`

### 2. Branches
- Settings → Branches
- Default branch: `main` ✅
- Branch protection rules (opcional):
  - Require pull request reviews
  - Require status checks

### 3. Issues e Projects
- Settings → Features
- ✅ Issues
- ✅ Projects (se quiseres roadmap)
- ✅ Discussions (para comunidade)

---

## 🔄 Atualizações Futuras

### Via GitHub Desktop
1. Faz mudanças nos ficheiros
2. Abre GitHub Desktop
3. Escreve descrição do commit
4. Commit to main
5. Push origin

### Via Linha de Comandos
```bash
# Depois de fazer mudanças
git add .
git commit -m "🔧 fix: Corrige bug X"
git push
```

---

## 🏷️ Criar Releases

Para versões importantes:

### Via Web
1. Vai ao repositório
2. Releases → Create a new release
3. Tag: `v15.0`
4. Title: `Versão 15.0 - Sistema Funcional`
5. Descrição: Copia do CHANGELOG.md
6. Publish release

### Via Linha de Comandos
```bash
git tag -a v15.0 -m "Versão 15.0 - Sistema Funcional"
git push origin v15.0
```

---

## 🌟 Tornar Repositório Público

Se criaste privado e quiseres tornar público:

1. Settings
2. Scroll até ao fundo
3. Danger Zone → Change visibility
4. Make public
5. Confirma escrevendo o nome do repositório

---

## 📊 Badge Status

Adiciona badges ao README:

```markdown
![Build Status](https://github.com/[username]/gestao-liturgica/workflows/Deploy%20to%20GitHub%20Pages/badge.svg)
![Version](https://img.shields.io/badge/version-15.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
```

---

## ✅ Verificação Final

Depois do upload, testa:

- [ ] Repositório está criado
- [ ] Todos os ficheiros aparecem
- [ ] GitHub Pages está ativo
- [ ] Site abre sem erros
- [ ] Tabs funcionam
- [ ] README está visível
- [ ] License está presente

---

## 🎉 Parabéns!

O teu projeto está agora no GitHub! 🚀

### Próximos Passos:

1. 🔗 Partilha o link: `https://github.com/[username]/gestao-liturgica`
2. ⭐ Pede a amigos para dar star
3. 📢 Partilha com a paróquia
4. 📝 Continua a desenvolver
5. 🤝 Aceita contribuições

---

## 📞 Problemas?

- **Erro ao push:** Verifica username e password
- **Pages não ativa:** Aguarda 2-3 minutos
- **Site não abre:** Força refresh (Ctrl+F5)
- **Ficheiros faltam:** Verifica .gitignore

---

## 🔗 Links Úteis

- **GitHub Desktop:** https://desktop.github.com/
- **Git Download:** https://git-scm.com/downloads
- **GitHub Docs:** https://docs.github.com/
- **GitHub Pages:** https://pages.github.com/

---

**O teu projeto está agora disponível para o mundo! 🌍**
