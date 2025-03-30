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

#### Custos e dados financeiros (Julio: DONE)

O setor de saúde continua sendo o mais afetado por violação de dados, com um custo médio de US$ 9,77 milhões por incidente, o maior entre as indústrias, segundo o relatório da IBM "Cost of a Data Breach 2024". Embora tenha havido uma redução de 10,6% em relação a 2023, o valor ainda é mais que o dobro da média global de US$ 4,88 milhões.

O uso de IA e automação reduziu os custos das violações em até US$ 2,22 milhões e acelerou a detecção e contenção dos incidentes. A OMS reportou um aumento de 500% nos incidentes de segurança cibernética em instalações de saúde durante a pandemia de COVID-19, período em que a digitalização acelerada dos serviços criou novas vulnerabilidades.

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

### Riscos Cibernéticos na Saúde: Como se Diferenciam do OWASP Top 10

O OWASP Top 10 concentra-se principalmente em vulnerabilidades de aplicações web, enquanto o setor de saúde enfrenta desafios mais amplos, incluindo ransomware, IoT attacks e social engineering.

Apesar dessas diferenças, há pontos em comum, como code injection, authentication failures e vulnerable APIs, que também representam riscos significativos para sistemas médicos.

#### Ransomware

O maior risco para hospitais e clínicas. Os invasores criptografam dados críticos e exigem resgate para liberar o acesso.

Exemplo real: WannaCry afetou hospitais no mundo todo, paralisando serviços essenciais.

#### Phishing

E-mails fraudulentos são usados para enganar funcionários, médicos e administradores, levando-os a revelar credenciais ou instalar malware, o que pode resultar no comprometimento de redes hospitalares.

Exemplo real: Entre dezembro de 2020 e abril de 2021, a UC San Diego Health foi alvo de uma campanha de phishing que resultou no acesso não autorizado a contas de e-mail de funcionários. Os invasores puderam visualizar dados pessoais e médicos de pacientes, incluindo nomes, diagnósticos e informações de tratamento. A instituição notificou os indivíduos afetados e implementou medidas adicionais de segurança para prevenir futuros incidentes. ​

#### Outdated Software and Systems

Muitos hospitais usam sistemas legados sem atualizações, facilitando invasões.

Exemplo: O ataque via [CVE-2017-0199](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2017-0199) falha no Microsoft Office.

#### Man-in-the-Middle

Hackers interceptam dados médicos sigilosos entre dispositivos médicos e servidores.

Exemplo de ataque: Em 2016, pesquisadores demonstraram que dispositivos médicos conectados, como marcapassos e bombas de insulina, podiam ser alvo de ataques cibernéticos. Esses dispositivos, ao perderem autenticação com a unidade médica, podem ser interceptados, permitindo que atacantes ouçam, modifiquem ou bloqueiem comunicações.

#### IoT Device Attacks

Equipamentos como marcapassos, bombas de insulina e monitores cardíacos podem ser hackeados.

Exemplo de ataque: Estudos já mostraram que marcapassos conectados podem ser desativados remotamente.

#### Data Breach

Prontuários eletrônicos contêm dados sensíveis, e embora a LGPD e a HIPAA busquem proteger essas informações, vazamentos ainda ocorrem.

#### Engenharia Social

Funcionários são manipulados para fornecer acesso a hackers.

Exemplo de ataque: Alguém se passando por técnico de TI pedindo credenciais para "manutenção".

#### DDoS

Ataques sobrecarregam sistemas hospitalares, impedindo o acesso a registros médicos e prejudicando emergências, forçando os hospitais a pagar resgates para encerrar o ataque.

Exemplo real: em 2023, o Idaho Falls Community Hospital, localizado nos Estados Unidos, sofreu um ataque cibernético que levou ao desvio de ambulâncias para outras instituições. Os profissionais de saúde tiveram que registrar informações dos pacientes manualmente devido à falha nos sistemas informatizados.

#### Healthcare API Attacks

Falhas de autenticação em aplicativos médicos e sistemas de telemedicina podem permitir acesso não autorizado, enquanto APIs mal configuradas possibilitam o acesso a registros médicos e receitas digitais.

#### Malware on USB Devices and Internal Connections

Funcionários conectam pendrives infectados, instalando vírus nos sistemas hospitalares, enquanto hackers podem comprometer impressoras, câmeras e computadores administrativos para escalar privilégios.

## Referências

### 1. Cost of a Data Breach Report 2024

- Data: 2024
- Autor: IBM Corporation
- Link: https://www.ibm.com/reports/data-breach

### 2. The Cybersecurity Consolidation Conundrum: Why Less is Sometimes More

- Data: June 17, 2022
- Autor: Check Point Research Team
- Link: https://blog.checkpoint.com/security/the-cybersecurity-consolidation-conundrum-why-less-is-sometimes-more/

### 3. As 10 principais vulnerabilidades e exposições comuns exploradas rotineiramente

- Data: 2020
- Autor: Health ISAC
- Link: https://health-isac.org/pt/10-principais-vulnerabilidades-comuns-exploradas-rotineiramente/

### 4. Vulnerabilidades

- Data: Não informada
- Autor: Kaspersky
- Link: https://www.kaspersky.com.br/resource-center/threats/ransomware-wannacry

- Data: 2019
- Autor: Troy Brown
- Link: https://portugues.medscape.com/verartigo/6504044?form=fpf

- Data: 2025
- Autor: Michael Manchas (NCC Group)
- Link: https://www.nccgroup.com/us/the-top-5-cyber-security-concerns-for-the-healthcare-industry-in-2025-part-1/

**// TODO (winter): colocar todas referências**
