# Simulador de Clínica Médica

Este projeto consiste no desenvolvimento de um simulador de funcionamento de uma clínica médica, implementado em Python, que permite analisar o impacto de diferentes configurações operacionais no desempenho do sistema de atendimento, nomeadamente nos tempos de espera dos pacientes e na ocupação dos médicos.
O sistema utiliza simulação de eventos discretos, oferecendo uma interface gráfica e funcionalidades avançadas de visualização, análise e exportação de resultados.

---

## 1. Objetivos do Projeto

- Simular o funcionamento diário de uma clínica médica
- Avaliar tempos médios de espera dos pacientes
- Analisar a taxa de ocupação dos médicos
- Estudar o impacto da taxa de chegada e do número de médicos
- Disponibilizar resultados estatísticos e gráficos
- Exportar dados para análise externa

---

## 2. Tecnologias Utilizadas

- PySimpleGUI – Interface gráfica
- Matplotlib – Visualização de gráficos
- NumPy – Análise estatística
- JSON / CSV – Armazenamento e exportação de dados

---

## 3. Estrutura do Sistema

O projeto está organizado de forma modular:
- Gestão de Dados
- Criação automática de cenários de pacientes
- Importação de ficheiros JSON externos
- Motor de Simulação
- Eventos de chegada e saída
- Filas por especialidade
- Prioridade dinâmica de pacientes
- Interface Gráfica
- Configuração da clínica
- Execução da simulação
- Visualização de gráficos
- Relatórios
- Tabela de atendimentos
- Exportação para CSV
- Previsão mensal

---

## 4. Parâmetros de Configuração

A clínica pode ser configurada através da interface gráfica com os seguintes parâmetros:

4.1 Recursos Humanos

Número de médicos de:
- Clínica Geral
- Cardiologia
- Ortopedia

4.2 Parâmetros Operacionais

Taxa de chegada de pacientes (pacientes/hora)
Tempo médio de consulta (minutos)
Distribuição estatística do tempo de consulta:
- Exponencial
- Normal
- Uniforme

4.3 Tempo de Simulação

Período fixo: 08h00 – 16h00 (480 minutos)

---

## 5. Modelo de Simulação

Simulação a eventos discretos

Eventos considerados:
- Chegada de paciente
- Início de atendimento
- Saída do paciente
- Filas independentes por especialidade

Atendimento baseado em:
- Prioridade do paciente
- Tempo de espera acumulado
- Disponibilidade do médico

---

6. Resultados Produzidos

Após a simulação, o sistema apresenta:

6.1 Estatísticas

Tempo médio de espera dos pacientes
Número total de pacientes atendidos
Tempo total de ocupação por médico
Taxa média de ocupação dos médicos

6.2 Gráficos

Distribuição dos tempos de espera
Ocupação total por médico
Evolução temporal das filas e da ocupação
Análise de sensibilidade (taxa de chegada vs espera média)

6.3 Relatórios

Tabela detalhada dos atendimentos
Exportação dos resultados para CSV
Previsão mensal apresentada em formato de calendário

---

7. Exportação de Dados

Os resultados podem ser exportados para um ficheiro:
relatorio_simulacao.csv

O ficheiro contém, para cada paciente:
- ID e nome
- Especialidade
- Prioridade
- Hora de chegada
- Hora de início e fim da consulta
- Duração da consulta
- Tempo de espera

---

8. Funcionalidades Adicionais

Importação de cenários personalizados em JSON
Geração automática de novos cenários
Análise de sensibilidade automática
Previsão de tempos médios de espera ao longo de um mês

---

9. Conclusão

Este simulador constitui uma ferramenta eficaz para o estudo e análise de sistemas de atendimento médico, permitindo avaliar o impacto de diferentes decisões operacionais. A flexibilidade do modelo, aliada à interface gráfica intuitiva e às capacidades de análise estatística, torna o sistema adequado para fins académicos e experimentais.
