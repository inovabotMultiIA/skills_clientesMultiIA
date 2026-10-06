---
name: fathom-board-followup-template
description: Converta calls em tarefas validadas no Board.
version: 0.1.0
author: João Maykon, MultiIA Agentes
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [Fathom, Board, Onboarding, Suporte, Vendas]
    related_skills: [multiia-meeting-intelligence]
---

# Fathom + Board: Follow-up Validado

Use esta habilidade para qualquer empresa ou equipe que precise transformar as últimas calls relevantes em acompanhamento operacional no Board. Adapte a seleção de reuniões, o card principal e os critérios de prioridade ao perfil do cliente, sem assumir CRM, vendas ou ferramentas específicas.

## When to Use

- Após calls de onboarding, suporte, vendas, implantação ou acompanhamento.
- Para localizar a última ou as duas últimas reuniões relacionadas a uma conta, área ou projeto.
- Para atualizar um registro principal e criar tarefas apenas quando os fatos estiverem confirmados.

Não usar para registrar transcrição integral, executar ações externas discutidas na reunião ou inventar responsáveis e prazos.

## Pré-requisitos

- Fathom conectado e disponível.
- Board acessível ao agente.
- Um contexto mínimo: empresa/projeto, perfil atendido, área responsável e card ou board de destino.
- Permissão explícita para escrita caso o usuário peça apenas análise.

## Configuração por cliente ou perfil

Antes da primeira execução, confirme e registre:

- empresa, área e pessoas envolvidas;
- tipos de call relevantes: suporte, onboarding, vendas, operação ou outros;
- card principal ou board que concentra o acompanhamento;
- responsáveis possíveis e regras de atribuição;
- definição de prioridade para aquele negócio;
- o que exige aprovação humana antes de criar tarefa;
- quais ferramentas não podem ser alteradas sem autorização.

## Procedimento

1. **Identifique o contexto.** Confirme empresa/projeto, perfil atendido e modo: leitura, proposta ou execução.

2. **Busque as calls relevantes.** Liste gravações no Fathom e selecione a última ou as duas últimas pelo conteúdo, data, participantes e tema. Se a listagem for insuficiente, use resumo e depois transcrição.

3. **Cheque histórico no Board.** Pesquise cada `recording_id` antes de analisar ou escrever. Classifique a gravação como nova, já sincronizada ou ambígua.

4. **Extraia fatos, não interpretações.** Liste decisões, compromissos, bloqueios, riscos, evidências, oportunidades e perguntas abertas. Marque speaker/timestamp quando a interpretação puder ser discutida.

5. **Reconcilie com o trabalho existente e objetivo final.** Abra card principal, objetivo final, checklist, subtarefas e anexos relacionados. Classifique cada ponto como coberto, atualizar, novo, duplicado ou pendente de validação. Em calls de onboarding ou venda, proponha pelo menos um próximo passo que aproxime o resultado atual do objetivo final do card.

6. **Proponha atualização completa.** Após toda call relevante, proponha atualização do card principal, checks que podem ser marcados ou criados, subtarefas independentes e um anexo de orientação quando a reunião gerar roteiro, diagnóstico, instrução, decisão documentada ou material de preparação. Cada proposta deve indicar evidência, impacto no objetivo final, responsável, dependência e prazo apenas se confirmado.

7. **Valide critérios de criação.** Antes de criar tarefa, check ou anexo, confirme resultado observável, responsável, dependência, escopo e evidência. Checklist só é marcado quando a condição de conclusão ocorreu. Use prazo apenas se combinado. Caso haja lacuna, registre uma pergunta ou uma pendência de decisão, sem criar tarefa disfarçada.

8. **Escreva somente no modo execução.** Atualize o card principal com síntese factual, próximo passo recomendado e origem Fathom. Crie subtarefa para uma entrega independente; crie novo card apenas se existir uma frente autônoma. Anexe somente artefatos concretos úteis para orientar equipe ou cliente. Sempre registre: `Fonte Fathom: recording_id=<id> | gravada_em=<ISO> | url=<url>`.

9. **Leia de volta.** Reabra os registros alterados e confira responsável, prazo, descrição, checklist, subtarefas, anexos e marcador de fonte.

## Modelo de atualização

```text
Atualização pós-call — <data>

Decisões confirmadas:
- <decisão>

Avanços/evidências:
- <fato>

Bloqueios ou riscos:
- <item e impacto>

Próximo passo recomendado para o objetivo final:
- <ação, motivo, responsável, prazo se confirmado>

Perguntas para validar:
- <lacuna>

Fonte Fathom: recording_id=<id> | gravada_em=<ISO> | url=<url>
```

## Pitfalls

- Reunião com título genérico não prova relação com o cliente.
- Transcrição automática pode conter erro; valide pontos sensíveis.
- Não confunda discussão com decisão.
- Não crie tarefa sem responsável e resultado verificável.
- Não transforme qualquer insight em nova frente de trabalho.
- Não marque checklist por intenção; exija evidência de conclusão.
- Não declare atualização concluída sem reler o registro no Board.

## Verificação

- [ ] Calls selecionadas por conteúdo e identificadas por `recording_id`.
- [ ] Registro prévio pesquisado no Board.
- [ ] Decisões e tarefas apoiadas por evidência.
- [ ] Sem dono, prazo ou escopo inventado.
- [ ] Existe próximo passo recomendado que aproxima o objetivo final.
- [ ] Checks foram marcados somente com evidência de conclusão.
- [ ] Anexo foi proposto ou criado quando útil para orientar cliente ou equipe.
- [ ] Escritas registram a fonte Fathom.
- [ ] Registros alterados foram relidos e confirmados.
