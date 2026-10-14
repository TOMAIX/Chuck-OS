# DNA e arquitetura de sistemas Chuck-OS

**Status:** canônico  
**Função:** definir os princípios permanentes e as responsabilidades arquiteturais dos sistemas Chuck-OS.  
**Escopo:** vale para sistemas práticos de IA em geral e, quando aplicável, para o padrão Executive/Personal OS.

## 1. Tese

O Chuck-OS desenha sistemas para melhorar percepção, julgamento, decisão e execução no ambiente real do usuário.

O sistema deve assumir a complexidade que puder ser removida do usuário. A sofisticação pode crescer por baixo da interface, mas só entra quando produz ganho observável.

**Princípios permanentes:**

- começar por comportamento, rotina, ambiente e resultado observável;
- não começar pela ferramenta;
- preservar fonte oficial, estado, integridade e possibilidade de correção;
- separar evidência de inferência;
- reduzir transporte e organização manual feitos pelo usuário;
- aumentar controle e verificação conforme o custo do erro;
- preferir a menor arquitetura que entregue valor sustentável;
- tratar componentes, fornecedores e implementações como substituíveis quando possível.

## 2. Unidade de desenho

Desenhe a partir de comportamentos observáveis:

- o que o usuário precisa capturar, encontrar, lembrar, decidir, produzir ou executar;
- quando e onde isso acontece;
- qual fricção existe hoje;
- qual decisão ou ação precisa melhorar;
- qual resultado deve mudar;
- como saberemos que mudou.

Preferência de interface, dispositivo ou ferramenta pode ser requisito legítimo de adoção. Registre-a como decisão do caso, não como princípio universal.

## 3. Regra de UX

### Capture first. Organize behind the scenes.

O usuário não deve administrar a organização necessária para que o sistema funcione.

Ele deve poder, conforme o caso:

- falar;
- escrever;
- anotar;
- perguntar;
- consultar;
- corrigir.

Sem precisar escolher continuamente pasta, tag, categoria, skill, ferramenta, banco ou destino técnico.

Isso não elimina estrutura. A estrutura continua existindo quando melhora confiabilidade, recuperação ou ação; apenas deixa de ser trabalho rotineiro do usuário.

O sistema também pode ingerir fontes autorizadas automaticamente. Captura não significa apenas entrada manual.

### 3.1 Padrão de produto para Executive/Personal OS - Context → Attention → Action

Executive/Personal OS Chuck-OS organizam sua experiência principal em três superfícies cognitivas:

- **Context - entender:** recuperar, relacionar e sintetizar o que ajuda o usuário a compreender uma situação, sua trajetória e suas relações;
- **Attention - priorizar:** selecionar o que merece atenção agora, considerando relevância, mudança, risco, dependências, timing e contexto;
- **Action - agir:** transformar entendimento e decisão em acompanhamento, preparação ou execução, respeitando estado, autorização, reversibilidade e custo do erro.

**Context, Attention e Action são pilares de produto e UX, não componentes técnicos.**

Podem se manifestar em dashboard, interface conversacional, briefing, navegação ou outras superfícies adequadas ao ambiente. Em dashboards de Executive/Personal OS, constituem a organização principal de referência.

A arquitetura que os sustenta continua composta por responsabilidades como:

- Cognitive Interface;
- Capture & Ingestion;
- Context Engine & Automated Indexing;
- Memory & State;
- Retrieval & Context Assembly;
- Evaluation & Attention;
- Agentic Journeys;
- Action & Autonomy;
- Feedback, Correction & Observability.

Uma mesma Agentic Journey pode alimentar uma ou mais dessas superfícies.

Esse padrão organiza a experiência do produto, mas não define:

- três agentes;
- três subagents;
- três bancos;
- três pipelines;
- três componentes técnicos obrigatórios.

As journeys específicas, ferramentas, bancos, agentes e mecanismos de execução podem variar por implementação.

## 4. Loop canônico

Um Executive/Personal OS Chuck-OS deve ser capaz, quando o caso justificar, de fechar o seguinte ciclo:

**capturar → contextualizar → lembrar → perceber → decidir → agir → acompanhar → aprender**

O loop descreve capacidades, não componentes físicos. Uma implementação pode concentrar várias responsabilidades na mesma ferramenta.

## 5. Responsabilidades arquiteturais

### 5.1 Cognitive Interface

Onde o usuário conversa, pergunta, captura, recebe contexto, recomendações e alertas.

A interface não é necessariamente fonte oficial nem local de estado.

### 5.2 Capture & Ingestion

Recebe entradas do usuário e fontes autorizadas, como:

- conversa;
- e-mail;
- calendário;
- reuniões;
- documentos;
- sistemas corporativos;
- eventos e registros.

Declare origem, identidade, timestamp e nível de confiança quando isso afetar a interpretação.

### 5.3 Context Engine & Automated Indexing

Interpreta e organiza o acumulado sem exigir administração manual contínua.

Pode executar:

- extração de pessoas, empresas, projetos, assuntos e outras entidades;
- resolução de aliases;
- continuidade de assunto;
- deduplicação;
- identificação de mudança de estado;
- datas, prazos e dependências;
- relações;
- compromissos;
- decisões;
- riscos;
- distinção entre fato, inferência e algo a confirmar.

Não invente relações para enriquecer uma representação. Quando a identidade ou relação for incerta, preserve a incerteza.

### 5.4 Memory & State

Separe logicamente pelo menos duas funções.

#### Operational Memory / State

Para informação cujo estado atual precisa ser determinístico ou consultável sem reconstrução probabilística:

- pendências;
- compromissos;
- status;
- prazo;
- responsável;
- próxima ação;
- decisões vigentes;
- riscos acompanhados;
- itens concluídos, reabertos ou cancelados.

#### Longitudinal / Contextual Memory

Para trajetória e contexto:

- reuniões;
- conversas;
- documentos;
- acontecimentos;
- histórico;
- evolução de assuntos;
- pessoas e relações;
- decisões anteriores;
- evidências e versões.

A separação é lógica, não necessariamente física. As duas podem viver no mesmo sistema ou em sistemas diferentes.

### 5.5 Retrieval & Context Assembly

Escolha o mecanismo pela pergunta e pela fonte.

**Direct retrieval:** uma fonte oficial resolve.  
**Structured retrieval:** estado, metadata ou consulta determinística resolvem.  
**Lexical search:** termos, nomes, IDs ou frases exatas importam.  
**Semantic/vector search:** similaridade e linguagem flexível melhoram recall.  
**Hybrid retrieval:** combina estrutura, lexical e semântica.  
**Agentic retrieval:** a pergunta exige decomposição, múltiplas fontes ou buscas sequenciais.  
**Graph-based retrieval:** relações entre entidades melhoram materialmente a resposta.

Princípio:

**Semântica traz flexibilidade. Estrutura e indexação trazem confiabilidade.**

Não use arquitetura agentic ou graph quando uma consulta direta resolve melhor.

### 5.6 Evaluation & Attention

Trabalha sobre memória, estado e contexto para decidir o que merece atenção.

**Importância e merecimento de atenção agora não são equivalentes.** Algo pode permanecer importante sem justificar nova interrupção naquele momento.

Pode produzir sinais como:

- relevância;
- mudança ou novidade;
- compromisso;
- loose end;
- risco;
- padrão temporal;
- relação ou correlação;
- confiança.

Um evaluator pode ser regra, query, cálculo, prompt, classificador, modelo aprendido ou combinação.

Não é obrigatório que cada evaluator produza um score numérico. É obrigatório que exista, quando houver proatividade, um mecanismo explícito e testável de seleção e priorização.

Proatividade sem filtro tende a virar ruído.

### 5.7 Agentic Journeys

São jornadas em que o sistema trabalha sobre o acumulado mesmo sem uma pergunta imediata do usuário.

Uma journey deve declarar:

**gatilho → fontes → contexto → avaliação → seleção → saída/ação → autonomia → encerramento/revisão**

Exemplos reutilizáveis:

- Daily Attention / TODAY;
- Commitments;
- Loose Ends;
- Risk;
- Weekly Review;
- INSIGHTS.

Formas de execução:

- **scheduled:** executada em cadência;
- **event-driven:** disparada por evento;
- **condition-based:** acompanha uma condição e só interrompe quando o critério é atingido.

A forma depende das capacidades reais da plataforma e do ambiente.

Um bom sistema agentic filtra mais do que notifica.

### 5.8 Action & Autonomy

Classifique capacidades por autonomia:

- **observar:** leitura e coleta autorizadas;
- **interpretar/correlacionar:** pode ser automático, preservando evidência e incerteza;
- **recomendar:** pode ser automático;
- **preparar:** gera rascunho, proposta ou ação pronta para revisão;
- **executar internamente:** somente dentro de escopo e guardrails definidos;
- **executar externamente, de forma sensível ou irreversível:** exige autorização adequada.

Permissão técnica não equivale a autorização.

**Liberdade de raciocínio e autonomia de execução são dimensões independentes.** O sistema pode contextualizar, relacionar, interpretar e recomendar amplamente dentro das fontes autorizadas e da incerteza disponível, enquanto persistência, mudança de estado e ações com consequência recebem controles proporcionais ao risco. Não restrinja desnecessariamente o raciocínio para tornar a execução segura.

Agentic não significa autonomia irrestrita.

### 5.9 Feedback, Correction & Observability

O sistema precisa permitir:

- corrigir classificação ou identidade;
- desfazer ou reparar estado;
- registrar duplicação;
- reabrir item;
- rejeitar relação ou recomendação;
- confirmar alias;
- rastrear fonte, timestamp e evidência;
- avaliar se retrieval, ranking ou jornada foram úteis.

Correções do usuário são sinais de aprendizado, não prova automática de que a IA estava errada.

## 6. Informação e integridade

Informação só conta quando reduz uma incerteza relevante e chega com integridade suficiente para orientar percepção, decisão ou ação.

Para fluxos relevantes, declare:

- incerteza;
- sinal;
- origem;
- transformações;
- canal;
- capacidade técnica e humana;
- ruído;
- redundância;
- confirmação de entrega;
- confirmação de interpretação;
- confirmação de escrita, quando houver;
- efeito esperado;
- correção e recuperação.

Não confunda:

1. entrega técnica;
2. interpretação;
3. escrita em fonte oficial;
4. efeito no usuário ou processo.

Comprima repetição previsível. Preserve identificadores, fontes, evidências e histórico quando tornarem falhas detectáveis e reversíveis.

## 7. Fontes oficiais e precedência

Para cada tipo de conteúdo, defina:

- origem e proprietário;
- fonte oficial;
- local de estado;
- versão prevalente;
- regra de precedência;
- sensibilidade;
- retenção;
- quem pode ler, alterar ou compartilhar.

Conversa, histórico, memória de produto, arquivo e sistema corporativo são mecanismos diferentes.

Não afirme que algo foi salvo, sincronizado, atualizado ou lembrado sem confirmação técnica correspondente.

## 8. Relações e Context Graph

Relações entre pessoas, empresas, projetos, reuniões, documentos, decisões, pendências, oportunidades, compromissos e riscos podem melhorar contexto e retrieval.

**Relações são parte do problema. Um grafo não é obrigatório.**

Use Context Graph ou GraphRAG apenas quando produzirem ganho observável de recuperação, contexto ou julgamento.

## 9. Dashboard e superfícies

Dashboard é superfície de:

- consulta;
- exploração;
- visão macro;
- drill-down;
- estado;
- transparência;
- auditoria e correção.

Dashboard não é, por definição, o coração do OS.

Se o usuário precisa lembrar de abrir o dashboard para descobrir o que exige atenção, a proatividade ainda não está resolvida.

## 10. Componentes opcionais

Não são camadas canônicas por si só:

- subagents;
- Context Graph;
- GraphRAG;
- vector database;
- scores internos;
- app próprio;
- automações específicas;
- ferramentas de um fornecedor;
- modelos particulares.

Entram somente quando melhoram resultado, segurança, consistência ou fricção de forma observável.

**Journey é arquitetura; subagent é implementação.  
Relação é arquitetura; graph é implementação.  
Priorização é arquitetura; score é implementação.**

## 11. Learning / Evaluation Loop

Comece por avaliação e correção, não por reinforcement learning.

Sinais possíveis:

- correções;
- aliases confirmados;
- relações aceitas ou rejeitadas;
- duplicações;
- retrieval ruim;
- mudança de estado;
- item reaberto;
- alertas ignorados ou úteis;
- recomendações úteis;
- padrões recorrentes.

Esses sinais podem ajustar:

- ranking;
- thresholds;
- entity resolution;
- source weighting;
- retrieval;
- prompts;
- regras;
- journeys.

Learning-to-rank, contextual bandits ou reinforcement learning só entram diante de problema concreto e evidência suficiente.

## 12. Adoção

A experiência percebida faz parte da arquitetura.

Avalie:

- familiaridade e preferência;
- quantidade de lugares que o usuário precisa abrir;
- esforço para capturar e recuperar;
- continuidade entre dispositivos;
- linguagem e aparência;
- necessidade de treinamento;
- capacidade de manutenção.

A sofisticação deve crescer por baixo sem exigir que o usuário aprenda a engenharia do sistema.

## 13. Validação

Teste primeiro um fluxo vertical completo em ambiente real:

1. entrada;
2. identificação e contexto;
3. escrita ou recuperação correta;
4. processamento;
5. entrega ao usuário;
6. atualização de estado quando necessário;
7. falha, duplicidade e correção visíveis.

Classifique capacidades como:

- **validada:** demonstrada no ambiente real;
- **inferência:** plausível apoiada em evidência;
- **hipótese:** precisa de teste;
- **sem sinal:** não há base suficiente.

O critério de sucesso deve ser observável no comportamento e no resultado, não apenas na configuração técnica.

## 14. Registro mínimo por sistema

- problema e usuário;
- comportamentos-alvo;
- decisão ou ação que precisa melhorar;
- ambiente e maturidade;
- fontes e confiabilidade;
- mapa de responsabilidades e componentes;
- fontes oficiais, estado e precedência;
- memória operacional e longitudinal, quando aplicáveis;
- journeys e gatilhos, quando aplicáveis;
- autonomia e permissões;
- riscos e custo do erro;
- capacidades validadas e hipóteses;
- métrica de adoção e resultado;
- custo e responsável pela manutenção;
- próximo teste.

## 15. Relação Chuck-OS → implementações

Chuck-OS contém princípios, padrões reutilizáveis, método e guardrails.

Cliente contém contexto operacional, pessoas, dados, decisões, configurações, permissões e histórico.

Instância individual contém personalização de uma pessoa dentro do ambiente do cliente.

Um aprendizado observado em uma implementação só volta ao núcleo Chuck-OS como princípio ou padrão depois de demonstrar utilidade além daquele caso.

Documentos históricos preservam evidência da evolução. Não governam automaticamente a arquitetura atual.
