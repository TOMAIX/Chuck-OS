# Executive OS | Princípios e experiência

**Status:** canônico - versão inicial de consolidação  
**Data:** 30/08/2026  
**Função:** governar os princípios de produto, raciocínio, interação e UX.

## 1. Capture first. Organize behind the scenes.

O usuário deve poder falar, escrever, anotar, perguntar, corrigir e deliberar naturalmente.

A organização necessária - interpretação, indexação, relação entre assuntos, recuperação, atualização de estado e seleção do que merece atenção - deve acontecer nos bastidores sempre que tecnicamente adequada e autorizada.

Isso não elimina estrutura. A estrutura permanece onde melhora confiabilidade, recuperação, integridade ou ação; ela apenas deixa de ser trabalho rotineiro do usuário.

Captura não significa registro operacional. Conversa, reflexão, hipótese, material recebido ou nota não viram tarefa, decisão ou compromisso automaticamente.

## 2. Context → Attention → Action

### Context - entender

Recuperar, relacionar e sintetizar somente o contexto necessário para compreender uma situação, seu estado, sua trajetória e suas relações.

### Attention - perceber e selecionar

Identificar o que realmente merece atenção agora. Importância permanente não é suficiente: deve existir razão para nova exposição naquele momento.

**Importance ≠ Attention Worthiness.**

### Action - avançar com segurança

Converter entendimento e decisão em acompanhamento, preparação ou execução, respeitando estado, autorização, reversibilidade e custo do erro.

Os três pilares podem aparecer em chat, voz, briefing, dashboard, lista, Kanban ou outra superfície. Não precisam ser seções explícitas em toda interação.

## 3. Simplicidade por cima; sofisticação proporcional por baixo

O usuário não deve precisar conhecer agentes, skills, bancos, schemas, conectores, índices ou flows para utilizar o sistema.

Complexidade técnica só entra quando resolve uma falha observável ou amplia valor de forma sustentável.

Construído não significa necessário. Disponível não significa adequado.

## 4. Precisão antes de concordância

O sistema não deve validar automaticamente premissas. Erros, pressupostos frágeis, alternativas ou contra-argumentos capazes de alterar uma decisão devem aparecer cedo.

Números e hipóteses devem ser avaliados de forma independente.

## 5. Liberdade cognitiva e controle de execução são dimensões diferentes

O sistema pode interpretar, contextualizar, relacionar, questionar e recomendar amplamente dentro das fontes autorizadas, preservando evidência e incerteza.

Persistência, mudança de estado e ações externas recebem determinismo, confirmação e verificação proporcionais ao risco, ao custo do erro e à irreversibilidade.

Permissão técnica não equivale a autorização.

## 6. Poucos guardrails fortes

Excesso de regras, prompts, ferramentas e processos pode restringir julgamento, aumentar latência, criar conflitos e reduzir qualidade percebida.

Os guardrails essenciais são:

- objetivo e escopo claros;
- fontes e precedência;
- evidência e incerteza;
- autonomia e autorização;
- confirmação técnica para persistência e execução;
- possibilidade de correção e recuperação.

## 7. Qualidade útil, não profundidade máxima

O produto deve buscar o melhor equilíbrio entre:

- qualidade suficiente para a decisão;
- latência percebida;
- confiabilidade;
- consistência;
- custo;
- manutenção;
- fricção.

Uma resposta marginalmente melhor pode ser um produto pior se trouxer penalidade desproporcional de tempo, complexidade ou fragilidade.

## 8. Informação não é decisão

Não confundir:

- conversa com decisão;
- resposta com conclusão;
- intenção com compromisso;
- disponibilidade com reunião marcada;
- nota com tarefa;
- material recebido com aprovação;
- entrega técnica com efeito produzido;
- acesso técnico com autorização.

## 9. Fontes têm contratos diferentes

Calendário, e-mail, mensagens, notas, documentos, memória estruturada e sistemas corporativos representam evidências diferentes.

O sistema deve usar retrieval proporcional ao problema e não atribuir a uma fonte mais significado do que ela demonstra.

Quando fontes divergirem, considerar natureza, autoria, data, precedência e se a informação posterior realmente corrige, atualiza, conclui, cancela ou substitui a anterior.

## 10. Memória operacional e longitudinal são responsabilidades distintas

- **Operational Memory:** preserva estado vigente que precisa ser recuperado deterministicamente.
- **Longitudinal Memory:** preserva contexto, histórico, precedentes, relações e evolução no tempo.

A separação é lógica e não obriga bancos físicos diferentes.

## 11. Relações importam; graph é opcional

Relações entre pessoas, projetos, organizações, reuniões, documentos, decisões, compromissos e riscos podem melhorar contexto e julgamento.

Não inventar relações. Semelhança não prova causalidade; repetição não prova padrão sem contexto.

Relação é responsabilidade do produto. Graph é um mecanismo de implementação e exige ganho observável.

## 12. Proatividade exige seleção e supressão

O sistema deve poder perceber mudanças, compromissos, loose ends, riscos, oportunidades, contradições e trajetórias quando houver base suficiente.

Um bom sistema filtra mais do que interrompe. Repetir algo apenas porque continua importante produz fadiga, não atenção.

Proatividade deve ser validada on-demand antes de ser automatizada.

## 13. Dashboard é superfície

Dashboard, listas e Kanban podem melhorar visibilidade, exploração, auditoria, transparência ou uso em reunião.

Eles não substituem memória, contextualização ou avaliação. Se o usuário precisa lembrar de abrir o dashboard para descobrir o que exige atenção, a proatividade ainda não está resolvida.

## 14. Base comum + delta real

O produto preserva responsabilidades comuns e permite variação por:

- organização;
- pessoa;
- domínio;
- plataforma;
- fontes;
- permissões;
- risco;
- rotina;
- maturidade;
- canal.

A primeira implementação não é o template automático das seguintes.

## 15. Correção e aprendizagem

O usuário deve poder corrigir identidade, classificação, estado, relação, recomendação e prioridade.

Correção é sinal de aprendizagem, não sentença automática. A fonte e a evidência mais adequadas prevalecem sobre preferência, memória ou repetição.

## Princípio final

O usuário deve experimentar simplicidade, continuidade e clareza. A engenharia do produto deve permanecer proporcional ao valor observável que entrega.
