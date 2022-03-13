# Mutação: 
Ela vai ser responsável por dar à população uma variedade de genes para os indivíduos, evitando que a solução fique presa em extremos locais, os parâmetros de mutação devem ser ajustados para o problema, caso seja pequena de mais, as soluções podem ficar presas em extremos locais, e caso a mutação seja grande demais vai acabar dificultando que o algoritmo encontre ótimos globais, já que os indivíduos vão sofrer muitas mutações.

# Seleção: 
É responsável pela avaliação e seleção dos indivíduos, com base em uma função de avaliação, a comparação dos valores da função de avaliação vai levar a escolha dos indivíduos que vão sobreviver e se reproduzir, havendo uma vantagem seletiva para os indivíduos com um valor da função de avaliação maior. Caso a seleção seja feita apenas com os indivíduos melhores avaliados, a população pode perder características(genes) que ajudariam a encontrar uma solução ótima.

# CrossOver(Cruzamento): 
É responsável por realizar uma mistura das características(genes) dos indivíduos, onde os filhos vão herdar parte das características dos pais. É necessário para dar a população uma variedade genética dos indivíduos.

# Metodos Ultilizados e Alterações:
No algoritmo foi criada uma classe chamada cidade que contém os valores X e Y correspondentes às coordenadas do plano cartesiano e uma função de calcular distância, responsável por calcular a distância euclidiana entre 2 cidades(2 pontos no mapa). A população inicial foi definida aleatoriamente com base no grupo de possíveis cidades a serem visitadas e com base nessas cidades são formadas listas contendo as cidades geradas que vão ser as possíveis rotas. O fitness foi calculado com base no somatório das distâncias entre as cidades visitadas que uma rota vai possuir. Para seleção das rotas que vão gerar filhos foi usado o método da roleta, onde a probabilidade de seleção da rota vai ser proporcional ao seu fitness em relação a todas as rotas. O cruzamento das rotas selecionadas foi feito com uma permutação das cidades contidas nas rotas, resultando nas rotas “filhas”. Para a mutação foi realizada uma troca das posições de 2 cidades dentro de uma mesma rota. O código vai ficar em loop com base no número de gerações desejadas, realizando estas etapas até que o número de gerações seja alcançado, descartando as rotas com menor fitness e mantendo as rotas com o melhor fitness e no final a melhor rota encontrada vai ser mostrada.

# Resultado:
É interessante ver como o algoritmo foi capaz de encontrar uma solução satisfatória para o problema, após uma quantidade suficiente de gerações, mesmo sendo a partir de rotas aleatórias, é também possível generalizar essa abordagem para outros tipos de problemas, o que me mostrou como esse tipo de abordagem é versátil.

### Geração Inicial
![Geração Inicial](https://user-images.githubusercontent.com/49374221/158063758-98d29e91-48d9-4266-9e76-1bdc8bb7afe9.png)

### Geração final
![Resultado](https://user-images.githubusercontent.com/49374221/158063797-77120499-9af9-4d62-9fb1-ff7982a0d39b.png)
