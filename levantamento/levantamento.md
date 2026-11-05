# Levantamento de Campo — DML CONTABILIDADE LTDA.

## 1. Identificação e metodologia

**Organização:** DML CONTABILIDADE LTDA.  
**Entrevistado nas três etapas:** Deni Maricato Maciel, proprietário da organização.  
**Única integrante do grupo que participou das entrevistas:** Valquíria Rodrigues de Macedo.  
**Metodologia:** entrevista estruturada em três etapas complementares. A primeira não concluiu todo o roteiro; as perguntas remanescentes foram respondidas na segunda etapa, e houve uma terceira rodada de perguntas por mensagens.

| Etapa | Data | Modalidade | Registro e abrangência |
|---|---|---|---|
| 1ª entrevista | 03/09/2026 | 100% presencial | Início do roteiro, concluído parcialmente |
| 2ª entrevista | 15/09/2026 | 100% por videochamada | Continuação e conclusão das perguntas restantes do roteiro inicial |
| 3ª entrevista | 26/10/2026 | Por mensagens | Perguntas complementares; o grupo informa possuir áudios com respostas desta etapa |

**Nota sobre autoria e participação:** os demais integrantes utilizaram as informações coletadas na elaboração do modelo e da documentação, mas não participaram diretamente das entrevistas. Não foram registrados aqui horários, duração das chamadas nem observações pessoais da visita, porque esses dados não foram confirmados.

## 2. Síntese das respostas das entrevistas de 03/09 e 15/09

Os pontos abaixo foram organizados a partir do levantamento informado anteriormente para a Entrega 1. **Esta é uma síntese temática, não uma transcrição literal nem uma atribuição de cada resposta à primeira ou à segunda data.** Para demonstrar as palavras exatas do entrevistado, o grupo deverá anexar o roteiro original respondido.

### 2.1 Contexto e operação

- Escritório de contabilidade com aproximadamente 50 anos de atuação, uma unidade, cerca de sete funcionários e aproximadamente 100 clientes ativos, entre pessoas físicas e jurídicas.
- Utiliza o sistema Alterdata, servidor de arquivos e controles complementares em planilhas Excel e documentos Word.
- Os documentos dos clientes podem chegar por captura com certificado digital A1, e-mail, WhatsApp ou entrega física.
- São executadas rotinas contábeis e fiscais, folha de pagamento, obrigações periódicas e atividades anuais.

### 2.2 Dificuldades e necessidades relatadas

- Não existe registro formal padronizado para cada recebimento e conferência documental.
- Tarefas, andamento e atrasos são acompanhados principalmente por departamento, sem visão unificada.
- Prazos de obrigações são conhecidos e acompanhados pelos setores, mas não há alerta centralizado de vencimento próximo.
- Documentos e informações enviados com atraso ou erros pelos clientes, especialmente para a folha de pagamento, geram pendências e retrabalho.
- Faturamento, conferências e contratos também dependem de planilhas e documentos externos ao ERP.
- **Não foi relatada dificuldade generalizada para localizar arquivos**, já que o ERP e o servidor concentram informações.

### 2.3 Processos observados por relato

- Cadastro do cliente e identificação por código interno; contratação de serviços com condições específicas por cliente.
- Recebimento de documentação, conferência, registro de pendências e solicitação de correções ao cliente.
- Distribuição de execuções e tarefas por áreas responsáveis, seguida de revisões antes de concluir serviços e obrigações.
- Emissão de faturas, recebimento de pagamentos e controle de inadimplência.

## 3. Síntese das respostas complementares de 26/10/2026

A terceira rodada abordou 18 perguntas divididas nos grupos abaixo. O texto apresenta **resumo fiel das informações disponíveis**, não reproduz perguntas ou áudios palavra por palavra.

### 3.1 Compras, fornecedores e contas a pagar (perguntas 1–4)

- O escritório compra materiais de escritório, papel, café, água, produtos de higiene e licenças/serviços de software necessários à operação.
- As necessidades de materiais são encaminhadas ao proprietário, que avalia e autoriza a aquisição. O proprietário também realiza os pagamentos.
- Licenças de software são avaliadas, aprovadas e contratadas pelo proprietário.
- Certificados digitais são adquiridos ou renovados conforme a necessidade, com apoio de empresa certificadora parceira.
- **Limite do levantamento:** não houve descrição suficiente do procedimento exato de escrituração e acompanhamento interno de todas as contas a pagar. O fluxo detalhado implementado no banco é proposta de modelagem.

### 3.2 Encerramento de contrato e entrega de documentos (perguntas 5–7)

- O cliente pode solicitar encerramento por e-mail ao proprietário ou à secretaria.
- O escritório também pode encerrar a relação por descumprimento contratual, inadimplência ou atividade que represente risco à responsabilidade profissional.
- A documentação é organizada e encaminhada ao cliente ou ao novo contador, geralmente por e-mail, podendo ocorrer retirada física ou envio por motofrete.

### 3.3 Certificados digitais (perguntas 8–10)

- Os vencimentos são acompanhados em planilha de controle.
- O escritório comunica o cliente aproximadamente um mês antes do fim da validade e a certificadora parceira conduz o processo de renovação.
- **Limite do levantamento:** não foi confirmada a consequência operacional exata de um certificado expirado sobre cada rotina de captura automática.

### 3.4 Funcionários e responsabilidades (perguntas 11–13)

- Funcionários são alocados nos departamentos conforme sua especialidade; substituições são realizadas conforme a necessidade da operação.
- **Limite do levantamento:** não foram detalhados critérios formais de redistribuição individual de clientes nem registros históricos de todas as mudanças de responsabilidade.

### 3.5 Faturas e inadimplência (perguntas 14–16)

- Os vencimentos de faturas podem ser nos dias 5, 10, 15 ou 30, conforme o combinado com o cliente.
- Foi relatada cobrança contratual de multa de 2% e juros de 0,3% ao dia sobre pagamentos em atraso. Tais percentuais são reproduzidos como **informação de entrevista**, sem declaração de conformidade jurídica ou automação no SQL.
- O proprietário decide sobre possíveis encerramentos por inadimplência.
- **Limite do levantamento:** não foi confirmado critério formal automático para suspender a prestação de serviços.

### 3.6 Privacidade e proteção de dados (perguntas 17–18)

- A empresa relatou cláusulas contratuais relacionadas à proteção de dados, acessos restritos por senha e cuidados com descarte de documentos.
- O proprietário é o contato interno mencionado para tratar dessas questões.
- Essas medidas relatadas **não significam** que o SQL implementa autenticação, autorização por perfil ou conformidade integral à LGPD.

## 4. Ligação do levantamento com o modelo de dados

| Informação levantada | Representação no projeto |
|---|---|
| Clientes, contratação e serviços | `cliente`, `contrato`, `contrato_servico`, `servico` |
| Documentos e pendências | `documento`, `pendencia_documental`, `execucao_documento` |
| Execuções, tarefas e responsáveis | `execucao_servico`, `tarefa`, `tarefa_funcionario`, `responsabilidade` |
| Obrigações e conferências | `obrigacao`, `revisao_obrigacao`, `revisao_execucao` |
| Faturamento e pagamentos de clientes | `fatura`, `pagamento` |
| Compras e despesas | `fornecedor`, `solicitacao_compra`, `item_compra`, `conta_pagar`, `pagamento_despesa` |
| Encerramento contratual | Campos de encerramento de `contrato` |
| Renovação de certificados | Campos de controle em `certificado_digital` |

**Distinção essencial:** o levantamento identifica práticas e necessidades; o DER e o SQL representam uma proposta de sistema. Não é correto afirmar que as novas tabelas ou consultas já estão em uso na empresa.

## 5. Evidências e privacidade

- **Evidência visual disponível segundo o grupo:** captura da videochamada de 15/09/2026, adicionada ao pacote em [`docs/evidencias/entrevista_videochamada_15-09-2026.png`](../docs/evidencias/entrevista_videochamada_15-09-2026.png). A divulgação pública depende da autorização das pessoas retratadas.
- **Evidência de áudio disponível segundo o grupo:** gravações com respostas da entrevista complementar de 26/10/2026, ainda a serem avaliadas para anexação, conforme consentimento e privacidade.
- O grupo informa que **conversou com o professor** e recebeu orientação de que, neste caso específico, a fotografia da entrevista presencial não seria absolutamente necessária. Esta afirmação registra a orientação relatada pelo grupo, **não substitui** confirmação escrita do professor nem dispensa outras evidências previstas na atividade.
- Evitar publicar telefones pessoais, imagens, vozes, documentos de clientes ou arquivos privados sem autorização de divulgação. Se não houver consentimento para publicar os áudios, registrar sua existência e apresentá-los ao professor por meio reservado, caso solicitado.

## 6. Pontos a conferir pelo grupo antes de enviar

1. Confirmar que as sínteses correspondem às anotações e aos áudios reais.
2. Confirmar a autorização de divulgação pública da captura da videochamada antes de subir a imagem para um repositório público.
3. Verificar se o professor solicitou algum comprovante específico da dispensa da foto presencial.
4. Manter os roteiros originais das entrevistas disponíveis como documentação complementar, caso sejam solicitados.
