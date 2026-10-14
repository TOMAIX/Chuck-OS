# Executive OS | Decisões e evidências

**Status:** ledger canônico inicial  
**Data:** 30/08/2026  
**Função:** preservar origem, escopo, evidência, vigência e promoção dos aprendizados do produto.

## 1. Regra de governança

Decisão posterior substitui decisão anterior somente quando isso for explicitamente registrado.

Para cada aprendizado, distinguir:

- origem;
- natureza;
- evidência;
- ambiente;
- escopo;
- condição de validade;
- decisão vigente;
- documento afetado;
- próximo teste.

## 2. Escala de evidência

- **Validado:** demonstrado por teste, registro ou fonte adequada no escopo declarado.
- **Inferência:** conclusão plausível apoiada em sinais.
- **Hipótese:** precisa de teste.
- **Sem sinal:** não há base suficiente.

Decisão de produto vigente e capacidade tecnicamente validada são dimensões diferentes.

## 3. Decisões de produto vigentes

### 3.1 Produto independente do Core Chuck-OS

**Decisão:** Executive OS passa a governar a carcaça reutilizável de sistemas operacionais executivos e pessoais.  
**Origem:** consolidação de projetos piloto e decisão do autor em 29-30/08/2026.  
**Natureza:** decisão de governança.  
**Evidência:** validado como decisão explícita; valor comercial ainda não validado.  
**Escopo:** produto.

### 3.2 Capture first. Organize behind the scenes.

**Decisão:** princípio central de experiência.  
**Origem:** Chuck-OS e projetos piloto; aderente ao desenho do Chuck-OS.  
**Natureza:** princípio do produto.  
**Evidência:** inferência forte apoiada em múltiplos casos; impacto de adoção ainda precisa de medição.

### 3.3 Context → Attention → Action

**Decisão:** modelo de produto e UX.  
**Origem:** Chuck-OS e projetos piloto.  
**Natureza:** padrão de experiência.  
**Evidência:** validado como decisão documental; experiência completa ainda não validada em PROD.

### 3.4 Operational Memory e Longitudinal Memory

**Decisão:** responsabilidades distintas.  
**Origem:** Chuck-OS, projeto piloto e Chuck-OS.  
**Natureza:** responsabilidade arquitetural.  
**Evidência:** estado operacional validado em fluxos limitados; memória longitudinal ampla ainda parcialmente demonstrada.

### 3.5 Retrieval proporcional à pergunta e à fonte

**Decisão:** usar o caminho mais simples que preserve evidência suficiente.  
**Origem:** Chuck-OS e projeto piloto.  
**Natureza:** padrão arquitetural.  
**Evidência:** validado parcialmente no LAB do projeto piloto.

### 3.6 Evaluation & Attention

**Decisão:** selecionar o que merece atenção é responsabilidade do produto.  
**Natureza:** responsabilidade arquitetural.  
**Evidência:** necessidade inferida; engine, ranking e proatividade não validados.  
**Condição:** não confundir responsabilidade canônica com mecanismo específico.

### 3.7 Dashboard como superfície

**Decisão:** dashboard, lista ou Kanban não são o coração do produto.  
**Origem:** Chuck-OS/projeto piloto.  
**Natureza:** princípio de UX/arquitetura.  
**Evidência:** inferência apoiada.

### 3.8 Autonomia graduada

**Decisão:** observar, interpretar, recomendar, preparar, persistir e executar têm controles diferentes.  
**Origem:** Chuck-OS e a organização piloto.  
**Natureza:** responsabilidade arquitetural e guardrail.  
**Evidência:** validado como decisão; amplitude de execução não testada.

### 3.9 Complexidade somente com ganho observável

**Decisão:** graph, vector DB, score, subagent, learned ranking, app própria e automações não são requisitos.  
**Origem:** Chuck-OS/projeto piloto.  
**Natureza:** princípio de arquitetura e ferramental.  
**Evidência:** inferência forte apoiada em falhas e simplificações do LAB.

## 4. Evidência do projeto piloto

### 4.1 Validado no LAB do autor

- Copilot Studio como Cognitive Interface no fluxo testado;
- Topic e Agent Flow de registrar/atualizar;
- criação no Microsoft Lists;
- atualização do mesmo assunto sem duplicação no caminho testado;
- preservação de campos omitidos;
- geração automática de NB-ID;
- Excel como espelho no workflow testado;
- confirmação técnica;
- consulta estruturada ao Lists;
- retrieval isolado de Mail, Calendar, Teams, OneDrive/SharePoint e Loop;
- combinação limitada de estado estruturado e contexto Microsoft 365.

### 4.2 Validado parcialmente

- Teams como experiência final;
- Team privado e SharePoint compartilhado;
- quatro páginas Loop;
- Attention Board como superfície;
- backend corporativo compartilhado como arquitetura-alvo.

### 4.3 Não validado

- PROD da instância executiva;
- identidade, consentimento e permissões da pessoa titular;
- controle negativo contra dados de outra instância;
- backend definitivo;
- mobile e voz em PROD;
- adoção e valor cotidiano;
- Attention Engine;
- Attention Fatigue e Trajectory Intelligence;
- publicação automática;
- Meeting Follow-up;
- TODAY / Daily Digest;
- Meeting Prep;
- Weekly Review / INSIGHTS;
- execução agendada/background;
- ranking aprendido.

## 5. Aprendizados do projeto piloto candidatos ao produto

### Operação explícita superou gatilho genérico de arquivo

**Observação:** sincronização Excel → Lists por arquivo modificado gerou múltiplas execuções e duplicação.  
**Evidência:** validado como falha no caso testado.  
**Aprendizado:** gatilho genérico de arquivo não é confiável para aquele fluxo.  
**Escopo:** implementação projeto piloto.  
**Candidato geral:** preferir eventos semanticamente explícitos quando o gatilho físico não preserva identidade e atomicidade. Ainda requer evidência em outros ambientes.

### Update parcial deve preservar estado omitido

**Evidência:** validado no LAB do projeto piloto.  
**Natureza:** padrão reutilizável candidato.  
**Condição:** aplicável quando ausência de campo significa “não alterar”, não “limpar”.

### Estrutura interna não deve virar formulário

**Evidência:** fricção observada em Tool global; Topic intermediário resolveu o caminho testado.  
**Natureza:** evidência de suporte a Capture first.  
**Escopo promovido:** princípio do produto; mecanismo Topic permanece local.

### LAB não prova PROD

**Evidência:** compartilhamento anterior gerou fricção e dependência de permissões.  
**Natureza:** princípio de validação.  
**Escopo:** produto, sem obrigar a recriação manual usada no caso Microsoft.

## 6. Evidência do Chuck-OS

### Demonstrado na operação disponível

- separação física entre estado vigente, eventos e memória sem ação;
- registro mediante intenção explícita;
- criação, conclusão, cancelamento e reabertura;
- preservação de histórico;
- identificação de fonte e evidência;
- distinção entre estado operacional e memória contextual.

### Limite da evidência

A evidência operacional disponível é parcial: o corpus arquitetural completo do projeto Chuck-OS não estava presente nas fontes auditadas em 30/08/2026.

Consequência: o Chuck-OS fornece evidência operacional parcial, não valida ainda a arquitetura completa nem a replicação do produto em ChatGPT.

### Particularidades que permanecem no Chuck-OS

- áreas e dados pessoais da instância;
- categorias e convenções próprias;
- codinomes e semântica locais;
- ChatGPT Sites, atalhos e canais específicos;
- Advisory Minds / Personal Advisory Council;
- referências intelectuais pessoais.

## 7. Aprendizados não promovidos

Permanecem como hipóteses ou mecanismos opcionais:

- Context Graph e GraphRAG;
- vector database;
- Candidate Generation;
- Context Hydration;
- Attention Gate;
- Attention Fatigue;
- Trajectory Intelligence;
- scores e thresholds universais;
- learned ranking;
- reinforcement learning;
- subagents;
- aplicação própria;
- automações específicas.

## 8. Regra de promoção

**instância → organização:** somente se reutilizável entre pessoas daquele contexto.  
**organização → produto:** somente se útil além daquele cliente e sustentado por evidência.  
**produto → Chuck-OS Core:** somente se generalizável além da família Executive OS.

Toda promoção deve preservar origem, problema resolvido, evidência, escopo e condição de validade.

## 9. Próximos testes de produto

1. validar uma segunda instância com arquitetura física diferente;
2. comparar o contrato comum com os deltas reais;
3. validar Attention on-demand antes de automação;
4. medir adoção, carga cognitiva e continuidade;
5. validar identidade, privacidade e controle negativo em PROD;
6. testar journeys candidatas verticalmente;
7. registrar capacidades descartadas e por quê.

## Princípio final

O produto aprende com implementações sem transformar experiência local em verdade universal. Evidência acompanha sempre ambiente, escopo e condição de validade.
