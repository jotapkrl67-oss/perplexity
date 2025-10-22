# 🚀 Deployment no Vercel - Guia Passo a Passo

## Solução Simples: Upload de Arquivo Único

Este é o método **mais simples e confiável** para fazer o deploy do site no Vercel.

### Pré-requisitos
- Conta no Vercel (crie em https://vercel.com se não tiver)
- Arquivo `fbgaming-standalone.html`

### Passo 1: Acessar o Vercel

1. Acesse https://vercel.com
2. Faça login com sua conta
3. Clique em **"New Project"** ou **"Add New"** → **"Project"**

### Passo 2: Fazer Upload do Arquivo

**Opção A: Arrastar e Soltar (Mais Fácil)**
1. Na página inicial do Vercel, você verá uma área que diz **"Drag and drop your project folder"**
2. Arraste o arquivo `fbgaming-standalone.html` para essa área
3. O Vercel detectará automaticamente que é um arquivo HTML estático

**Opção B: Usar Git (Recomendado para Atualizações)**
1. Crie uma pasta vazia no seu computador: `fbgaming-code-monitor`
2. Coloque o arquivo `fbgaming-standalone.html` dentro
3. Renomeie para `index.html` (importante!)
4. Crie um repositório Git:
   ```bash
   cd fbgaming-code-monitor
   git init
   git add index.html
   git commit -m "Initial commit"
   ```
5. Crie um repositório no GitHub (https://github.com/new)
6. Faça push do código:
   ```bash
   git remote add origin https://github.com/seu-usuario/fbgaming-code-monitor.git
   git branch -M main
   git push -u origin main
   ```
7. No Vercel, clique em **"New Project"**
8. Selecione o repositório `fbgaming-code-monitor`
9. Clique em **"Deploy"**

### Passo 3: Configurar o Projeto

Quando o Vercel perguntar sobre configurações:
- **Framework**: Selecione **"Other"** ou deixe em branco
- **Root Directory**: Deixe vazio (padrão)
- **Build Command**: Deixe vazio
- **Output Directory**: Deixe vazio

### Passo 4: Aguardar Deploy

O Vercel fará o deploy automaticamente. Você verá:
- ✅ Status: **"Ready"** quando estiver completo
- Um link como `https://seu-projeto.vercel.app`

### Passo 5: Usar o Site

1. Acesse o link do seu projeto
2. Preencha com suas credenciais do mail.tm:
   - Email: `fbgaminggmax@tiffincrane.com`
   - Senha: `FBGAMINGGMAX`
3. Clique em "Conectar"
4. Pronto! O site está funcionando

### Atualizar o Site

Se precisar fazer alterações:

**Com Git:**
1. Edite o arquivo `index.html` localmente
2. Faça commit e push:
   ```bash
   git add index.html
   git commit -m "Atualização"
   git push
   ```
3. O Vercel fará deploy automaticamente

**Sem Git:**
1. Acesse o Vercel
2. Vá até seu projeto
3. Clique em **"Settings"** → **"Git"**
4. Desconecte o Git
5. Arraste o novo arquivo HTML para fazer upload manual

---

## Troubleshooting

### Problema: "404 Not Found"
- **Solução**: Certifique-se de que renomeou o arquivo para `index.html`

### Problema: Site não carrega os códigos
- **Solução**: Verifique se está usando as credenciais corretas do mail.tm
- **Nota**: A API do mail.tm pode ter rate limiting. Aguarde alguns minutos e tente novamente

### Problema: "Falha ao autenticar"
- **Solução**: Verifique se o email e senha estão corretos
- **Nota**: O email deve ser um endereço válido do mail.tm (ex: `seu-email@tiffincrane.com`)

---

## Dicas Importantes

✅ **Faça**: Usar nomes de domínio personalizados (veja "Domains" nas configurações do projeto)
✅ **Faça**: Manter o arquivo HTML atualizado em seu repositório Git
✅ **Faça**: Testar localmente antes de fazer deploy

❌ **Não faça**: Compartilhar suas credenciais do mail.tm publicamente
❌ **Não faça**: Usar senhas fracas
❌ **Não faça**: Deletar o repositório Git sem fazer backup

---

## Próximos Passos

Após o deploy bem-sucedido:

1. **Adicionar Domínio Personalizado** (opcional)
   - Vá em **"Settings"** → **"Domains"**
   - Adicione seu domínio personalizado
   - Siga as instruções para configurar o DNS

2. **Configurar Variáveis de Ambiente** (opcional)
   - Vá em **"Settings"** → **"Environment Variables"**
   - Adicione variáveis se precisar (não necessário para este projeto)

3. **Monitorar Logs** (se houver problemas)
   - Vá em **"Deployments"**
   - Clique no deploy mais recente
   - Veja os logs em **"Logs"**

---

## Suporte

Se tiver dúvidas:
- Documentação do Vercel: https://vercel.com/docs
- Comunidade do Vercel: https://vercel.com/support
- Documentação do mail.tm: https://mail.tm

