# clinica-medica-db

# Storytelling: Modelando o Banco de Dados da Clínica Médica

Em uma clínica médica, a gestão eficiente das consultas, médicos, pacientes e convênios é fundamental para garantir um atendimento de qualidade e um controle adequado dos dados. Para atender às necessidades do negócio e otimizar a operação, foi criado um Modelo Entidade-Relacionamento (MER) que será o alicerce do sistema de informações da clínica.

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

![Modelo Entidade-Relacionamento (MER)](MER.png)

## Scripts

O arquivo `database_model.sql` contém a definição do banco de dados.
