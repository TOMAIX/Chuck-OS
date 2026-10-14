# Executive OS | Contrato de instanciação e validação

**Status:** canônico - versão inicial  
**Data:** 30/08/2026  
**Função:** definir o mínimo necessário para desenhar, implantar e validar uma instância.

## 1. Modelo de instanciação

**base comum do produto + delta organizacional + delta individual + variante de plataforma + validação real**

Nem toda implementação terá todas as camadas explicitamente separadas, mas suas responsabilidades devem permanecer distinguíveis.

## 2. Antes de construir

Identificar:

- pessoa, função e rotina;
- problema observável;
- decisão ou ação a melhorar;
- comportamento natural de captura;
- fontes e confiabilidade;
- memória e estado necessários;
- ambiente e dispositivos;
- identidade, permissões e consentimentos;
- autonomia autorizada;
- risco e custo do erro;
- critério observável de sucesso;
- adoção e manutenção.

Não escolher ferramenta antes de entender as responsabilidades.

## 3. Contrato de personalização

O delta organizacional pode definir:

- políticas e segurança;
- fontes corporativas;
- identidade e ownership;
- ambiente tecnológico;
- padrões compartilhados;
- informação organizacional autorizada;
- manutenção e suporte.

O delta individual pode definir:

- nome e linguagem;
- categorias e convenções;
- canais e rotina;
- fontes pessoais autorizadas;
- modelo físico de memória;
- journeys;
- capacidades especializadas;
- níveis de autonomia;
- estilo de resposta;
- superfícies.

## 4. Contrato de dados e memória

Antes de automações, declarar:

- fonte canônica de cada tipo de estado;
- local de histórico e eventos;
- memória persistente sem estado operacional;
- fontes que compõem memória longitudinal;
- projeções ou espelhos;
- regra de precedência;
- detecção de divergência;
- deduplicação e identidade de assunto;
- retenção, acesso e correção.

## 5. Primeiro fluxo vertical

Provar um caminho completo antes de ampliar infraestrutura:

**captura → contextualização → recuperação de contexto/estado → julgamento → atualização ou ação autorizada → confirmação → recuperação posterior correta**

Quando houver fonte canônica + projeção:

**captura → atualização canônica → projeção correta → recuperação consistente**

Quando houver proatividade:

**estado/contexto → avaliação → seleção → entrega → feedback**

## 6. Ambientes

Usar ambiente de teste controlado quando necessário, mas revalidar no ambiente, identidade, licença, permissões, dispositivo e volume reais da pessoa.

**LAB não prova PROD.**

O padrão não obriga um LAB específico nem determina que a implantação seja recriada manualmente. Exige apenas que evidência de teste não seja apresentada como evidência de produção fora do escopo demonstrado.

## 7. Testes mínimos

### Identidade e segurança

- usuário e ownership corretos;
- conexões e permissões corretas;
- ausência de acesso indevido;
- controle negativo com conteúdo de outro usuário;
- autorização compatível com ações externas.

### Captura

- canais naturais relevantes;
- voz/mobile quando aplicável;
- captura não vira tarefa automaticamente;
- baixa fricção.

### Fontes e retrieval

- cada fonte isoladamente;
- identidade, precisão, latência e consentimento;
- combinação somente quando necessária;
- fonte oficial prevalece no escopo adequado.

### Operational Memory

- criação;
- leitura;
- atualização do mesmo assunto;
- conclusão, cancelamento e reabertura;
- ausência de duplicação indevida;
- campos não inventados;
- preservação de valores omitidos quando aplicável;
- recuperação correta do estado vigente.

### Longitudinal Memory

- continuidade de assunto;
- precedente relevante;
- distinção entre informação posterior e atualização real;
- relações sustentadas;
- contexto distribuído;
- ausência de conexão fabricada.

### Julgamento

- contrariar premissa errada;
- preservar incerteza;
- não transformar narrativa em fato;
- indicar o que mudaria a conclusão;
- usar lentes somente quando alterarem a leitura.

### Attention

Primeiro on-demand:

- sinal relevante;
- poucos itens;
- novidade e timing;
- sustentação;
- supressão de ruído;
- ausência de repetição sem mudança;
- explicação de “por que agora” quando material.

### Action

- autorização correta;
- confirmação técnica;
- falha sem duplicação ou falsa alegação de sucesso;
- reversão ou reparo quando aplicável.

## 8. Estados de evidência

- **Validado:** demonstrado por teste, registro ou fonte adequada no escopo declarado.
- **Inferência:** conclusão plausível apoiada em sinais.
- **Hipótese:** precisa de teste.
- **Sem sinal:** base insuficiente.

Pode-se usar “validado parcialmente” operacionalmente, desde que condições e lacunas sejam explicitadas.

Decisão documental vigente não equivale a capacidade validada.

## 9. Critérios de sucesso

Definir baseline e mudança observável em pelo menos uma dimensão:

- captura;
- recuperação;
- continuidade;
- percepção;
- julgamento;
- decisão;
- ação;
- acompanhamento;
- redução de carga cognitiva;
- redução de fricção;
- adoção.

Configuração técnica bem-sucedida não prova valor para a pessoa.

## 10. Performance e complexidade

Comparar a versão mais simples com alternativas especializadas antes de adicionar nova camada.

Avaliar conjuntamente:

- qualidade;
- latência percebida;
- confiabilidade;
- custo;
- manutenção;
- fragilidade;
- fricção cognitiva.

Alterar uma variável relevante por vez quando isso for viável e útil para isolar causa.

## 11. Promoção de capacidades

Caminho:

**referência ou ideia → hipótese → teste real → capacidade útil no caso → candidato reutilizável → padrão com evidência**

Uma capacidade pode permanecer individual, organizacional, experimental ou ser descartada. Não há obrigação de promoção.

## 12. Aceite mínimo de uma instância

Uma instância só deve ser declarada operacionalmente validada quando a pessoa conseguir, no ambiente real:

- capturar com baixa fricção;
- recuperar contexto e estado corretos;
- atualizar estado sem duplicação indevida;
- distinguir evidência de interpretação;
- receber julgamento útil;
- usar as fontes autorizadas com identidade correta;
- perceber sinais úteis com ruído aceitável, se Attention estiver no escopo;
- executar apenas dentro da autonomia definida;
- corrigir falhas e recuperar histórico;
- obter confirmação técnica das ações realizadas.

## Princípio final

Replicação não é copiar ferramentas. É preservar responsabilidades, contratos e critérios enquanto o desenho físico se adapta ao caso real.
