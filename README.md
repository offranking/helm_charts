# Helm Commands & Helmfile Guide

This document provides a set of commonly used **Helm** commands along with an introduction to **Helmfile** for managing multiple Helm charts efficiently.

## Helm Commands

###  Installing and Managing Helm Charts
```sh
helm install <release-name> <chart-name>
helm upgrade <release-name> <chart-name>
helm rollback <release-name> <chart-name>
helm uninstall <chart-name>
```

###  Chart Management
```
helm create <chart-name>       # Create a new Helm chart
helm list -a                   # List all installed Helm releases
helm repo list                 # List all Helm repositories
helm template <chart-name>      # Render the template of a Helm chart
helm lint <chart-name>          # Validate the Helm chart
helm install <release-name> --dry-run --debug <chart-name>
```

### helmfile 
used to manage multiple helm charts along with easier installations & uninstallations
