## Cenário 02: Cadastro de Fornecedores.

### Caso de Teste 01: Cadastro válido de fornecedor.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C2-CT01 | O fornecedor será cadastrado com CNPJ e dados válidos.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Estar na página "Cadastrar Fornecedor".                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Fornecedor"             |
| **E** preenchemos "Ferro LTDA" no campo Razão Social   |
| **E** preenchemos "12.345.678/0001-90" no campo CNPJ              |
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** o fornecedor será cadastrado com sucesso                |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O fornecedor deve aparecer na listagem após o cadastro.         |

---

### Caso de Teste 02: Tentativa de cadastrar fornecedor com CNPJ inválido.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C02-CT02 | O cadastro falhará quando o CNPJ informado for inválido. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Estar na página "Cadastrar Fornecedor".                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Fornecedor"             |
| **E** preenchemos "Ferro LTDA LTDA" no campo Razão Social   |
| **E** preenchemos "00000000000000" no campo CNPJ                  |
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** o sistema exibirá a mensagem "CNPJ inválido"            |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O cadastro não deve ser concluído.                              |

---

### Caso de Teste 03: Tentativa de cadastrar fornecedor já existente.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C03-CT03 | O sistema deve impedir o cadastro com CNPJ duplicado.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Fornecedor com CNPJ "12.345.678/0001-90" já cadastrado.       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página "Cadastrar Fornecedor"             |
| **E** preenchemos "Ferro LTDA LTDA" no campo Razão Social   |
| **E** preenchemos "12.345.678/0001-90" no campo CNPJ              |
| **QUANDO** clicarmos em "Salvar"                                  |
| **ENTÃO** o sistema exibirá a mensagem "Fornecedor já cadastrado" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O registro duplicado não deve ser salvo.                        |

## 🔗 Evidências (Jam.dev)

- **C01-CT01** → [Execução](https://jam.dev/c/5ede05e7-d9b3-49db-96df-332cf447653a) 
- **C01-CT02** → [Execução](https://jam.dev/c/955d152e-d266-427d-aea5-2ccd3d7a6f10) 
- **C01-CT03** → [Execução](https://jam.dev/c/8032b963-21e4-49dc-b827-65e639c2fcc2)

