# Como por essa receita para funcionar

## OBS: Para esse projeto iremos utilizar uma imagem não oficial do Onlyoffice.
O que motivou essa escolha é o fato das imagens oficiais do OnlyOffice estão restritas a 20 usuários e como não é possível para mim o custeio da licença, preferi essa opção. 
Pesando também que personalização é muito complexa nas imagens oficiais.
Só resalto, que mesmo que a imagem tenha condições de suportar mais de 20 pessoas, lembre-se de observar se a máquina suporta um grande volume de acessos e se você sabe escalar corretamente o serviço para que não fique instável ou fora do ar.

## Explicando o que é o docker-compose.yml
Esse arquivo é como uma receita de bolo: Lá está expecificado como cada serviço irá funcionar. Se algo estiver errado, provavelmente seu arquivo está com erros.

## Preste atenção!
### Portas
Na docker-compose.yml teremos que definir apenas a porta que o serviço irá escutar. 
Neste caso a porta 91 da minha máquina aponta para a porta 80 do Onlyoffice, está marcado como '91:80'.

## Configurações
Aproveito para te convidar a prestar bastante atenção no arquivo config.env. Nele estão configurações sensíveis para funcionamento do serviço.
Por padrão, o JWT está habilitado. Com o JWT é possível usar uma senha para acessar os serviços do OnlyOffice.
Deixei uma recomendação de serviço para gerar uma senha aleatória. Após esta ser gerada, cole a senha logo a frente de:

#### JWT_SECRET=

## Como por tudo em funcionamento
Para colocar seu serviço em funcionamento, na pasta onde se enconta o arquivo docker-compose.yml insira o comando 

#### sudo docker-compose up -d

## Outros comandos úteis

#### sudo docker-compose down
Desmonta o Onlyoffice.

#### sudo docker-compose restart
Reinicia o Onlyoffice

## Obrigado por chegar até aqui.
