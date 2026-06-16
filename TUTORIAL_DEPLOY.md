# Tutorial: Subindo repositório no GitHub e fazendo Deploy na Vercel

Este guia explica o passo a passo de como enviar seus códigos locais para o GitHub e depois hospedá-los gratuitamente na Vercel.

## 1. Subindo o código no GitHub

### Pré-requisitos
- Ter o Git instalado no seu computador.
- Ter uma conta no [GitHub](https://github.com/).

### Passo a passo

1. **Inicie o Git na sua pasta (se for a primeira vez):**
   Abra o terminal na pasta do seu projeto e digite:
   ```bash
   git init
   ```

2. **Adicione os arquivos para serem acompanhados:**
   ```bash
   git add .
   ```

3. **Crie o primeiro "commit" (versão do seu código):**
   ```bash
   git commit -m "Meu primeiro commit"
   ```

4. **Crie o repositório no GitHub:**
   - Acesse o GitHub e clique em **New repository** (Novo repositório).
   - Dê um nome para ele e deixe as opções de "Add a README file" ou ".gitignore" em branco. O projeto deve nascer vazio.
   - Clique em **Create repository**.

5. **Conecte o seu projeto local ao repositório do GitHub e envie os arquivos:**
   Na página que carregar após você criar o repositório, copie as instruções que o próprio GitHub lhe fornece para repositórios locais existentes e cole no seu terminal. Será algo assim:
   ```bash
   git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
   git branch -M main
   git push -u origin main
   ```

Pronto! Seu código estará no GitHub. 
Toda vez que você alterar seu código futuramente e quiser atualizar no GitHub, você só precisa usar:
```bash
git add .
git commit -m "O que você alterou"
git push
```

---

## 2. Conectando e fazendo o Deploy na Vercel

O mais legal da Vercel é que, uma vez conectada ao seu projeto do GitHub, toda vez que você enviar uma mudança (o famoso `git push`), seu site será atualizado na internet para todo mundo ver, instantaneamente.

> **Importante:** Em projetos HTML puro sem framework, a Vercel sempre vai procurar um arquivo principal chamado `index.html` para carregar o seu site. Garanta que o seu arquivo de entrada sempre tenha esse nome e não letras maiúsculas ou espaços!

### Passo a passo

1. **Acesse o Painel:**
   Entre no site da [Vercel](https://vercel.com/) e faça login, preferencialmente utilizando a opção "Continue with GitHub".

2. **Crie o Projeto:**
   - No Dashboard inicial, clique no botão preto chamado **Add New...**. 
   - Selecione a opção **Project**.

3. **Importe o Repositório do GitHub:**
   - Na lista "Import Git Repository", você verá os repositórios da sua conta do GitHub.
   - Encontre o seu repositório (ex: `mapaMental`) e clique no botão **Import** localizado ao lado dele.
   *(Se a sua conta for nova e os seus repositórios não aparecerem, clique em "Adjust GitHub App Permissions" e permita que a Vercel leia as suas pastas no GitHub.)*

4. **Configurações do Deploy:**
   - Você será levado à tela "Configure Project". Se for apenas um arquivo HTML, CSS e JavaScript comum, você não precisa fazer nenhuma alteração nas configurações avançadas, apenas mantenha a configuração natural que aparecer.
   - Clique no botão azul **Deploy**.

5. **Aguarde os confetes 🎉!**
   Em alguns segundos a Vercel vai processar seu código e retornar "Congratulations!". Clicando em "Continue to Dashboard" você terá o seu `Domain` público acessível por qualquer pessoa na internet!
