# Desafio Engenheiro Back-End Pleno 👩‍💻

### Primeiramente, agradecemos seu interesse em se tornar um membro da equipe.

### Sobre a empresa e o ambiente de trabalho geral 🚀

Somos a GDM, uma empresa especializada em marketing digital voltada para o mercado de iGaming. Prestamos serviços para grandes players do setor, como CassinoPix e Bet7k. No nosso time de gestão de tráfego, por exemplo, os gestores têm o costume de investir mais de **meio milhão** de reais por dia em tráfego pago. Estamos em plena expansão exponencial e nossa equipe é composta pelos melhores profissionais em suas áreas. Se você for escolhido, é porque acreditamos que você também é um dos melhores na sua especialidade.

Nossa empresa é altamente competitiva. Não nos contentamos apenas com grandes investimentos em tráfego pago — buscamos a excelência em tudo o que fazemos e queremos levar os melhores junto conosco. Valorizamos a entrega pontual e a alta qualidade em cada projeto. Apesar da intensidade do ambiente de trabalho, cultivamos uma cultura de colaboração e apoio mútuo. Aqui, todos se ajudam na medida do possível, e temos o suporte total da diretoria e da coordenação. Sabemos equilibrar a pressão de um mercado competitivo com um ambiente leve e descontraído no dia a dia.

### Sobre o ambiente de trabalho no departamento de T.I ☕

O departamento de TI da GDM reflete a cultura colaborativa da empresa, sendo composto por profissionais altamente qualificados, cada um com profunda expertise em suas respectivas áreas de tecnologia. O que realmente destaca esses profissionais, além de seu vasto conhecimento técnico, é a humildade com que compartilham suas habilidades. Nosso objetivo no setor de TI é manter um equilíbrio saudável entre expertise individual e colaboração, promovendo um crescimento coletivo, como uma verdadeira família tecnológica.

Nossa equipe é formada por dois Engenheiros Front-End com um nível excepcional de conhecimento em tecnologias e ferramentas de ponta. Aqui na GDM, nosso front-end é desenvolvido utilizando React.js e Next.js, garantindo interfaces robustas e de alto desempenho.

Contamos também com um Arquiteto de Software que possui uma vasta experiência no setor de iGaming e uma bagagem impressionante de conhecimento. Seu talento para arquitetar soluções eficazes e inovadoras é notável, sendo um profissional de excelência no desenvolvimento Back-End (stack JS), DevOps e infraestrutura em nuvem AWS.

Além disso, temos um Engenheiro Back-End que domina com maestria a stack de JavaScript para desenvolvimento server-side e automação de infraestrutura, contribuindo para a construção de sistemas robustos e escaláveis.

Esse conjunto de competências e talentos nos posiciona como uma equipe altamente preparada para enfrentar desafios tecnológicos e criar soluções impactantes.

### Descrição 📰

Se você pensa que o papel de um Engenheiro Back-End se resume a criar C.R.U.D. e consumir APIs, está muito enganado. Estamos procurando alguém que vá além, com habilidade de pensar sistemicamente e atuar de forma crítica em todo o ciclo de desenvolvimento de soluções robustas, escaláveis e orientadas a resultados.

#### Desafio: Desenvolvimento de Aplicação para Processamento de Dados em Batch

Você encontrará em nosso repositório um arquivo .csv contendo 2 milhões de linhas e 3 colunas. Seu desafio como engenheiro back-end será desenvolver duas aplicações utilizando NestJS, aplicando os princípios de DDD (Domain-Driven Design) e SOLID, para processar, tratar e armazenar esses dados.

#### Descrição do desafio:
Aplicação 1 - Leitura e Envio dos Dados:
* O seu papel é desenvolver uma aplicação que seja capaz de:
* Ler o arquivo .csv com eficiência.
* Processar os dados, tratando qualquer inconsistência.
* Dividir os dados em batches de 1000 registros, respeitando o limite de envio de 1000 dados por segundo para a segunda aplicação.
* Enviar esses batches para a segunda aplicação por meio de uma interface de comunicação (como uma API REST ou mensageria).

Aplicação 2 - Recepção e Armazenamento dos Dados:
- **A segunda aplicação já possui parte do código implementado, mas precisa ser completada.**

- Esta aplicação será responsável por:

- * Receber os batches de dados da primeira aplicação.
- * Processar e armazenar os dados recebidos em um banco de dados não relacional, preferencialmente MongoDB.
- * O dado que será armazenado no banco é o nome dos estados presentes no arquivo .csv, juntamente com a quantidade total de pessoas para cada estado (i.e., um somatório de pessoas por estado).

#### Requisitos Técnicos:
* Ambas as aplicações devem ser desenvolvidas em NestJS, seguindo os padrões de arquitetura DDD e aplicando os princípios de SOLID.
* Cada aplicação deve incluir uma imagem Docker e um Dockerfile para facilitar o empacotamento e a execução em containers.
* Se desejar, pode incluir um docker-compose para cada uma das aplicações, o que facilitará a simulação do deploy na AWS.
* A comunicação entre as duas aplicações pode ser feita via HTTP, gRPC, ou através de algum sistema de mensageria (como RabbitMQ ou Kafka), à sua escolha, desde que seja justificada e eficiente para o envio em batches.

#### Etapas:
1. Leitura de Dados (Aplicação 1):
- * Ler o arquivo .csv com 2M de linhas de maneira eficiente, evitando carregar o arquivo inteiro na memória de uma vez.
* Processar os dados para garantir sua integridade (tratar dados nulos, duplicados, etc.).
* Implementar uma lógica de envio dos dados em batches de 1000 registros por segundo para a segunda aplicação.

2. Armazenamento e Processamento (Aplicação 2):

* Completar a aplicação para que ela possa receber os dados enviados pela primeira aplicação em batches.
* Armazenar as informações no MongoDB, salvando a quantidade total de pessoas por estado.
* Garantir que a aplicação seja capaz de lidar com grande volume de dados sem perda ou duplicidade.

3. Deploy e Execução:

* Criar Dockerfiles para ambas as aplicações, garantindo que elas possam ser empacotadas e executadas em containers de forma isolada.
* Opcionalmente, criar um docker-compose para simular o ambiente de produção.
* Certifique-se de que a solução seja escalável e eficiente para um possível deploy na AWS.

#### Considerações:
A solução deve ser testável e escalável, garantindo que possa suportar o envio contínuo de dados em batch.
Utilize boas práticas de desenvolvimento, como testes unitários, tratamento de erros, e logs para monitorar o comportamento das aplicações.
Documente a solução para facilitar a compreensão e o deploy por outros desenvolvedores ou engenheiros.

#### O que será avaliado:
* Qualidade do código, organização e aderência aos princípios de DDD e SOLID.
* Eficiência na leitura e processamento dos dados do arquivo .csv.
* Capacidade de enviar os dados em batches respeitando o limite de 1000 registros por segundo.
* Implementação do armazenamento eficiente dos dados no banco de dados MongoDB.
* Uso adequado de containers Docker e, se aplicável, docker-compose.

**Boa sorte!**

### Requisitos Técnicos 😁

- NodeJS ✔
- TypeScript ✔
- Nest.JS ✔
- Docker ✔
- MongoDb ✔

### Requisitos comportamentais

- Aprendizado continuo
- Empatia

### Diferenciais 💖

-

### Próximos passos

1. Enviar o link do repositório para: ;
2. .

![Alt Text](https://media0.giphy.com/media/bGgsc5mWoryfgKBx1u/200w.gif?cid=6c09b952b9ldwmlfeyplodki2qm3x1fcknis1hr0ow41lk9w&ep=v1_gifs_search&rid=200w.gif&ct=g)
