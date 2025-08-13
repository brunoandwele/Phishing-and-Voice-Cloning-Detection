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
 
- **Ambiente físico e social**:
  - Uso em centrais de atendimento, ambientes corporativos e plataformas de comunicação remota
  - Possível integração com sistemas internos de segurança

---

## Benefícios Esperados
- Detecção mais precisa de chamadas fraudulentas.
- Redução do impacto financeiro e de danos à reputação de empresas e indivíduos.
- Aplicação prática de tecnologias de **IA** para segurança digital.

## Público-alvo
- Organizações que realizam atendimento por telefone e lidam com informações sensíveis.
- Empresas de médio e grande porte, especialmente nos setores financeiro, telecomunicações e tecnologia.
- **Áreas jurídicas**: departamentos de compliance, escritórios de advocacia e autoridades policiais que necessitam de provas técnicas para investigações e processos.
- Necessidade de prevenir fraudes e se adequar a normas de segurança.

---

## Análise de concorrência
**Principais soluções no mercado:**
- **Pindrop** – detecção de fraude por voz usando análise acústica.
- **Nuance Gatekeeper** – autenticação e detecção de fraude com biometria de voz.
- **Veridas** – biometria de voz para autenticação.
- **ID R&D** – detecção de *deepfakes* e falsificação de áudio.

**Observações:**
- Soluções existentes são eficazes, mas muitas não combinam análise textual e acústica.
- Custos podem ser altos, limitando o acesso de pequenas empresas.
- Há espaço para abordagens de código aberto com foco em pesquisa acadêmica.

---

## Benefícios esperados
- Melhorar a detecção de golpes com voz falsificada.
- Apoiar investigações e processos jurídicos com evidências técnicas.
- Contribuir para estudos acadêmicos na área de segurança digital e IA multimodal.
- Oferecer uma base para sistemas mais robustos no futuro.

### Personas

- Descreva as personas que irão interagir com a aplicação ou produto. Deixe claro suas principais caracteristicas e contextos sociais, econômicos e culturais.
- Quais informações sobre o usuário o serviço ou poduto deve guardar?

  - Persona primaira ...
  - Persona secundária ...
  - Outras personas ...

### Mapa de empatia

![Mapa de empatia](empatia.png)

- Determine o mapa de empatia[^1] de pelo menos uma persona primária e uma sercundária.
  - O que o usuário vê: aqui estamos falando do ambiente visual em que o usuário se encontra. Ou seja, o que ele efetivamente enxerga, as pessoas e objetos que estão ao seu redor. Isso ajuda a entender o contexto em que o usuário está inserido e as influências visuais que está recebendo.
  - O que o usuário ouve: neste quadrante, buscamos entender o que o usuário está ouvindo, os sons que o cercam e como eles influenciam suas ações.
  - O que o usuário diz e faz: aqui consideramos ações e comportamentos que o usuário apresenta durante sua interação com serviço ou poduto.
  - O que o usuário pensa e sente: neste quadrante, buscamos entender os pensamentos, sentimentos, emoções e percepções que o usuário tem em relação ao serviço ou poduto. Quais expectativas o usuário cria sobre o serviço ou poduto?
  Que tipo de serviço ou poduto mais agrada essa persona?
  - Dores: quando falamos sobre dores do usuário, estamos fazendo referência a quaisquer obstáculos, necessidades ou frustrações que o usuário possa experimentar ao tentar realizar uma tarefa ou alcançar um objetivo. Isso inclui, por exemplo, problemas de usabilidade, dificuldades de acesso ou outros desafios que podem afetar a experiência do usuário.
  - Ganhos: nesse caso estamos falando de quaisquer benefícios ou recompensas que o usuário possa experimentar ao utilizar o serviço ou poduto. Isso pode incluir economia de tempo ou facilidade de uso, por exemplo. Que desejos do usuário o serviço ou poduto satisfaz?

## Contexto de uso

- Descreva o ambiente em que o serviço ou poduto deve ser utilizado.
- Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?
- Quais informações sobre o ambiente, o serviço ou poduto deve guardar antes de iniciar a interação?
- O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou poduto?

## Jornada do usuário

- Criar uma narrativa para o o seu serviço ou poduto com o usuário.
- Determine o que o usuário realiza desde a primeira até o última interação com o serviço ou poduto.
  - Descreva o que acontece ou pode acontecer passo a passo
  - Como a tarefa começa? Como a tarefa se desenvolve? Como a tarefa termina?


<!--
## Análise de concorrência

- Pesquise serviços ou podutos existentes atualmente que possam realizar o objetivo deste projeto.
- Selecione pelo menos 3 serviços ou podutos diferentes.
- Em relação aos concorrentes, respondam as seguintes perguntas?
  - Existe plataforma similar que atende o mesmo mercado e funcionalidades? Se sim: Quais os pontos positivos? Quais os pontos negativos?
  - Existe plataforma diferente quanto ao serviço, mas que atenda esse mercado? Se sim: Quais os pontos positivos? Quais os pontos negativos?
 -->
 
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
