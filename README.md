# hbase 
Para acessar o docker digitar: docker exec -it hbase-furb /bin/bash.  
Para acessar o hbase digitar: hbase shell no root do docker.  

Exercícios do hbase

Agora, de dentro da imagem faça os sefuintes procedimentos:  
1. Crie a tabela com 2 famílias de colunas:  
a. personal-data  
b. professional-data   
`create 'italians', 'personal-data', 'professional-data'`  

2. Importe o arquivo via linha de comando  
`hbase shell /tmp/italians.txt`  

Agora execute as seguintes operações:  
1. Adicione mais 2 italianos mantendo adicionando informações como data de nascimento nas informações pessoais e um atributo de anos de
experiência nas informações profissionais;  

`put 'italians', '11', 'personal-data:name', 'Giuseppe Domini'`  
`put 'italians', '11', 'personal-data:city', 'Emilia Romagna'`  
`put 'italians', '11', 'personal-data:born', '14/03/1985'`  
`put 'italians', '11', 'professional-data:role', 'Analista de BI'`  
`put 'italians', '11', 'professional-data:salary', '5000'`  
`put 'italians', '11', 'professional-data:experienceyears', '5'`  
`put 'italians', '12', 'personal-data:name', 'Luigia Domini'`  
`put 'italians', '12', 'personal-data:city', 'Emilia Romagna'`  
`put 'italians', '12', 'personal-data:born', '20/10/1989'`  
`put 'italians', '12', 'professional-data:role', 'Analista de Sistemas'`  
`put 'italians', '12', 'professional-data:salary', '5300'`  
`put 'italians', '12', 'professional-data:experienceyears', '6'`  

2. Adicione o controle de 5 versões na tabela de dados pessoais.  


3. Faça 5 alterações em um dos italianos;  


4. Com o operador get, verifique como o HBase armazenou o histórico.  


5. Utilize o scan para mostrar apenas o nome e profissão dos italianos.  


6. Apague os italianos com row id ímpar  


7. Crie um contador de idade 55 para o italiano de row id 5  


8. Incremente a idade do italiano em 1  






