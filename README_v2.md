# Visualizador de NFTs para BNB Smart Chain Testnet

Este projeto é um visualizador de NFTs que permite aos usuários conectar suas carteiras MetaMask e visualizar os NFTs que possuem na rede BNB Smart Chain Testnet. A aplicação utiliza a API Moralis v2 para buscar e exibir informações detalhadas sobre os NFTs.

## Índice

1. [Requisitos](#requisitos)
2. [Configuração](#configuração)
3. [Como Usar](#como-usar)
4. [Funcionalidades](#funcionalidades)
5. [Opções de Hospedagem](#opções-de-hospedagem)
6. [Solução de Problemas](#solução-de-problemas)
7. [Personalização](#personalização)

## Requisitos

Para usar esta aplicação, você precisará:

- Uma conta no [Moralis](https://moralis.io/)
- Uma chave de API do Moralis
- MetaMask instalado no navegador
- Acesso à rede BNB Smart Chain Testnet

## Configuração

### 1. Obter uma API Key do Moralis

1. Acesse [moralis.io](https://moralis.io/) e crie uma conta ou faça login
2. Vá para a seção "Web3 APIs" > "API Keys" no painel
3. Crie uma nova API key ou use uma existente
4. Copie a API key

### 2. Configurar a Aplicação

1. Abra o arquivo `app_v2.js`
2. Localize a linha:
   ```javascript
   const MORALIS_API_KEY = "INSIRA_SUA_API_KEY_AQUI";
   ```
3. Substitua `"INSIRA_SUA_API_KEY_AQUI"` pela sua API key do Moralis

### 3. Configurar a MetaMask para BNB Smart Chain Testnet

Se você ainda não configurou a MetaMask para a BNB Smart Chain Testnet:

1. Abra a extensão MetaMask
2. Clique no menu de redes (geralmente mostra "Ethereum Mainnet")
3. Clique em "Adicionar rede"
4. Preencha com os seguintes dados:
   - Nome da Rede: BNB Smart Chain Testnet
   - URL do RPC: https://data-seed-prebsc-1-s1.binance.org:8545/
   - ID da Cadeia: 97
   - Símbolo da Moeda: tBNB
   - URL do Explorador: https://testnet.bscscan.com

5. Obtenha tBNB de teste no [faucet oficial](https://testnet.bnbchain.org/faucet-smart)

## Como Usar

1. Abra o arquivo `index_v2.html` no seu navegador
2. Clique no botão "Conectar MetaMask"
3. Autorize a conexão na janela pop-up da MetaMask
4. Verifique se você está na rede BNB Smart Chain Testnet
   - Se não estiver, a aplicação oferecerá a opção de mudar automaticamente
5. Opcionalmente, insira o endereço do contrato NFT específico que deseja visualizar
6. Clique em "Buscar NFTs"
7. Os NFTs encontrados serão exibidos em cards
8. Clique em "Ver detalhes" em qualquer NFT para ver informações completas

## Funcionalidades

- **Conexão com MetaMask**: Conecte-se facilmente à sua carteira
- **Detecção de Rede**: Verifica automaticamente se você está na BNB Testnet
- **Busca de NFTs**: Visualize todos os NFTs da sua carteira ou de um contrato específico
- **Visualização Detalhada**: Veja imagens, metadados e atributos de cada NFT
- **Links Externos**: Acesse facilmente o NFT no BscScan e OpenSea Testnet
- **Visualização de Metadados**: Examine os metadados completos em formato JSON
- **Interface Responsiva**: Funciona em dispositivos móveis e desktop

## Opções de Hospedagem

Esta aplicação é estática (HTML, CSS e JavaScript puro) e pode ser hospedada em diversos serviços:

### GitHub Pages (Gratuito)

1. Crie um repositório no GitHub
2. Faça upload dos arquivos `index_v2.html` (renomeie para `index.html`) e `app_v2.js` (renomeie para `app.js`)
3. Vá para Settings > Pages e ative o GitHub Pages

### Netlify (Gratuito)

1. Crie uma conta em [netlify.com](https://www.netlify.com/)
2. Arraste e solte a pasta com os arquivos `index_v2.html` (renomeie para `index.html`) e `app_v2.js` (renomeie para `app.js`)
3. Ou conecte ao seu repositório GitHub

### Vercel (Gratuito)

1. Crie uma conta em [vercel.com](https://vercel.com/)
2. Importe seu repositório GitHub ou faça upload dos arquivos
3. A implantação será automática

### Hospedagem Local

Para testar localmente, basta abrir o arquivo `index_v2.html` diretamente no navegador.

## Solução de Problemas

### NFTs Não Aparecem

- Verifique se você está conectado à rede BNB Smart Chain Testnet
- Confirme se a carteira conectada possui NFTs nessa rede
- Verifique se a API key do Moralis está correta e ativa
- Abra o console do navegador (F12) para ver mensagens de erro detalhadas

### Problemas de Conexão com MetaMask

- Certifique-se de que a MetaMask está instalada e desbloqueada
- Tente atualizar a página e reconectar
- Verifique se você tem permissões para conectar sites à MetaMask

### Imagens de NFT Não Carregam

- Alguns NFTs podem usar gateways IPFS que estão offline
- A aplicação tenta converter URLs IPFS para gateways públicos, mas nem sempre funciona
- Verifique o console para ver a URL da imagem que está tentando carregar

### Erro "API key inválida"

- Verifique se você inseriu corretamente sua API key do Moralis no arquivo `app_v2.js`
- Confirme se sua API key está ativa no painel do Moralis
- Verifique se você não excedeu o limite de requisições gratuitas

## Personalização

### Alterar Cores e Estilo

Para personalizar a aparência:

1. Edite as variáveis CSS no início da tag `<style>` no arquivo `index_v2.html`
2. Ou adicione suas próprias regras CSS

### Adicionar Funcionalidades

Para desenvolvedores que desejam estender a aplicação:

- O código está bem comentado para facilitar modificações
- Você pode adicionar suporte a outras redes modificando as constantes no início do arquivo `app_v2.js`
- Para adicionar funcionalidades de mintagem ou transferência, você precisará implementar funções adicionais usando Web3.js

---

Para suporte adicional ou dúvidas, entre em contato com o desenvolvedor ou consulte a documentação do Moralis em [docs.moralis.io](https://docs.moralis.io/)
