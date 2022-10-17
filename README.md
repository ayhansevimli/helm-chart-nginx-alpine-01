**********************************************************************************************************
#
# Helm Chart for nginx-alpine-01
**********************************************************************************************************
### Clone helm-chart-nginx-alpine-01 from github
```
git clone https://github.com/ayhansevimli/helm-chart-nginx-alpine-01.git

```
### lets run some Helm Commands for creating our first Helm Chart
```
helm create helm-chart-nginx-alpine-01

```
### Render chart templates locally and display the output
```
helm template helm-chart-nginx-alpine-01

```
### This command takes a path to a chart and runs a series of tests to verify that the chart is well-formed.
```
helm lint helm-chart-nginx-alpine-01

```
### Check which we are going to do is -dry-run. Helm is full of such useful utility which allows developer to test its configuration before running the final install command. Use the following -dry-run command to verify your helm-chart-nginx-alpine-01 Helm Chart
```
helm install release-helm-chart-nginx-alpine-01 --debug --dry-run helm-chart-nginx-alpine-01

```
### Lets run the install command.
```
helm install release-helm-chart-nginx-alpine-01 helm-chart-nginx-alpine-01

```
### to see all the releases use the following list command to list down all the releases
```
helm list -a

```
### verification using kubectl commands also, so that we can make sure helm has done its work.
```
kubectl get all
kubectl get services

```
### The upgrade arguments must be a release and chart.
```
helm upgrade release-helm-chart-nginx-alpine-01 helm-chart-nginx-alpine-01
```
### Verify your helm upgrade by running following list command
```
helm list -a

```
### Here is the command for Helm Diff. 1 represents the first release and 2 represents the second release of release-helm-chart-nginx-alpine-01 After running the helm diff command you will see the values.yaml showing the difference between replicas.
```
helm diff revision release-helm-chart-nginx-alpine-01 1 2

```
```
helm diff revision release-helm-chart-nginx-alpine-01 2 3

```
### Lets again run kubectl get deployment
```
kubectl get deployments
kubectl get services

```
### Rollback Helm release. In the Step we upgraded the Helm chart release from version 1 to version 2. So let's see one more rollback feature of Helm Chart.
```
helm rollback release-helm-chart-nginx-alpine-01 1

```
### As you can see from the above screenshot we successfully rolled back the release to the previous version. But one interesting thing about Helm is, it still updates the REVISION to 3
```
helm list -a

```
### To confirm that we have actually rolled back our Helm Chart release, lets run some kubectl commands
```
kubectl get deployments
kubectl get services

```
### Delete Helm release Wouldn't it be nice if you need to run only one command to delete your Helm release and you do not have to do anything else.
```
helm delete release-helm-chart-nginx-alpine-01

```
### Extras : install the Helm Diff plugin
```
helm plugin install https://github.com/databus23/helm-diff

```
### After installation you can verify the plugin using following command
```
helm plugin list

```

