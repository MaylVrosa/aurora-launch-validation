
# Aurora Siger – Sistema de Pré-Decolagem

## Descrição do Projeto

Este projeto simula um **sistema de verificação de pré-decolagem** de uma nave espacial fictícia chamada **Aurora Siger**.

O objetivo do sistema é analisar **dados de telemetria da nave** antes do lançamento e verificar se todos os parâmetros estão dentro das **faixas operacionais seguras**. Caso todas as condições estejam adequadas, a nave está **pronta para decolar**. Caso contrário, a decolagem é **abortada**.

Este projeto foi desenvolvido como parte de uma atividade acadêmica voltada para os conceitos iniciais de:

* Lógica computacional
* Estruturas condicionais em Python
* Simulação de sistemas embarcados
* Interpretação de dados de telemetria

---

# Parâmetros de Telemetria

O sistema analisa cinco parâmetros principais da nave:

| Parâmetro              | Descrição                                            |
| ---------------------- | ---------------------------------------------------- |
| Temperatura interna    | Temperatura dentro da nave                           |
| Integridade estrutural | Indica se a estrutura da nave está intacta           |
| Energia                | Percentual de energia disponível                     |
| Pressão dos tanques    | Pressão do combustível                               |
| Módulos críticos       | Verifica se os sistemas essenciais estão funcionando |

---

# Organização da Telemetria

Exemplo de leitura dos sensores da nave antes da decolagem:

| Parâmetro              | Valor | Faixa Segura | Status |
| ---------------------- | ----- | ------------ | ------ |
| Temperatura interna    | 72°C  | ≤ 80°C       | OK     |
| Integridade estrutural | 1     | 1 = OK       | OK     |
| Energia                | 68%   | ≥ 50%        | OK     |
| Pressão dos tanques    | 95    | 90 – 110     | OK     |
| Módulos críticos       | OK    | OK           | OK     |

### Conclusão

Todos os parâmetros encontram-se dentro das **faixas operacionais seguras**, indicando que a nave está apta para iniciar o processo de decolagem.

---

# Código Python

```python
print("=== SISTEMA DE PRÉ-DECOLAGEM - AURORA SIGER ===")

# Coleta de dados da aeronave
temperatura = float(input("Digite a temperatura interna (°C): "))
integridade = int(input("Integridade estrutural (1 = OK / 0 = FALHA): "))
energia = float(input("Nível de energia (%): "))
pressao = float(input("Pressão dos tanques: "))
modulos = input("Módulos críticos OK? (s/n): ")

modulos_ok = modulos.lower() == "s"

# Verificar se está pronto para decolar
if (temperatura <= 80 and
    integridade == 1 and
    energia >= 50 and
    90 <= pressao <= 110 and
    modulos_ok):

    print("🚀 PRONTO PARA DECOLAR")

else:
    print("❌ DECOLAGEM ABORTADA")
```

---

# Como Executar o Projeto

1. Faça o download do arquivo **AuroraSiger.ipynb** disponível neste repositório.

2. Certifique-se de que o **Python 3** esteja instalado no computador.

3. Abra o arquivo utilizando um ambiente compatível com **Jupyter Notebook**, como:

* Jupyter Notebook
* JupyterLab
* Google Colab
* PyCharm
* VS Code

4. Execute as células do notebook na ordem apresentada.

5. O sistema solicitará os dados de telemetria da nave:

* Temperatura interna
* Integridade estrutural
* Nível de energia
* Pressão dos tanques
* Status dos módulos críticos

6. Após inserir os valores, o sistema analisará os parâmetros e exibirá o resultado:

🚀 **PRONTO PARA DECOLAR**

ou

❌ **DECOLAGEM ABORTADA**


---

# Prints da Execução

Exemplo de execução do sistema:

=== SISTEMA DE PRÉ-DECOLAGEM - AURORA SIGER ===

Digite a temperatura interna (°C): 72

Integridade estrutural (1 = OK / 0 = FALHA): 1

Nível de energia (%): 68

Pressão dos tanques: 95

Módulos críticos OK? (s/n): s

🚀 PRONTO PARA DECOLAR

---

# Lógica do Sistema

O sistema utiliza **estruturas condicionais (`if`)** para verificar se todos os parâmetros estão dentro dos limites de segurança:

* Temperatura interna ≤ 80°C
* Integridade estrutural = 1
* Energia ≥ 50%
* Pressão entre 90 e 110
* Módulos críticos funcionando

Se **todas as condições forem verdadeiras**, o sistema autoriza a decolagem.

---

# Contexto Acadêmico

Este projeto foi desenvolvido para simular **processos reais de validação de sistemas embarcados** utilizados em missões aeroespaciais. Em operações reais, sistemas computacionais analisam continuamente dados de sensores para garantir a segurança da missão.

---

# Tecnologias Utilizadas

* Python
* Lógica condicional
* Simulação de telemetria

---

# Autora

Mayara Rosa
Estudante de Ciência da Computação

