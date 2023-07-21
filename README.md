# Resilience Automation Framework on Kubernetes using HelmChart, Chaos, Litmus and Jenkins

Install and run the resilience test cases generated and extracted by the litmus tools to cover the chaos rule and experiments on kubernetes distributed cluster environment.

* Install HelmChart
* Clone the git repo from master branch
* Go to 'chart' folder

## Main Features:

      1. Resilience test arrangement
      2. Integrate kubernetes environment
      3. Integrate performance framework

## Start Resilience Helmchart

Execute following command from 'chart' folder

```bash
helm install resilience resilience
```

1. To copy a file:
```bash
kubectl cp <HOME>/scripts/<resilience>-Script.yaml $(kubectl get pod -l "app=resilience" -o jsonpath='{.items[0].metadata.name}'):/scripts/
```

2. To copy multiple files:
```bash
kubectl cp ../scripts/ $(kubectl get pod -l "app=resilience" -o jsonpath='{.items[0].metadata.name}'):/
```

* Execute the resilience scripts using following command

```bash
kubectl exec  -it $(kubectl get pod -l "app=resilience" -o jsonpath='{.items[0].metadata.name}') -- sh -c 'ONE_SHOT=true; /<resilience>-Script.yaml'

```

![Logo](https://github.com/vikum1407/chaos-resilience-automation/blob/master/ResilienceAutomationFramework.PNG)