# Avaliação — Engenharia de Software
**Sistema Integrado de Gestão de Farmácia — MVP Definido pelo Estudante**

Aluno: Juan Pablo Souza de Melo
RA: 24000028  
Data: 26/03/2026 

---

# 1. Definição do MVP
Descreva aqui **qual parte do sistema** foi incluída no seu MVP.  
Explique claramente:

- O que está **dentro** do MVP  
- O que está **fora** do MVP  
- Por que você fez essas escolhas  

Exemplo de início:  
> “Meu MVP cobre o processo de venda de produtos em uma farmácia, desde a consulta de um produto até a finalização da venda".

> Dentro do MVP está incluido a funcionalidade de consulta de produtos, verificação com validação de estoque, controle de quantidades diponiveis de produtos, verificação de produtos que apresentam receita médica, atualização automatica do estoque após a venda.

> Fora do MVP estão presentes funcionalidades como o controle de compras, relatórios e gestão de usuários.

> Essa escolha foi feita pelo simples fato que as vendas são a principal atividade de uma farmácia, o que a torna fundamental para o funcionamento do Sistema.

---

# 2. Regras de Negócio (mínimo: 5)
Liste e descreva **cada RN** de forma clara.

**RN01 Produtos que estão fora de estoque não podem ser vendidos.

**RN02 Produtos com receita só podem ser vendidos com aprovação do farmacêutico.

**RN03 Toda venda deve emitir comprovante para o cliente

**RN04 A quantidade vendida de produtos não podem ser maior do que o valor disponivel no estoque. 

**RN05 Atualização automatica do estoque após a venda. 


---

# 3. Requisitos Funcionais (mínimo: 8)
Liste os requisitos funcionais do seu MVP.

**RF01 Cadastro do Cliente

**RF02 Registro da Venda 

**RF03 Controlar o Estoque 

**RF04 Identificar Cliente

**RF05 Consultar Produtos do Estoque 

**RF06 Atualização automatica do Estoque

**RF07 Identificação de Produtos que exigem receita 

**RF08 Bloqueio da venda quando a quantidade do produto for maior do que o valor disponivel no estoque 

**RF09 Registrar Pagamento 

**RF10 Emitir Comprovante 


---

# 🛡 4. Requisitos Não Funcionais (mínimo: 4)
Liste os RNFs do sistema conforme seu MVP.

**RNF01 Segurança login

**RNF02 Garantia de integridade dos dados  

**RNF03 Disponibilidade do Sistema 

**RNF04 Agilidade do Sistema  


---

# 5. Casos de Uso (mínimo: 10)
### Inserir **diagrama de casos de uso geral**, demonstrando claramente:
- os 10 casos
- relação entre eles e atores
- pelo menos 3 includes
- pelo menos 3 extends
- Cadastrar Cliente
- Identificar Cliente
- Consultar Produto
- Verificação do Estoque
- Atualizar Estoque
- Realizar a Venda
- Registrar Pagamento
- Validar receita médica
- Emitir Comprovante

  <img width="646" height="251" alt="image" src="https://github.com/user-attachments/assets/f66a2049-95b9-4dfd-bf71-c1e2a77b474c" />


---

# 6. Documentação dos Casos de Uso
Para **cada caso de uso**, utilize o template abaixo:
---

## **UC01 — Realizar Venda**
**Ator(es):** Atendente  
**Descrição:**  Permite registrar produto para um cliente
**Pré-condições:** Produto cadastrado no sistema 
**Pós-condições:** Venda registrada, estoque atualizado e comprovante emitido

### Fluxo Principal
1. O atendente inicia a venda
2. O sistema solicita identificação do cliente
3. O atendente consulta o produto  
4. O sistema verifica o estoque
5. O sistema valida a quantidade
6. O atendente confirma a venda
7. O sistema registra o pagamento
8. O sistema atualiza o estoque
9. O sistema emite o comprovante

### Fluxos Alternativos / Exceções
- FA01 — Produto sem Estoque 
- FA02 — Produto com Receita 

### Relacionamentos
- **Include:** Identificar Cliente, Consultar Produto, Verificar Estoque, Registrar Pagamento, Emitir comprovante
- **Extend:** Validar a receita médica

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.
<img width="605" height="739" alt="image" src="https://github.com/user-attachments/assets/d8483ce2-10fd-4c1a-941e-c5f68cced116" />

---

## **UC02 — Cadastrar Cliente**
**Ator(es):** Atendente  
**Descrição:**  Permite cadastrar um novo cliente no sistema
**Pré-condições:** Cliente sem cadastro
**Pós-condições:** Cliente registrado no sistema

### Fluxo Principal
1. O atendende acessa o cadastro
2. Permite cadastrar um novo cliente no sistema
3. Cliente não cadastrado
4. Cliente registrado no sistema 

### Fluxos Alternativos / Exceções
- FA01 — Cliente ja existe no sistema
- FA02 — Sistema informa 

### Relacionamentos
- **Include: 
- **Extend:

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

<img width="268" height="282" alt="image" src="https://github.com/user-attachments/assets/fbd9e585-ad29-4b19-8c17-a6ca2aeb9683" />


---

## **UC03 — Identificar Cliente**
**Ator(es):**  Atendente
**Descrição:**  Permite localizar um cliente no sistema
**Pré-condições:** Cliente cadastrado 
**Pós-condições:** Cliente identificado 

### Fluxo Principal
1.  O atendente informa o CPF ou nome
2.  O sistema realiza a busca
3.  O sistema localiza o cliente
4.  O sistema exibe os dados

### Fluxos Alternativos / Exceções
- FA01 —  Cliente não encontrado
- FA02 —  Sistema solicita cadastro

### Relacionamentos
- **Include:**   
- **Extend:** Cadastrar Cliente 

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

<img width="263" height="282" alt="image" src="https://github.com/user-attachments/assets/529d3468-d21b-42da-a956-89cc16d91b86" />


---
## **UC04 — Consultar Produto**
**Ator(es):** Atendente  
**Descrição:** Permite consultar produtos no sistema
**Pré-condições:** Produto cadastrado
**Pós-condições:** Produto exibido  

### Fluxo Principal
1. O atendente informa nome ou código
2. O sistema realiza a busca  
3. O sistema encontra o produto  
4. O sistema exibe as informações  

### Fluxos Alternativos / Exceções
- FA01 — Produto não encontrado
- FA02 —  Sistema informa se o produto está indisponivel

### Relacionamentos
- **Include:**  
- **Extend:** 

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

<img width="292" height="282" alt="image" src="https://github.com/user-attachments/assets/f95781f1-235a-4904-992b-2d0ea3eeb43d" />


---

## **UC05 — Verificar Estoque**
**Ator(es):** Sistema
**Descrição:** Verifica a quantidade disponível de um produto
**Pré-condições:** Produto selecionado 
**Pós-condições:** Quantidade validada 

### Fluxo Principal
1. O sistema recebe o produto  
2. O sistema consulta o estoque 
3. O sistema verifica a quantidade
4. O sistema retorna a informação 

### Fluxos Alternativos / Exceções
- FA01 —  Produto sem estoque
- FA02 —  Quantidade insuficiente

### Relacionamentos
- **Include:**   
- **Extend:**  

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

<img width="292" height="282" alt="image" src="https://github.com/user-attachments/assets/c4900d3f-d5d3-47e2-91f6-b2ee5ac92d94" />


---
## **UC06 — Atualizar Estoque**
**Ator(es):** Sistema
**Descrição:** Atualiza o estoque após a venda 
**Pré-condições:** Venda realizada 
**Pós-condições:** Estoque atualizado 

### Fluxo Principal
1. O sistema recebe os dados da venda 
2. O sistema calcula a quantidade 
3. O sistema atualiza o estoque
4.  O sistema salva a atualização

### Fluxos Alternativos / Exceções
- FA01 —  Erro na atualização do estoque
- FA02 —  Falha no sistema

### Relacionamentos
- **Include:**   
- **Extend:** 

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

<img width="180" height="248" alt="image" src="https://github.com/user-attachments/assets/9870cb3d-df45-4547-b309-b5edd4889d69" />


---
## **UC07 — Selecionar Forma de Pagamento**
**Ator(es):** Atendente  
**Descrição:** Permite registrar a forma de pagamento
**Pré-condições:** Venda iniciada 
**Pós-condições:** Forma de pagamento definida

### Fluxo Principal
1. O atendente acessa as opções de pagamento
2. O sistema exibe as formas disponíveis 
3. O atendente seleciona a forma de pagamento
4. O sistema registra a forma escolhida  

### Fluxos Alternativos / Exceções
- FA01 —  Forma de pagamento inválida
- FA02 —  Falha ao registrar a forma de pagamento

### Relacionamentos
- **Include:** 
- **Extend:** 

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

<img width="322" height="282" alt="image" src="https://github.com/user-attachments/assets/6556ac26-9aaa-4cdf-a71d-6088fb2fdd00" />



---
## **UC08 — Registrar Pagamento**
**Ator(es):** Atendente 
**Descrição:** Permite registrar o pagamento da venda
**Pré-condições:** Venda iniciada 
**Pós-condições:** Pagamento registrado  

### Fluxo Principal
1. O atendente seleciona forma de pagamento 
2. O sistema processa o pagamento 
3. O sistema valida o pagamento
4. O sistema confirma o pagamento  

### Fluxos Alternativos / Exceções
- FA01 — Pagamento recusado 
- FA02 — Erro no processo 

### Relacionamentos
- **Include:** Selecionar forma de pagamento
- **Extend:** 

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

<img width="235" height="227" alt="image" src="https://github.com/user-attachments/assets/667b08b0-c621-4832-a223-4593fb287269" />


---
## **UC09 — Validar Receita Médica**
**Ator(es):** Farmacêutico  
**Descrição:** Autoriza a venda de medicamentos controlados 
**Pré-condições:** Produto exige receita  
**Pós-condições:** Receita validada 

### Fluxo Principal
1. O sistema solicita validação
2. O farmacêutico analisa a receita 
3. O farmacêutico valida a receita  
4. O sistema autoriza a venda  

### Fluxos Alternativos / Exceções
- FA01 —  Receita inválida
- FA02 —  Receita não aprovada   

### Relacionamentos
- **Include:**  
- **Extend:** 

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

<img width="147" height="193" alt="image" src="https://github.com/user-attachments/assets/c762ecbc-4b4a-426b-a0b1-c6ec13bb9a53" />


---
## **UC10 — Emitir Comprovante**
**Ator(es):** Sistema
**Descrição:** Gera o comprovante da venda  
**Pré-condições:** Venda finalizada
**Pós-condições:** Comprovante emitido

### Fluxo Principal
1.  O sistema coleta os dados da venda
2.  O sistema gera o comprovante
3.  O sitema exibe o comprovante
4.  O sistema finaliza o processo

### Fluxos Alternativos / Exceções
- FA01 —  Falha na geração do comprovante
- FA02 —  Erro de impressão

### Relacionamentos
- **Include:**  
- **Extend:** 

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

<img width="338" height="337" alt="image" src="https://github.com/user-attachments/assets/b3f8296f-87e0-4491-8f85-e06187b5da4c" />
