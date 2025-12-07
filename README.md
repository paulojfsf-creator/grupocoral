# 🎵 Gestão Litúrgica - Coro Paroquial São João Batista

Aplicação web completa para gestão de programas litúrgicos, cânticos e folhetos para o Coro Paroquial de São João Batista de Rio Caldo.

![Versão](https://img.shields.io/badge/versão-15.0-blue)
![Status](https://img.shields.io/badge/status-ativo-success)
![Licença](https://img.shields.io/badge/licença-MIT-green)

---

## 📋 Funcionalidades

### 🎼 Gestão de Programas
- ✅ Criação e edição de programas litúrgicos completos
- ✅ 13 momentos litúrgicos (Entrada, Glória, Salmo, Comunhão, etc.)
- ✅ Preenchimento automático de títulos litúrgicos por data
- ✅ Upload de imagem do domingo
- ✅ Histórico de programas guardados (até 50)

### 📅 Calendário Litúrgico
- ✅ Calendário interativo mensal
- ✅ Marcação automática de datas litúrgicas especiais
- ✅ Visualização de programas guardados no calendário
- ✅ Navegação entre meses (anterior/seguinte/hoje)
- ✅ Cores por tempo litúrgico (Advento, Natal, Páscoa, Tempo Comum)

### 📄 Folhetos da Assembleia
- ✅ Geração automática de folhetos para impressão
- ✅ Biblioteca de folhetos guardados (até 30)
- ✅ Visualização e impressão direta
- ✅ Formatação profissional A4

### 📚 Catálogo de Cânticos
- ✅ Integração com Google Sheets (catálogo CSV)
- ✅ Histórico de utilização por cântico
- ✅ Estatísticas de uso
- ✅ Pesquisa e filtragem

### 🎶 Cânticos Personalizados
- ✅ Adicionar cânticos não catalogados
- ✅ Upload de partituras (PDF ou imagem)
- ✅ Captura de fotos via câmara
- ✅ Visualização in-app de partituras
- ✅ Gestão completa (adicionar/ver/eliminar)

### 📊 Histórico e Estatísticas
- ✅ Registo automático de uso de cânticos
- ✅ Histórico detalhado por data e momento litúrgico
- ✅ Carregar programas anteriores
- ✅ Análise de frequência de uso

### 🎥 Recursos Multimédia
- ✅ Partituras do Google Drive (2 pastas)
- ✅ Vídeos do YouTube embebidos
- ✅ Links para ensaios (WhatsApp e Email)

### 🎨 Interface
- ✅ Tema escuro/claro
- ✅ Totalmente responsivo (mobile-first)
- ✅ 8 tabs organizadas
- ✅ Design moderno e intuitivo
- ✅ Animações suaves

---

## 🚀 Instalação

### Opção 1: GitHub Pages (Recomendado)

1. **Fork** este repositório
2. Vai a **Settings** → **Pages**
3. Seleciona `main` branch como source
4. A aplicação ficará disponível em: `https://[teu-username].github.io/[repo-name]`

### Opção 2: Local

1. **Clone** o repositório:
```bash
git clone https://github.com/[teu-username]/gestao-liturgica.git
cd gestao-liturgica
```

2. **Abre** o ficheiro `index.html` num browser moderno

**Requisitos:**
- Navegador moderno (Chrome, Firefox, Safari, Edge)
- JavaScript ativado
- LocalStorage disponível

---

## 📁 Estrutura do Projeto

```
gestao-liturgica/
├── index.html              # Página principal
├── scripts/
│   └── scripts.js          # JavaScript completo (1200+ linhas)
├── README.md               # Este ficheiro
└── LICENSE                 # Licença MIT
```

**Nota:** Não há ficheiros CSS externos - todo o estilo está inline no `index.html` para facilitar deployment.

---

## 🔧 Configuração

### Catálogo de Cânticos (Google Sheets)

O catálogo carrega de um Google Sheet público. Para usar o teu próprio:

1. Cria uma Google Sheet com as colunas: `Título`, `Tema`
2. Publica como CSV: `File` → `Share` → `Publish to web` → `CSV`
3. Substitui o URL no `scripts.js` (linha ~395):

```javascript
const url = "https://docs.google.com/spreadsheets/d/e/[TEU-ID]/pub?output=csv";
```

### Calendário Litúrgico

Datas especiais estão pré-programadas no objeto `LITURGICAL_CALENDAR` (linha ~35 do `scripts.js`).

Para adicionar mais datas:

```javascript
const LITURGICAL_CALENDAR = {
  '2025-12-25': {title: 'Natal do Senhor', color: 'Branco', season: 'natal'},
  // Adiciona mais aqui...
};
```

### Partituras do Google Drive

Links estão hardcoded no HTML (linha ~2118). Substitui pelos teus:

```html
<a href="https://drive.google.com/drive/folders/[TEU-FOLDER-ID]" target="_blank">
```

---

## 💾 Armazenamento de Dados

Todos os dados são guardados no **localStorage** do browser:

| Chave | Conteúdo | Limite |
|-------|----------|--------|
| `coroHistory` | Programas guardados | 50 |
| `coroLeaflets` | Folhetos guardados | 30 |
| `coroCustomSongs` | Cânticos personalizados | Ilimitado |
| `coroSongUsage` | Histórico de uso | 500 |
| `coroSundayImage` | Imagem do domingo | 2MB |
| `coroActiveTab` | Última tab aberta | - |
| `coroTheme` | Tema (dark/light) | - |

**⚠️ Importante:**
- Dados ficam no browser local
- Limpar dados do browser = perder tudo
- Para sincronização entre dispositivos, considera adicionar backend

---

## 🎨 Personalização

### Cores Litúrgicas

Edita as variáveis CSS no `index.html` (linha ~13):

```css
:root {
  --primary: #004b80;        /* Cor principal */
  --header-bg: var(--primary);
  /* ... */
}
```

### Tempos Litúrgicos

Cores automáticas por tempo (linha ~47):

```css
body.liturgic-advento,
body.liturgic-quaresma {
  --header-bg: #4b2c6f;  /* Roxo */
}
```

---

## 🔌 API Externa

A aplicação não usa backend, mas integra com:

- **Google Sheets** - Catálogo de cânticos (CSV público)
- **Google Drive** - Partituras (links diretos)
- **YouTube** - Vídeos embebidos (iframes)

---

## 📱 Responsividade

A aplicação é **mobile-first** com 3 breakpoints:

- **Mobile:** < 768px
- **Tablet:** 768px - 1024px  
- **Desktop:** > 1024px

Testado em:
- ✅ Chrome (Desktop + Mobile)
- ✅ Firefox
- ✅ Safari (iOS)
- ✅ Edge

---

## 🐛 Resolução de Problemas

### Tabs não mudam
```javascript
// Abre o Console (F12) e verifica:
console.log(document.querySelectorAll('.tabs button[data-tab]'));
// Deve retornar 8 botões
```

### Catálogo não carrega
- Verifica conexão à internet
- Confirma que o URL do Google Sheets está correto
- Vê erros no Console (F12)

### Dados desaparecem
- Verifica se não estás em modo **Incógnito**
- Confirma que o browser permite localStorage
- Faz backup exportando dados manualmente

### Imagens não carregam
- Máximo 2MB para imagem do domingo
- Máximo 5MB para partituras
- Verifica formato (JPG, PNG, WebP, PDF)

---

## 🤝 Contribuir

Contribuições são bem-vindas! Para contribuir:

1. **Fork** o projeto
2. Cria um **branch** para a tua feature (`git checkout -b feature/MinhaFeature`)
3. **Commit** as mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. **Push** para o branch (`git push origin feature/MinhaFeature`)
5. Abre um **Pull Request**

---

## 📜 Licença

Este projeto está sob a licença **MIT**. Vê o ficheiro [LICENSE](LICENSE) para mais detalhes.

---

## 👨‍💻 Autor

**Coro Paroquial São João Batista**  
Rio Caldo, Terras de Bouro, Braga, Portugal

---

## 🙏 Agradecimentos

- Paróquia de São João Batista de Rio Caldo
- Todos os membros do coro
- Comunidade de desenvolvimento web

---

## 📞 Suporte

Para questões ou sugestões:
- Abre uma [Issue](https://github.com/[teu-username]/gestao-liturgica/issues)
- Email: [teu-email@exemplo.com]

---

## 🔮 Roadmap

Funcionalidades planeadas:

- [ ] Export para PDF dos folhetos
- [ ] Sincronização cloud (Firebase)
- [ ] App mobile nativa
- [ ] Sistema de utilizadores
- [ ] Partilha de programas entre coros
- [ ] Integração com calendário Google
- [ ] Notificações de ensaios
- [ ] Estatísticas avançadas

---

## 📸 Screenshots

### Página Inicial
![Dashboard](https://via.placeholder.com/800x400?text=Calendário+Litúrgico)

### Programa
![Programa](https://via.placeholder.com/800x400?text=Gestão+de+Programas)

### Catálogo
![Catálogo](https://via.placeholder.com/800x400?text=Catálogo+de+Cânticos)

---

## 🌟 Changelog

### v15.0 (Dezembro 2024)
- 🔧 Corrigido sistema de tabs
- ➕ Adicionado calendário interativo
- ✨ Melhorado preview de imagens
- 🗑️ Removidas leituras do dia (simplificação)
- 🎨 Interface optimizada para mobile

### v14.0 (Novembro 2024)
- ➖ Removida tab "Pré-visualização"
- ✨ Workflow simplificado Programa → Folhetos
- 📱 Optimizações mobile

### v13.0
- ➕ Cânticos personalizados
- 📷 Captura de partituras por câmara
- 📊 Histórico de uso de cânticos

---

**Feito com ❤️ para a comunidade paroquial**
