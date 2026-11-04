# Fisco

Fisco é um plugin complementar para servidores de Minecraft focado em gestão financeira avançada, voltado para servidores que já utilizam um sistema de economia principal. Ele foi pensado para expandir a funcionalidade do núcleo econômico com recursos como transações, empresas, impostos, controle de balanço e organização financeira de jogadores e grupos.

Com uma abordagem moderna e prática, o Fisco permite criar um ambiente econômico mais realista e profissional, ideal para servidores de survival, roleplay, cidade, factions e redes de alta demanda.

## Visão Geral

O objetivo do projeto é fornecer uma camada de gestão econômica que vai além do simples saldo de moedas. O plugin permite:

- transferências entre jogadores;
- gerenciamento de empresas e grupos econômicos;
- controle de impostos e taxas;
- registro de movimentações financeiras;
- painel administrativo para monitoramento do mercado;
- integração com plugins populares de economia e permissões.

## Funcionalidades

### Sistema de transações
- Pagamentos diretos entre jogadores;
- Histórico de transações por conta;
- Suporte a valores fixos e porcentuais;
- Alertas e logs de movimentação;
- Validação de saldo antes da execução.

### Empresas
- Criação de empresas e organizações;
- Gestão de membros e cargos;
- Depósitos e saques da conta da empresa;
- Sistema de lucros e despesas internas;
- Permissões específicas por papel dentro da empresa.

### Impostos
- Taxas sobre transações;
- Impostos por grupo, guilda ou empresa;
- Configuração por tipo de atividade econômica;
- Coleta automática ou manual;
- Registro de pagamentos e pendências.

### Administração e monitoramento
- Visualização do saldo geral do servidor;
- Relatórios financeiros por jogador, empresa ou categoria;
- Logs detalhados para auditoria;
- Alertas para movimentações suspeitas;
- Compatibilidade com comandos administrativos.

### Compatibilidade
- Integração com plugins de economia baseados em Vault;
- Compatível com servidores que utilizam sistemas de permissões e grupos;
- Estrutura pensada para fácil extensão e customização.

## Requisitos

Antes de instalar o Fisco, certifique-se de que seu servidor possui:

- Minecraft Java Edition
- Servidor compatível com Spigot, Paper, Purpur ou forks similares
- Plugin de economia principal instalado e funcionando
- Vault (ou equivalente para integração do sistema econômico)
- Permissão e configuração adequadas do ambiente do servidor

## Instalação

1. Baixe o arquivo do plugin em formato .jar;
2. Coloque o arquivo na pasta plugins do seu servidor;
3. Reinicie o servidor ou carregue o plugin com o gerenciador correspondente;
4. Verifique se a integração com o sistema de economia principal está ativa;
5. Ajuste o arquivo de configuração conforme a sua estrutura de servidor.

## Configuração

O plugin deve possuir um arquivo de configuração principal para definir:

- taxa padrão de imposto;
- configuração de transações;
- permissões do sistema;
- limites por tipo de empresa;
- nome da conta do sistema financeiro;
- ativação de logs e auditoria.

Exemplo de estrutura conceptual:

```yaml
config:
  imposto_padrao: 5.0
  taxa_transferencia: 2.0
  logs_ativados: true
  empresas_ativas: true
  limites:
    empresas: 50
    membros_por_empresa: 20
```

## Comandos principais

Os comandos podem variar conforme a versão final do plugin, mas a estrutura geral pode incluir:

```text
/fisco saldo
/fisco pagar <jogador> <valor>
/fisco historico
/empresa criar <nome>
/empresa info
/empresa depositar <valor>
/empresa sacar <valor>
/imposto pagar
/imposto status
/admin fisco reload
```

## Permissões

A estrutura de permissões pode incluir:

```text
fisco.use
fisco.admin
fisco.transfer
fisco.empresa.create
fisco.empresa.manage
fisco.imposto.manage
fisco.logs.view
```

## Arquitetura do projeto

O projeto foi pensado para ser modular e fácil de manter. A estrutura pode seguir uma organização como:

```text
Fisco/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/fisco/
│   │   │       ├── FiscoPlugin.java
│   │   │       ├── commands/
│   │   │       ├── managers/
│   │   │       ├── models/
│   │   │       ├── services/
│   │   │       └── utils/
│   │   └── resources/
│   │       ├── config.yml
│   │       └── plugin.yml
├── pom.xml
├── README.md
└── LICENSE
```

## Roadmap

- implementação do sistema de saldo e transações;
- criação das entidades de empresas;
- módulo de imposto e auditoria;
- painel administrativo;
- suporte a economia por múltiplos provedores;
- melhorias de performance e estabilidade;
- expansão com eventos e integração de mercado.

## Contribuição

Contribuições são bem-vindas. Se você quiser melhorar o projeto, sugerir novas funcionalidades ou reportar bugs, abra uma issue ou envie um pull request com uma descrição clara das alterações.

## Licença

Este projeto está em desenvolvimento e pode ser distribuído sob a licença escolhida pelo mantenedor do projeto. Ajuste este campo conforme a licença final adotada.

## Observação

Este README foi estruturado para apresentar o plugin como uma solução de economia empresarial para servidores Minecraft, com foco em gestão financeira, empresas e impostos. Se quiser, posso continuar e criar também:

- uma versão mais técnica para desenvolvedores;
- uma versão mais comercial para publicação no GitHub;
- a estrutura completa de arquivos do projeto em Java para Spigot/Paper.
