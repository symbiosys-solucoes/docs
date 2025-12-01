# Produção e Conversão

Este módulo é responsável por gerenciar o fluxo de entrada de Notas Fiscais (NFs) e convertê-las em registros de produção no sistema.

Acesse através do menu: **Movimentos para Conversão**.

## Consultar Movimentos

A tela inicial apresenta filtros para localizar notas fiscais de entrada que precisam ser processadas:

*   **Data Inicial / Data Final:** Período de emissão da NF.
*   **Cliente:** Filtrar por um fornecedor ou cliente específico.

Ao clicar em **Buscar**, o sistema lista os movimentos encontrados com as seguintes colunas:
*   Número da NF
*   Cliente
*   Data de Emissão
*   Valor
*   Status de Produção
*   Filial

## Gerar Produção

Para movimentos com status `NAO_REALIZADO`, a coluna de ações exibirá o botão **"Gerar Produção"**.

### O que acontece ao clicar?

1.  O sistema exibe uma confirmação.
2.  Ao confirmar, é executada a *procedure* `dbo.SYM_REGISTRO_PRODUCAO`.
3.  Esta rotina de banco de dados é responsável por:
    *   Registrar a entrada dos produtos acabados.
    *   Atualizar o status do movimento.
4.  O sistema exibe uma notificação de sucesso ou erro.

## Detalhes dos Itens

Ao dar um **duplo clique** em uma linha da grade, abre-se uma janela de diálogo (`MovimentoItensDialog`) mostrando os itens contidos naquela Nota Fiscal. Isso permite conferir os produtos antes de gerar a produção.

## Baixa de Matéria-Prima

Além de registrar a produção, o sistema também possui funcionalidades (via *stored procedures*) para dar saída na matéria-prima consumida (`dbo.SYM_SAIDA_MATERIA_PRIMA`), garantindo que o estoque de insumos seja atualizado conforme as fórmulas utilizadas.