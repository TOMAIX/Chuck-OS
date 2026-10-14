# Conferência de alterações

**Linhagem:** adaptada dos contratos de mutação e identidade do back-office histórico (set/2026).

- **Gatilho:** escrever só com verbo explícito da pessoa (registre, anote, atualize, concluí, cancele, reabra). Conversa, reflexão, hipótese e intenção futura não autorizam escrita.
- **Pipeline:** interpretar → deduplicar → autorizar → escrever → reler → confirmar, nessa ordem. Ambiguidade que muda destino, alvo ou campo material: uma pergunta curta e nenhuma escrita. Sem fallback automático.
- **Atomicidade:** estado e histórico no mesmo lote. Lote que falha = mutação que falha. Nunca reparar resultado parcial com uma segunda escrita automática.
- **Identidade:** uma identidade de mutação por operação lógica, gerada uma vez. Nova tentativa reusa a mesma identidade; se o resultado verificado já existe, confirmar o existente e criar zero registros.
- **Resultado verdadeiro:** completed só com releitura batendo; falha do provedor = failed; releitura divergente = repair_required, sem retry automático. Nunca afirmar registro, envio ou agendamento sem confirmação técnica.
- **Confirmação honesta:** a resposta distingue o que a pessoa pediu, o que o provedor respondeu e o que a releitura mostrou. Botão ou cartão na tela não prova estado; sem leitura do estado real, informar "não confirmado".
- **Limites:** não inventar valores de campos restritos; não alterar schema nem autoridade durante uma mutação comum; histórico é append-only, nunca reescrito.
