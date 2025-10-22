# 🚀 Deployment no Netlify - Guia Passo a Passo

## Solução Simples: Upload Direto

Netlify é ainda mais simples que Vercel para arquivos estáticos!

### Pré-requisitos
- Conta no Netlify (crie em https://netlify.com se não tiver)
- Arquivo `fbgaming-standalone.html`

### Passo 1: Acessar o Netlify

1. Acesse https://netlify.com
2. Faça login com sua conta (Google, GitHub, etc.)
3. Você verá a página inicial com a opção **"Drag and drop your site here"**

### Passo 2: Upload do Arquivo (Método Mais Fácil)

**Opção A: Arrastar e Soltar**
1. Renomeie o arquivo para `index.html`
2. Arraste o arquivo `index.html` para a área **"Drag and drop your site here"**
3. Pronto! O site está online em segundos

**Opção B: Usar Git (Para Atualizações Automáticas)**
1. Crie uma pasta: `fbgaming-code-monitor`
2. Coloque o arquivo `index.html` dentro
3. Inicialize Git:
   ```bash
   cd fbgaming-code-monitor
   git init
   git add index.html
   git commit -m "Initial commit"
   ```
4. Crie um repositório no GitHub (https://github.com/new)
5. Faça push:
   ```bash
   git remote add origin https://github.com/seu-usuario/fbgaming-code-monitor.git
   git branch -M main
   git push -u origin main
   ```
6. No Netlify, clique em **"New site from Git"**
7. Selecione GitHub e o repositório `fbgaming-code-monitor`
8. Clique em **"Deploy"**

### Passo 3: Obter o Link

Após o upload, você receberá um link como:
- `https://seu-projeto-12345.netlify.app`

### Passo 4: Usar o Site

1. Acesse o link gerado
2. Preencha com suas credenciais:
   - Email: `fbgaminggmax@tiffincrane.com`
   - Senha: `FBGAMINGGMAX`
3. Clique em "Conectar"

### Passo 5: Personalizar o Domínio (Opcional)

1. Clique em **"Site settings"**
2. Vá em **"Domain management"**
3. Clique em **"Add custom domain"**
4. Digite seu domínio personalizado
5. Siga as instruções para configurar o DNS

---

## Vantagens do Netlify

✅ **Mais rápido** que Vercel para sites estáticos
✅ **Sem configuração** necessária
✅ **SSL/HTTPS automático**
✅ **Redirecionamentos automáticos**
✅ **Suporte a variáveis de ambiente** (se precisar depois)

---

## Atualizar o Site

**Com Git:**
1. Edite o arquivo `index.html` localmente
2. Faça commit e push:
   ```bash
   git add index.html
   git commit -m "Atualização"
   git push
   ```
3. Netlify fará deploy automaticamente

**Sem Git:**
1. Acesse https://netlify.com
2. Clique no seu site
3. Arraste o novo arquivo `index.html` para atualizar

---

## Troubleshooting

### Problema: "404 Not Found"
- **Solução**: Certifique-se de que o arquivo está nomeado como `index.html`

### Problema: Site não carrega os códigos
- **Solução**: Verifique as credenciais do mail.tm
- **Nota**: Aguarde alguns minutos se houver rate limiting

### Problema: "Falha ao autenticar"
- **Solução**: Verifique email e senha
- **Dica**: Use um email válido do mail.tm

---

## Comparação: Vercel vs Netlify

| Recurso | Vercel | Netlify |
|---------|--------|---------|
| Deploy de arquivo único | ✅ | ✅ |
| Integração Git | ✅ | ✅ |
| Domínio personalizado | ✅ | ✅ |
| SSL/HTTPS | ✅ | ✅ |
| Facilidade | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Velocidade | Rápido | Muito Rápido |

**Recomendação**: Use **Netlify** para máxima simplicidade!

---

## Próximos Passos

1. **Monitorar o Site**
   - Vá em **"Analytics"** para ver estatísticas
   - Configure **"Notifications"** para alertas

2. **Configurar Redirecionamentos** (se precisar)
   - Crie um arquivo `_redirects` na pasta raiz
   - Exemplo:
     ```
     /old-page /new-page 301
     ```

3. **Adicionar Formulários** (se precisar depois)
   - Netlify tem suporte nativo a formulários
   - Basta adicionar um `<form>` no HTML

---

## Suporte

- Documentação Netlify: https://docs.netlify.com
- Comunidade Netlify: https://community.netlify.com
- Status do Netlify: https://www.netlifystatus.com

