# Projeto-Joystick-TCW
Projeto desenvolvido como parte da disciplina Technological Craftsmanship Works (ELN8DI).

## Descrição do Projeto

Este projeto tem como objetivo o desenvolvimento de um dispositivo de controle remoto para cadeiras de rodas elétricas, permitindo sua operação por meio de um smartphone conectado via Bluetooth.

A solução foi concebida para ser totalmente não invasiva, dispensando qualquer modificação na eletrônica original da cadeira de rodas. Em vez de acessar diretamente os circuitos de controle do equipamento, o sistema utiliza um mecanismo eletromecânico acoplado ao joystick original, capaz de reproduzir fisicamente os movimentos realizados pelo usuário.

Essa abordagem proporciona maior compatibilidade entre diferentes modelos de cadeiras de rodas, além de preservar a integridade do equipamento original e permitir a remoção do sistema sempre que desejado.

## Objetivos

* Permitir o controle remoto de uma cadeira de rodas elétrica utilizando um dispositivo móvel.
* Desenvolver uma solução universal e independente do fabricante da cadeira.
* Garantir instalação rápida e reversível por meio de um sistema de engate rápido.
* Implementar mecanismos de segurança para operação confiável.
* Integrar hardware, software embarcado e aplicativo móvel em uma única solução.

## Arquitetura do Sistema

O sistema é composto por três subsistemas principais:

### Sistema Mecânico

Responsável pelo acoplamento ao joystick original da cadeira de rodas e pela transmissão dos movimentos gerados pelos atuadores. A estrutura foi projetada para ser removível, compacta e de fácil instalação.

### Sistema Eletrônico

Baseado em um microcontrolador ESP32 responsável pelo processamento dos comandos recebidos via Bluetooth e pelo controle dos motores de acionamento do joystick.

Principais componentes:

* ESP32 DevKit
* Drivers TMC2209
* Motores de passo NEMA 17 Pancake
* Sensores de Efeito Hall NJK-5001C
* Bateria de lítio 12V com BMS
* Fusível de proteção
* Botão de emergência

### Sistema de Comunicação

A comunicação entre o aplicativo móvel e o dispositivo embarcado é realizada via Bluetooth. Os comandos enviados pelo usuário são interpretados pelo ESP32 e convertidos em movimentos físicos do joystick, permitindo controlar a direção da cadeira.

## Tecnologias Utilizadas

### Firmware Embarcado

* ESP32
* Arduino Framework
* Linguagem C/C++

### Aplicativo Mobile

* Flutter
* Dart
* Android

### Desenvolvimento Mecânico

* Modelagem CAD (Solidworks)
* Impressão 3D (PLA)
* Prototipagem rápida (Corte e dobra de chapas de aço)

## Segurança

Como o projeto está relacionado ao controle de um equipamento de mobilidade, foram incorporados mecanismos de segurança para minimizar riscos operacionais, incluindo:

* Parada de emergência por botão físico.
* Retorno automático à posição neutra em caso de falha.
* Detecção de perda de comunicação Bluetooth.
* Proteções elétricas contra sobrecorrente.

## Estrutura do Repositório

```text
/
├── Firmware/
│   ├── ESP32/
│   └── Bibliotecas/
│
├── App/
│   ├── Flutter/
│   └── APK/
│
├── CAD/
│   ├── Modelos_3D/
│   └── STEP e STL/
│
├── Eletronica/
│   ├── Esquematicos/
│   └── PCB/
│
├── Documentacao/
│   ├── Relatorios/
│   ├── Requisitos/
│   └── Cronograma/
│
└── README.md
```

## Status do Projeto

Projeto em desenvolvimento no contexto acadêmico, envolvendo as áreas de mecânica, eletrônica, sistemas embarcados e desenvolvimento de software para aplicações assistivas.

## Licença

Este projeto é disponibilizado exclusivamente para fins acadêmicos e de pesquisa.
