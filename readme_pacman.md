# 🟡 Grafico de Pacman - Tutorial

Este guia explica como adicionar o gráfico de contribuições em formato de **Pacman** no seu perfil do GitHub.

---

## 📌 Pré-requisitos
- Ter um repositório com o mesmo nome do seu usuário  
  (ex: usuário `ana`, repositório `ana`)

1. Clique em New repository
2. O nome do repositório deve ser igual ao seu username
3. Marque a opção Add a README
4. Clique em Create repository

---

## Passo 1 – Copiar o workflow do Pacman

1. Acesse o meu repositório:
   ```arduino
   https://github.com/anaclarasantos-dev/anaclarasantos-dev
   ```
2. Copie o arquivo main.yml 
3. No seu repositório, crie a pasta:
   ```bash
     .github/workflows/
   ```
4. Cole o arquivo dentro dessa pasta
   
⚠️ Apenas copiar o código NÃO é suficiente.  
O Pacman funciona via **GitHub Actions**.

---

## Passo 2 – Configurar o workflow

No seu próprio repositório:

1. Vá em `.github/workflows`
2. Abra o arquivo `main.yml`
3. Altere o valor abaixo para o **seu usuário do GitHub**:

```yml
github_user_name: SEU_USUARIO_AQUI
```

Salve o arquivo

## Passo 3 – Liberar as permissões (ESSENCIAL)
Antes de rodar o workflow:
 1. Vá em Settings
 2. Clique em Actions → General
 3. Role até Workflow permissions
 4. Selecione:

```pgsql
 Read and write permissions
```
 5. Marque
```pgsql
 Allow GitHub Actions to create and approve pull requests
```
6. Clique em **Save**
   
⚠️ Se você não fizer isso, o workflow vai falhar com erro de permissão.

## Passo 4 – Rodar o workflow

1. Vá na aba Actions
2. Clique em gerador pacman
3. Clique em Run workflow
4. Aguarde finalizar (status verde ✅)

## Passo 5 – Conferir a branch output

Após o workflow rodar:
- Um pasta chamada output será criada
- Dentro dela haverá arquivos svg do Pacman

Exemplo: 

```lua
output/
├── pacman-contribution-graph.svg
└── pacman-contribution-graph-dark.svg
```

## Passo 6 – Adicionar no README do perfil
No seu README.md, cole:

```html
<picture>
  <source media="(prefers-color-scheme: dark)"
    srcset="https://raw.githubusercontent.com/SEU_USUARIO/SEU_USUARIO/output/pacman-contribution-graph-dark.svg">
  <img alt="pacman contribution graph"
    src="https://raw.githubusercontent.com/SEU_USUARIO/SEU_USUARIO/output/pacman-contribution-graph.svg">
</picture>
```

Substitua `SEU_USUARIO` pelo seu username.

## ✅ Pronto!

Agora seu perfil terá um gráfico animado estilo Pacman!
O workflow roda automaticamente todos os dias.
