# Sistema Bancário em Python

## Descrição
Este projeto implementa um sistema bancário simples utilizando Python. Ele permite criar contas bancárias, realizar depósitos, saques, transferências e visualizar saldos. O projeto segue duas abordagens: **Programação Orientada a Objetos (POO)** e **estrutura procedural com funções e dicionários**.

## Estrutura do Projeto

```
Sistema-Banco/
│── conta.py    # Classe Conta (POO)
│── data.py     # Classe Data para formatação de datas
│── banco.py    # Implementação procedural com funções
│── README.md   # Documentação do projeto
```

## Arquivos e Funcionalidades

### 📌 `conta.py` (Orientado a Objetos)
Este arquivo define a classe `Conta`, que encapsula os dados de uma conta bancária.

**Funcionalidades:**
- Criar uma conta com **número, titular, saldo e limite**.
- **Extrato** do saldo.
- **Depósito** de valores.
- **Saque** com verificação de limite.
- **Transferência** entre contas.
- **Encapsulamento** de atributos privados.
- **Métodos estáticos** para obter códigos de bancos.

**Exemplo de Uso:**
```python
from conta import Conta

conta1 = Conta(1234, "João", 1000, 500)
conta2 = Conta(5678, "Maria", 2000, 1000)

conta1.deposita(500)
conta1.saca(200)
conta1.transfere(300, conta2)
conta1.extrato()
conta2.extrato()
```

---

### 📌 `data.py` (Classe para Formatação de Datas)
Este arquivo define a classe `Data`, usada para armazenar e formatar datas.

**Funcionalidade:**
- Armazena **dia, mês e ano**.
- Exibe a data formatada no formato **DD/MM/AAAA**.

**Exemplo de Uso:**
```python
from data import Data

d = Data(15, 3, 2025)
d.formatada()  # Saída: 15/3/2025
```

---

### 📌 `banco.py` (Implementação Procedural)
Este arquivo implementa operações bancárias utilizando **funções e dicionários**.

**Funcionalidades:**
- Criar uma conta (**dicionário** com saldo e limite).
- Realizar **depósitos**.
- Realizar **saques**.
- Exibir **extrato**.

**Exemplo de Uso:**
```python
from banco import cria_conta, deposita, saca, extrato

conta = cria_conta(1234, "Carlos", 1500, 500)
deposita(conta, 200)
saca(conta, 300)
extrato(conta)  # Saída: Saldo 1400
```

---

## 📌 Comparativo: POO vs. Procedural

| Característica        | `conta.py` (POO) | `banco.py` (Funções) |
|--------------------|----------------|----------------|
| Estrutura         | Usa classes e objetos | Usa funções e dicionários |
| Encapsulamento    | Protege dados (`__saldo`) | Nenhuma proteção (dados públicos) |
| Reutilização      | Mais flexível | Mais simples, mas menos escalável |
| Facilidade de leitura | Melhor organizados | Pode ficar confuso com muitas funções |

---

## 💻 Como Executar o Projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/projeto-banco.git
   cd projeto-banco
   ```
2. Execute um dos arquivos Python:
   ```bash
   python3 conta.py
   ```

---

## 📌 Melhorias Futuras
- 📌 Adicionar suporte a banco de dados (SQLite ou PostgreSQL).
- 📌 Criar uma interface gráfica para facilitar o uso.
- 📌 Implementar autenticação de usuários.

---

## 📌 Contribuição
Sinta-se à vontade para contribuir com melhorias! Basta abrir um **Pull Request** ou sugerir ideias via **Issues** no repositório.

---

## 📌 Licença
Este projeto está licenciado sob a **MIT License**. Você pode usá-lo livremente para estudos e melhorias!

---

🚀 **Desenvolvido com Python!**

