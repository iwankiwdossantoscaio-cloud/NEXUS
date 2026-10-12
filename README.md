# ✦ Nexus — IA + Notas Pessoais

> Assistente de IA com Google Gemini integrado e sistema completo de notas, tudo em um único arquivo HTML.

![Preview](https://img.shields.io/badge/status-ativo-brightgreen)
![License](https://img.shields.io/badge/licença-MIT-blue)
![HTML](https://img.shields.io/badge/HTML-puro-orange)
![Gemini](https://img.shields.io/badge/IA-Gemini%201.5%20Flash-4285F4)

---

## 📸 Funcionalidades

### 🔐 Autenticação
- Cadastro com nome, sobrenome, e-mail e senha
- Login com sessão persistente (localStorage)
- Barra de força de senha animada
- Dados salvos por usuário — cada conta tem suas próprias notas

### 🤖 Chat com IA (Google Gemini)
- Powered by **Gemini 1.5 Flash** — rápido e gratuito
- Configuração da API Key direto na interface (sem precisar editar código)
- Histórico de conversa mantido durante a sessão
- Botão **"Salvar como nota"** em cada resposta da IA
- Sugestões rápidas de perguntas na tela inicial
- Formatação de código, negrito e blocos de código

### 📝 Sistema de Notas
- Criar, editar e excluir notas
- Títulos personalizados
- Sistema de **tags** (pressione Enter ou vírgula para adicionar)
- **Autosalvamento** automático (800ms após parar de digitar)
- Notas recentes na sidebar
- Contador de notas em tempo real
- Dados persistidos por usuário no localStorage

### 🎨 Design
- Estética editorial paper/ink — clean e profissional
- Tipografia: **Instrument Serif** + **Geist** + **Geist Mono**
- Paleta creme/verde-escuro com textura sutil
- Sidebar recolhível
- Toast notifications
- Responsivo para mobile

---

## 🚀 Como usar

### 1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/nexus-ia.git
cd nexus-ia
```

### 2. Abra o arquivo
Basta abrir `index.html` no navegador — **sem servidor, sem dependências, sem build**.

```bash
# Ou use o Live Server do VS Code
# Ou simplesmente dê duplo clique no index.html
```

### 3. Configure a API Key do Gemini
1. Acesse [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Crie uma conta Google (se ainda não tiver)
3. Clique em **"Create API Key"** — é **gratuito**, sem cartão de crédito
4. Copie a chave gerada
5. No Nexus, faça login → cole a chave no banner amarelo → clique **Salvar**

> A chave fica salva no `localStorage` do navegador. Não precisa reinserir toda vez.

---

## 📁 Estrutura do Projeto

```
nexus-ia/
├── index.html       ← Aplicação completa (HTML + CSS + JS)
├── README.md        ← Este arquivo
├── LICENSE          ← Licença MIT
└── .gitignore       ← Arquivos ignorados pelo Git
```

> O projeto é **zero dependências** — tudo em um único arquivo HTML autocontido.

---

## 🔧 Configuração (opcional)

Se quiser alterar a API Key diretamente no código, abra `index.html` e localize:

```javascript
let GEMINI_API_KEY = localStorage.getItem('nx_gemini_key') || '';
```

Substitua por:

```javascript
let GEMINI_API_KEY = 'SUA_CHAVE_AQUI';
```

Para trocar o modelo do Gemini, localize:

```javascript
const GEMINI_URL = `https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent?key=${GEMINI_API_KEY}`;
```

Modelos disponíveis:
- `gemini-1.5-flash` — rápido, gratuito (recomendado)
- `gemini-1.5-pro` — mais inteligente, limite menor no plano gratuito
- `gemini-2.0-flash` — mais recente

---

## 🛡️ Segurança e Privacidade

- ✅ Nenhum dado é enviado para servidores externos (exceto a API do Gemini)
- ✅ Senhas são armazenadas como hash base64 (não em texto puro)
- ✅ Notas e usuários ficam apenas no `localStorage` do seu navegador
- ⚠️ A API Key fica salva no localStorage — não compartilhe o dispositivo sem considerar isso
- ⚠️ Para produção real, use um backend para gerenciar a API Key com segurança

---

## 🛠️ Tecnologias

| Camada | Tecnologia |
|--------|-----------|
| Frontend | HTML5 + CSS3 + JavaScript ES2022 |
| IA | Google Gemini 1.5 Flash API |
| Fontes | Google Fonts (Instrument Serif, Geist, Geist Mono) |
| Dados | localStorage (sem banco de dados) |
| Build | Nenhum — arquivo único |

---

## 📄 Licença

MIT © 2025 — Sinta-se livre para usar, modificar e distribuir.

---

## 🙋 Contribuição

Pull requests são bem-vindos! Para mudanças maiores, abra uma issue primeiro para discutir o que você gostaria de mudar.

1. Fork o projeto
2. Crie sua branch (`git checkout -b feature/minha-feature`)
3. Commit suas mudanças (`git commit -m 'feat: adiciona minha feature'`)
4. Push para a branch (`git push origin feature/minha-feature`)
5. Abra um Pull Request
