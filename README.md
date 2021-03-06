# Welcome to your CDK Java project!

This is a blank project for Java development with CDK.

The `cdk.json` file tells the CDK Toolkit how to execute your app.

It is a [Maven](https://maven.apache.org/) based project, so you can open this project with any Maven compatible Java IDE to build and run tests.

## Useful commands

 * `mvn package`     compile and run tests
 * `cdk ls`          list all stacks in the app
 * `cdk synth`       emits the synthesized CloudFormation template
 * `cdk deploy`      deploy this stack to your default AWS account/region
 * `cdk diff`        compare deployed stack with current state
 * `cdk docs`        open CDK documentation

Enjoy!

## Stacks criadas pelo cdk

* VPC
    * Classe `VpcStack.java`
    * ```
      cdk deploy Vpc
      ```
* Cluster
  * Classe `ClusterStackcdk.java`
  * ```
      cdk deploy Vpc Cluster
    ```

* Service 01
  * Classe `Service01.java`
    * Criado Application Load Balancer
    * Criado Target Group
    * Auto-Scaling
  * ```
      cdk deploy Vpc Cluster Service01
    ```
* Banco de dados RDS
  * Classe `RdsStack.java`
    * Cria Cloud formation Parameter para o password
    * Cria datasouce com a i `DatabaseInstance`
    * Exporta paramentrops para outras stacks
  * Ocorre uam mudança no comando devido agora com a criação do Banco precisamos passar o valor do password foi definido 
    na Stack Rds com nome `databasePassword`
    ```
      cdk deploy --parameters Rds:databasePassword=jairo123456 Rds Service01
    ```
    
## Atualizar o serviço
```
cdk deploy Service01
```
    
## Destruir as Stack criadas
```
cdk destroy Vpc Cluster Service01
```