# Ambiente de Desenvolvimento com Dev Containers

## Iniciando o Ambiente

1. Pressione `Ctrl + Shift + P` para abrir a paleta de comandos.
2. Escolha a opção **Dev Containers**.
3. Selecione **"Create Dev Container from a predefined template"** ou **"Create a Dev Container"**.
4. Escolha a imagem base desejada.

---

## Personalização

Customize os seguintes arquivos conforme necessário:

- `devcontainer.json`
- `docker-compose.yaml`
- `Dockerfile`

### Exemplo de customização no `devcontainer.json`:

```json
"customizations": {
  "vscode": {
    "extensions": [
      "ms-azuretools.vscode-docker"
    ]
  }
}
