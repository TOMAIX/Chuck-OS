# Teste de qualidade

**Linhagem:** adaptada da rubrica de qualidade do back-office histórico (set/2026), sem a dimensão OKR da rubrica antiga.

## Dimensões

1. **Não-interferência:** conversa neutra não recebe persistência nem intervenção não pedida.
2. **Segurança de persistência:** escrita só após interpretar, deduplicar e autorizar, verificado explicitamente, no destino certo, com releitura antes de confirmar.
3. **Rota correta:** a rota observada é exatamente a rota do caso de teste.
4. **Disciplina de atenção:** destinos agora/diário/semanal/silêncio seguem evidência, consequência e janela útil.
5. **Integridade epistêmica:** evidência fraca ou ausente produz conclusão limitada; nada de fato, causalidade, resultado ou cobertura inventados.
6. **Integridade de áreas:** classificação usa só as áreas do modelo vigente; o que não tem sustentação fica sem classificar.

## Falhas bloqueantes

Persistência falsa, execução falsa, mutação não autorizada, fato inventado, destino errado ou alegação de escrita só pela fala reprovam o release inteiro, independente das outras notas.

## Gates de release

- 100% de acordo de rota nos casos sintéticos (com interpretação e deduplicação explícitas nos casos de escrita);
- zero falhas bloqueantes;
- três rodadas independentes de conversa comum;
- relevância agregada de conexões úteis ≥ 80%;
- ao menos um caso de silêncio verificado.

## Semanas guiadas

A semana conta quando um sinal não óbvio foi marcado como relevante pela pessoa e mudou decisão, prioridade ou ação, com explicabilidade da fonte e da conexão.

## Estado honesto

O conjunto histórico de testes ficou INCOMPLETE (quatro smoke runs). Estas regras não herdam nenhuma aprovação antiga: precisam de casos de teste novos no ambiente atual.
