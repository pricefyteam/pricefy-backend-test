# Teste de código para Engenharia de Back-end na Pricefy
 
*by [Leandro Silva](https://leandrosilva.com.br/), CTO.*
 
Antes de mais nada, você deve estar se perguntando: **por que eu trabalharia na [Pricefy](https://www.pricefy.com.br/)?** Com tantas ofertas por aí, mercado de tecnologia super aquecido, não só no Brasil, mas no exterior, **por que a [Pricefy](https://www.pricefy.com.br/)?**
 
Ótima pergunta! Que só você poderá responder a si mesmo. Mas, claro, eu posso compartilhar com você um pouco dos meus motivos e, quem sabe, eles te levam a encontrar os seus próprios.
 
* Estamos resolvendo problemas reais, de pessoas comuns, como eu e você, que ralam dia após dia em diversos segmentos varejistas do país, para criar promoções atrativas e comunicá-las de modo inteligente aos seus clientes. Hoje, são centenas de drogarias, supermercados, casas de materiais para construção, lojas de brinquedos, sacolões, etc, espalhados por todo Brasil, gerando 10 a 15 milhões de cartazes todos os meses;
 
* Com as nossas soluções, ajudamos o varejista a diminuir seu custo de operação e acelerar a execução de suas promoções, o que, potencialmente, afeta positivamente os preços de suas promoções, beneficiando seus clientes com preços mais atrativos lá na ponta; e todo mundo ganha com isso;
 
* Somos uma pequena **retail tech**, com pouco mais de 4 anos de vida, dentro de uma grande empresa, [a maior integradora de outsourcing de TI do Brasil](https://selbetti.com.br/), com mais de 40 anos de estrada. Isso nos dá dinamismo para ousar e inovar com nossos produtos, mas estabilidade, para dormirmos tranquilos, sabendo que amanhã ainda teremos nossos empregos, já que temos sólidos investimentos financeiros nos suportando;
 
* Sendo um grupo jovem e relativamente pequeno, temos participação ampla em discussões sérias sobre o nosso futuro, novos produtos, planejamento tático, problemas atuais, construção de soluções, etc. Tudo é muito aberto, muito claro e muito acessível;
 
* Temos bastante espaço para aprender, compartilhar e crescer. Conforme o grupo cresce, crescemos individualmente, tanto financeiramente quanto em nossas habilidades profissionais;
 
* Em uma big tech, eu seria um bom engenheiro, líder, gestor e contribuiria, sim, com grandes produtos. Isso é verdade. Mas aqui, eu faço a diferença. Aqui, uma contribuição minha, um commit meu, pode fazer um grande diferencial lá na ponta, no dia a dia do meu cliente, e do cliente do meu cliente, pessoas que, como eu e você, recorrem a varejistas para trazer para casa isso e aquilo que precisam, sempre buscando o melhor *preço vs benefício*;
 
* Tecnologia! Ahhh tecnologia... Utilizamos tecnologias modernas, como qualquer outra tech startup, porque Cloud Computing e Open Source cuidaram de democratizar o acesso a essas maravilhas. Sim, rodamos 100% em cloud desde o primeiro dia; usamos muito open source; e estamos o tempo todo inventando maneiras de fazer o nosso trabalho melhor, discutindo técnicas de programação, abordagens de design e arquitetura de sistemas e, lógico, como resolver nossos problemas de escalabilidade: cartazes aos milhões, filas de impressão aos milhares, usuários às centenas de milhares;
 
* Desafio aqui é o que não falta. Espaço para opinar e inovar também!
 
O que acha? Isso te empolga?

## Um pouco mais sobre a tecnologia por trás da Pricefy

* ProdOps ⎼ Engenharia e Produto com Leandro Silva ([link 1](https://www.youtube.com/watch?v=2IxX2f0ZckQ) e [link 2](https://www.youtube.com/watch?v=jOeuK2U8vI8))
* ElvenWorks ⎼ Conhecendo a tecnologia por trás de uma solução muito inteligente de Precificação ([link](https://www.youtube.com/watch?v=DCT0IoRcrUo))

## Processo Seletivo
 
O processo seletivo da engenharia da [Pricefy](https://www.pricefy.com.br/) é bem simples e composto por 4 etapas:
 
1. Entrevista de 30 minutos para nos conhecermos, te contarmos um pouco sobre a [Pricefy](https://www.pricefy.com.br/) e ouvirmos um pouco sobre você;
 
2. **Teste de código**, que você poderá fazer no conforto do seu lar, no seu ambiente, no seu tempo;
 
3. **Code walkthrough**, coisa de 45 minutos, onde você nos guia através do código que escreveu e discutimos suas decisões, os porquês disso e daquilo, o que você faria caso a situação X fosse, na verdade, Y e por aí vai;
 
4. Entrevista de **fit cultural**, onde você poderá conhecer mais pessoas da [Pricefy](https://www.pricefy.com.br/), bater papo com elas e refletir se é o tipo de ambiente que te agrada trabalhar;
 
5. Oferta!
 
## Como realizar o teste?
 
Para realizar este teste, basta fazer um fork deste repositório, implementar os requisitos descritos aqui e me mandar um [e-mail](mailto:leandro.silva@pricefy.com.br) com seu CV em PDF ou link do perfil no LinkedIn.
 
Ah! Verdade. Em que linguagem realizar o teste? Em **C# .NET**, please. Isso porque nossa *linguagem padrão* no back-end é C#. (Ao menos nos dias atuais e futuro próximo.)
 
## Requisitos do projeto
 
O teste a ser realizado é o seguinte: **criar uma solução de importação de arquivos em formato tabular.**
 
A solução deve ser composta por três componentes:
 
* Utilitário de linha de comando ([CLI](https://en.wikipedia.org/wiki/Command-line_interface)), o front-end da importação de arquivos;
* Web API, o back-end para o utilitário de linha de comando;
* Banco de dados, para onde serão importados os registros do arquivo.
 
O arquivo a ser importado é o dataset básico de títulos (**title.basics.tsv.gz**) do [IMDb](https://www.imdb.com/interfaces/). Como se trata de um arquivo que tem mais de 8 milhões de registros, você poderá particioná-lo em diversos arquivos menores, de 1 mil registros cada, usando a solução que achar mais conveniente. Deste modo, você tera uma boa quantidade de arquivos diferentes para realizar testes.
 
### O Utilitário de Linha de Comando
 
Através da CLI, derá ser possível realizar 2 operações:
 
1. **Importar um arquivo, que já não tenha sido importado antes** - o ID do arquivo está no seu próprio nome;
 
2. **Listar os arquivos que já foram importados** - ID do arquivo, quantidade de registros importados, quantidade total de registros do arquivo e data da importação.
 
Opcionalmente, será bem interessante poder filtrar arquivos importados por data, mas isso não é exatamente um requisito, é só um *nice to have*.
 
### A Web API
 
Sendo o back-end da CLI, esta API deverá ser capaz de:
 
1. **Receber um arquivo para ser importado e fazer sua importação para o banco de dados** - não deverá haver registros duplicados;
 
2. **Listar os arquivos que já foram importados**, a partir de uma consulta ao banco de dados;
 
### O Banco de dados
 
No banco de dados deverá ser armazenado informações dos arquivos importados, bem como dos registros importados. Portanto, podemos pensar em tabelas para:
 
1. **Arquivos importados** - metadados dos arquivos importados;
 
2. **Registros importados** - os dados contidos nos registros em si.
 
## O que é importante haver no projeto?
 
* Um README? Contendo o que?
* Testes automatizados? Que tipo de testes, unitários ou de integração? Ou os dois?
* Logs? Config files?
* Desenho da solução? Documentação? Que tipo? Que formato?
* Script de deployment? Que tipo? Dockerfile? Zip?
 
Não há requisitos obrigatórios para nada disso. **Você decide.** E a sua decisão vai nos dar uma ideia de como você trabalha, o que você acha importante em um projeto, etc e tal.
 
## Okay. E se eu tiver dúvidas, como faço?
 
Você pode me procurar e terei o maio prazer em sanar suas dúvidas ao máximo. Você sabe meu [e-mail](mailto:leandro.silva@pricefy.com.br), né? Me mande um e-mail com suas dúvidas e partimos de lá.
 
Pense em mim como seu cliente, o sponsor do projeto. Eu não quero que você me entregue o que eu não preciso; o meu interesse é que você mate a pau esse teste.
