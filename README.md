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

Stacks criadas pelo cdk

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

* Application Load Balancer
  * Classe `Service01.java`
  * ```
      cdk deploy Vpc Cluster
    ```