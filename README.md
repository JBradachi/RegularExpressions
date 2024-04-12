# RegularExpressions
Repositório reservado para aprendizagem de espressões regulares em python

# Guia rápido de expressões regulares:

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/a35b4a1a-93ca-49d7-a9cb-e88e808d7d9e)

Para executar expressões regulares em python, é necessário importar uma biblioteca
> import re

Voce pode usar a expressão abaixo para ver se a string entra na expressão regular (similar ao find)
> re.search('\{O que quer encontrar\}', arquivo)

No termo entre chaves podemos adicionar as expressões regulares, exemplo:

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/4d23eda6-3b1a-418a-876b-47537486bae3)


### Voce pode usar a expressão abaixo para extrair porções de uma string que  entra na expressão regular, similar ao usar find() e slice[5:10]
> re.findall()

uma função que encontra todas as ocorrencias de uma expressão na string 

### Exemplo

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/6f03aaca-59e1-4033-88b6-8128175a7e3b)

nesse exemplo a função findall() irá procurar digitos de 0 a 9 ([0-9]) uma ou mais vezes seguidas (+)

o caractere "." significa qualquer caractere
os caracteres ".*" significam de zero a qualquer caractere de zero a qualquer numero de vezes

### Exemplo 1:

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/6d136452-d441-4ce3-90f6-28faef932a76)

aqui selecionamos as strings que começam com X (^X), seguidas de quaisquer caracteres (.) zero ou mais vezes (*) seguidos de dois pontos (:)


### Exemplo 2:

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/fdbd3c6d-3921-4916-8ce4-12a954759492)

aqui selecionamos as strings que começam com X (^X), seguidos por um hífem (-), seguidas de quaisquer caracteres sem ser espaços (\S) uma ou mais vezes (+), seguidos de dois pontos (:)

os caracteres "[]" simbolizam um unico digito, exemplo: [0-9] é um unico dígito de zero a nove
