# 🚀 Deployment no GitHub Pages - Guia Passo a Passo

## Solução Gratuita e Permanente

GitHub Pages permite hospedar sites estáticos **gratuitamente** e com **domínio personalizado**.

### Pré-requisitos
- Conta no GitHub (crie em https://github.com se não tiver)
- Git instalado no seu computador
- Arquivo `fbgaming-standalone.html`

### Passo 1: Criar Repositório no GitHub

1. Acesse https://github.com/new
2. Preencha:
   - **Repository name**: `fbgaming-code-monitor`
   - **Description**: "Site para monitorar códigos do mail.tm"
   - **Public**: Selecione (necessário para GitHub Pages)
   - **Initialize with README**: Deixe desmarcado
3. Clique em **"Create repository"**

### Passo 2: Preparar os Arquivos Localmente

1. Crie uma pasta no seu computador:
   ```bash
   mkdir fbgaming-code-monitor
   cd fbgaming-code-monitor
   ```

2. Coloque o arquivo `fbgaming-standalone.html` e renomeie para `index.html`:
   ```bash
   cp fbgaming-standalone.html index.html
   ```

3. Inicialize o Git:
   ```bash
   git init
   git add index.html
   git commit -m "Initial commit"
   ```

### Passo 3: Fazer Push para GitHub

1. Copie o comando de push do GitHub (ele mostrará algo como):
   ```bash
   git remote add origin https://github.com/seu-usuario/fbgaming-code-monitor.git
   git branch -M main
   git push -u origin main
   ```

2. Execute os comandos no seu terminal

### Passo 4: Ativar GitHub Pages

1. Acesse seu repositório no GitHub
2. Vá em **"Settings"** (aba no topo)
3. No menu esquerdo, clique em **"Pages"**
4. Em **"Source"**, selecione:
   - Branch: `main`
   - Folder: `/ (root)`
5. Clique em **"Save"**

### Passo 5: Aguardar Deploy

GitHub Pages fará o deploy automaticamente. Você verá:
- Uma mensagem: **"Your site is ready to be published at https://seu-usuario.github.io/fbgaming-code-monitor/"**
- Pode levar alguns minutos

### Passo 6: Acessar o Site

Seu site estará disponível em:
```
https://seu-usuario.github.io/fbgaming-code-monitor/
```

---

## Usar Domínio Personalizado (Opcional)

Se você tem um domínio próprio (ex: `seu-dominio.com`):

1. No GitHub, vá em **"Settings"** → **"Pages"**
2. Em **"Custom domain"**, digite seu domínio
3. Clique em **"Save"**
4. Configure o DNS do seu domínio:
   - Adicione um registro `CNAME` apontando para `seu-usuario.github.io`
   - Ou configure os registros `A` conforme instruções do GitHub

---

## Atualizar o Site

### Método 1: Linha de Comando (Recomendado)

1. Edite o arquivo `index.html` localmente
2. Faça commit e push:
   ```bash
   git add index.html
   git commit -m "Atualização do site"
   git push
   ```
3. GitHub Pages atualizará automaticamente em poucos segundos

### Método 2: Interface Web

1. Acesse seu repositório no GitHub
2. Clique em **"Add file"** → **"Upload files"**
3. Arraste o novo arquivo `index.html`
4. Clique em **"Commit changes"**

---

## Vantagens do GitHub Pages

✅ **Completamente gratuito**
✅ **Sem limite de tempo**
✅ **Domínio personalizado incluído**
✅ **SSL/HTTPS automático**
✅ **Integração com Git**
✅ **Versionamento automático**
✅ **Histórico completo de mudanças**

---

## Desvantagens

❌ Requer Git (mas é fácil de aprender)
❌ Não suporta backend/servidor (mas não precisa para este projeto)
❌ Pode levar alguns minutos para atualizar

---

## Troubleshooting

### Problema: "404 Not Found"
- **Solução**: Certifique-se de que o arquivo está nomeado como `index.html`
- **Verificação**: Acesse `https://seu-usuario.github.io/fbgaming-code-monitor/index.html`

### Problema: GitHub Pages não ativa
- **Solução**: Certifique-se de que o repositório é **público**
- **Verificação**: Vá em **"Settings"** → **"Danger zone"** → verifique se está público

### Problema: Mudanças não aparecem
- **Solução**: Aguarde alguns minutos
- **Cache**: Limpe o cache do navegador (Ctrl+Shift+Delete)

### Problema: Domínio personalizado não funciona
- **Solução**: Verifique se o DNS está configurado corretamente
- **Teste**: Use https://dnschecker.org para verificar

---

## Estrutura do Repositório

```
fbgaming-code-monitor/
├── index.html          ← Seu arquivo HTML
├── README.md           ← Descrição do projeto (opcional)
└── .gitignore          ← Arquivos a ignorar (opcional)
```

---

## Exemplo de README.md

Crie um arquivo `README.md` para documentar seu projeto:

```markdown
# FbgaminGGMAX - Perplexity

Site para monitorar códigos de email em tempo real usando mail.tm.

## Características

- ✅ Monitoramento em tempo real
- ✅ Interface moderna roxo e preto
- ✅ Expiração automática de códigos
- ✅ Copiar código com um clique
- ✅ Sem login necessário

## Como Usar

1. Acesse https://seu-usuario.github.io/fbgaming-code-monitor/
2. Preencha com suas credenciais do mail.tm
3. Clique em "Conectar"
4. Pronto! Os códigos aparecerão automaticamente

## Tecnologia

- HTML5
- CSS3
- JavaScript Vanilla
- API mail.tm

## Licença

MIT
```

---

## Próximos Passos

1. **Adicionar Ações do GitHub** (para automação)
   - Crie um arquivo `.github/workflows/deploy.yml`
   - Automatize builds e deploys

2. **Adicionar Badges** ao README
   - Status do deploy
   - Versão
   - Licença

3. **Configurar Proteção de Branch**
   - Vá em **"Settings"** → **"Branches"**
   - Exija revisão antes de merge

---

## Dicas Importantes

✅ **Faça**: Manter o repositório atualizado
✅ **Faça**: Usar mensagens de commit descritivas
✅ **Faça**: Fazer backup local dos arquivos

❌ **Não faça**: Compartilhar credenciais no repositório
❌ **Não faça**: Fazer commits de arquivos sensíveis
❌ **Não faça**: Deletar o repositório sem backup

---

## Suporte

- Documentação GitHub Pages: https://docs.github.com/en/pages
- Guia Git: https://git-scm.com/doc
- Comunidade GitHub: https://github.community

