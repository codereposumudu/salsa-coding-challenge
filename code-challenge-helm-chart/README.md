# salsa-coding-challenge
Test helm chart for code challenge

* Deployed on the EKS cluster instead of Minikube kubernetes cluster.
* Below controllers deployed on the cluster.

  ![helm_install](https://github.com/codereposumudu/salsa-coding-challenge/blob/feature/initial_commit/demonstration/kubesystem.png)

* This helm chart deploy nginx container as a deployment in EKS cluster, and it exposes via  kubernetes ingress.
* Used below commands for create helm chart

  ```bash
    helm create salsatest
  ```
* To install helm chart

  ```bash
    helm install salsatest salsatest --namespace test 
  ```
  ![helm_install](https://github.com/codereposumudu/salsa-coding-challenge/blob/feature/initial_commit/demonstration/helm_install.png)
    

Note : if you don't set namespace it will provision under the default namespace

* To list installed helm revisions
   ```bash
    helm ls -n test
  ```
  ![helm](https://github.com/codereposumudu/salsa-coding-challenge/blob/feature/initial_commit/demonstration/helm.png)

* To RollBack to older revision 

   ```bash
    helm rollback salsatest 1 --namespace test
  ```
## Helm Chart File Structure

   ```bash
    Chart.yaml :- A YAML file containing information about the chart
    
    values.yaml :- The default configuration values for this chart
    
    Templates/ :- A directory of templates that, when combined with values, will 
    generate valid Kubernetes manifest files.
    
    charts/ :- A directory containing any charts upon which this chart depends.
    
    Demonstration :- This is not the part of hrlm chart, It created for store demo screenshots
  ```

## Deployment Details ( DEMO )

* application deployment

  ![deployment](https://github.com/codereposumudu/salsa-coding-challenge/blob/feature/initial_commit/demonstration/deployment.png)

* Ingress Deployment

  ![ing](https://github.com/codereposumudu/salsa-coding-challenge/blob/feature/initial_commit/demonstration/ingress.png)

* Application

  ![app](https://github.com/codereposumudu/salsa-coding-challenge/blob/feature/initial_commit/demonstration/app.png)

## Additional Commands

* To delete helm chart
  ```bash
  helm delete salsatest --purge
  ```