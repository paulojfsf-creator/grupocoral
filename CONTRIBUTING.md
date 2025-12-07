# Contribuir para Gestão Litúrgica

Obrigado por considerares contribuir para este projeto! 🎵

Este documento fornece diretrizes para contribuições.

---

## 📋 Código de Conduta

### Nossos Valores

- **Respeito** - Trata todos com dignidade
- **Colaboração** - Trabalha em equipa
- **Qualidade** - Mantém padrões elevados
- **Inclusão** - Acolhe todas as pessoas

---

## 🐛 Reportar Bugs

Antes de reportar um bug:

1. **Verifica** se já foi reportado nas [Issues](https://github.com/[username]/gestao-liturgica/issues)
2. **Confirma** que é realmente um bug (não uma funcionalidade esperada)
3. **Testa** na última versão

### Como Reportar

Cria uma [nova issue](https://github.com/[username]/gestao-liturgica/issues/new) com:

**Título:** Descrição breve do problema

**Descrição:**
```
### Descrição do Bug
[Explica o que acontece]

### Passos para Reproduzir
1. Vai para '...'
2. Clica em '...'
3. Vê o erro

### Comportamento Esperado
[O que deveria acontecer]

### Comportamento Atual
[O que acontece realmente]

### Screenshots
[Se aplicável]

### Ambiente
- Browser: [Chrome 120]
- OS: [Windows 11]
- Versão: [15.0]

### Console Errors
[Copia erros do console se houver]
```

---

## ✨ Sugerir Funcionalidades

Para sugerir novas funcionalidades:

1. **Verifica** se já foi sugerida
2. **Explica** o caso de uso
3. **Descreve** como deve funcionar

### Template

```
### Funcionalidade Proposta
[Descrição clara]

### Motivação
[Porque é útil?]

### Solução Proposta
[Como deve funcionar?]

### Alternativas Consideradas
[Outras abordagens?]

### Screenshots/Mockups
[Se tiveres]
```

---

## 🔧 Contribuir com Código

### Setup Inicial

1. **Fork** o repositório
2. **Clone** o teu fork:
```bash
git clone https://github.com/[teu-username]/gestao-liturgica.git
cd gestao-liturgica
```

3. **Cria um branch** para a tua feature:
```bash
git checkout -b feature/minha-feature
```

### Desenvolvimento

1. **Código**
   - Segue as convenções existentes
   - Comenta código complexo
   - Mantém funcionalidades existentes

2. **Testa**
   - Testa em múltiplos browsers
   - Verifica responsividade mobile
   - Confirma que não quebrou nada

3. **Commit**
```bash
git add .
git commit -m "✨ Adiciona funcionalidade X"
```

### Convenções de Commit

Use emojis e mensagens claras:

- `✨ feat:` Nova funcionalidade
- `🔧 fix:` Correção de bug
- `📝 docs:` Documentação
- `🎨 style:` Formatação, CSS
- `♻️ refactor:` Refatoração de código
- `⚡ perf:` Optimização
- `🧪 test:` Testes
- `🔨 chore:` Tarefas de manutenção

Exemplos:
```bash
git commit -m "✨ feat: Adiciona export PDF de folhetos"
git commit -m "🔧 fix: Corrige erro ao carregar catálogo"
git commit -m "📝 docs: Atualiza README com novas funcionalidades"
```

### Pull Request

1. **Push** para o teu fork:
```bash
git push origin feature/minha-feature
```

2. **Cria Pull Request** no GitHub

3. **Preenche o template:**
```
### Descrição
[O que esta PR faz?]

### Tipo de Mudança
- [ ] Bug fix
- [ ] Nova funcionalidade
- [ ] Breaking change
- [ ] Documentação

### Checklist
- [ ] Código testado
- [ ] Documentação atualizada
- [ ] Sem console.logs desnecessários
- [ ] Funciona em mobile
- [ ] Não quebra funcionalidades existentes

### Screenshots
[Se aplicável]
```

---

## 📝 Convenções de Código

### JavaScript

```javascript
// ✅ BOM
function loadSongs() {
  const songs = getSongsFromStorage();
  return songs.filter(s => s.active);
}

// ❌ MAU
function load_songs(){
var songs=getSongsFromStorage()
return songs.filter(s=>s.active)}
```

**Regras:**
- camelCase para variáveis e funções
- Nomes descritivos
- Comentários quando necessário
- Espaçamento consistente
- Ponto e vírgula sempre

### HTML

```html
<!-- ✅ BOM -->
<section id="tab-programa" class="tab">
  <h2>Programa Litúrgico</h2>
  <form id="programForm">
    <!-- conteúdo -->
  </form>
</section>

<!-- ❌ MAU -->
<section id=tab-programa class=tab><h2>Programa Litúrgico</h2><form id=programForm>
```

**Regras:**
- Indentação de 2 espaços
- Atributos entre aspas
- Tags sempre fechadas
- Comentários descritivos

### CSS

```css
/* ✅ BOM */
.liturgical-calendar {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  gap: 0.5rem;
}

/* ❌ MAU */
.liturgical-calendar{display:grid;grid-template-columns:repeat(7, 1fr);gap:.5rem}
```

**Regras:**
- Propriedades em linhas separadas
- Espaço após dois pontos
- Unidades sempre explícitas (0.5rem, não .5rem)
- Comentários para secções

---

## 🧪 Testes

Antes de submeter, testa:

### Funcionalidades Críticas

- [ ] Tabs mudam corretamente
- [ ] Tema escuro/claro funciona
- [ ] Programa guarda e carrega
- [ ] Folhetos guardam e imprimem
- [ ] Catálogo carrega do Google Sheets
- [ ] Cânticos personalizados funcionam
- [ ] Calendário navega corretamente
- [ ] Upload de imagens funciona
- [ ] Histórico guarda e carrega

### Browsers

- [ ] Chrome (última versão)
- [ ] Firefox (última versão)
- [ ] Safari (última versão)
- [ ] Edge (última versão)

### Dispositivos

- [ ] Desktop (1920x1080)
- [ ] Tablet (768x1024)
- [ ] Mobile (375x667)

### Console

- [ ] Sem erros no console
- [ ] Sem warnings desnecessários
- [ ] console.logs removidos

---

## 📚 Documentação

Ao adicionar funcionalidades:

1. **Atualiza README.md** - Descreve a nova funcionalidade
2. **Atualiza CHANGELOG.md** - Adiciona à versão atual
3. **Comenta o código** - Explica partes complexas
4. **Screenshots** - Se mudou a UI

---

## 🎯 Prioridades

Estas áreas precisam de atenção:

### Alta Prioridade
- 🐛 Bugs críticos
- 🔒 Segurança
- ♿ Acessibilidade
- 📱 Mobile

### Média Prioridade
- ✨ Novas funcionalidades
- ⚡ Performance
- 🎨 Melhorias de UI

### Baixa Prioridade
- 📝 Documentação
- ♻️ Refatoração não crítica
- 🎨 Ajustes estéticos menores

---

## ❓ Dúvidas?

- **Issues**: [Abre uma issue](https://github.com/[username]/gestao-liturgica/issues)
- **Discussões**: [GitHub Discussions](https://github.com/[username]/gestao-liturgica/discussions)
- **Email**: [teu-email@exemplo.com]

---

## 📜 Licença

Ao contribuir, concordas que as tuas contribuições serão licenciadas sob a [Licença MIT](LICENSE).

---

## 🙏 Agradecimentos

Obrigado por ajudar a melhorar este projeto! Cada contribuição, por menor que seja, faz diferença.

---

**Última atualização:** Dezembro 2024
