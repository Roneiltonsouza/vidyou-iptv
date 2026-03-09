# VidYou IPTV

Um player de IPTV de alta performance, focado em P2P e simplicidade. Este player foi desenvolvido para receber listas M3U via parâmetro de URL, permitindo uma sincronização rápida com o Painel VidYou.

## 📺 Funcionalidades
- **Suporte a M3U/M3U8:** Processamento eficiente de listas de canais, filmes e séries.
- **Categorização Automática:** Separa o conteúdo em Canais, Filmes e Séries.
- **Player Integrado:** Utiliza `hls.js` para uma reprodução fluida e com baixa latência.
- **Modo Galeria:** Permite carregar arquivos de vídeo locais diretamente do seu dispositivo.
- **Sincronização via URL:** Recebe listas externas automaticamente através de parâmetros de busca.

## 🚀 Como Funciona
O player aguarda uma URL via parâmetro na query string (`?lista=URL_DA_LISTA`). 
- Exemplo de acesso: `https://seu-usuario.github.io/vidyou-iptv/?lista=URL_DA_LISTA_M3U`

## ⚙️ Tecnologias
- **HTML5/CSS3/JS:** Estrutura responsiva.
- **HLS.js:** Para suporte avançado de streaming HLS.
- **LocalStorage:** Persistência de dados para uso offline (após a primeira sincronização).

## ⚠️ Observação
Este projeto utiliza recursos de `fetch` para carregar listas externas. Certifique-se de que a lista M3U que você está carregando permita acesso via CORS ou utilize um proxy se encontrar bloqueios pelo navegador.
