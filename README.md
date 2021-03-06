<div align="center">
    <img src="https://img.shields.io/badge/feito%20por-Artaxerxes Nazareno-blue"/>
    <a href="https://twitter.com/Artaxerxes0001">
    • 
    <img src="https://img.shields.io/twitter/follow/Artaxerxes0001?style=social">
    </a><br>
  </div>

# Stream API

### O que é?

API do java para operações com coleções, ela abitrai grande parte do trabalho do desenvolvedor, fazendo com que o
desenvolvedor foque na sua logica de negocio sem necessariamente se preocupar com a implementação de todo o codigo.

---

### Operações com Stream

Existem mais de 30 operações e 7 staticos que podem ser feitas com Stream:

- **Build** - construtor de stram
- **Intermediarias** - sempre retornam uma stream, que pode ser reutiliazado
- **Terminais** - geram algo diferente de um stram, podendo ser : void, double, int, String, etc.

---

### Tipos de Stream

- **Ordenada**
- **Não ordenada**
- **sequencial** - processa a stream de forma sequencial
- **paralela** - executa o processamento de forma paralela. Internamente seram craidas varias linhas paralelas de
  processamento sem se preocupar com a implementação

---

### Função do Filter

#### Função MAP

MAP recebe uma lambda ou referencia de metodo que usa para transformar os elementos de uma stream gerando uma nova
stream com os dados mapeados. A nova stream tera o mesmo tamanho que a anterior

exemplo: temos uma stream com produto (nome, preço), o map abaixo fornecera uma stream com os nomes dos produtos

![exemplo de um Map](imagens/map.jpg)

desse modo criamos uma nova stream com os nomes dos produtos apenas.

#### Função Filter

Filter como o propio nome sugere serve para filtrar dados, usamos para obter uma nova stream de dados filtrados com base
a um criterio. Se o criterio for verdadeioro fara parte da stream caso for falso não fara parte, caso todos os dados
forem falsos sera um stream vazio.

Para implementar o Filter passamos como argumento a interface funcional Predicate, pois a expressão lambda retorna
verdadeiro ou falso.

Exemplo: Filtrar os numeros pares de um Stream

![exemplo de ilustração de um filter](./assets/image.png)

#### Função Reduce

Consegue transforma uma stream de dados em algo completamente diferente. Nao precisa ter nem mesmo uma ligaçao direita
com os tipos de cada um dos elementos.

Pode pegar um array e retornar um unico elemento, por exemplo a soma de todos os elementos do array.

Na sintaxe do Reduce (acumulado, n). n sao os valores da stream. O acumulador e passado para todos os elementos da
stream durante a iterraçao, ja que na primeira nao teve a funçao anterior, podemos passar um valor inicial ou nao.

O acumulador nos da flexibilidade para definir o que vai ser, pode ser um objeto, array, tipo primitivo, etc.

Exemplo: calcular o valor total em uma Stream.

![](.images/reduce.png)

**OBS:** no final o reduce não gera outra stream, o reduce é um metodo terminal da API Stream.

#### Função Match

Verifica se todos os elementos do stream cumprem totalmente ou parcialmente ao um deteminado criterio

- **allMatch** - verifca se todos os elementos satisfazem ao criterio
- **anyMatch** - verifca se pelomenos um dos elementos satisfaz ao criterio
- **noneMatch** - verifca se todos os elementos não satisfazem ao criterio. Faz a verificação de forma inversa ao
  allMatch

#### Função Max e Min

Retornam o maior ou menor elemento da stream com base em um Comparator

#### Outras Funções interessantes

- **distinct** - não aceita valores dublicados na construção da stream
- **skip** - pula elementos da stream
- **limit** - limita o numero de elementos que vão ser processados
- **takeWhile** - pega os elementos enquanto acontecer uma determinada condição.

### Autor

#### Artaxerxes Nazareno
<img src="https://github.com/artaxerxes001/artaxerxes001/raw/main/imagens/eu.jpg" width="200">

##### Sigam me:
[![Twitter Badge](https://img.shields.io/badge/-@artaxerxes0001-1ca0f1?style=flat-square&labelColor=1ca0f1&logo=twitter&logoColor=white&link=https://twitter.com/tgmarinho)](https://twitter.com/Artaxerxes0001)  [![Linkedin Badge](https://img.shields.io/badge/-Artaxerxes_Nazareno-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/artaxerxes-nazare/)](https://www.linkedin.com/in/artaxerxes-nazare/) [![Gmail Badge](https://img.shields.io/badge/-artaxerxesnazare@gmail.com-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:artaxerxesnazare@gmail.comm)](mailto:artaxerxesnazare@gmail.com)
