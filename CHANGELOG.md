# Changelog

Todas as mudanças notáveis neste projeto serão documentadas neste ficheiro.

O formato é baseado em [Keep a Changelog](https://keepachangelog.com/pt/1.0.0/),
e este projeto segue [Semantic Versioning](https://semver.org/lang/pt-BR/).

---

## [15.0] - 2024-12-07

### 🔧 Corrigido
- **Sistema de tabs completamente funcional** - Corrigida incompatibilidade entre botões (data-tab) e sections (id)
- **JavaScript agora corresponde 100% ao HTML** - Todos os IDs e classes alinhados
- **Calendário interativo** - Adicionada funcionalidade de navegação mensal
- **IDs de elementos** - Corrigidos: `upcomingEvents`, `addCustomSongBtn`, etc.

### ✨ Adicionado
- **Calendário interativo completo** com navegação (anterior/seguinte/hoje)
- **Marcação visual de dias** com programa guardado
- **Clique em dias** do calendário para carregar programas
- **Cores por tempo litúrgico** no calendário
- **Função renderCalendar()** para geração dinâmica do calendário

### ♻️ Refatorado
- Sistema de tabs usa `getElementById()` para sections
- Código limpo e bem comentado (~1200 linhas)
- Estrutura modular por funcionalidade

### 🗑️ Removido
- Leituras do dia (simplificação v15.0)
- Código obsoleto de API Evangelizo.org (~700 linhas)
- Sistema de cache de leituras

---

## [14.7] - 2024-11

### 🔧 Corrigido
- Scope da função `updateDashboard`
- Código obsoleto de margens removido

---

## [14.6] - 2024-11

### 🔧 Corrigido
- Erro `applyCustomMargins` não definido
- Console limpo sem erros

---

## [14.5] - 2024-11

### ✨ Adicionado
- **Leituras integradas no programa** ao selecionar data
- Cache inteligente de leituras por data (24h)
- Limpeza automática de cache antigo (>30 dias)

---

## [14.3] - 2024-11

### ✨ Adicionado
- **Cânticos personalizados** com upload de partituras
- **Câmara integrada** para captura de partituras
- Suporte para PDF e imagens
- Visualização in-app de partituras
- Validação de ficheiros (5MB máximo)

---

## [14.2] - 2024-11

### 🎨 Melhorado
- **Cantos completamente retos** (border-radius: 0)
- Texto sempre visível em smartphones
- Font-size optimizado para mobile

---

## [14.1] - 2024-11

### 📱 Melhorado
- Optimização completa para smartphones
- Tabs retangulares para melhor usabilidade mobile
- 3 breakpoints responsivos (mobile/tablet/desktop)

---

## [14.0] - 2024-11

### 🗑️ Removido
- **Tab "Pré-visualização"** - Simplificação da interface
- Controles de margem personalizadas
- Modo editável do folheto

### ♻️ Alterado
- Workflow simplificado: Programa → Folhetos (direto)
- Geração automática de folhetos em segundo plano
- Interface reduzida para 8 tabs

### ✨ Vantagens
- Menos cliques para guardar folhetos
- Interface mais limpa
- Workflow mais intuitivo

---

## [13.0] - 2024-10

### ✨ Adicionado
- Sistema de histórico de uso de cânticos
- Modal com detalhes de utilização por cântico
- Estatísticas de frequência
- Registo automático ao guardar programa

---

## [12.0] - 2024-10

### ✨ Adicionado
- Sistema de folhetos guardados
- Biblioteca de até 30 folhetos
- Visualização e impressão
- Gestão completa (guardar/ver/eliminar)

---

## [11.0] - 2024-09

### ✨ Adicionado
- Calendário litúrgico na página inicial
- Datas especiais pré-programadas
- Próximas celebrações
- Cores por tempo litúrgico

---

## [10.0] - 2024-09

### ✨ Adicionado
- Sistema de tabs (8 secções)
- Tema escuro/claro
- Histórico de programas (até 50)
- Upload de imagem do domingo

---

## [9.0] - 2024-08

### ✨ Adicionado
- Integração com Google Sheets
- Catálogo de cânticos dinâmico
- Preenchimento automático de selects

---

## [8.0] - 2024-08

### ✨ Adicionado
- Formulário completo de programa litúrgico
- 13 momentos litúrgicos
- Preenchimento automático por data

---

## [7.0] - 2024-07

### ✨ Adicionado
- Links para partituras do Google Drive
- Vídeos do YouTube embebidos
- Links para ensaios (WhatsApp/Email)

---

## [1.0-6.0] - 2024-01 a 2024-06

### ✨ Adicionado
- Estrutura inicial HTML/CSS
- Design responsivo
- Formulários básicos
- Primeira versão funcional

---

## Tipos de Mudanças

- `✨ Adicionado` - Novas funcionalidades
- `♻️ Alterado` - Mudanças em funcionalidades existentes
- `🗑️ Removido` - Funcionalidades removidas
- `🔧 Corrigido` - Correção de bugs
- `🔒 Segurança` - Correções de vulnerabilidades
- `📱 Melhorado` - Melhorias de UI/UX
- `⚡ Performance` - Optimizações de velocidade
- `📝 Documentação` - Mudanças na documentação

---

## Links

- [Repositório GitHub](https://github.com/[username]/gestao-liturgica)
- [Issues](https://github.com/[username]/gestao-liturgica/issues)
- [Releases](https://github.com/[username]/gestao-liturgica/releases)
