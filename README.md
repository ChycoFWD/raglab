# RAGlab
Implementa um ambiente de desenvolvimento local utilizando Ollama, um framework leve e extensível para construção e execução de modelos de linguagem.

## Requisitos

## Instalação das ferramentas necessárias

### Linux

## Configuração do Traefik
Configure o Traefik para usar o DNS Challenge da Cloudflare para SSL.

### Credenciais necessárias:
- `CF_API_EMAIL`: Email da conta Cloudflare
- `CF_API_KEY`: Chave da API da Cloudflare
- `LETSENCRYPT_EMAIL`: Email para Let’s Encrypt

## Configuração do Cloudflare Tunnel
Adicione o serviço `cloudflared` para criar um túnel seguro para seus serviços.

### Credenciais necessárias:
- `CLOUDFLARE_TUNNEL_TOKEN`: Token do túnel da Cloudflare

##  Configuração do Ollama
Configure o serviço Ollama para gerenciar os modelos de IA.

Você precisará de credenciais para acessar e gerenciar os modelos de IA.

### Portas de C
comunicação:
- 11434: Porta padrão para o serviço Ollama

## Configuração do OpenWebUI
Configure o OpenWebUI para interagir com o Ollama.

### Credenciais necessárias:
- Variáveis de ambiente para configurar a URL base da API do Ollama.

### Portas de comunicação:
- 8080: Porta padrão para o serviço OpenWebUI

## Exemplo de arquivo .env

```dotenv
# Traefik
LETSENCRYPT_EMAIL=your-email@example.com
CF_API_EMAIL=your-email@example.com
CF_API_KEY=your-cloudflare-api-key

# Cloudflare Tunnel
CLOUDFLARE_TUNNEL_TOKEN=your-cloudflare-tunnel-token

# Ollama
OLLAMA_API_BASE_URL=http://ollama:11434/api
```

## Iniciar os serviços
Inicie os serviços com o Docker Compose:

```sh
docker-compose up -d
```

## Referências
- [Documentação do Traefik](https://doc.traefik.io/traefik/user-guides/docker-compose/acme-dns/)
- [Documentação do Cloudflare Tunnel](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/)
- [Documentação do Ollama](https://github.com/ollama/ollama)
- [Documentação do OpenWebUI](https://openwebui.com/docs)
