# Inteligência Artificial

## Equipe
Marcos Oliveira

Arylan Santos

Matheus Paixao


##
![](img/titulo.png)

## Abstract
![](img/abstract.png)


## Introdução
* Trade-off da animação gráfica
    * complexidade x controle
    * controle de mocimento x simulação dinâmica

* Métodos foram desenvolvidos para:
    * rastejar
        * McKenna, M., and Zeltzer, D., “Dynamic Simulation of Autonomous Legged Locomotion,” Computer Graphics, Vol.24, No.4, July 1990, pp.29-38.
    * andar
        * Miller, G., “The Motion Dynamics of Snakes and Worms,” Computer Graphics, Vol.22, No.4, July 1988, pp.169-178.
    * correr 
        * Raibert, M., and Hodgins, J.K., “Animation of Dynamic
        Legged Locomotion,” Computer Graphics, Vol.25, No.4, July
        1991, pp.349-358.

* Novo comportamento -> novo algorítmo


## Introdução (continuação)
* Algorítmos Genéticos usados em problemas de otimização
* Algorítmos Genéticos podem ser usados para gerar entidades virtuis
  sem conhecer os parâmetros e procedimentos usados para criar estas entidade
* fitness podem ser gerados automaticamente ou informado pelo usuário
* Iterativas evoluções pode gerar como resultados indivíduos mais adptados
* Automatização da criação compensa a perda de controle

## Posição do artigo em relação a outros trabalhos
* Trabalhos citados no artigo em que são feitas comparações
    * de Garis, H., “Genetic Programming: Building Artificial Ner-
    vous Systems Using Genetically Programmed Neural Network Modules,” Proceedings of the 7th International Conference on Machine Learning, 1990, pp.132-139.
    * Ngo, J.T., and Marks, J., “Spacetime Constraints Revisited,”
    Computer Graphics, Annual Conference Series, 1993, pp.343-350.
    * van de Panne, M., and Fiume, E., “Sensor-Actuator Net-
    works,” Computer Graphics, Annual Conference Series, 1993,
    pp.335-342.

* Os metodos acima conseguiram bons resultados em ambiente 2D

## Posição do artigo em relação a outros trabalhos (Continuação)
* Nos trabalhos acima foram gerados sistemas de controle em estrutura fixas desenhadas pelo usuário
* Neste artigo temos:
    * estrutura morfológica quanto a estrutura de controle evoluem
    * os corpos das criaruras são tridimencionais e baseados na física
    * as estruras físicas da criaturas podem se adptar aos sistemas de controle e vice-versa
    * "O sistemas nervoso" da criatura também é produto da otimização (nodes, conexções e funções de cada neural node)
    * Não há a necessidade de informar informações específicas da criatura

## Morfologia das Criaturas
![](img/morfologia.png)

## Morfologia das Criaturas (Continuação)
* Cada node descreve:
    * tipo de junção: rigida, revolute, torção, universal, esférica
    * limite de recursão
    * um conjunto de nurônios locais
* Conexões:
    * posição, orientação, escala e reflecção

## Controle das critauras
* Uma cérebro virtual determina o comportamento das criaturas
* Sistemas dinâmico que aceita valores de entrada de sensores e envia respostas para atuadores
* Sendores, atuadores e neuronio internos são presentadas por variáveis escalares contínuas que podem ser positivos ou negativos que podem representas puxar ou empurrar.

## Controle das Criaturas (Continuação)
![](img/controle.png)

## Sensores
* Sensores de angulos das juntas
* Sensores de contato
* Fotosensores
* Outros sensores não usados neste artigo: acelerometros, de som e cheiro.  

## Neurônios
* Usados nós neurais internos
* Diferentes nós neurais desempenham diferentes funções
    * sum, product, divide, sum-threshold, greater-than, sign-of, min, max, abs, if, interpolate, sin, cos, atan, log, expt, sigmoid, integrate, differentiate, smooth, memory, oscillate-wave, and oscillate-saw.

## Atuadores
* Reponsaveis por movimentar as criaturas
* Recebem valores dos neorônios e sensores

## Combinando morfologia e controle
![](img/morfologia_controle.png)

## Combinando morfologia e controle (Continuação)
![](img/genotipo.png)

## Combinando morfologia e controle
![](img/sistema_nervoso.png)

## Simulação Física
* Usado um ambiente virtul 3D
* Componentes da simulação física: dinâmica dos corpos articulados, integração numérica, detecção de colisão, fricção, viscosidade
* Feathermore's recursive O(N) metodo usado para calcular a velocidade e aceleração
* Integração é usada para clacular os movimentos usando Runge-Kutta-Fehlberg método


## Seleção do comportamento
* Evolução das criaturas são otimizadas para específicos comportamentos
* Natação
    * fitness: velocidade
* Caminhar
    * fitness: velocidade
* Pular
    * fitness: altura
* Seguir
    * firness: valocidade


## Evolução da criaturas
* Criação da população Inicial
  * Aleatoriamente
  * Ou genótipo de uma evolução anterior
  * Ou gerado manualmente
* Tamanho típico da população - 300
* Taxa de sobrevivência: 1/5
* Para cada evolução o fitness é recalculado

## Mutação de Grafos Dirigidoa
1. Parametros internos dos nodes são objetos de possíveis alterações
2. Novos nodes são adicionados aleatoriamente dos grafos
3. Parâmetros de de conexões sofrem alterações
4. Novas conexões são adicionadas aletoriamente
5. Elementos não conectados são descartados

## Combinando Grafos Dirigidos
![](img/cross_graft.png)

## Implementação Pararela
* Connection Machine CM-5
    * Novembro 1993
    * 131 GFlops
    * 1024 cores
* População 300, 100 gerações, 3 horas, 32 processadores CM-5

## Resultados
![](img/swimming.png)

## Resultados
![](img/walking.png)

## Resultados
![](img/jumping.png)

## Resultados
![](img/following.png)

## Trabalhos Futuros
colocar conteúdo aqui

## Conclusão
colocar conclusão aqui


## Referências
colocar referencias aqui...
