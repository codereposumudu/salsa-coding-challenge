# salsa-coding-challenge
Test helm chart for code challenge

* This helm chart deploy nginx container as a deployment in EKS cluster, and it exposes via  kubernetes ingress.
* Used below commands for create helm chart

  ```bash
    helm create salsatest
  ```
* To install helm chart

  ```bash
    helm install salsatest salsatest --namespace test 
  ```
  ![helm_install](https://github.com/codereposumudu/servians-coding-challenge/blob/356a5020640ed93740e4ba4e444f92f62eb5d9f6/infrastructure/Diagrams/application.png)
    Note : if you don't set namespace it will provision under the default namespace

* 