# Desafio Técnico - Cadastro de Condomínios

Este desafio tem como objetivo avaliar suas habilidades em desenvolvimento, consistindo em desenvolver um endpoint para cadastrar um condomínio e uma tela front-end para efetuar essa ação.

---

## Descrição Geral

Você deverá implementar:

- **Backend:**  
  Um endpoint em Node.js (utilizando TypeScript e Express) que permita o cadastro de um condomínio.

- **Frontend:**  
  Uma interface (preferencialmente em Vue) que possibilite ao usuário realizar o cadastro do condomínio por meio de um formulário.

O cadastro do condomínio deve ser associado a um imóvel, cuja lista será obtida a partir do endpoint:  
`https://dev.imoflow.app.br/api/portal/imoveis/comercio/Venda`  
A lista deverá filtrar os imóveis do tipo “apartamento” para popular um dropdown.

---

## Especificações do Endpoint e da Tela de Cadastro

### Endpoint (Backend)

- **Objetivo:**  
  Criar um registro de condomínio no banco de dados MongoDB (utilizando o MongoDB Cloud gratuito).

- **Campos:**
  - **id:** Gerado automaticamente (identificador único).
  - **id_imovel:** Obtido a partir da seleção do imóvel.
  - **nome_condominio:** Texto.
  - **cep:** Número.
  - **rua:** Texto.
  - **numero:** Número.
  - **complemento:** Texto.
  - **cidade:** Texto.
  - **estado:** Dropdown que carrega uma lista de estados.
  - **tipo (Horizontal ou Vertical):** Representado por um checkbox.

- **Validações:**
  - Não permitir o cadastro de dois condomínios com o mesmo **nome**.
  - Não permitir o cadastro de dois condomínios com o mesmo **CEP** e **número** quando os nomes forem diferentes.

### Tela de Cadastro (Frontend)
  - **Nome do Condomínio:** Texto.
  - **CEP:** Número.
  - **Rua:** Texto.
  - **Número:** Número.
  - **Complemento:** Texto.
  - **Cidade:** Texto.
  - **Estado:** Dropdown que carrega uma lista de estados.
  - **Tipo (Horizontal ou Vertical):** Representado por um checkbox.

- **Fluxo da Tela:**
  - Inicialmente, somente o dropdown de imóveis deve estar habilitado.
  - Após a seleção de um imóvel, os demais campos do formulário serão habilitados para preenchimento.

- **Componentes do Formulário:**
  - **Dropdown de Imóveis:**  
    Carrega os imóveis do tipo “apartamento” a partir do endpoint informado.
  - Campos para os dados do condomínio (conforme listados acima).

- **Ação:**
  - **Botão Salvar:**  
    Ao ser clicado, os dados preenchidos deverão ser enviados para o endpoint de cadastro.
  - Após um cadastro bem-sucedido, exiba uma mensagem de sucesso e limpe os campos do formulário.

---

## Stack

- **Backend:**  
  Node.js com TypeScript e Express.
- **Banco de Dados:**  
  MongoDB (utilize o MongoDB Cloud gratuito para criar a base e a coleção de condomínios).
- **Frontend:**  
  Utilize Vue (preferencialmente) ou outro framework moderno (React, Angular, etc.).

---

## Instruções de Submissão

- **Repositório no GitHub:**  
  Crie um repositório com o nome: `desafio_dev_imoflow_nome_do_candidato`

- **Envio do Projeto:**  
Suba todo o projeto (backend e frontend) neste repositório criado.  

## Considerações Finais

Este desafio visa avaliar sua capacidade de desenvolver uma solução integrada, desde a implementação do endpoint até a criação da interface de usuário. 

Boa sorte!