# Walmart Checkout App - Kubernetes Helm Deployment

## Built For Sony/Walmart Scale Production Traffic

Production-grade Helm chart to deploy 3-tier retail application on Kubernetes.

## Tech Stack
Kubernetes | Helm 3 | Docker | GitHub Actions CI/CD | AWS | HPA

## Features I Implemented
- *Zero-downtime deployment* + Auto Rollback strategy
- *HPA*: Auto-scale pods from 2→10 during sale traffic spikes  
- *CI/CD Pipeline*: GitHub Actions - Code push = Auto deploy to K8s cluster
- *Prod Hardening*: values-prod.yaml with CPU/Memory limits + Liveness/Readiness probes
- *Impact*: Reduced manual deployment time from 30 mins → 2 mins

## Used At Sony
Applied same Helm pattern for internal tools. Automated deployments, saved 5+ hrs/week manual work.

## Deploy Locally
helm install walmart-app ./chart
kubectl get pods
kubectl get hpa

## Architecture
User → Ingress → Service → Deployment → HPA → Pods
