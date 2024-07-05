# Projeto para reduzir o tamanho do json

- Um arquivo json é nada mais, nada menos que um arquivo txt estrutura, por isso não é possivel aplicar téncicas de compressão

- Observando o arquivo em um editor de texto foi observado que 99% do tamanho do arquivo era formado por imagens binarias.

- Essa técnica é comumente utilizada para reduzir o tempo de load de imagens em sites, porém nesse caso se trata de mais de 900 imagens que acaba gerando um tamanho muito grande no arquivo json.

- Foi identificado  que 99% do tamanho do arquivo era formado por essas imagens, a  estratégia utilizada foi extrair essas imagens para um site que realize a hospedagem.

- Com um servidor armazenado essas imagens o sistema que for consumir poderá adotar técnicas para carregar essas  imagens de forma paralela ou sequencial.

- Todas as imagens armazenadas no mesmo arquivo, o receptor só teria acesso após a transferencia, usando o formato o consumo poderá ser dinamico

- O resultado foi a reduzão de 30MB para 400kb

- (400/30000 - 1) *100 = redução de 98%
