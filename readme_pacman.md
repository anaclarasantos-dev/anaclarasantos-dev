# 🟡 Grafico de Pacman - contribuições

Este guia explica como adicionar o gráfico de contribuições em formato de **Pacman** no seu perfil do GitHub.

---

## 📌 Pré-requisitos

- Ter um repositório com o mesmo nome do seu usuário  
  (ex: usuário `ana`, repositório `ana`)

---

## Passo 1 – Copiar o repositório base

1. Acesse o meu repositório: https://github.com/anaclarasantos-dev/anaclarasantos-dev
2. Clique em **Fork**
3. Confirme o fork no seu perfil

⚠️ Apenas copiar o código NÃO é suficiente.  
O Pacman funciona via **GitHub Actions**.

---

## Passo 2 – Configurar o workflow

No repositório forkado:

1. Vá em `.github/workflows`
2. Abra o arquivo `pacman.yml`
3. Altere o valor abaixo para o **seu usuário do GitHub**:

```yml
github_user_name: SEU_USUARIO_AQUI
```

Salve o arquivo

## Passo 3 – Rodar o workflow

1. Vá na aba Actions
2. Clique em gerador pacman
3. Clique em Run workflow
4. Aguarde finalizar (status verde ✅)

## Passo 4 – Conferir a pasta output

Após o workflow rodar:
- Um pasta chamada output será criada
- Dentro dela haverá arquivos svg do Pacman

Exemplo: 

```lua
output/
├── pacman-contribution-graph.svg
└── pacman-contribution-graph-dark.svg
```


## Passo 5 – Adicionar no README do perfil
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
