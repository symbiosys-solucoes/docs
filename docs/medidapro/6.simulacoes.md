# Simulações

O módulo de Simulações permite calcular custos e prever cenários de venda para os produtos, baseando-se nas fórmulas cadastradas e custos atuais.

## Criando uma Simulação

Acesse **Simulações > Nova Simulação** no menu.

### Passo 1: Dados Gerais

Preencha as informações básicas da simulação:

*   **Cliente (CliFor):** Selecione o cliente para quem a simulação está sendo feita.
*   **Observação:** Campo livre para anotações.
*   **Incluir Mão de Obra:** Checkbox para indicar se os custos de mão de obra devem ser somados ao custo final.

### Passo 2: Adicionar Itens

Adicione os produtos que farão parte desta simulação. O sistema utilizará a fórmula padrão de cada produto para calcular os custos dos ingredientes.

1.  Selecione o **Produto**.
2.  Informe a **Quantidade**.
3.  O sistema calculará automaticamente com base nos custos dos ingredientes vinculados à fórmula do produto.

### Passo 3: Salvar

Ao clicar em **"Salvar Simulação"**, o sistema:
1.  Grava a simulação no banco de dados.
2.  Registra a data e hora atual.
3.  Vincula ao usuário logado.

## Histórico de Simulações

Você pode visualizar simulações passadas na tela de listagem (**Simulações > Listar**). Isso é útil para comparar a evolução dos custos ao longo do tempo ou recuperar orçamentos antigos.

## Integração com Orçamentos

Uma simulação pode estar vinculada a um **Orçamento**. Isso permite que, após aprovada a simulação, ela se torne um orçamento formal para o cliente.