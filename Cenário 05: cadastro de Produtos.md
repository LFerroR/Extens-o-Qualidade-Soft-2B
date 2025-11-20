## Cenário 05: Cadastro de Produtos

### Caso de Teste 01: Cadastro válido.

| ID       | Descrição                                                         |
| :------- | :---------------------------------------------------------------- |
| C05-CT01 | O produto será cadastrado corretamente com dados válidos.         |

| **Pré-condições** |
| :---------------- |
| Nenhuma.          |

| **Passos**                                                                    |
| :----------------------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Produto"                             |
| **E** preenchemos "Monitor 24 Polegadas" no campo Nome                        |
| **E** preenchemos "350.00" no campo Preço                                      |
| **E** preenchemos "5" no campo Quantidade                                      |
| **QUANDO** clicarmos em "Salvar"                                               |
| **ENTÃO** o produto será cadastrado com sucesso                                |

| **Critérios de aceitação**               |
| :--------------------------------------- |
| O produto deve ser registrado no sistema |

---

### Caso de Teste 02: Preço negativo.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C05-CT02 | O cadastro deve falhar quando o preço inserido for negativo |

| **Pré-condições** |
| :---------------- |
| Nenhuma.          |

| **Passos**                                                           |
| :------------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Produto"                   |
| **E** preenchemos "Monitor 24 Polegadas" no campo Nome               |
| **E** preenchemos "-100" no campo Preço                              |
| **QUANDO** clicarmos no botão "Salvar"                               |
| **ENTÃO** será exibida a mensagem "Preço inválido"                   |

| **Critérios de aceitação**             |
| :------------------------------------- |
| O cadastro deve ser bloqueado.         |

---

### Caso de Teste 03: Produto já cadastrado.

| ID       | Descrição                                                        |
| :------- | :--------------------------------------------------------------- |
| C05-CT03 | O sistema deve impedir que produtos duplicados sejam cadastrados |

| **Pré-condições** |
| :---------------- |
| Produto "Monitor 24 Polegadas" já cadastrado. |

| **Passos**                                                          |
| :------------------------------------------------------------------ |
| **DADO** que estamos na página "Cadastrar Produto"                 |
| **E** preenchemos "Monitor 24 Polegadas" no campo Nome             |
| **E** preenchemos "350.00" no campo Preço                          |
| **E** preenchemos "5" no campo Quantidade                          |
| **QUANDO** clicarmos em "Salvar"                                   |
| **ENTÃO** será exibida a mensagem "Produto já cadastrado"          |

## 🔗 Evidências (Jam.dev)

- **C01-CT01** → [Execução](https://jam.dev/c/e7d782b9-5541-4462-9d51-94d36b08c903)
- **C01-CT02** → [Execução](https://jam.dev/c/3ced595f-ae36-4539-aa8c-920e16fa3184)
- **C01-CT03** → [Execução](https://jam.dev/c/af10606d-1c3f-45b4-9fd6-bfb6dd6db780)



| **Critérios de aceitação**           |
| :----------------------------------- |
| O sistema não deve aceitar duplicidade |
