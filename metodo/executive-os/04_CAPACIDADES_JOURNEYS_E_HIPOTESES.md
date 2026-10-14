# Executive OS | Capacidades, journeys e hipóteses

**Status:** registro canônico inicial  
**Data:** 30/08/2026  
**Função:** impedir que mecanismos, referências e ideias sejam confundidos com arquitetura obrigatória ou capacidade validada.

## 1. Regra de classificação

Para cada item, registrar:

- natureza;
- problema que pretende resolver;
- origem;
- evidência;
- escopo atual;
- baseline mais simples;
- próximo teste;
- condição de promoção ou descarte.

## 2. Responsabilidades canônicas do produto

São responsabilidades arquiteturais, não componentes físicos:

- Cognitive Interface;
- Capture & Ingestion;
- contextualização e indexação;
- Memory & State;
- Retrieval & Context Assembly;
- Evaluation & Attention;
- Agentic Journeys;
- Action & Autonomy;
- Feedback, Correction & Observability.

## 3. Journeys candidatas

| Journey | Natureza | Evidência atual | Observação |
|---|---|---|---|
| Registrar ou atualizar estado | Padrão reutilizável candidato | Validado no LAB do projeto piloto; operação semelhante no Chuck-OS | Generalização entre plataformas ainda precisa de teste |
| Consultar estado vigente | Padrão reutilizável candidato | Validado no LAB do projeto piloto e na operação Chuck-OS | Contrato é reutilizável; mecanismo varia |
| Attention on-demand | Journey candidata | Arquitetura definida; qualidade não validada | Deve preceder automação |
| Meeting Follow-up | Journey candidata | Hipótese | Não validada no projeto piloto |
| TODAY / Daily Digest | Journey candidata | Hipótese | Deve ser seletiva, não lista integral |
| Meeting Prep | Journey candidata | Hipótese | Não validada |
| Weekly Review | Journey candidata | Hipótese | Exige memória longitudinal suficiente |
| INSIGHTS | Journey candidata | Hipótese | Risco elevado de padrões fabricados sem corpus suficiente |
| Commitments / Loose Ends | Journey candidata | Inferência | Pode compor Attention ou outras journeys |
| Risk / Opportunity monitoring | Journey candidata | Inferência | Necessita fonte, condição e autorização claras |

## 4. Mecanismos opcionais de retrieval e memória

| Mecanismo | Natureza | Evidência | Regra atual |
|---|---|---|---|
| Structured retrieval | Mecanismo | Validado no projeto piloto | Preferir para estado determinístico |
| Semantic/vector retrieval | Mecanismo opcional | Sem necessidade demonstrada no produto comum | Usar quando ganho de recall for material |
| Hybrid retrieval | Mecanismo opcional | Inferência | Usar somente quando combinação alterar a resposta |
| Agentic retrieval | Mecanismo opcional | Hipótese | Exige investigação multietapas real |
| Context Graph / GraphRAG | Mecanismo opcional | Sem sinal suficiente | Relações não obrigam graph |
| Base longitudinal adicional | Mecanismo opcional | Sem sinal suficiente | Adicionar apenas após falha observada das fontes existentes |

## 5. Mecanismos opcionais de Attention

| Conceito | Origem | Natureza | Evidência atual |
|---|---|---|---|
| Candidate Generation | Referência Twitter/X e projeto piloto | Mecanismo candidato | Hipótese |
| Context Hydration | Referência Twitter/X e projeto piloto | Mecanismo candidato | Hipótese |
| Evaluation | Arquitetura do produto | Responsabilidade; mecanismo variável | Necessidade conceitual apoiada |
| Attention Gate | Projeto piloto | Mecanismo candidato | Hipótese |
| Change / Novelty | Projeto piloto | Sinal candidato | Hipótese |
| Decision Need | Projeto piloto | Sinal candidato | Hipótese |
| Stalling / Action Readiness | Projetos piloto | Sinal candidato | Hipótese |
| Trajectory / Timing | Projetos piloto | Capacidade candidata | Sem sinal suficiente |
| Contradiction / Fragile Assumption | Projeto piloto | Sinal candidato | Inferência |
| Attention Fatigue | Twitter/X e projeto piloto | Mecanismo candidato | Sem sinal suficiente |
| Score/threshold | Referências | Implementação opcional | Não obrigatório |
| Learned ranking | Referências | Implementação experimental | Sem sinal suficiente |
| Reinforcement learning | Referências | Implementação experimental | Sem sinal suficiente |

## 6. Specialized Capabilities

Capacidades especializadas devem permanecer no escopo onde nasceram até demonstrarem reutilização.

### Advisory Minds / Personal Advisory Council

- **Origem:** instância pessoal do autor.
- **Natureza:** hipótese experimental individual.
- **Função:** aplicar, com fidelidade a fontes documentadas, princípios e lentes de referências pessoais a situações reais.
- **Exemplos iniciais:** referências pessoais a definir por cada instância.
- **Evidência:** hipótese; não implementada nem validada.
- **Escopo:** Chuck-OS.
- **Regra:** não altera outras instâncias, não é princípio Chuck-OS e não é herdada automaticamente por outras instâncias.

### Capacidade analítica por domínio

Exemplos como Investment Analyst podem existir quando o domínio justificar fontes, ferramentas e critérios próprios. Permanecem deltas organizacionais ou individuais até evidência de reutilização.

## 7. Estratégias de execução opcionais

- prompt;
- skill;
- Topic;
- Flow;
- automação agendada;
- evento ou webhook;
- monitoramento por condição;
- subagent;
- connected agent;
- aplicação própria.

Nenhuma é requisito arquitetural. Agentic não significa múltiplos agentes.

## 8. Referências intelectuais e técnicas

Referências podem ampliar repertório e gerar hipóteses, mas não entram automaticamente no runtime.

Fontes observadas nesta consolidação:

- algoritmo de recomendação do Twitter/X;
- modelos de recomendação e trajetória observados em projetos piloto;
- lentes Chuck-OS de decisão e sistemas;
- referências pessoais do Chuck-OS.

Conceitos históricos sem fonte canônica recuperada devem permanecer como histórico ou “a confirmar”, não como base formal.

## 9. Critério de permanência

Uma capability merece permanecer quando melhora materialmente uma decisão, seleção, ação ou experiência em relação à alternativa mais simples e mantém qualidade, latência, custo e manutenção aceitáveis.

Se apenas acrescentar arquitetura, vocabulário ou aparência de sofisticação, deve ser adiada ou removida.
