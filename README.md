# Assistente Jurídico com IA para Cadastro de Processos

Prompt estruturado para o Microsoft Copilot que analisa petições iniciais e classifica o cadastro de novas ações com base em um glossário jurídico, sem inventar informações.

> Projeto criado em uma operação de Legal Operations. Todos os dados, nomes e critérios internos foram removidos ou substituídos por exemplos fictícios.

## O problema

Em uma operação de Legal Operations de alto volume, cada nova ação precisava ser lida e cadastrada manualmente, seguindo critérios do cliente (tipo de ação, causa raiz e produto). O processo era lento e sujeito a erro:

- **7 a 12 minutos** para cadastrar um processo;
- meta de **50 cadastros por dia**;
- risco de classificação inconsistente entre pessoas da equipe.

## A solução

Criei um prompt que ensina a IA a trabalhar como assistente jurídico. Ele define:

1. **Papel da IA:** assistente jurídico que analisa petições iniciais e sugere a classificação do cadastro.
2. **Trilha de análise:** a sequência de passos que a IA segue para ler a petição e chegar à classificação.
3. **Critérios de classificação:** tipo de ação, causa raiz e produto.
4. **Glossário como fonte única:** uma planilha com todos os tipos de ação, causas raízes e produtos. A IA só pode classificar com base no glossário.
5. **Regra anti-invenção:** se o caso não se enquadra em nenhuma hipótese do glossário, a IA não força uma classificação. Ela explica por que o caso não pode ser classificado daquela forma.

## Estrutura do prompt (exemplo fictício)

```text
PAPEL
Você é um assistente jurídico de uma operação de Legal Operations.
Sua tarefa é analisar uma petição inicial e sugerir a classificação do cadastro.

TRILHA DE ANÁLISE
1. Leia a petição inicial completa.
2. Identifique o tipo de ação.
3. Identifique a causa raiz do pedido.
4. Identifique o produto envolvido.
5. Confira cada item no GLOSSÁRIO.

REGRAS
- Classifique SOMENTE com base nas opções do glossário.
- Não invente tipos de ação, causas raízes ou produtos.
- Se o caso não se enquadrar em nenhuma opção do glossário, NÃO classifique.
  Explique qual informação está faltando ou por que nenhuma opção se aplica.

FORMATO DA RESPOSTA
- Tipo de ação: ...
- Causa raiz: ...
- Produto: ...
- Justificativa (trecho da petição que sustenta a escolha): ...
- Observações / casos fora do glossário: ...

GLOSSÁRIO
[tabela de tipos de ação, causas raízes e produtos]
```

## Resultados

| Indicador | Antes | Depois |
| --- | --- | --- |
| Tempo médio de cadastro (TMA) por processo | 7 a 12 minutos | 3 a 5 minutos |
| Cadastros por dia | 50 (meta) | 100 |
| Conformidade no checklist de qualidade | 85% | 95% |

A produtividade da operação dobrou e a qualidade subiu ao mesmo tempo. A equipe passou a usar o mesmo prompt, o que deixou a classificação mais padronizada.

## Como validei

A IA sugeria a classificação, mas a decisão final era humana. Eu conferia cada sugestão com a minha análise crítica de operadora, comparando com a petição e com o glossário, e registrava o resultado no checklist de conformidade da operação.

Esse controle de qualidade mostrou o efeito do prompt: a conformidade subiu de **85% para 95%** depois que a equipe passou a usar a IA com o prompt.

## O que aprendi

- Instruções claras e um glossário fechado reduzem muito as respostas inventadas pela IA.
- Pedir a justificativa e o motivo de não classificar torna a conferência humana mais rápida.
- A IA acelera, mas a conferência humana com checklist é o que garante a qualidade.
- O prompt melhora com o uso: cada erro da IA vira uma regra nova.

## Ferramentas

Microsoft Copilot, engenharia de prompts, Excel (glossário).

## Autora

**Ana Beatriz Pio de Oliveira**
[LinkedIn](https://www.linkedin.com/in/ana-beatriz-pio-b2519a245)
