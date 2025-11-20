## Cenário 07: Realizar uma Venda

### Caso de Teste 01: Venda válida.

| ID       | Descrição                                            |
| :------- | :--------------------------------------------------- |
| C07-CT01 | A venda será registrada corretamente com dados válidos |

| **Pré-condições** |
| :---------------- |
| Cliente e produtos cadastrados. |

| **Passos**                                                                |
| :------------------------------------------------------------------------ |
| **DADO** que estamos na página "Registrar Venda"                          |
| **E** selecionamos o cliente "João Silva"                                 |
| **E** adicionamos o produto "Monitor 24 Polegadas" quantidade "1"         |
| **QUANDO** clicarmos em "Finalizar Venda"                                 |
| **ENTÃO** a venda será concluída com sucesso                              |

| **Critérios de aceitação** |
| :-------------------------- |
| A venda deve ser registrada |

---

### Caso de Teste 02: Produto sem estoque.

| ID       | Descrição                                             |
| :------- | :---------------------------------------------------- |
| C07-CT02 | O sistema deve impedir venda quando não há estoque    |

| **Pré-condições** |
| :---------------- |
| Produto com estoque 0. |

| **Passos**                                                          |
| :------------------------------------------------------------------ |
| **DADO** que estamos na página "Registrar Venda"                    |
| **E** selecionamos o cliente "João Silva"                           |
| **E** adicionamos o produto "Monitor 24 Polegadas" quantidade "1"   |
| **QUANDO** clicarmos em "Finalizar Venda"                           |
| **ENTÃO** será exibida a mensagem "Estoque insuficiente"            |

| **Critérios de aceitação**    |
| :---------------------------- |
| A venda deve ser bloqueada     |

---

### Caso de Teste 03: Venda sem cliente.

| ID       | Descrição                                        |
| :------- | :----------------------------------------------- |
| C07-CT03 | O sistema deve impedir venda sem selecionar cliente |

| **Pré-condições** |
| :---------------- |
| Produto com estoque disponível. |

| **Passos**                                                                |
| :------------------------------------------------------------------------ |
| **DADO** que estamos na página "Registrar Venda"                          |
| **E** adicionamos o produto "Monitor 24 Polegadas" quantidade "1"         |
| **E** deixamos o campo cliente vazio                                      |
| **QUANDO** clicarmos em "Finalizar Venda"                                 |
| **ENTÃO** será exibida a mensagem "Selecione um cliente"                  |

| **Critérios de aceitação** |
| :--------------------------- |
| O sistema deve impedir concluir a venda |

## 🔗 Evidências (Jam.dev)

- **C01-CT01** → [Execução](https://jam.dev/c/2b39963b-6b9e-4c42-a6d8-5210f2705907) 
- **C01-CT02** → [Execução](https://jam.dev/c/c3f21786-5911-41fa-98a7-be64bc2ff66b) 
- **C01-CT03** → [Execução](https://jam.dev/c/b655d298-bcec-4a78-92f6-f406caee84bc)


