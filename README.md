# VideoIA Pro — Roteiro Multi-Cliente com IA

Sistema de roteiro interativo para criação de vídeos de produto com IA.
Multi-cliente, persistência por usuário, assistente Claude integrado.

---

## 📁 Estrutura de Arquivos

```
roteiro-ia/
├── index.html      ← Tela de Login (página inicial)
├── roteiro.html    ← App principal (7 etapas + IA)
└── README.md       ← Este arquivo
```

---

## 🚀 Como Publicar no GitHub Pages (Passo a Passo)

### 1. Crie uma conta no GitHub
→ https://github.com (gratuito)

### 2. Crie um repositório novo
- Clique em **"New repository"**
- Nome: `roteiro-ia` (ou qualquer nome)
- Deixe **Public**
- Clique em **"Create repository"**

### 3. Faça upload dos arquivos
- Na página do repositório, clique em **"uploading an existing file"**
- Arraste os 3 arquivos: `index.html`, `roteiro.html`, `README.md`
- Clique em **"Commit changes"**

### 4. Ative o GitHub Pages
- Vá em **Settings** (aba do repositório)
- No menu lateral, clique em **Pages**
- Em "Source", selecione **Deploy from a branch**
- Branch: **main** → pasta: **/ (root)**
- Clique em **Save**

### 5. Acesse seu site
Após ~2 minutos, seu site estará em:
```
https://SEU_USUARIO.github.io/roteiro-ia/
```

---

## 🔐 Configuração Inicial

### Alterar a senha de admin
Abra o arquivo `index.html` e encontre a linha:
```javascript
const ADMIN_PASSWORD = 'rarili2025admin';
```
Troque pelo valor desejado antes de publicar.

### Criar clientes (via Admin)
1. Acesse o site
2. Clique na aba **Admin**
3. Digite a senha admin
4. Crie os clientes com nome e senha

### Dados pré-configurados (demo)
| Usuário | Senha |
|---------|-------|
| demo | demo123 |
| admin | admin123 |

---

## ⚙️ Como Funciona

### Multi-Cliente
- Cada cliente tem login próprio
- Progresso de checklists salvo separadamente por cliente
- Histórico de conversas com a IA salvo por perfil
- Dados armazenados no navegador (localStorage)

### Assistente IA
- Powered by **Claude Sonnet** via API Anthropic
- Contexto automático da etapa atual
- Ações rápidas específicas por etapa
- Histórico de conversa mantido na sessão

### Persistência
- Checklists marcados são salvos automaticamente
- Ao reabrir o site e logar, o progresso é restaurado
- Indicador visual de "Salvo" no topo

---

## ⚠️ Observação sobre a API

O assistente IA usa a API da Anthropic diretamente do navegador.
Para produção em escala, considere criar um backend simples para
proteger a chave de API.

Para uso pessoal/freelance como está, funciona perfeitamente.

---

## 📱 Compatibilidade

- ✅ Chrome / Edge / Firefox / Safari
- ✅ Desktop e tablet
- ⚠️ Mobile: sidebar oculta, painel IA oculto (layout simplificado)

---

## 🔄 Atualizar o Site

Para atualizar qualquer arquivo:
1. Abra o repositório no GitHub
2. Clique no arquivo que quer editar
3. Clique no ícone de lápis ✏️
4. Faça as alterações e clique em **"Commit changes"**
5. O site atualiza automaticamente em ~1 minuto
