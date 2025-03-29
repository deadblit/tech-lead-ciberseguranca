# Projeto Executivo: SOC para [Nome do Hospital Fictício]

### Estruturação Estratégica de um Security Operations Center (SOC)
### em Ambiente Hospitalar

<br><br><br><br>

**Apresentado por:**  
- Amarildo Lucena - [ajfl@cesar.school](mailto:ajfl@cesar.school)
- Julio Vilar - [jvmm@cesar.school](mailto:jvmm@cesar.school)
- Rafael Winter - [rwt@cesar.school](mailto:rwt@cesar.school)


**Instituição:**  
[Nome da Instituição de Ensino]

<br><br>

**Data:**  
[Mês/Ano]

## Sumário

(fazer por último)

## Introdução

### Contextualização (temporário)

O setor de saúde tem se tornado um alvo cada vez mais atrativo para ataques cibernéticos devido ao alto valor dos dados de pacientes, à crescente digitalização dos serviços médicos e à dependência crítica de sistemas tecnológicos para procedimentos e atendimentos. Hospitais são particularmente vulneráveis devido à combinação de dados sensíveis, sistemas legados, dispositivos médicos conectados (IoMT) e o impacto potencialmente fatal de interrupções operacionais.

#### Custos e dados financeiros (Julio)

De acordo com o relatório da IBM "Cost of a Data Breach 2024", o setor de saúde continua mantendo o título de indústria com o maior custo médio de violação de dados pelo 14º ano consecutivo, atingindo US$ 9,77 milhões por incidente. Mesmo representando uma leve redução de 10,6% em relação a 2023, este valor permanece mais que o dobro da média global de US$ 4,88 milhões por incidente (que, por sua vez, aumentou 10% em relação ao ano anterior). O tempo médio global para identificar e conter uma violação de dados diminuiu para 258 dias em 2024, uma redução em relação aos 277 dias do ano anterior, mas o setor de saúde continua enfrentando desafios específicos devido à complexidade de seus ambientes. O relatório também destaca que o uso de IA e automação reduziu significativamente os custos de violação de dados em até US$ 2,22 milhões e acelerou a detecção e contenção de incidentes em média 98 dias. A Organização Mundial da Saúde (OMS) reportou um aumento de 500% nos incidentes de segurança cibernética em instalações de saúde durante a pandemia de COVID-19, período em que a digitalização acelerada dos serviços criou novas vulnerabilidades.

**// TODO (julio): revisar e sumarizar parágrafo acima**

#### Consequencias de ataques e cases (Amarildo)

Segundo relatórios recentes, ataques ransomware contra instituições de saúde aumentaram significativamente nos últimos anos, com consequências que vão desde o cancelamento de cirurgias até o redirecionamento de ambulâncias. Violações de dados expõem informações médicas confidenciais, que possuem valor persistente no mercado negro, diferentemente de dados financeiros que podem ser rapidamente invalidados. Um registro médico completo pode valer até 50 vezes mais que um número de cartão de crédito no mercado negro.

Casos notáveis como o do Hospital Universitário de Düsseldorf em 2020, onde um ataque ransomware resultou na morte de uma paciente que precisou ser transferida quando os sistemas do hospital ficaram inacessíveis, evidenciam o potencial letal dessas ameaças. No Brasil, ataques como o sofrido pela Rede D'Or São Luiz em 2021 demonstram que nenhuma instituição está imune, independentemente de seu porte ou recursos.

**// TODO (amarildo): revisar e expandir os dois parágrafos acima - e falar sobre o incidente da Rede D'Or**

#### Influência da pandemia, evolução tecnológica e cenário regulatório (Winter)

A expansão da telemedicina, acelerada durante a pandemia, introduziu novos vetores de ataque, com dispositivos remotos nem sempre adequadamente protegidos. Paralelamente, o aumento de equipamentos médicos conectados (IoMT) - de bombas de infusão a marcapassos - ampliou significativamente a superfície de ataque. Estima-se que um hospital médio possua entre 10 e 15 dispositivos conectados por leito, muitos dos quais com vulnerabilidades conhecidas e sem possibilidade de atualização.

O cenário regulatório também evoluiu com a implementação da Lei Geral de Proteção de Dados (LGPD) no Brasil, estabelecendo obrigações específicas para o tratamento de dados sensíveis de saúde e impondo sanções severas para violações, que podem chegar a 2% do faturamento anual, limitado a R$ 50 milhões por infração.

Este contexto de ameaças sofisticadas, superfícies de ataque expandidas e requisitos regulatórios rigorosos torna imperativa a implementação de um Centro de Operações de Segurança (SOC) dedicado e especializado para ambientes hospitalares.

### Perfil do Hospital

**// TODO (amarildo): ver o hospital de House**

O Hospital Princeton-Plainsboro (HPP) é uma instituição de grande porte localizada em uma capital brasileira, e faz parte da liga Ivy League, com capacidade para 350 leitos, sendo 50 de UTI. O hospital possui diversas especialidades médicas, com destaque para cardiologia, oncologia e neurocirurgia. A instituição conta com cerca de 1.500 funcionários e atende aproximadamente 15.000 pacientes mensalmente.

Em termos tecnológicos, o HPPT possui:
- Sistema de Prontuário Eletrônico de Paciente (PEP)
- Sistema de Gestão Hospitalar (ERP)
- Equipamentos médicos conectados à rede
- Plataforma de telemedicina
- Diversos sistemas departamentais (laboratório, farmácia, radiologia)
- Infraestrutura híbrida com serviços em nuvem e on-premises

### Objetivos do Projeto

Este projeto executivo visa estabelecer um Security Operations Center (SOC) personalizado para o Hospital Central Tecnológico, com foco em:

1. Proteger dados sensíveis de pacientes e informações clínicas
2. Garantir a disponibilidade ininterrupta de sistemas críticos para o atendimento
3. Detectar e responder rapidamente a ameaças cibernéticas específicas do setor hospitalar
4. Assegurar conformidade com a LGPD e outras regulamentações aplicáveis
5. Desenvolver capacidades internas para monitoramento, detecção e resposta a incidentes
6. Estabelecer protocolos de cooperação para compartilhamento de informações sobre ameaças

O SOC proposto será dimensionado para as necessidades específicas do HCT, considerando seus recursos tecnológicos, humanos e financeiros, bem como os riscos específicos ao seu ambiente operacional.

## Referências

### 1. Cost of a Data Breach Report 2024

- Data: 2024
- Autor: IBM Corporation
- Link: https://www.ibm.com/reports/data-breach

### 2. The Cybersecurity Consolidation Conundrum: Why Less is Sometimes More

- Data: June 17, 2022
- Autor: Check Point Research Team
- Link: https://blog.checkpoint.com/security/the-cybersecurity-consolidation-conundrum-why-less-is-sometimes-more/

**// TODO (winter): colocar todas referências**
