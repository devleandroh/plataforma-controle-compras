# Decisões de arquitetura

Este documento registra decisões de alto nível para contextualizar o desenho da solução. Não substitui documentação operacional.

## Separação entre origem e consumo

**Decisão:** manter o ERP como sistema transacional e disponibilizar dados analíticos por uma camada de serving.

**Motivo:** reduzir consultas analíticas sobre a origem e permitir que a aplicação consuma estruturas preparadas para leitura.

## Arquitetura medalhão

**Decisão:** organizar a engenharia de dados em Bronze, Silver e Gold.

**Motivo:** separar preservação da origem, padronização e modelagem orientada ao consumo. Isso facilita rastreabilidade e manutenção das transformações.

## Banco de consumo

**Decisão:** utilizar PostgreSQL gerenciado pelo Supabase como camada de serving da aplicação.

**Motivo:** oferecer uma interface relacional de consulta para a aplicação, com recursos de autenticação e controle de acesso disponíveis na plataforma.

## Backend e interface

**Decisão:** manter responsabilidades de aplicação no backend Flask/Jinja e componentes de interface em Next.js.

**Motivo:** separar rotas e renderização do servidor da experiência de interface. A integração entre os dois lados deve ser explícita e documentada.

## Portfólio independente

**Decisão:** publicar uma edição documental e demonstrativa, em vez de espelhar o repositório operacional.

**Motivo:** preservar confidencialidade e evitar que histórico, configurações ou dados da empresa sejam publicados acidentalmente.

## Pontos que exigem validação em uma implantação

- Contrato exato de publicação e estratégia de rollback.
- Política de retenção e reprocessamento das camadas.
- Regras oficiais para cancelamentos, exclusões lógicas e recebimentos parciais.
- Matriz de autorização e segregação de acesso.
- Metas de disponibilidade, latência e recuperação.