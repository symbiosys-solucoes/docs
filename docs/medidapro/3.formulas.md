# Gestão de Fórmulas

As fórmulas são a base do sistema MedidaPro. Elas definem como um produto final é composto a partir de diversos ingredientes e parâmetros de produção.

## Visão Geral

Na tela de cadastro de fórmulas, você pode visualizar todas as fórmulas cadastradas, filtrar por nome e acessar as opções de edição e criação.

Acesse através do menu principal: **Fórmulas**.

## Listagem de Fórmulas

A grade principal exibe as seguintes informações:

*   **Produto Final:** O nome e código do produto que é gerado pela fórmula.
*   **Desperdício:** O percentual de desperdício configurado para a fórmula.
*   **Ações:** Botão para editar a fórmula existente.

![Lista de Fórmulas](https://via.placeholder.com/800x400?text=Tela+de+Listagem+de+Formulas) *(Exemplo visual)*

## Criando uma Nova Fórmula

1.  Na tela de Fórmulas, clique no botão **"Adicionar Fórmula"** na barra de ferramentas.
2.  Você será redirecionado para o formulário de cadastro.
3.  Preencha os campos obrigatórios:
    *   **Nome da Fórmula:** Um identificador descritivo.
    *   **Produto Final:** Selecione o produto que será produzido.
    *   **Percentual de Desperdício:** Informe a perda esperada no processo (ex: 5.0 para 5%).
    *   **Usa Quantidade:** Marque se a fórmula deve respeitar quantidades estritas.
4.  **Adicionar Ingredientes:**
    *   Selecione os ingredientes que compõem a fórmula e suas respectivas quantidades.
5.  Clique em **Salvar**.

### Exemplo de Criação

Imagine que você quer cadastrar uma fórmula para um "Bolo de Chocolate".

*   **Nome:** Bolo de Chocolate Tradicional
*   **Produto Final:** Bolo de Chocolate (Cod: 101)
*   **Desperdício:** 2.5%
*   **Ingredientes:**
    *   Farinha de Trigo (500g)
    *   Açúcar (300g)
    *   Chocolate em Pó (200g)
    *   Ovos (3 un)

## Editando uma Fórmula

Para editar, basta clicar no ícone de lápis na coluna "Ações" da linha correspondente na listagem. Todos os campos disponíveis na criação podem ser alterados.

> **Nota:** Alterações em fórmulas podem impactar simulações futuras, mas geralmente não alteram simulações já consolidadas, dependendo da regra de negócio específica.