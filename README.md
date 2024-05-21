# AF_BDD_ViniciusMachado_224016

# Sistema de Locação de Carros - BDD

## Enunciado do Cenário

Imagine que você está planejando alugar um carro para uma viagem. Para facilitar esse processo, uma empresa de locação de carros desenvolveu um sistema com diferentes comportamentos, dependendo das circunstâncias da locação e do cliente.

Inicialmente, considere um cliente que deseja alugar um carro de luxo. Se esse cliente realizar a reserva com antecedência de pelo menos uma semana, o sistema deve oferecer um desconto especial no valor total da locação. Por outro lado, suponha um cliente que necessita alugar um carro utilitário de última hora, sem qualquer reserva prévia. Nesse caso, o sistema deve ainda conseguir encontrar um veículo disponível e processar a locação rapidamente, mesmo que isso implique em um custo um pouco mais elevado devido à demanda urgente.

Esses cenários exemplificam como o sistema de locação de carros responde às diferentes necessidades e condições dos clientes, adaptando-se para garantir uma experiência satisfatória de locação, seja para reservas antecipadas ou demandas de última hora.

## Gherkin do Cenário

```gherkin
Feature: Sistema de Locação de Carros

  Scenario: Cliente aluga um carro de luxo com antecedência
    Given que o cliente deseja alugar um carro de luxo
    And a reserva é feita com antecedência de pelo menos uma semana
    When o cliente confirma a reserva
    Then o sistema deve oferecer um desconto especial no valor total da locação

  Scenario: Cliente aluga um carro utilitário de última hora
    Given que o cliente deseja alugar um carro utilitário
    And a reserva não foi feita previamente
    When o cliente solicita a locação
    Then o sistema deve encontrar um veículo disponível
    And o sistema deve processar a locação rapidamente
    And o custo da locação deve ser um pouco mais elevado devido à demanda urgente
