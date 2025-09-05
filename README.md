# Code-Girls

Primeiro desafio do curso Code Girl da Dio.

Descrição: O diagrama foi separado em dois grupos, devs e sysadmins onde ambos realizam o acesso a console/cli. Cada grupo possui suas permissões definidas pelo IAM, onde o time de dev possui apenas acesso aos buckets s3, assim conseguem realizar o upload do arquivo para novo deploy nas máquinas ec2. Já o time de sysadmins, possui acesso as instâncias ec2 que foram previamente configuradas com uma role que permita o acesso da ec2 nos buckets s3. Um EBS foi configurado e atachado na instância para gravar os arquivos de deployment.
_____________________________________________________________________________________________________________________
Comandos que poderão ser utilizados:

  # Equipe Dev: 
  1. Caso utilize a cli:
  ```
    aws s3 cp /diretório/do/arquivo s3://nome-do-bucket/
   ```
  2. Em caso de utilização do console, basta acessar o serviço do s3 e clicar na opção de upload dentro do bucket.

  # Equipe Sys
  1. Para acesso a ec2 via cli, é necessário a chave pem. Em caso da console, basta acessar o serviço da ec2 e uma outra alternativa de login é utilizar o session manager.
  2. Rodar o comando para copiar o arquivo do s3 para o ec2.
  ```
  #aws s3 cp s3://nome-do-bucket/nome-do-arquivo /diretório/

  ```
  3. Prosseguir com a execução do deployment de acordo com o que o owner definiu.

Diagrama completo no diretório images.
