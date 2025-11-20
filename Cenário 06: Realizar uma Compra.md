## Cenário 06: Realizar uma Compra

### Caso de Teste 01: Compra válida.

| ID       | Descrição                                                   |
| :------- | :---------------------------------------------------------- |
| C06-CT01 | A compra será registrada corretamente quando os dados forem válidos |

| **Pré-condições** |
| :---------------- |
| Fornecedor e produtos cadastrados. |

| **Passos**                                                                          |
| :---------------------------------------------------------------------------------- |
| **DADO** que estamos na página "Registrar Compra"                                    |
| **E** selecionamos o fornecedor "Ferro LTDA"                              |
| **E** adicionamos o produto "Monitor 24 Polegadas" quantidade "10"                   |
| **QUANDO** clicarmos em "Confirmar Compra"                                           |
| **ENTÃO** a compra será registrada com sucesso                                       |

| **Critérios de aceitação**                     |
| :--------------------------------------------- |
| A compra deve ser salva corretamente no sistema |

---

### Caso de Teste 02: Compra sem fornecedor.

| ID       | Descrição                                                          |
| :------- | :----------------------------------------------------------------- |
| C06-CT02 | O sistema deve impedir registrar compra sem selecionar fornecedor. |

| **Pré-condições** |
| :---------------- |
| Produtos cadastrados. |

| **Passos**                                                                      |
| :------------------------------------------------------------------------------ |
| **DADO** que estamos na página "Registrar Compra"                                |
| **E** não selecionamos nenhum fornecedor                                         |
| **E** adicionamos o produto "Monitor 24 Polegadas" quantidade "10"               |
| **QUANDO** clicarmos em "Confirmar Compra"                                       |
| **ENTÃO** deve ser exibida a mensagem "Selecione um fornecedor"                 |

| **Critérios de aceitação**   |
| :--------------------------- |
| O sistema deve bloquear a compra |

---

### Caso de Teste 03: Compra sem produtos.

| ID       | Descrição                                                    |
| :------- | :----------------------------------------------------------- |
| C06-CT03 | O sistema deve impedir registrar compra sem itens.           |

| **Pré-condições** |
| :---------------- |
| Fornecedor cadastrado. |

| **Passos**                                                                  |
| :-------------------------------------------------------------------------- |
| **DADO** que estamos na página "Registrar Compra"                           |
| **E** selecionamos o fornecedor "Tech Suprimentos LTDA"                     |
| **E** não adicionamos nenhum produto                                        |
| **QUANDO** clicarmos em "Confirmar Compra"                                  |
| **ENTÃO** será exibida a mensagem "Adicione pelo menos um produto"          |

| **Critérios de aceitação**    |
| :---------------------------- |
| A compra não deve ser registrada |

## 🔗 Evidências (Jam.dev)

- **C01-CT01** → [Execução](https://jam.dev/c/3da397f6-e092-4282-bcef-f973e5f40392)  
- **C01-CT02** → [Execução](https://jam.dev/c/b8acb042-ea6d-4466-901c-dd2c0070aba5)  
- **C01-CT03** → [Execução](https://jam.dev/c/5b7d1c8c-cdc7-4540-8161-91aad842ef4e) 

