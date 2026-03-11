# VidYou IPTV

O **VidYou IPTV** é uma solução profissional para gerenciamento e distribuição centralizada de listas de canais IPTV em tempo real. Este sistema elimina a necessidade de bancos de dados complexos, utilizando o GitHub como infraestrutura principal para envio e recepção de dados.

## 🚀 Como Funciona
O sistema é dividido em duas partes fundamentais que se comunicam via API do GitHub:

1.  **Painel de Controle:** Ferramenta administrativa onde você cola sua lista M3U e, com um clique, atualiza o arquivo `lista.txt` no seu repositório.
2.  **VidYou IPTV (App):** Interface do usuário que consome o arquivo `lista.txt` em tempo real. O aplicativo consulta automaticamente o servidor a cada 5 minutos, garantindo que todos os usuários recebam as atualizações sem precisar reinstalar nada.

## 🛠 Funcionalidades
- **Distribuição Instantânea:** Atualize a grade de canais para todos os dispositivos de uma só vez.
- **Sincronização Automática:** Atualização em background (a cada 300 segundos).
- **Sem Servidores Externos:** Tudo é hospedado e gerenciado pelo seu repositório GitHub.
- **Interface Otimizada:** Player HLS robusto com suporte a dispositivos móveis e desktop.

## ⚙️ Configuração Inicial

### 1. Preparação do GitHub
- Crie um repositório no seu GitHub.
- Crie um arquivo chamado `lista.txt` na raiz do repositório (com conteúdo inicial `#EXTM3U`).

### 2. Configuração do App (`index.html`)
- Localize a constante `URL_GITHUB` no código do app.
- Substitua pelo link **Raw** do seu arquivo `lista.txt` (ex: `https://raw.githubusercontent.com/USUARIO/REPO/main/lista.txt`).

### 3. Configuração do Painel (`painel.html`)
- Obtenha um **Personal Access Token** no GitHub (*Settings > Developer settings > Personal access tokens*). O token precisa de permissão de `repo`.
- Ao abrir o painel, insira o Token e o caminho do repositório (`usuario/nome-do-repositorio`) para habilitar o envio.

## 🔐 Requisitos
- Conta no GitHub.
- Repositório público ou privado (com Token configurado).
- GitHub Pages habilitado para hospedar o `index.html` e o `painel.html`.

---
*Projeto desenvolvido para alta performance em distribuição de mídia IPTV.*
