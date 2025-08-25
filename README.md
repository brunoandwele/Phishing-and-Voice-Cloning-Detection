# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **Uma abordagem multimodal para detecção de phishing e deepfakes em chamadas telefônicas** sob orientação do Professor **Prof. Dr.
Charles Henrique Porto Ferreira** e desenvolvido pelos seguintes alunos:

- Ana Beatriz Tavares Malheiro
- Bruno Andwele Alves Antunes

## Resumo

Nos últimos anos, o avanço das tecnologias de inteligência artificial transformou profundamente o cenário da cibersegurança.  
O **phishing**, uma técnica de engenharia social que explora vulnerabilidades humanas para obter informações confidenciais, tem se tornado cada vez mais sofisticado.  

Com a popularização das técnicas de **síntese de voz** e **deepfake**, criminosos agora podem criar áudios falsos extremamente convincentes, capazes de imitar a voz de pessoas conhecidas e, assim, aumentar a eficácia dos golpes. Esse cenário representa um desafio significativo para sistemas de detecção tradicionais, que geralmente analisam apenas o conteúdo textual ou apenas o sinal de áudio.

Este projeto propõe uma abordagem híbrida, combinando análise textual e análise de áudio bruto para detectar fraudes envolvendo *phishing* e *deepfake* de voz.  
A solução utiliza modelos avançados como **BERT** para análise semântica de transcrições, **Wave2Vec** para extração de características do áudio e um **Multilayer Perceptron (MLP)** para classificação em quatro categorias distintas, permitindo uma detecção mais precisa e robusta.

 
##  Propósito e Benefícios
O projeto tem como objetivo desenvolver uma solução automatizada para **detecção de golpes baseados em phishing e deepfakes de voz em chamadas telefônicas**.

**Principais benefícios para os usuários:**
- Aumento da **segurança** contra fraudes de engenharia social.
- **Identificação** de chamadas suspeitas, permitindo ações preventivas.
- Redução de prejuízos financeiros e vazamento de informações sigilosas.
- Melhoria da confiança em comunicações corporativas e pessoais.

---

## Problemas e Necessidades que o Produto Resolve
- Golpistas utilizam **phishing** para induzir vítimas a fornecer dados confidenciais.
- Avanços em **síntese de voz** e **deepfake** aumentam a credibilidade de ataques.
- Falta de soluções integradas que analisem **tanto o conteúdo textual quanto o áudio bruto**.
- Sistemas atuais de detecção tendem a focar apenas em um tipo de dado (texto ou áudio), reduzindo a eficácia.

---

## Características e Funcionalidades
1. **Análise Textual de Transcrições**  
   - Uso do modelo **BERT** para extrair o significado e padrões de linguagem suspeitos.
2. **Análise de Áudio Bruto**  
   - Uso do **Wave2Vec** para identificar características acústicas associadas a deepfakes.
3. **Classificação Multiclasse**  
   - Classificação das chamadas em quatro categorias:  
     1. Golpe e *deepfake*  
     2. Golpe sem *deepfake*  
     3. Não é golpe, mas é *deepfake*  
     4. Nem golpe, nem *deepfake*
4. **Processamento Multimodal**  
   - Combinação das saídas de análise textual e de áudio para aumentar a precisão.
5. **Interface de Monitoramento**  
   - Exibição dos resultados e histórico de chamadas analisadas.

---

## Tecnologias e Ferramentas Computacionais
- **Linguagem de programação**: Python
- **Modelos de IA**:
  - BERT (análise textual)
  - Wave2Vec (análise de áudio)
  - Multilayer Perceptron (classificação)
  - Whisper (Transcrição textual)
- **Bibliotecas e Frameworks**:
  - PyTorch ou TensorFlow
  - Transformers (Hugging Face)
- **Ambiente de desenvolvimento**: Jupyter Notebook, VS Code
- **Controle de versão**: Git/GitHub

---

## Contexto de Uso
- **Usuários**:
  - Equipes de segurança da informação
  - Empresas com alto volume de chamadas de clientes
  - Organizações governamentais e financeiras
- **Tarefas**:
  - Analisar chamadas recebidas
  - Classificar chamadas como seguras ou suspeitas
- **Equipamentos (hardware, software e materiais)**:
  - Servidor ou máquina com GPU para treino e execução de modelos

---

## Benefícios Esperados
- Detecção mais precisa de chamadas fraudulentas.
- Redução do impacto financeiro e de danos à reputação de empresas e indivíduos.
- Aplicação prática de tecnologias de IA para segurança digital.

## Público-alvo
- Organizações que realizam atendimento por telefone e lidam com informações sensíveis.
- Empresas de médio e grande porte, especialmente nos setores financeiro, telecomunicações e tecnologia.
- Áreas jurídicas: departamentos de compliance, escritórios de advocacia e autoridades policiais que necessitam de provas técnicas para investigações e processos.

## Análise de concorrência
**Principais soluções no mercado:**
### **Pindrop**  
- **Foco**: Antifraude, autenticação de chamadas e detecção de deepfakes.  
- **Preços**:  
  - US$ 100k – Call Verification (1M chamadas/ano)  
  - US$ 275k – Anti-Fraud (1–2M chamadas/ano)  
  - US$ 325k – Anti-Fraud + Deepfake (1–2M chamadas/ano)  
- **Feedbacks**: Gartner Peer Insights – bom desempenho na detecção de fraude, porém integração complexa.  
- **Pontos Positivos**: Alta acurácia (99,2% em materiais de marketing), clientes enterprise.  
- **Pontos Negativos**: Custos elevados, rollout complexo.  

### **Nuance Gatekeeper (Microsoft)**  
- **Foco**: Biometria de voz (ativa e passiva), detecção de fraude e fala sintética.  
- **Preços**: Sob cotação (modelo por usuário).  
- **Feedbacks**: Diretórios como TrustRadius e G2 – usado em escala por contact centers.  
- **Pontos Positivos**: Autenticação em ~1s, escala comprovada em IVR.  
- **Pontos Negativos**: Preço pouco transparente, integração com legados pode ser complexa.  

### **Veridas**  
- **Foco**: Autenticação biométrica de voz em ~3 segundos.  
- **Preços**: Sob cotação (disponibiliza ROI calculator).  
- **Feedbacks**: Gartner Peer Insights e Capterra – avaliações positivas em usabilidade.  
- **Pontos Positivos**: Integrações nativas com cloud contact centers, validação rápida.  
- **Pontos Negativos**: Pouca transparência nos preços, benchmarks limitados.  

### **ID R&D (Mitek)**  
- **Foco**: Detecção de deepfakes, falsificação de áudio e liveness multimodal.  
- **Preços**: Sob cotação (SDKs e containers).  
- **Feedbacks**: Reconhecido em testes independentes (NIST/DHS).  
- **Pontos Positivos**: Destaque em testes de liveness e PAD, detecção de ataques por injeção.  
- **Pontos Negativos**: Custos não divulgados, exige conhecimento técnico para integração.  

## Limitações gerais das soluções existentes 
- Foco restrito: a maioria analisa apenas áudio ou biometria, não combinando texto e voz.  
- Dependência da qualidade do áudio: ruídos ou gravações ruins podem afetar a detecção.  
- Proprietário e pouco transparente: modelos fechados dificultam personalização e compreensão.  
- Custos altos e escalabilidade limitada, exigindo hardware ou licenças caras.  
- Integração complexa com sistemas internos.  
- Atualização constante necessária devido à evolução rápida de *deepfakes*.  

## Tendências de Mercado  
- Tentativas de fraude com deepfakes cresceram **+1300% em 2024**.  
- Regulamentações como o **EU AI Act** exigem rotulagem de conteúdos sintéticos.  
- Golpes de alto impacto envolvendo **áudio e vídeo falsificados** vêm se tornando mais frequentes. 

## Benefícios esperados
- Melhorar a detecção de golpes com voz falsificada.
- Apoiar investigações e processos jurídicos com evidências técnicas.
- Contribuir para estudos acadêmicos na área de segurança digital e IA multimodal.
- Oferecer uma base para sistemas mais robustos no futuro.

## Personas
A seguinte descrição de personas utiliza o modelo de Mapa de Empatia para detalhar os principais grupos de usuários da solução de detecção de phishing e *deepfakes* em chamadas telefônicas.  
![Mapa de empatia](empatia.png)

O objetivo é compreender as necessidades, dores, comportamentos e expectativas de cada persona, permitindo o desenvolvimento de uma ferramenta mais eficaz e alinhada ao contexto de uso.  
As personas estão divididas em:  

- **Primárias:** Segurança da Informação e Jurídico/Compliance, responsáveis por decisões estratégicas e validação jurídica.  
- **Secundária:** Operadores de Call Center, usuários operacionais que interagem diretamente com chamadas suspeitas.

### Primária - Profissional de Segurança da Informação em uma empresa de médio porte

**O que vê:**

- Ambiente corporativo com ferramentas de segurança.
- Produção e analise de relatórios de incidentes e auditorias.
- Concorrentes que já utilizam soluções avançadas de proteção.

**O que ouve:**

- Demandas sobre redução de riscos.
- Reclamações de colaboradores sobre golpes e chamadas suspeitas.
- Notícias sobre novas técnicas de deepfake e fraudes digitais.

**O que diz e faz:**

- Cobra soluções eficazes para mitigar riscos.
- Participa de reuniões estratégicas sobre cibersegurança.
- Defende investimentos em tecnologias emergentes.

**O que pensa e sente:**

- Preocupação constante em evitar brechas que prejudiquem a reputação da empresa.
- Insegurança sobre até que ponto as soluções atuais dão conta das ameaças.
- Desejo por inovação.

**Dores:**

- Soluções caras e difíceis de integrar com os sistemas existentes.
- Baixa transparência nos relatórios de ferramentas concorrentes.
- Pressão de compliance e risco jurídico em caso de falha.

**Ganhos:**

- Ter uma solução acessível, multimodal e auditável.
- Redução significativa do risco de fraude por voz.
- Capacidade de demonstrar resultados claros à diretoria.

### Primária – Profissional da área Jurídica / Compliance

**O que vê:**
- Processos judiciais e arbitrais envolvendo fraude digital.  
- Casos de seguros, cartões de crédito e bancos contestados por clientes.  
- Relatórios técnicos inconclusivos sobre autenticidade de áudios em chamadas telefônica.  

**O que ouve:**
- Demandas de advogados, seguradoras e instituições financeiras por provas robustas.  
- Relatos de clientes alegando clonagem de voz ou golpes por telefone.  
- Pressão de juízes e reguladores por evidências técnicas confiáveis.  

**O que diz e faz:**
- Conduz investigações sobre se o golpe envolveu ou não *deepfake*.  
- Solicita laudos periciais e relatórios de autenticidade de áudios.  
- Usa evidências para sustentar defesa, acusação ou decisões de compliance.  

**O que pensa e sente:**
- Insegurança quanto à validade jurídica de tecnologias de detecção.  
- Preocupação em evitar injustiças ou responsabilizações indevidas.  
- Necessidade de ferramentas auditáveis e aceitas como prova legal.  

**Dores:**
- Falta de métodos confiáveis para diferenciar áudios reais de falsos.  
- Risco de não conseguir comprovar fraude em processos de alto valor.  
- Lacunas legais sobre uso de *deepfake detection* em tribunais.  

**Ganhos:**
- Evidências técnicas claras e auditáveis para uso jurídico.  
- Redução de fraudes em seguros, bancos e contratos.   

### Secundária – Operador de Call Center / Atendimento

**O que vê:**
- Sistemas de atendimento com dados de clientes.
- Scripts de chamadas e metas de desempenho.
- Clientes confusos ou irritados por fraudes e golpes.

**O que ouve:**
- Reclamações de clientes sobre tentativas de fraude.
- Orientações de supervisores sobre como agir em situações suspeitas.
- Pressão por agilidade e cumprimento de indicadores (tempo médio de atendimento, satisfação etc.).

**O que diz e faz:**
- Segue protocolos de validação de identidade, mas nem sempre consegue evitar golpes.
- Reporta suspeitas de fraude ao time de segurança ou supervisão.
- Tenta tranquilizar clientes em situações de risco.

**O que pensa e sente:**
- Sente-se inseguro quando não consegue diferenciar clientes reais de fraudadores.
- Ansiedade por cometer erros que prejudiquem clientes ou a empresa.
- Desejo de ferramentas que facilitem identificar tentativas de fraude sem aumentar a burocracia.

**Dores:**
- Processos manuais lentos que prejudicam a experiência do cliente.
- Falta de clareza ou feedback imediato sobre a validade da chamada.
- Pressão por produtividade x responsabilidade de detectar fraude.

**Ganhos:**
- Ferramenta automática que auxilia na validação do cliente.
- Redução do estresse e da responsabilidade individual em detectar fraude.
- Melhora da experiência do cliente e confiança no atendimento.

## Contexto de Uso

- **Ambiente:**
  - Corporativo: Segurança da Informação e Jurídico/Compliance em empresas.  
  - Operacional: Call centers que lidam com clientes e verificações de identidade.  
  - Público geral: usuários comuns validando áudios suspeitos em dispositivos móveis.  

- **Contexto social, econômico e cultural:**
  - Empresas precisam cumprir LGPD/GDPR e proteger clientes contra fraudes.  
  - Usuários finais expostos a golpes digitais sofisticados, buscando confiança em transações.  
  - Crescente preocupação social sobre deepfakes e fraudes por telefone.  

- **Informações que o sistema deve guardar antes da interação:**
  - Histórico de áudios e chamadas analisadas.  
  - Dados básicos do cliente ou usuário (ID, número da chamada, data/hora).  
  - Parâmetros de detecção, limiares de confiabilidade e logs de análise.  

- **Situação do ambiente durante a interação:**
  - Call centers atendendo clientes em tempo real.  
  - Profissionais de segurança/jurídico avaliando casos suspeitos.  
  - Usuários finais recebendo alertas ou validando áudios em seus dispositivos.  

## Jornada do Usuário

1. **Início da interação:**
   - Usuário recebe áudio suspeito ou chamada.  
   - Abre a ferramenta de detecção de phishing / deepfake.  

2. **Execução da tarefa:**
   - Faz upload do áudio ou insere informações da chamada.  
   - Sistema realiza análise multimodal:  
     - Transcrição e análise textual via BERT.  
     - Análise de áudio bruto via Wave2Vec.  
   - Modelo MLP processa resultados e classifica a ocorrência.  

3. **Resultados e feedback:**
   - Indica se o áudio é suspeito ou legítimo e se há indícios de *deepfake*.  
   - Gera relatórios para decisão imediata (usuário comum) ou auditoria jurídica (profissionais primários).  

4. **Conclusão da tarefa:**
   - Usuário toma decisão: bloqueia/aprova, reporta ou encaminha para investigação.  
   - Histórico e logs ficam armazenados para futuras consultas ou processos legais.  




 
## Coleta de dados

## Modelo de tarefas

## Design

- Pense nas características de Affordances do seu serviço ou poduto. 
    - Que tipo de acessibilidades devem ser consideradas dentro do seu projeto?
- Discuta o papel das expectativas do usuário no projeto deste serviço ou poduto. Qual a importância e pontos a serem considerados se você quiser vender esse serviço ou poduto?

### Prototipação em baixo nível (papel)
#### Avaliação heurística

### Prtotipação em médio nível (Figma)
#### Avaliação heurística

### Prtotipação em alto nível (React)
#### Avaliação heurística

[^1]: Fonte: Adaptado de <https://hazeshift.com.br/mapa-de-empatia/>

<!-- TODOs:
- Add exemplos
 -->
