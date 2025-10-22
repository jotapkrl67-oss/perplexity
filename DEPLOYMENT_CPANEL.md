# 🚀 Deployment em cPanel/Hostinger - Guia Passo a Passo

## Solução para Hospedagem Compartilhada

Se você tem hospedagem em cPanel (Hostinger, Bluehost, GoDaddy, etc.), este guia é para você.

### Pré-requisitos
- Conta de hospedagem com cPanel
- Acesso ao cPanel
- Arquivo `fbgaming-standalone.html`

### Passo 1: Acessar o cPanel

1. Acesse o painel de controle da sua hospedagem:
   - **Hostinger**: https://hpanel.hostinger.com
   - **Bluehost**: https://my.bluehost.com
   - **GoDaddy**: https://www.godaddy.com/account
   - **Outro**: Verifique o email de boas-vindas

2. Faça login com suas credenciais

3. Procure por **"cPanel"** ou **"File Manager"**

### Passo 2: Acessar o Gerenciador de Arquivos

1. No cPanel, clique em **"File Manager"**
2. Navegue até a pasta **"public_html"** (pasta raiz do seu site)
3. Se você quer que o site seja a página inicial, coloque o arquivo aqui

### Passo 3: Upload do Arquivo

**Opção A: Upload via cPanel (Mais Fácil)**

1. No File Manager, clique em **"Upload"** (ou ícone de seta para cima)
2. Selecione o arquivo `fbgaming-standalone.html`
3. Renomeie para `index.html`:
   - Clique com botão direito no arquivo
   - Selecione **"Rename"**
   - Mude para `index.html`
4. Pronto! O site está online

**Opção B: Upload via FTP**

1. No cPanel, procure por **"FTP Accounts"** ou **"FTP Connections"**
2. Crie uma nova conta FTP (se não tiver)
3. Use um cliente FTP como:
   - **FileZilla** (gratuito): https://filezilla-project.org
   - **WinSCP** (gratuito): https://winscp.net
4. Conecte com as credenciais FTP
5. Navegue até `public_html`
6. Arraste o arquivo `fbgaming-standalone.html` para lá
7. Renomeie para `index.html`

### Passo 4: Verificar Permissões

1. No File Manager, clique com botão direito em `index.html`
2. Selecione **"Change Permissions"**
3. Defina como `644` (padrão)
4. Clique em **"Change"**

### Passo 5: Acessar o Site

Seu site estará disponível em:
```
https://seu-dominio.com
```

Se colocou em uma subpasta:
```
https://seu-dominio.com/fbgaming/
```

---

## Usar em Subdomínio (Opcional)

Se quer usar um subdomínio (ex: `codes.seu-dominio.com`):

1. No cPanel, procure por **"Addon Domains"** ou **"Subdomains"**
2. Crie um novo subdomínio
3. Defina a pasta raiz como a pasta onde colocou o arquivo
4. Acesse `https://codes.seu-dominio.com`

---

## Atualizar o Site

### Método 1: File Manager

1. Acesse o cPanel → **"File Manager"**
2. Navegue até `public_html`
3. Clique com botão direito em `index.html`
4. Selecione **"Delete"**
5. Faça upload do novo arquivo
6. Renomeie para `index.html`

### Método 2: FTP

1. Conecte via FTP
2. Navegue até `public_html`
3. Arraste o novo arquivo para substituir

### Método 3: Editor de Texto (Para Pequenas Mudanças)

1. No File Manager, clique com botão direito em `index.html`
2. Selecione **"Edit"**
3. Faça as alterações
4. Clique em **"Save"**

---

## Troubleshooting

### Problema: "404 Not Found"
- **Solução 1**: Certifique-se de que o arquivo está em `public_html`
- **Solução 2**: Verifique se está nomeado como `index.html`
- **Solução 3**: Limpe o cache do navegador

### Problema: "403 Forbidden"
- **Solução**: Verifique as permissões do arquivo (deve ser `644`)
- **Passo**: Clique direito → "Change Permissions" → `644`

### Problema: Site não carrega os códigos
- **Solução**: Verifique as credenciais do mail.tm
- **Nota**: Pode haver rate limiting da API

### Problema: "500 Internal Server Error"
- **Solução**: Verifique se o arquivo HTML está correto
- **Dica**: Teste localmente antes de fazer upload

---

## Dicas para Hostinger Especificamente

✅ **Hostinger** é muito fácil para este projeto
✅ Suporta HTTPS automático
✅ Tem bom desempenho para sites estáticos

**Passos Rápidos no Hostinger:**
1. Acesse https://hpanel.hostinger.com
2. Clique em seu site
3. Vá em **"File Manager"**
4. Arraste o arquivo para `public_html`
5. Renomeie para `index.html`
6. Pronto!

---

## Comparação: Hostinger vs Vercel vs Netlify

| Recurso | Hostinger | Vercel | Netlify |
|---------|-----------|--------|---------|
| Custo | Pago | Gratuito | Gratuito |
| Facilidade | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Domínio próprio | ✅ | ✅ | ✅ |
| Suporte | 24/7 | Comunidade | Comunidade |
| Velocidade | Bom | Muito Bom | Muito Bom |

**Recomendação**: 
- Se já tem hospedagem: **Use Hostinger**
- Se quer gratuito: **Use Netlify**
- Se quer máxima performance: **Use Vercel**

---

## Próximos Passos

1. **Configurar SSL/HTTPS**
   - Hostinger faz automaticamente
   - Verifique em **"SSL/TLS Status"**

2. **Adicionar Certificado SSL**
   - Procure por **"AutoSSL"** no cPanel
   - Clique em **"Check & Install"**

3. **Configurar Email**
   - Crie contas de email no cPanel
   - Use para receber notificações (se precisar depois)

4. **Monitorar Performance**
   - Use **"Analytics"** no cPanel
   - Verifique estatísticas de acesso

---

## Suporte

- **Hostinger**: https://support.hostinger.com
- **cPanel**: https://docs.cpanel.net
- **Bluehost**: https://www.bluehost.com/support
- **GoDaddy**: https://www.godaddy.com/help

---

## Segurança

⚠️ **Importante**: Suas credenciais do mail.tm são armazenadas **apenas no navegador** do usuário. Não são enviadas para o servidor.

✅ **Seguro**: O site usa HTTPS
✅ **Seguro**: Nenhum dado sensível é armazenado no servidor
✅ **Seguro**: Você controla completamente seus dados

---

## Exemplo de Estrutura Final

```
seu-dominio.com/
├── index.html          ← Seu arquivo (renomeado)
├── robots.txt          ← (opcional)
└── sitemap.xml         ← (opcional)
```

Pronto! Seu site está online! 🎉

