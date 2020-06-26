---
title: Azure Cloud Shell scripting
date: '2019-03-07'
tags:
  - azure
  - bash
---

## Storing variables

I want to store the Resource Group name in a variable to use in a bash script. 

```shell
RgName=`az group list --query '[].name' --output tsv`
```

The ` back tick is important - as it executes the command inside. Or just found out you can use:

```
RgName=$(az group list --query '[].name' --output tsv)
```
