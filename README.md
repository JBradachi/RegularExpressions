# RegularExpressions
Repositório reservado para aprendizagem de espressões regulares em python

Documentação de regex: https://docs.python.org/3/howto/regex.html

# Guia rápido de expressões regulares:

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/a35b4a1a-93ca-49d7-a9cb-e88e808d7d9e)


| Simbulo | Significado|
| - | - |
| ^ | Corresponde ao início de uma linha |
| $ | Corresponde ao final da linha |
| . | Corresponde a qualquer caractere |
| \s | Corresponde a espaços em branco |
| \S | Corresponde a qualquer caractere que não seja espaço em branco |
| * | Repete um caractere zero ou mais vezes |
| *? | Repete um caractere zero ou mais vezes (não ganancioso) |
| + | Repete um caractere uma ou mais vezes |
| +? | Repete um caractere uma ou mais vezes (não ganancioso) |
| [aeiou] | Corresponde a um único caractere no conjunto listado |
| [^XYZ] | Corresponde a um único caractere que não está no conjunto listado | 
| [a-z0-9] | O conjunto de caracteres pode incluir um intervalo | 
| ( | Indica onde a extração da string deve começar | 
| ) | Indica onde a extração da string deve terminar | 

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

aqui selecionamos as strings que começam com X (^X), seguidas de quaisquer caracteres (.) zero ou mais vezes (*) seguidos da ultima ocorrencia de dois pontos (:) na string


### Exemplo 2:

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/fdbd3c6d-3921-4916-8ce4-12a954759492)

aqui selecionamos as strings que começam com X (^X), seguidos por um hífem (-), seguidas de quaisquer caracteres sem ser espaços (\S) uma ou mais vezes (+), seguidos da ultima ocorrencia de dois pontos (:) na string

os caracteres "[]" simbolizam um unico digito, exemplo: [0-9] é um unico dígito de zero a nove

### Exemplo 3

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/6e9d4862-604e-4bc5-91ec-3854a98b6bd8)

aqui selecionamos todas as ocorrencias de A ou E ou I ou O ou U (maiúsculos) ([AEIOU]) uma ou mais vezes (+)

### Exemplo 4

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/d4d70f1d-654c-4a15-bb1f-2d5a8d6ce807)

aqui temos algo diferente, os caracteres ".+?" significam que após o F podem vir quaisquer caracteres (.) uma ou mais vezes (+) mas finalizando na menor string possível que contenha ":" (?)

se não houvesse o caractere "?" a string retornada seria "From: Using the :"


### Exemplo 5

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/bbaab7be-5727-4a3e-b72c-eb7e75fa92b9)

aqui vamos usar o findall para pegar seções das strings que contenham quaisquer caracteres sem espaço (\S) uma ou mais vezes (+), concatenadas com um @ e concatenadas com quaisquer caracteres sem espaço (\S) uma ou mais vezes (+)


os caracteres "()" denotam o começo e o fim do que irá ser retornado pela função, como um slice

### Exemplo 6

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/1e859ace-bac7-436e-b16c-965da78d88ea)

aqui temos que a função findall vai retornar das strings que começam com F seguidos de "room ", seções das strings que contenham quaisquer caracteres sem espaço (\S) uma ou mais vezes (+), concatenadas com um @ e concatenadas com quaisquer caracteres sem espaço (\S) uma ou mais vezes (+). note que só é retornado o que está entre parenteses


### Exemplo 7

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/591416c5-9275-435d-ba40-ad6d0982248f)

aqui das strings que contenham @ irá ser retornado o que vem depois do @  que não são espaços ([^ ]) zero ou mais vezes (*)

os caracteres "[^x]" significam que irá procurar por strings que não possuem x ou qualquer item listado

### Exemplo 8

![image](https://github.com/JBradachi/RegularExpressions/assets/105111795/6df74001-5e40-41e8-a9a0-de474c5ff2e1)



