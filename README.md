# Ambiente de Desenvolvimento com Dev Containers

## Iniciando o Ambiente

1. Pressione `Ctrl + Shift + P` para abrir a paleta de comandos.
2. Escolha a opção **Dev Containers**.
3. Selecione **"Create Dev Container from a predefined template"** ou **"Create a Dev Container"**.
4. Escolha a imagem base desejada.

---

## Personalização de Arquivos

Edite os seguintes arquivos conforme necessário:

- `devcontainer.json`
- `docker-compose.yaml`
- `Dockerfile`

### Extensões do VS Code

No arquivo `devcontainer.json`, adicione:

```json
"customizations": {
  "vscode": {
    "extensions": [
      "ms-azuretools.vscode-docker"
    ]
  }
}
```

---

## Rebuild no Container

Após configurar os arquivos, reconstrua o container usando:

- Paleta de comandos: `Ctrl + Shift + P` → **Dev Containers: Rebuild Container**

---

## Comando de Inicialização

No `devcontainer.json`, adicione o comando de inicialização para instalar dependências automaticamente:

```json
"postCreateCommand": "npm install"
```

---

## Configuração de Debug

1. Pressione `Ctrl + Shift + P` e selecione **Debug: Add Configuration...**
2. Escolha **Node.js**.
3. O VS Code criará automaticamente o arquivo `launch.json`.

### Atalhos de Debug

- `F5`: Inicia o debug
- `F10`: Pula o breakpoint atual

---

## Ambiente de Produção (PRD)

1. Crie um novo `Dockerfile` para produção.
2. Crie um `docker-compose.yaml` específico para PRD.
3. Para rodar localmente em modo produção, execute:

```bash
docker compose up -d --build
```

---

## Observações

- Separe os arquivos de desenvolvimento e produção.
- Verifique as configurações antes de realizar o build final.
