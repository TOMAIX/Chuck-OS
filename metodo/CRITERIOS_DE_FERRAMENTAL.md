# Critérios de ferramental

**Função:** governar a escolha e a reavaliação de modelos, ferramentas e componentes.

Não fixa ranking de produtos. Não transforma decisão de um projeto em regra universal.

## Pergunta central

Qual é a menor arquitetura que resolve a dor no ambiente real, com qualidade suficiente, fricção aceitável e manutenção sustentável?

Ferramenta entra depois de definidos:

- comportamento a melhorar;
- fonte oficial;
- estado;
- autonomia;
- risco do erro;
- critério observável de sucesso.

## 1. Primeiro classifique a necessidade

- conversa, síntese ou apoio à decisão;
- captura;
- estado operacional;
- memória longitudinal;
- recuperação de conhecimento;
- retrieval híbrido;
- avaliação/priorização;
- journey agentic;
- produção de documento ou interface;
- ação autenticada em sistema externo;
- rotina agendada;
- automação por evento;
- monitoramento de condição;
- aplicação com estado e interface própria;
- desenvolvimento de código;
- captura de reunião;
- base de notas cultivada pelo cliente.

Uma necessidade pode combinar categorias, mas cada componente deve ter função principal declarada.

## 2. Critérios de escolha

Para cada alternativa, avalie:

- aderência ao hábito e ao ambiente atual;
- qualidade necessária;
- latência aceitável;
- fontes e formatos suportados;
- identidade e resolução de usuários;
- leitura e escrita reais;
- permissões técnicas;
- autorização organizacional;
- segurança e sensibilidade;
- residência e retenção de dados;
- confiabilidade e observabilidade;
- tratamento de falhas e duplicidade;
- continuidade entre computador, celular e execução remota;
- capacidade de rodar agendado, por evento ou por condição;
- portabilidade de dados, prompts e fluxos;
- custo recorrente e variabilidade;
- implantação, treinamento e suporte;
- manutenção pelo cliente e pelo Chuck-OS;
- dependência do fornecedor;
- facilidade de substituição.

O peso depende do fluxo.

Em interação por voz, latência pode dominar. Em ação financeira, jurídica ou institucional, confiabilidade, autorização e revisão humana prevalecem.

## 3. Capacidade declarada não é capacidade validada

Documentação, marketing e demonstrações indicam possibilidade. Não provam funcionamento no ambiente do cliente.

Classifique cada capacidade como:

- **validada:** demonstrada com conta, licença, permissões, dados e dispositivo reais;
- **inferência:** plausível com base em documentação ou evidência próxima;
- **hipótese:** precisa de teste;
- **sem sinal:** não há base suficiente.

Não prometa leitura, escrita, memória, sincronização, execução em segundo plano, alerta, evento, webhook ou ação autenticada sem validar no ambiente contratado.

Capacidades mutáveis, preços e limites devem ser revalidados no momento da proposta e antes da implantação.

## 4. Componentes e quando usá-los

### Prompt
Orientação para comportamento ou tarefa. Use quando instrução e contexto bastarem.

### Arquivo de conhecimento
Contexto relativamente estável e consultável. Não use como estado operacional sem mecanismo confiável de escrita e atualização.

### Skill / fluxo reutilizável
Procedimento funcional que merece execução consistente.

### Conector
Acesso autorizado a dados ou ações externas. Existência não comprova permissão nem adequação.

### Automação agendada
Trabalho futuro ou recorrente em cadência definida.

### Orquestrador por evento
Gatilhos, ramificações e integrações entre sistemas.

### Monitoramento por condição
Executa verificações e só interrompe quando um critério é atendido.

### Aplicação
Interface e estado próprios quando conversa, configuração ou automação não bastam.

### Agente de código
Trabalho substancial em repositório, testes e execução técnica.

### Mecanismo de retrieval
Pode ser direto, estruturado, lexical, semântico, híbrido, agentic ou baseado em relações. Escolha pela pergunta e pelas fontes.

### Evaluator / mecanismo de atenção
Produz um sinal útil para ranking, seleção ou decisão. Pode ser regra, query, cálculo, prompt, classificador, modelo ou combinação.

Não crie um componente separado apenas porque a responsabilidade existe conceitualmente.

## 5. Escolha de modelo

Modelo não é sistema.

O resultado depende da combinação entre:

- modelo;
- prompt;
- contexto;
- tools;
- fontes;
- estado;
- retrieval;
- permissões;
- arquitetura do fluxo.

Escolha pelo fluxo real, não por ranking abstrato de inteligência.

Busque equilíbrio entre:

- qualidade suficiente;
- latência percebida;
- confiabilidade;
- consistência;
- uso de ferramentas e contexto;
- custo;
- risco do erro.

Prefira o modelo menos pesado que cumpra o critério com margem adequada ao risco.

## 6. Prompt, rigor e latência

Prompts devem conter poucos guardrails fortes:

- objetivo;
- fontes;
- autonomia;
- evidência;
- confirmação técnica;
- padrão de entrega.

Excesso de prescrição pode:

- criar conflitos;
- reduzir julgamento útil;
- elevar latência e custo;
- produzir respostas mecânicas;
- dificultar manutenção.

Rigor vem do sistema inteiro. Prompt não compensa arquitetura frágil, fonte ausente ou permissão inexistente.

## 7. Retrieval

Use o mecanismo mais simples que preserve confiabilidade.

- não use vector search quando IDs, campos ou busca lexical resolvem;
- não use Agentic RAG quando uma fonte oficial resolve;
- não use GraphRAG quando relações não alteram materialmente o resultado;
- não abandone semântica quando ela melhora recall;
- não abandone metadata e indexação quando precisão ou estado importam.

Valide retrieval com casos conhecidos, falsos positivos, ambiguidades, aliases, itens antigos e mudanças de estado.

## 8. Evaluators e modelos cognitivos

Antes de criar uma biblioteca formal, valide o problema.

Para cada evaluator relevante, defina:

- pergunta que responde;
- entradas;
- sinais;
- saída;
- confiança;
- critério de ativação;
- consequência do erro;
- journey que o consome;
- como medir utilidade;
- baseline sem o evaluator;
- ganho marginal esperado e observado;
- falsos positivos e falsos negativos relevantes;
- latência, custo e manutenção incrementais.

Um evaluator só merece permanecer quando melhora materialmente seleção, ranking, decisão ou ação em relação à alternativa mais simples.

Quando custo ou latência importarem, use **avaliação progressiva**: aplique primeiro o mecanismo mais simples capaz de resolver ou eliminar casos e aumente o custo de avaliação apenas quando informação adicional puder mudar a decisão final. Regra, query, cálculo, prompt ou modelo mais pesado são opções; não fixe light/heavy evaluation como camadas arquiteturais.

Score numérico, threshold e modelo aprendido são opções, não requisitos.

Uma família de evaluators só deve virar **biblioteco Chuck-OS** depois de demonstrar reutilização em implementações diferentes.

## 9. Agentic execution

Antes de chamar algo de agentic, declare:

- o que dispara;
- quais fontes pode usar;
- como seleciona o que merece atenção;
- o que pode fazer sem confirmação;
- o que exige autorização;
- onde roda;
- dependência de sessão ou dispositivo;
- destino;
- tratamento de falha;
- regra de encerramento.

Agentic não é sinônimo de mais agentes.

Subagent é uma estratégia de execução, não requisito arquitetural.

## 10. Teste comparável

Valide modelo + prompt + ferramentas + fontes com tarefas representativas:

- caso simples e frequente;
- caso ambíguo;
- caso com fonte oficial;
- caso com mudança de estado;
- caso em que deve pedir confirmação ou não agir;
- falha conhecida ou regressão anterior.

Registre:

- aderência factual;
- aderência à fonte;
- utilidade;
- respeito a permissões;
- latência;
- sucesso técnico;
- clareza;
- correção humana necessária;
- falhas silenciosas.

Quando possível, altere uma variável por vez.

## 11. Regras de decisão

- Não construir aplicação quando configuração, conversa ou automação simples resolver.
- Não adicionar componente sem ligá-lo a uma dor, comportamento e critério.
- Não criar base paralela sem fonte oficial e precedência.
- Não usar arquivo como estado operacional sem mecanismo confiável de atualização.
- Não confundir permissão técnica com autorização.
- Não afirmar execução sem confirmação técnica.
- Não tornar dashboard responsável por proatividade.
- Não criar graph, subagent ou score apenas porque a tecnologia existe.
- Testar um fluxo vertical antes de ampliar infraestrutura.
- Preferir decisões reversíveis enquanto a evidência é limitada.
- Declarar: **Escolhemos X porque Y; descartamos Z porque W.**
- Definir antecipadamente que evidência faria a escolha mudar.

## 12. Registro mínimo de decisão

| Campo | Registro |
| --- | --- |
| Dor e comportamento atendidos | |
| Usuário, tarefa e ambiente | |
| Fonte oficial e estado | |
| Alternativas consideradas | |
| Escolha e razão | |
| Modelo e versão, se aplicável | |
| Prompt/configuração | |
| Retrieval/evaluator, se aplicável | |
| Permissões e autonomia | |
| Risco e tratamento de falha | |
| Revisão humana | |
| Qualidade observada | |
| Latência observada | |
| Custo e manutenção | |
| Critério de sucesso | |
| Evidência e status | |
| Data e responsável | |
| Gatilho de reavaliação | |

## Critério final

A melhor ferramenta é a menor combinação que entrega o resultado esperado, no tempo compatível com a rotina, dentro das permissões reais e com manutenção sustentável.
