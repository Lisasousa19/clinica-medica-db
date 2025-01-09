# Modelando o Banco de Dados da Clínica Médica

Em uma clínica médica, a gestão eficiente das consultas, médicos, pacientes e convênios é fundamental para garantir um atendimento de qualidade e um controle adequado dos dados. Para atender às necessidades do negócio e otimizar a operação, foi criado um Modelo Entidade-Relacionamento (MER) que será o alicerce do sistema de informações da clínica.

## Desafio

A Clínica precisa de uma solução que consiga registrar todas as consultas realizadas, incluindo informações detalhadas sobre os médicos, pacientes e os convênios envolvidos. As regras de negócio definem que a estrutura do banco de dados deve garantir a integridade dos dados, com a definição de chaves primárias e estreangeiras, permitindo que a relação entre as diferentes entidades sejam bem representadas.

## Entidades e Atributos

### Médico
- CRM (Chave Primária)
- Nome
- Especialidade
- Telefone
- E-mail
- Endereço: Rua, Número, Complemento, Bairro, CEP, Cidade, Estado

### Consulta
- Identificação da consulta (Chave Primária)
- Data
- Horário
- CRM (Chave Estrangeira para Médico)
- CPF (Chave Estrangeira para Paciente)

### Paciente
- CPF (Chave Primária)
- Nome
- Telefone
- E-mail
- Endereço: Rua, Número, Complemento, Bairro, CEP, Cidade, Estado

### Convênio
- Identificação do convênio (Chave Primária)
- Empresa
- Tipo
- Vencimento
- Percentual de Coparticipação

## Relacionamentos

- **Médico-Consulta**: Um médico pode realizar várias consultas (1:N).
- **Médico-Convênio**: Muitos médicos podem atender a muitos convênios (N:M).
- **Paciente-Consulta**: Um paciente pode marcar várias consultas (1:N).
- **Paciente-Convênio**: Muitos pacientes podem ter muitos convênios (N:M).

 ## Diagrama do Modelo Entidade-Relacionamento (MER)
 O diagrama ilustrará visualmente todas as entidades, seus atributos, chaves primárias, as cardinalidades dos relacionamentos, e como as tabelas se interconectam.

  ![MER](https://github.com/user-attachments/assets/1fd91fc9-055a-46dc-b06e-5bf9243a0a39)

 ## Conclusão

O modelo de Banco de Dados desenvolvido oferece uma estrutura eficiente para gerenciar as informações da clínica médica, abrangendo médicos, pacientes, consultas e convênios. Com entidades bem definidas, relacionamentos claros e chaves estabelecidas corretamente, o sistema permitirá um controle preciso e ágil dos dados, contribuindo para o crescimento e aprimoramento contínuo da clínica.
