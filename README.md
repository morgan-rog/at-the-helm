# at-the-helm
## About

Creator: Morgan Rogers

Roles: Designer, Platform Engineer

## Description

This project will be deploying Jenkins, which is a CI/CD service, on GKE (Google Kubernetes Engine). The GKE will be deployed using Terraform which is an infrastructure as code tool.

## Motivation

I (Morgan) currently work as a Platform Engineer and my team is starting to work with Kubernetes more (mainly in AWS) and I want to get more experience with it outside of the work environment. My team is DevOps focused and we have Jenkins running on on-premise services but I want to attempt to get it running on Kubernetes. I am using GCP/GKE because they offer a $300 credit and cloud kubernetes services can get quite expensive if it is kept running for long periods.

## Tools/Technologies

Terraform (for deploying GKE and Google Compute Network), GKE (Kubernetes), Helm (configuration and installation of Jenkins), kubectl (command line tool for interacting with kubernetes).

## System Architecture

![lucid chart](images/at-the-helm-lucid-chart.png)
