# 🚀 Instalação Rápida

Guia rápido para começar a usar a aplicação em 5 minutos.

---

## 📦 Método 1: GitHub Pages (Recomendado)

### Passo 1: Fork do Repositório
1. Clica em **"Fork"** no topo da página
2. Aguarda alguns segundos

### Passo 2: Ativar GitHub Pages
1. Vai a **Settings** (⚙️) do teu repositório
2. Clica em **Pages** no menu lateral
3. Em **Source**, seleciona:
   - Branch: `main`
   - Folder: `/ (root)`
4. Clica em **Save**

### Passo 3: Aceder à Aplicação
- URL: `https://[teu-username].github.io/gestao-liturgica/`
- Demora 1-2 minutos a ficar disponível

**✅ Pronto! A aplicação está online.**

---

## 💻 Método 2: Local (Desenvolvimento)

### Requisitos
- Git instalado
- Browser moderno

### Instalação

```bash
# 1. Clone o repositório
git clone https://github.com/[teu-username]/gestao-liturgica.git

# 2. Entra na pasta
cd gestao-liturgica

# 3. Abre no browser
# Windows
start index.html

# Mac
open index.html

# Linux
xdg-open index.html
```

**✅ A aplicação abre no browser.**

---

## 🌐 Método 3: Download Direto

### Passo 1: Download
1. Clica no botão verde **"Code"**
2. Seleciona **"Download ZIP"**
3. Extrai o ZIP

### Passo 2: Abrir
- Duplo clique em `index.html`
- Ou arrasta para o browser

**✅ Pronto para usar.**

---

## ⚙️ Configuração Inicial

### 1. Google Sheets (Catálogo)

Se quiseres usar o teu próprio catálogo:

1. Cria uma Google Sheet com colunas: `Título`, `Tema`
2. Publica como CSV:
   - File → Share → Publish to web
   - Formato: CSV
   - Copia o URL

3. Edita `scripts/scripts.js` (linha ~395):
```javascript
const url = "https://docs.google.com/spreadsheets/d/e/[TEU-ID]/pub?output=csv";
```

### 2. Google Drive (Partituras)

Para adicionar links das tuas partituras:

1. Cria pastas no Google Drive
2. Torna públicas (Anyone with the link can view)
3. Copia os IDs das pastas

4. Edita `index.html` (linha ~2118):
```html
<a href="https://drive.google.com/drive/folders/[TEU-ID]" target="_blank">
  📁 Partituras Antigas
</a>
```

### 3. Calendário Litúrgico

Para adicionar mais datas especiais:

1. Edita `scripts/scripts.js` (linha ~35)
2. Adiciona datas no formato:
```javascript
const LITURGICAL_CALENDAR = {
  '2025-01-01': {
    title: 'Santa Maria, Mãe de Deus',
    color: 'Branco',
    season: 'natal'
  },
  // Adiciona mais...
};
```

---

## 🧪 Verificação

Depois de instalar, verifica:

### Checklist Rápida

- [ ] Abre a página sem erros
- [ ] As 8 tabs mudam
- [ ] Botão tema (☀️/🌙) funciona
- [ ] Calendário mostra o mês atual
- [ ] Consegues selecionar uma data
- [ ] Catálogo carrega (pode demorar 2-3 segundos)

### Se algo não funcionar:

1. **Abre o Console** (F12)
2. **Vê erros** a vermelho
3. **Força refresh** (Ctrl+F5 ou Cmd+Shift+R)
4. **Verifica** se o browser permite localStorage

---

## 📱 Testar em Mobile

### Via GitHub Pages
- Acede ao URL no telemóvel: `https://[teu-username].github.io/gestao-liturgica/`

### Via Local (Wi-Fi)
1. No computador, descobre o IP:
```bash
# Windows
ipconfig

# Mac/Linux
ifconfig
```

2. No telemóvel, acede a: `http://[IP-DO-PC]:8000`

*Nota: Requer servidor local (ex: `python -m http.server`)*

---

## 🐛 Problemas Comuns

### Tabs não mudam
**Solução:** Força refresh (Ctrl+F5)

### Catálogo não carrega
**Causa:** URL do Google Sheets inválido  
**Solução:** Verifica o URL no `scripts.js`

### Imagens não aparecem
**Causa:** Ficheiros muito grandes  
**Solução:** 
- Imagem domingo: máx 2MB
- Partituras: máx 5MB

### Dados desaparecem
**Causa:** Browser em modo incógnito  
**Solução:** Usa janela normal

### GitHub Pages não funciona
**Causa:** Demora 1-2 minutos  
**Solução:** Aguarda e força refresh

---

## 📊 Dados de Teste

Para testar rapidamente, usa estes dados:

### Programa de Teste
```
Data: 2024-12-08
Título: II Domingo do Advento
Cor: Roxo
Entrada: Vinde, Senhor Jesus
Glória: (omitir)
Salmo: Sl 84
Ofertório: Ofício Divino
Santo: Santo (Advento)
Comunhão: Vem, Senhor Jesus
Final: Vinde, ó Deus salvador
```

---

## 🔄 Atualizar

### Atualizar do GitHub
```bash
cd gestao-liturgica
git pull origin main
```

### Atualizar GitHub Pages
- Faz push das mudanças
- GitHub Pages atualiza automaticamente em 1-2 minutos

---

## 📞 Ajuda

**Não funciona?**

1. Vê o [README.md](README.md) completo
2. Procura nas [Issues](https://github.com/[username]/gestao-liturgica/issues)
3. Abre uma [nova issue](https://github.com/[username]/gestao-liturgica/issues/new)

---

## ⏱️ Tempos Estimados

- **GitHub Pages:** 5 minutos (setup) + 2 minutos (deploy)
- **Local:** 2 minutos
- **Download:** 1 minuto

---

## ✅ Próximos Passos

Depois de instalar:

1. 📖 Lê o [README.md](README.md) completo
2. 🎨 Personaliza as cores no CSS
3. 📚 Configura o teu catálogo
4. 🎵 Cria o teu primeiro programa!

---

**Instalação simples, uso poderoso! 🎵**
