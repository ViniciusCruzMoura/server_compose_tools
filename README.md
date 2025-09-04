# Docker Compose Tools for Servers

Arquivos de Docker Compose para implantar aplicações essenciais de servidor — como Jenkins, PostgreSQL e Redis — prontas para uso ou adaptação.

Este repositório reúne uma coleção de arquivos Docker Compose para facilitar o deploy e a orquestração de serviços de infraestrutura e desenvolvimento em contêineres. Cada arquivo representa uma stack ou serviço específico, configurável conforme suas necessidades.

**Propósito:** fornecer exemplos prontos e reutilizáveis para acelerar a criação de ambientes locais, de teste ou produção leve.

## Serviços incluídos

- **autoheal.yml** — container que monitora e reinicia automaticamente contêineres com falha.  
- **dockovpn.yml** — configuração para rodar VPN dentro de contêineres.
- **dozzle-agent.yml** — agente Dozzle para streaming de logs.
- **dozzle-manager.yml** — serviço gerenciador Dozzle (visualização de logs centralizada).
- **gitea.yml** — serviço Gitea (Git self-hosted leve).
- **gitlab.yml** — GitLab (instância self-hosted, maior e com mais recursos).
- **jenkins-agent.yml** — agente Jenkins (para execução de jobs).
- **jenkins-manager.yml** — servidor Jenkins (master/controller).
- **nginx-proxy-manager.yml** — Nginx Proxy Manager para gerenciamento de proxies reversos e certificados.
- **oracle.yml** — container com banco de dados Oracle (image/uso sujeito a licenças).
- **portainer-agent.yml** — agente Portainer (para gestão de hosts remotos).
- **portainer.yml** — Portainer (interface de gestão de contêineres).
- **postgres.yml** — PostgreSQL (banco de dados relacional).
- **privatebin.yml** — PrivateBin (pastebin minimal e privado).
- **redis.yml** — Redis (store em memória / cache).

## Como usar

1. Clone o repositório:
```bash
git clone https://github.com/ViniciusCruzMoura/server_compose_tools.git
cd server_compose_tools
```

2. Escolha o arquivo compose do serviço que deseja rodar (ex.: `postgres.yml`) e inicie:
```bash
docker compose -f postgres.yml up -d
```

3. Para parar e remover os containers:
```bash
docker compose -f postgres.yml down
```

4. Personalize variáveis de ambiente, volumes e portas dentro de cada arquivo YAML antes do deploy para ajustar ao seu ambiente e requisitos de segurança.
