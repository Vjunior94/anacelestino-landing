# Landing Page Ana Celestino - Instruções de Hospedagem

## 📦 Arquivos da Landing Page

Esta pasta contém todos os arquivos necessários para hospedar a landing page do aplicativo Ana Celestino:

- `index.html` - Página principal
- `styles.css` - Estilos CSS
- `logo.png` - Logo Ana Celestino
- `favicon.png` - Ícone do navegador

## 🚀 Opções de Hospedagem Gratuita

### Opção 1: GitHub Pages (Recomendado - Mais Simples)

**Passo a passo:**

1. Crie uma conta no GitHub (se ainda não tiver): https://github.com
2. Crie um novo repositório público chamado `anacelestino-landing`
3. Faça upload de todos os arquivos desta pasta para o repositório
4. Vá em Settings → Pages
5. Em "Source", selecione "Deploy from a branch" e escolha "main"
6. Aguarde alguns minutos e sua página estará disponível em: `https://seu-usuario.github.io/anacelestino-landing`

**Configurar domínio personalizado:**
1. No GitHub Pages, adicione `anacelestino.com.br` no campo "Custom domain"
2. Siga as instruções de DNS abaixo

---

### Opção 2: Vercel (Recomendado - Mais Profissional)

**Passo a passo:**

1. Acesse: https://vercel.com
2. Crie uma conta gratuita (pode usar conta do GitHub)
3. Clique em "Add New" → "Project"
4. Faça upload da pasta ou conecte ao repositório GitHub
5. Clique em "Deploy"
6. Após o deploy, vá em "Settings" → "Domains"
7. Adicione `anacelestino.com.br`

**Configurar domínio personalizado:**
- A Vercel fornecerá automaticamente as configurações de DNS necessárias

---

### Opção 3: Netlify

**Passo a passo:**

1. Acesse: https://www.netlify.com
2. Crie uma conta gratuita
3. Arraste a pasta `landing-page-anacelestino` para a área de upload
4. Aguarde o deploy
5. Vá em "Domain settings" → "Add custom domain"
6. Adicione `anacelestino.com.br`

---

## 🌐 Configuração DNS no GoDaddy

Após escolher uma das opções de hospedagem acima, você precisará configurar o DNS no GoDaddy:

### Para GitHub Pages:

1. Acesse sua conta GoDaddy
2. Vá em "Meus Produtos" → "DNS"
3. Adicione os seguintes registros:

**Registro A (para domínio raiz):**
```
Tipo: A
Nome: @
Valor: 185.199.108.153
TTL: 600 segundos
```

Adicione mais 3 registros A com os mesmos dados, mas com valores:
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

**Registro CNAME (para www):**
```
Tipo: CNAME
Nome: www
Valor: seu-usuario.github.io
TTL: 1 hora
```

---

### Para Vercel ou Netlify:

A plataforma fornecerá automaticamente as configurações específicas de DNS. Geralmente será algo como:

**Registro A:**
```
Tipo: A
Nome: @
Valor: [IP fornecido pela plataforma]
TTL: 600 segundos
```

**Registro CNAME:**
```
Tipo: CNAME
Nome: www
Valor: [domínio fornecido pela plataforma]
TTL: 1 hora
```

---

## ⏱️ Tempo de Propagação

Após configurar o DNS, pode levar de 15 minutos a 48 horas para o domínio começar a funcionar. Geralmente funciona em 1-2 horas.

---

## ✅ Verificar se está funcionando

Após a propagação do DNS, acesse:
- `http://anacelestino.com.br`
- `http://www.anacelestino.com.br`

Ambos devem exibir a landing page.

---

## 🔒 HTTPS (Certificado SSL)

Todas as plataformas mencionadas (GitHub Pages, Vercel, Netlify) fornecem **HTTPS gratuito e automático** após a configuração do domínio personalizado.

---

## 📝 Notas Importantes

1. **URL do App**: A landing page está configurada para redirecionar para a URL atual do app Manus. Se essa URL mudar, você precisará editar o arquivo `index.html` e atualizar o link no botão "Acessar Aplicativo"

2. **Atualizar conteúdo**: Para fazer alterações na landing page, basta editar os arquivos HTML/CSS e fazer novo upload na plataforma escolhida

3. **Domínio sem www**: Configure tanto `anacelestino.com.br` quanto `www.anacelestino.com.br` para garantir que ambos funcionem

---

## 🆘 Precisa de Ajuda?

Se tiver dificuldades em qualquer etapa, me avise que posso te guiar passo a passo!
