# Roadmap de Estudos em C e AVR Bare Metal

> Objetivo: dominar C moderno, gerenciamento de memória, estruturas de dados, manipulação de arquivos e programação bare-metal em microcontroladores AVR (Arduino Leonardo ATmega32U4), utilizando apenas C e datasheets.

# Fase 1 — C Puro

## Semana 1 — Jogo de Adivinhação

**Pasta**

```
fase-1-c/
└── semana-01-jogo-adivinhacao/
```

### Projeto

Desenvolver um jogo de adivinhação com pontuação.

### Objetivos

- scanf
- printf
- if
- switch
- while
- for
- rand()
- srand()
- time()
- arquivos texto

### Funcionalidades

- número aleatório
- 7 tentativas
- muito alto
- muito baixo
- acertou
- salvar placar
- registrar nome do jogador

### Extras

- dificuldade
- limite de tempo
- ranking

---

## Semana 2 — Agenda de Contatos

**Pasta**

```
fase-1-c/
└── semana-02-agenda/
```

### Projeto

Agenda utilizando array de structs.

### Objetivos

- struct
- arrays
- funções
- ponteiros
- strcmp
- strcpy
- arquivos

### Funcionalidades

- adicionar
- listar
- remover
- buscar
- salvar
- carregar

### Extras

- qsort
- busca parcial
- impedir duplicados

---

## Semana 3 — To-Do List Dinâmica

**Pasta**

```
fase-1-c/
└── semana-03-todo-dinamico/
```

### Projeto

Lista de tarefas usando memória dinâmica.

### Objetivos

- malloc
- realloc
- free
- ponteiros
- ponteiros para structs

### Funcionalidades

- adicionar
- remover
- concluir
- listar
- filtros

### Extras

- salvar
- carregar
- undo
- ordenar prioridade

---

## Semana 4 — HexDump

**Pasta**

```
fase-1-c/
└── semana-04-hexdump/
```

### Projeto

Clone simples do comando hexdump.

### Objetivos

- argv
- argc
- fread
- arquivos binários
- manipulação de bits

### Funcionalidades

- offset
- hexadecimal
- ASCII
- leitura em blocos

### Extras

- checksum
- destacar padrões
- binário
- octal

---

## Semana 5 — Mini Shell

**Pasta**

```
fase-1-c/
└── semana-05-mini-shell/
```

### Projeto

Interpretador simples de comandos.

### Objetivos

- strtok
- parsing
- strings
- system()

### Comandos

```
ajuda

sair

echo

soma

data

ler

exec
```

### Extras

- histórico
- pipe
- variáveis

---

## Semana 6 — Game of Life

**Pasta**

```
fase-1-c/
└── semana-06-game-of-life/
```

### Projeto

Implementação do Jogo da Vida de Conway.

### Objetivos

- matrizes
- alocação dinâmica
- modularização
- lógica

### Funcionalidades

- grid configurável
- carregar padrões
- animação

### Extras

- ncurses
- edição
- salvar estado

---

# Fase 2 — AVR Bare Metal

## Semana 7 — Pisca LED

**Pasta**

```
fase-2-avr/
└── semana-07-led/
```

### Projeto

Controle do LED usando registradores.

### Objetivos

- DDR
- PORT
- PIN
- bitwise
- datasheet

### Extras

- SOS
- delay calibrado

---

## Semana 8 — UART

**Pasta**

```
fase-2-avr/
└── semana-08-uart/
```

### Projeto

Botão controla LED e UART.

### Objetivos

- USART
- debounce
- pull-up

### Implementar

```c
uart_init();

uart_putchar();

uart_print();

uart_getchar();
```

### Extras

- interrupções

---

## Semana 9 — LCD

**Pasta**

```
fase-2-avr/
└── semana-09-lcd/
```

### Projeto

Driver HD44780.

### Objetivos

Criar biblioteca própria.

### Implementar

```c
lcd_init();

lcd_clear();

lcd_print();

lcd_set_cursor();
```

### Extras

- contador
- timer

---

## Semana 10 — I²C

**Pasta**

```
fase-2-avr/
└── semana-10-i2c/
```

### Projeto

Sensor de temperatura.

### Objetivos

- protocolo I²C
- datasheet
- TWI

### Implementar

```c
i2c_start();

i2c_stop();

i2c_write();

i2c_read();
```

### Extras

- JSON
- LCD

---

## Semana 11 — PWM

**Pasta**

```
fase-2-avr/
└── semana-11-pwm/
```

### Projeto

Controle de servo.

### Objetivos

- PWM
- ADC
- Timer1

### Funcionalidades

- serial
- potenciômetro
- LCD

---

## Semana 12 — Estação Meteorológica

**Pasta**

```
fase-2-avr/
└── semana-12-estacao-meteorologica/
```

### Projeto

Projeto integrador.

### Componentes

- LCD
- Sensor temperatura
- Sensor luminosidade
- UART
- EEPROM

### Menu Serial

```text
temp

light

dump
```

### Objetivos

- EEPROM
- Máquina de Estados
- Integração
- Documentação

---

# Documentação

## docs/referencias.md

- Linguagem C
- Ponteiros
- Memória
- Estruturas
- Bits

---

## docs/datasheets.md

Adicionar os datasheets utilizados.

- ATmega32U4
- HD44780
- TMP102
- LM75
- BMP280

---

## docs/comandos-gcc.md

Guardar comandos úteis.

Exemplo:

```bash
gcc main.c -o programa

gcc *.c -o programa

gcc -Wall -Wextra -Werror -pedantic
```

---

## docs/debugging.md

Anotações sobre:

- gdb
- valgrind
- objdump
- size
- nm
- avr-objdump

---

# Objetivo Final

Ao concluir este roadmap você será capaz de:

- Desenvolver aplicações completas em C.
- Manipular memória manualmente.
- Criar bibliotecas próprias.
- Trabalhar com arquivos texto e binários.
- Ler datasheets profissionais.
- Programar AVR diretamente pelos registradores.
- Desenvolver drivers de periféricos.
- Implementar protocolos de comunicação.
- Criar firmware bare-metal.
- Construir projetos embarcados completos.

---

# Regras de Estudo

- Não usar IA para escrever o código.
- Ler a documentação antes de implementar.
- Commitar diariamente.
- Escrever comentários explicando decisões.
- Refatorar ao final de cada semana.
- Registrar aprendizados em `notas.md`.
- Sempre compilar com:

```bash
gcc -Wall -Wextra -Werror -pedantic
```

---

**Bons estudos.**
