# Sistema de Gerenciamento de Ordens de Serviço para Oficina Mecânica

## Descrição
Este projeto consiste na modelagem conceitual de um banco de dados para um sistema de gerenciamento de execução de ordens de serviço (OS) em uma oficina mecânica. O objetivo é organizar e facilitar o controle de serviços realizados, peças utilizadas, clientes e mecânicos envolvidos no processo.

## Modelo Conceitual
O sistema possui as seguintes entidades principais:

### 1. **Clientes**
- Representam os clientes da oficina.
- Um cliente pode possuir um ou mais veículos cadastrados.

### 2. **Veículos**
- Associados aos clientes.
- Cada veículo pode ter uma ou mais ordens de serviço relacionadas.

### 3. **Ordens de Serviço (OS)**
- Criadas quando um veículo chega à oficina para manutenção ou revisão.
- Contêm informações como data de emissão, data de entrega, status e valor total da OS.
- Associadas a um cliente e a um veículo.
- Podem conter várias peças e serviços.

### 4. **Peças**
- Representam os itens utilizados na manutenção do veículo.
- Cada peça tem um valor unitário e pode ser utilizada em várias OS.
- Relacionadas à OS por meio da tabela `OS_Peca`, que define a quantidade usada em cada serviço.

### 5. **Serviços**
- Definem os tipos de manutenção realizados nos veículos (conserto ou revisão).
- Também possuem uma descrição e valor unitário.
- Relacionados às OS por meio da tabela `OS_Servico`, que define a quantidade aplicada.

### 6. **Mecânicos**
- São os profissionais responsáveis por executar os serviços nas OS.
- Possuem um código, nome, endereço e especialidade.
- Associados às OS por meio da tabela `EquipeMecanico_OS`, que define quais mecânicos trabalharam em determinada OS.

## Relacionamentos
- Um cliente pode possuir múltiplos veículos.
- Um veículo pode ter várias OS associadas.
- Uma OS pode conter múltiplas peças e serviços.
- Uma peça pode estar presente em várias OS.
- Um serviço pode estar contido em várias OS.
- Uma OS pode ser atendida por vários mecânicos.

## Tecnologias
O modelo foi implementado utilizando MySQL Workbench.

![oficina_mecanica](https://github.com/user-attachments/assets/e7d763fb-c7c7-435a-83fd-3990e709e1a1)
