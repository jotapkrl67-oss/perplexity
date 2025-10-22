# 🎮 FbgaminGGMAX - Perplexity | Monitorador de Códigos

Um site moderno e responsivo para monitorar códigos de email em tempo real usando a API do mail.tm.

## ✨ Características

- ✅ **Monitoramento em Tempo Real**: Atualiza automaticamente a cada 10 segundos
- ✅ **Interface Moderna**: Design roxo e preto elegante e responsivo
- ✅ **Copiar com Um Clique**: Botão para copiar códigos com notificação de sucesso
- ✅ **Expiração Automática**: Códigos expiram após 1 hora com aviso de 5 minutos
- ✅ **Deletar Manualmente**: Botão para remover códigos individuais
- ✅ **Persistência**: Códigos deletados não reaparecem ao atualizar a página
- ✅ **Sem Login Necessário**: Acesse direto com suas credenciais do mail.tm
- ✅ **Funciona em Qualquer Lugar**: Arquivo HTML único, sem dependências
- ✅ **Totalmente Seguro**: Dados armazenados apenas no navegador do usuário
- ✅ **Responsivo**: Funciona perfeitamente em desktop, tablet e mobile

## 🚀 Como Usar

### Pré-requisitos
- Uma conta no mail.tm (crie em https://mail.tm se não tiver)
- Um navegador web moderno (Chrome, Firefox, Safari, Edge)

### Passo 1: Acessar o Site

Acesse o site onde foi feito o deployment:
- **Netlify**: `https://seu-projeto.netlify.app`
- **Vercel**: `https://seu-projeto.vercel.app`
- **GitHub Pages**: `https://seu-usuario.github.io/fbgaming-code-monitor`
- **Hostinger**: `https://seu-dominio.com`

### Passo 2: Conectar sua Conta

1. Preencha com suas credenciais do mail.tm:
   - **Email**: seu email do mail.tm (ex: `seu-email@tiffincrane.com`)
   - **Senha**: sua senha do mail.tm

2. Clique em **"Conectar"**

3. Aguarde a autenticação (pode levar alguns segundos)

### Passo 3: Visualizar Códigos

Após conectar, o site mostrará:
- Todos os códigos recebidos no seu email
- Hora de recebimento de cada código
- Tempo restante antes de expiração
- Botões para copiar ou deletar cada código

### Passo 4: Usar os Códigos

**Para copiar um código:**
1. Clique no botão 📋 **"Copiar"**
2. Você verá a mensagem "✅ Código copiado com sucesso!"
3. Cole em qualquer lugar (Ctrl+V ou Cmd+V)

**Para deletar um código:**
1. Clique no botão 🗑️
2. O código desaparecerá imediatamente
3. Não reaparecerá mesmo se atualizar a página

**Para atualizar manualmente:**
1. Clique no botão 🔄 **"Atualizar"**
2. O site buscará novos códigos

## 📋 Informações Técnicas

### Arquitetura
- **Frontend**: HTML5 + CSS3 + JavaScript Vanilla
- **Backend**: Nenhum (tudo no navegador)
- **API**: mail.tm REST API (https://api.mail.tm)
- **Armazenamento**: localStorage do navegador

### Fluxo de Dados
```
Navegador → mail.tm API → Códigos Extraídos → Exibição no Site
```

### Segurança
- ✅ Credenciais armazenadas **apenas no navegador** (localStorage)
- ✅ Nenhum servidor intermediário
- ✅ HTTPS automático em todos os deployments
- ✅ Sem tracking ou analytics
- ✅ Sem compartilhamento de dados

### Padrões de Extração de Código
O site procura automaticamente por códigos nos seguintes formatos:
- `token=XXXXXX`
- `código: XXXXXX`
- `code: XXXXXX`
- Códigos de 6 dígitos: `123456`
- Códigos alfanuméricos: `ABC123`

## 📱 Responsividade

O site funciona perfeitamente em:
- ✅ Desktop (1920x1080, 1366x768, etc.)
- ✅ Tablet (iPad, Android tablets)
- ✅ Mobile (iPhone, Android phones)

O layout se adapta automaticamente ao tamanho da tela.

## 🌐 Opções de Deployment

Escolha a opção que melhor se encaixa:

### 1. **Netlify** ⭐ (Recomendado - Mais Fácil)
- Arraste e solte o arquivo
- Deploy em segundos
- Guia: `DEPLOYMENT_NETLIFY.md`

### 2. **Vercel**
- Integração com Git
- Muito rápido
- Guia: `DEPLOYMENT_VERCEL.md`

### 3. **GitHub Pages** (Gratuito)
- Hospedagem permanente
- Versionamento automático
- Guia: `DEPLOYMENT_GITHUB_PAGES.md`

### 4. **cPanel/Hostinger** (Se já tem hospedagem)
- Upload via FTP ou File Manager
- Seu próprio domínio
- Guia: `DEPLOYMENT_CPANEL.md`

## 📊 Estatísticas de Uso

- **Tamanho do arquivo**: ~29 KB (comprimido)
- **Tempo de carregamento**: < 1 segundo
- **Requisições à API**: 1 a cada 10 segundos
- **Consumo de banda**: Mínimo (< 10 KB por requisição)

## 🔧 Personalização

### Mudar Cores
Edite o arquivo `index.html` e procure por:
```css
background: linear-gradient(135deg, #a855f7 0%, #7c3aed 100%);
```

Substitua pelos códigos de cor desejados.

### Mudar Intervalo de Atualização
Procure por:
```javascript
CONFIG = {
    AUTO_REFRESH_INTERVAL: 10000, // 10 segundos
```

Mude `10000` para o intervalo desejado em milissegundos.

### Mudar Tempo de Expiração
Procure por:
```javascript
CODE_EXPIRATION_TIME: 3600000, // 1 hora
```

Mude `3600000` para o tempo desejado em milissegundos.

## ⚠️ Limitações Conhecidas

- A API do mail.tm pode ter rate limiting (máx ~100 requisições/minuto)
- Códigos expiram após 1 hora (configurável)
- Requer conexão com internet
- Não funciona offline
- Não suporta múltiplas contas simultaneamente

## 🐛 Troubleshooting

### "Falha ao autenticar"
- Verifique se o email e senha estão corretos
- Certifique-se de que a conta existe no mail.tm
- Aguarde alguns minutos se houver rate limiting

### "Nenhum código encontrado"
- Verifique se há emails no seu inbox do mail.tm
- Clique em "Atualizar" para buscar manualmente
- Aguarde alguns segundos para a próxima atualização automática

### "Erro ao buscar códigos"
- Verifique sua conexão com internet
- Limpe o cache do navegador
- Tente novamente em alguns minutos

### Site não carrega
- Verifique se o arquivo está nomeado como `index.html`
- Limpe o cache do navegador (Ctrl+Shift+Delete)
- Tente em outro navegador

## 📞 Suporte

### Para Problemas com o Site
- Verifique os guias de deployment
- Limpe o cache e cookies
- Teste em outro navegador

### Para Problemas com mail.tm
- Documentação: https://mail.tm
- Comunidade: https://github.com/mail-tm/mail.tm

## 📝 Licença

Este projeto é fornecido como está, sem garantias.

## 🎯 Roadmap Futuro

Possíveis melhorias:
- [ ] Suporte a múltiplas contas
- [ ] Notificações de som
- [ ] Histórico de códigos
- [ ] Filtros por remetente
- [ ] Temas personalizáveis
- [ ] Sincronização entre abas

## 💡 Dicas e Truques

### Dica 1: Usar com Múltiplos Emails
- Abra o site em abas diferentes
- Conecte com emails diferentes em cada aba
- Monitore múltiplas contas simultaneamente

### Dica 2: Integrar com Outras Ferramentas
- Copie os códigos e cole em qualquer lugar
- Use com formulários online
- Integre com automações (se souber programar)

### Dica 3: Manter Atualizado
- Verifique regularmente por atualizações
- Teste novas versões antes de usar em produção
- Faça backup de suas configurações

## 🙏 Agradecimentos

- mail.tm pela excelente API
- Comunidade open source
- Você por usar este projeto!

---

**Versão**: 1.0.0  
**Última atualização**: Outubro 2025  
**Status**: ✅ Totalmente funcional e testado

Aproveite! 🎉

