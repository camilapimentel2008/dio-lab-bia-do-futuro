# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Analisar padrões de gastos do usuário (categorias, frequência, valores) |
| `perfil_investidor.json` | JSON | Armazenar informações básicas (nome, renda, objetivo financeiro) |
| `produtos_financeiros.json` | JSON | Classificar e organizar os tipos de gastos (alimentação, lazer, transporte, etc.) |
| `transacoes.csv` | CSV | Classificar e organizar os tipos de gastos (alimentação, lazer, transporte, etc.) |

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Os dados mockados foram adaptados para refletir melhor a realidade de usuários iniciantes em organização financeira.

Foram incluídas:

- Categorias de gastos mais comuns (delivery, transporte, lazer, contas fixas)
- Estrutura simplificada de renda e despesas
- Regras básicas de controle financeiro (ex: porcentagem ideal de gastos por categoria)

Além disso, os dados foram organizados de forma simples para facilitar a análise pelo agente e permitir respostas mais rápidas e diretas.

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

Os arquivos JSON e CSV são carregados no início da execução do sistema e armazenados em memória para acesso rápido durante a interação com o usuário.

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

Os dados do usuário são inseridos dinamicamente no contexto do prompt a cada interação.

O agente utiliza:

- Dados recentes de transações
- Informações do perfil do usuário
- Regras financeiras pré-definidas

Esses dados são enviados junto com a pergunta do usuário para que a IA gere respostas personalizadas e contextualizadas.

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Cliente:

- Nome: Camila
- Renda mensal: R$ 2.000
- Objetivo: Controlar gastos e economizar

Resumo financeiro do mês:

- Total gasto: R$ 1.750
- Saldo restante: R$ 250

Gastos por categoria:

- Alimentação: R$ 800
- Transporte: R$ 300
- Lazer: R$ 450
- Contas fixas: R$ 200

Últimas transações:

- 05/03: Delivery - R$ 60
- 07/03: Uber - R$ 25
- 08/03: Cinema - R$ 40
- 10/03: Mercado - R$ 120
...
```
