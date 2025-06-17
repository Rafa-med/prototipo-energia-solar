# Projeto de Automação Sustentável com Arduino

## Descrição do Projeto
Este repositório contém os arquivos para um sistema de controle de energia inteligente, simulando a transição automática entre fontes solar e bateria. Desenvolvido no Tinkercad como prova de conceito para a SPRINT 2, o projeto demonstra como implementar soluções sustentáveis com componentes básicos.

## Componentes Principais
- `Arduino Uno R3`: Unidade de controle central
- `Potenciômetro 10kΩ`: Simula sensor de luz solar
- `LED`: Representa carga elétrica (lâmpada)
- `Resistor 220Ω`: Protege o circuito
- `Serial Monitor`: Exibe status do sistema

## Funcionamento
O sistema:
1. Lê valores do potenciômetro (0-1023)
2. Aciona o LED quando valor > 500 (modo bateria)
3. Desliga o LED quando valor < 500 (modo solar)

## Como Usar
1. Abra o arquivo txt e entre no link do Tinkercad
2. Carregue o código no Arduino
3. Gire o potenciômetro para simular variação de luz
4. Observe o LED e Serial Monitor respondendo


graph LR
    P[Potenciômetro] -->|Lê valor| A(Arduino)
    A -->|Valor > 500?| L[Liga LED]
    A -->|Valor < 500?| D[Desliga LED]
    A --> S[Serial Monitor]
