# Sistema baseado em blockchain para melhorar o tempo de atendimento pelos serviços públicos de saúde devido à falta de informatização do setor
Rodrigo César Reis <br>
Banco de Dados, 5ºSem <br>
Fatec São José dos Campos, 2021/1 <br>

# 1. INTRODUÇÃO
Agendamentos de consultas com especialistas dentro da rede pública de saúde podem demorar meses para acontecer (G1, 2018). A falta de prazo máximo para encaminhamento, exceto em casos de alguns tipos de câncer (JUSBRASIL, 2016), faz com que os pacientes fiquem sem perspectiva de atendimento e tratamento (G1, 2018)(A TRIBUNA, 2019).<br>

A falta de controle e supervisão dos pacientes em espera agrega ao problema, onde os registros são feitos em ferramentas insuficientes (CORREIO DO ESTADO, 2018), com 39% das instituições de saúde possuindo registros exclusivamente manuscritos (GALILEU, 2019).<br>

A demora no atendimento em casos oncológicos dificulta o tratamento e diminui as chances de recuperação do paciente (O TEMPO, 2019), o que poderia ser evitado com um melhor controle dos pacientes e dos especialistas.<br>

## 1.1 Objetivos
Com o Projeto que permite a digitalização de prontuários médicos (SENADO NOTÍCIAS, 2018) o desenvolvimento de uma ferramenta que reúna as informações dos pacientes atendidos pelo SUS se torna não só viável como necessário. Cada município deve controlar suas demandas da rede de saúde (O TEMPO, 2019) e alguns já utilizam ferramentas digitais para os prontuários, mas é possível coletar mais informações e utilizá-las para melhorar a qualidade do atendimento.<br>

Para isso, o objetivo deste trabalho é a implementação de um banco de dados que contenha os prontuários dos pacientes cadastrados no Sistema Único de Saúde, disponibilizando informações de seus históricos clínicos e especialidades para os quais precisam ser encaminhados, facilitando a comunicação entre unidades de atendimento e potencialmente agilizando os processos de encaminhamento dos pacientes para os especialistas. Disponibilizar o cadastro do paciente aos profissionais da saúde permitiria a evolução dos prontuários após consultas e atendimentos, mantendo atualizadas suas informações e necessidades.<br>

## 1.2 Conteúdo do trabalho
O presente trabalho está estruturado em seis capítulos:

### 2. Fundamentação Técnica:
Capítulo que aborda o conteúdo que fundamenta este trabalho.
### 3. Desenvolvimento:
Apresentação do desenvolvimento do trabalho, descrevendo as pesquisas realizadas e processos.
### 4. Resultados:
Exposição dos resultados obtidos e dados coletados.
### 5. Considerações Finais:
Apresentação das considerações, contribuições obtidas, conclusão do trabalho e possibilidades de continuidade.
### 6. Referências.

# 2. FUNDAMENTAÇÃO TÉCNICA
Neste capítulo serão abordados os conceitos fundamentais das tecnologias que serão utilizadas para o desenvolvimento do projeto. As soluções supracitadas são:<br>

## 2.1 Blockchain
Blockchain se trata de uma tecnologia para a criação de redes distribuídas e descentralizadas de informações. Entradas são feitas nesta rede de forma que as informações adicionadas são imutáveis e persistentes, sendo facilmente referenciáveis e não possibilitando quaisquer alterações retroativas, o que garante a confiabilidade daquela informação.
Dado que uma informação é inserida por um elemento e que seja armazenada na rede de blockchain, esta será replicada e se apresentará nos registros de todos os pares que compõem esta rede, formando um sistema peer-to-peer que autentica as informações através da replicação, utilizando um algoritmo de consenso.
### 2.1.1 Algoritmo de consenso
Algoritmos de consenso são elementos fundamentais na implementação de blockchains pois permitem que usuários ou máquinas em uma rede distribuída mantenham-se coordenados e sincronizados. Diferentemente do modelo adotado por bancos de dados centralizados onde existe um ou mais administradores com controle absoluto sobre os dados inseridos, um banco distribuído faz a validação dos dados inseridos passando por todos os nós que compõem a rede, onde cada um deles pode validar a legitimidade e autenticidade daquela informação e a creditar como confiável.

# 3. DESENVOLVIMENTO
## 3.1 IBM Blockchain Platform e Hyperledge Fabric
A solução proposta para o problema utilizará a ferramenta IBM Blockchain Platform para criação de registros em forma de smart contracts escritos pelo Hyperledge Fabric. Desta forma, todas as instituições que utilizarem do sistema terão acesso às mesmas informações gravadas no ledger que será replicado em cada uma das organizações desta rede. Todas as replicações deste ledger serão mantidas em sincronia utilizando um algoritmo de consenso.<br>

A natureza do blockchain faz com que as entradas feitas - neste caso as evoluções dos prontuários dos pacientes - sejam imutáveis e irreversíveis, impedindo alterações que não sejam feitas por futuras evoluções de prontuário. A replicação e validação dos contratos gerados pelo sistema garante que as informações dos pacientes não só sejam facilmente acessadas e utilizadas pelas partes interessadas como também garante sua persistência, eliminando atrasos no atendimento em decorrência de perda de documentos ou inconsistências em registros, comum em práticas que adotam um registro físico destas informações.

## 3.2 Aplicação
A aplicação faz a interface dos usuários com os _ledgers_. A utilização do sistema deve ser versátil e acessível, uma vez que seu objetivo é substituir modelos consolidados, simples e de baixo custo. Para que isso aconteça a aplicação será desenvolvida buscando um modelo multiplataforma utilizando front-end em AngularJS de modo que possa ser utilizada pela web nos computadores das unidades de saúde ou nos celulares dos profissionais se preciso for. Uma aplicação multiplataforma traz maior facilidade e versatilidade no acesso, tornando a solução mais convidativa. O back-end será feito utilizando Node, adotado tanto pela integração com Angular quanto com Hyperledger.

# 4. RESULTADOS

# 5. CONSIDERAÇÕES FINAIS

# 6. REFERÊNCIAS
ALMEIDA, S. **Familiares questionam demora e burocracia para atendimento médico pelo SUS**. Disponível em A Tribuna https://www.atribuna.com.br/cidades/saovicente/familiares-questionam-demora-e-burocracia-para-atendimento-médico-pelo-sus-1.74934 Acesso em: 02/12/2020.<br>
YAHN, N. **Espera por consulta demora até 7 anos, revela CGU**. Disponível em Correio do Estado https://correiodoestado.com.br/cidades/espera-por-consulta-no-sus-demorabr-ate-7-anos-revela-cgu/336933 Acesso em: 02/12/2020.<br>
OLIVEIRA, S.; MONTEIRO, L. **Medicina de dados: as promessas (e os desafios) do big data na saúde**. Disponível em Galileu https://revistagalileu.globo.com/Ciencia/Saude/noticia/2019/11/medicina-de-dados-promessas-e-os-desafios-do-big-data-na-saude.html Acessado em: 02/12/2020.<br>
**Marcar consulta com especialista é o maior problema no SUS, diz pesquisa**. Disponível em G1 http://g1.globo.com/jornal-nacional/noticia/2018/06/marcar-consulta-com-especialista-e-o-maior-problema-no-sus-diz-pesquisa.html Acessado em: 02/12/2020.<br>
POSOCCO ADVOGADOS ASSOCIADOS. **Vinte direitos dos pacientes: atendimento pelo SUS e particular**. Disponível em Jusbrasil  https://posocco.jusbrasil.com.br/noticias/407793198/vinte-direitos-dos-pacientes-atendimento-pelo-sus-e-particular Acessado em: 02/12/2020.<br>
LAGÔA, T. **Demora em diagnosticar câncer pelo SUS reduz chances de cura**. Disponível em O Templo https://www.otempo.com.br/cidades/demora-em-diagnosticar-cancer-pelo-sus-reduz-chances-de-cura-1.2229775 Acessado em: 02/12/2020.<br>
**Aprovada digitalização de prontuários médicos em hospitais**. Disponível em Senado Notícias https://www12.senado.leg.br/noticias/materias/2018/04/03/aprovada-digitalizacao-de-prontuarios-medicos-em-hospitais Acessado em: 02/12/2020.<br>
**Blockchain vs banco de dados: Entenda a diferença**. Disponível em 101 Blockchains https://101blockchains.com/pt/blockchain-vs-banco-de-dados/ Acessado em: 08/06/2021.<br>
**O que é um algoritmo de consenso**. Disponível em Binance Academy https://academy.binance.com/pt/articles/what-is-a-blockchain-consensus-algorithm Acessado em: 08/06/2021.<br>
