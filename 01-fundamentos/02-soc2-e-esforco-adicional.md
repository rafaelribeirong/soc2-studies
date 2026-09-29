# Por que o SOC 2 pode exigir esforço adicional em relação à ISO/IEC 27001?

A ISO/IEC 27001 e o SOC 2 possuem objetivos diferentes.

A **ISO/IEC 27001** é uma norma de sistema de gestão. Ela avalia se a organização estabeleceu, implementou, mantém e melhora continuamente um Sistema de Gestão de Segurança da Informação (SGSI).

O **SOC 2** é um trabalho de atestação realizado sobre os controles de uma organização de serviços, considerando critérios relacionados a segurança, disponibilidade, integridade de processamento, confidencialidade e privacidade.

Por isso, uma organização que já possui um SGSI maduro pode reaproveitar grande parte de seus processos e controles, mas ainda assim pode precisar de esforço adicional para se preparar para um SOC 2.

O principal motivo não é a necessidade de criar mais políticas. O esforço adicional normalmente está em **definir o sistema avaliado com maior precisão, relacionar controles aos Trust Services Criteria e produzir evidências suficientes para demonstrar a operação dos controles**.

---

## 1. O escopo precisa estar fortemente ligado ao serviço

Em um SOC 2, é necessário definir claramente qual sistema e quais serviços serão avaliados.

Isso normalmente envolve identificar:

- serviços prestados;
- aplicações;
- infraestrutura;
- pessoas;
- processos;
- dados;
- locais;
- fornecedores;
- subservice organizations;
- limites do sistema.

O objetivo é deixar claro para o usuário do relatório **o que está dentro e o que está fora do exame**.

Uma empresa que já possui ISO/IEC 27001 pode ter um escopo de SGSI bem definido, mas ainda precisar detalhar melhor o sistema utilizado para fornecer determinado serviço aos clientes.

## 2. Service Commitments e System Requirements precisam ser identificados

O SOC 2 considera os compromissos assumidos pela organização e os requisitos necessários para operar o sistema.

Exemplos:

- compromissos contratuais;
- SLAs;
- disponibilidade prometida;
- requisitos de segurança;
- confidencialidade;
- requisitos regulatórios;
- requisitos técnicos e operacionais.

Exemplo prático:

**Compromisso com o cliente:** disponibilidade de 99,9%

**Risco:** indisponibilidade acima do nível acordado.

**Controles possíveis:** monitoramento, redundância, gestão de capacidade, backup e disaster recovery.

**Evidências possíveis:** relatórios de uptime, alertas, tickets, testes de DR e registros de incidentes.

O controle não é analisado isoladamente. Ele deve contribuir para que os compromissos e requisitos do sistema sejam atingidos.

## 3. Os controles precisam estar claramente relacionados aos critérios

Os Trust Services Criteria não funcionam como uma lista única e obrigatória de tecnologias ou controles.

A organização precisa:

1. definir seus objetivos;
2. identificar os riscos que podem impedir esses objetivos;
3. selecionar ou desenvolver controles;
4. demonstrar como esses controles atendem aos critérios aplicáveis.

A lógica de trabalho passa a ser:

**Trust Services Criterion → Objetivo → Risco → Controle → Responsável → Frequência → Evidência**

Uma organização pode já possuir muitos desses controles por causa da ISO/IEC 27001, mas será necessário mapear e documentar essa relação.

## 4. A evidência operacional ganha grande importância

Uma política demonstra que uma regra existe.

Ela não demonstra, sozinha, que a regra foi executada.

Exemplo de controle:

> Todo novo acesso a sistemas críticos deve possuir aprovação prévia.

Uma política de controle de acesso ajuda a demonstrar o desenho do processo.

Para avaliar a execução do controle, porém, é necessário verificar ocorrências reais, como:

- solicitação de acesso;
- aprovação;
- data da aprovação;
- usuário;
- perfil concedido;
- data da concessão.

Isso exige evidências como tickets, logs, relatórios, registros de aprovação, configurações e histórico de alterações.

## 5. No Type II, é necessário demonstrar operação durante um período

Esta é uma das principais fontes de esforço adicional.

No **SOC 2 Type I**, a avaliação ocorre em uma determinada data e considera, entre outros elementos, o desenho dos controles.

No **SOC 2 Type II**, também é avaliada a efetividade operacional dos controles durante um período.

Isso faz surgir conceitos muito importantes:

- população;
- frequência do controle;
- amostra;
- período de observação;
- exceção;
- resultado do teste;
- operating effectiveness.

Exemplo:

> Os acessos de colaboradores desligados devem ser removidos.

Durante o período analisado ocorreram 20 desligamentos. Esses 20 desligamentos formam a população relevante para o controle.

A preparação para auditoria precisa permitir demonstrar:

- quem foi desligado;
- quando ocorreu o desligamento;
- quais acessos existiam;
- quando os acessos foram removidos;
- quem executou a remoção;
- se houve exceções.

A pergunta deixa de ser somente:

> Existe um processo de offboarding?

E passa a incluir:

> Conseguimos provar que o processo funcionou de forma consistente durante o período?

## 6. Mudanças, acessos e outros controles geram populações auditáveis

Considere uma empresa de software.

> Toda mudança em produção deve passar por revisão e aprovação.

Durante seis meses ocorreram 350 mudanças. Essas mudanças podem formar a população utilizada no teste do controle.

Para cada ocorrência, podem existir evidências como:

- Pull Request;
- autor;
- reviewer;
- aprovação;
- resultado dos testes;
- pipeline CI/CD;
- deployment;
- data da mudança.

Portanto, ferramentas como GitHub, GitLab, Jira, Entra ID, SIEM, sistemas de RH e plataformas de tickets deixam de ser somente ferramentas operacionais e passam a ser também importantes fontes de evidência.

## 7. Ter ISO/IEC 27001 reduz significativamente o esforço de preparação

Uma organização com ISO/IEC 27001 madura provavelmente já possui elementos importantes, como:

- gestão de riscos;
- governança;
- políticas de segurança;
- gestão de acessos;
- offboarding;
- gestão de incidentes;
- backups;
- gestão de fornecedores;
- vulnerabilidades;
- testes de segurança;
- gestão de mudanças;
- auditoria interna;
- treinamento;
- criptografia;
- monitoramento e logs.

Esses elementos não precisam necessariamente ser recriados.

O trabalho normalmente será:

**Controles existentes → Mapeamento para os TSC → Avaliação do desenho → Avaliação da implementação → Análise das evidências → Identificação dos gaps → Adequação para o SOC 2**

## 8. Onde costuma estar a demanda adicional

Em uma organização já madura em ISO/IEC 27001, o esforço adicional tende a se concentrar em:

- definição detalhada do escopo do sistema;
- System Description;
- Service Commitments;
- System Requirements;
- seleção dos Trust Services Criteria aplicáveis;
- mapeamento dos controles aos critérios;
- identificação de subservice organizations;
- definição de CUECs e CSOCs quando aplicável;
- matriz de controles SOC 2;
- identificação das populações dos controles;
- organização de evidências históricas;
- testes de operating effectiveness;
- tratamento de exceções;
- preparação para os testes do service auditor.

Por isso, o SOC 2 não deve ser tratado como uma simples extensão da ISO/IEC 27001.

A existência de um SGSI maduro reduz muito o esforço de preparação, mas o SOC 2 acrescenta uma camada importante de **escopo do serviço, estrutura de reporte, rastreabilidade dos controles e demonstração da operação desses controles**.

## Resumo

Uma forma simples de diferenciar:

**ISO/IEC 27001:** sistema de gestão → riscos → controles → implementação → evidências.

**SOC 2, especialmente Type II:** critério → risco → controle → responsável → frequência → evidência → população → amostra/teste → exceções → conclusão sobre efetividade.

A pergunta central para preparação de um SOC 2 Type II é:

> **O controle apenas existe ou conseguimos provar que funcionou de forma consistente durante o período examinado?**

## Referências de estudo

- AICPA — *2017 Trust Services Criteria for Security, Availability, Processing Integrity, Confidentiality, and Privacy (with Revised Points of Focus — 2022)*
- AICPA — *Information for Service Organization Management in a SOC 2 Engagement*
- COSO — *Internal Control — Integrated Framework*

> Este material é uma síntese de estudo. Exemplos de controles, ferramentas e evidências apresentados aqui não devem ser interpretados como requisitos prescritivos da AICPA.
