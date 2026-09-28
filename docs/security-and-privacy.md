# Segurança e limites de publicação

Este repositório é público e foi separado do ambiente corporativo. A regra de publicação é simples: documentar a solução sem transportar dados, segredos ou detalhes que permitam acesso ao ambiente real.

## Permitido nesta edição

- Nomes de tabelas do Protheus usados como referência técnica.
- Descrições genéricas do processo e da arquitetura.
- Diagramas conceituais sem endereços internos ou identificadores reais.
- Capturas sanitizadas ou mockups com conteúdo fictício.
- Exemplos sintéticos que não possam ser associados a pessoas, fornecedores ou operações reais.

## Não publicar

- Registros de solicitações, pedidos, notas fiscais ou fornecedores.
- Valores, volumes, datas ou indicadores extraídos da operação real.
- Dados pessoais ou identificadores de usuários.
- Credenciais, tokens, chaves, arquivos `.env`, certificados ou strings de conexão.
- IPs, hostnames, URLs privadas, nomes de recursos internos ou topologia sensível.
- Logs, dumps, exports, arquivos parquet ou planilhas do ambiente corporativo.
- Código proprietário ou configurações que revelem controles internos.

## Revisão antes de cada publicação

- [ ] Conferir arquivos adicionados e modificados.
- [ ] Procurar por tokens, senhas, URLs privadas, e-mails e identificadores internos.
- [ ] Confirmar que imagens são mockups ou foram devidamente sanitizadas.
- [ ] Confirmar que exemplos e números são sintéticos.
- [ ] Revisar histórico Git: remover um arquivo em um commit posterior não apaga seu conteúdo dos commits anteriores.
- [ ] Verificar que nenhum segredo foi incluído em arquivos ocultos ou metadados.

## Limite importante

Uma cópia de um repositório privado ou operacional não se torna segura apenas por remover dados de arquivos visíveis. Histórico Git, branches, tags, artefatos e arquivos ignorados também precisam ser considerados. Esta edição pública deve ser construída como um projeto independente, com conteúdo selecionado para portfólio.