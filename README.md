# Terraform Beginner Bootcamp 2023

## SEMANTIC VERSIONING

Este projeto utilizará versionamento semantico para suas tags :mage:

[semver.org](https://semver.org/)

Given a version number MAJOR.MINOR.PATCH, increment the:

- MAJOR version when you make incompatible API changes
- MINOR version when you add functionality in a backward compatible manner
- PATCH version when you make backward compatible bug fixes

# Instalar a CLI do Terraform

## A respeito das mudanças da CLI do Terraform
Os passos originais mudaram por causa das mudanças da gpg keyring, por isso a documentação de instruções de instalação foi usada para alterar o script de instalação.

[Instalar Terraform CLI](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)


## Considerações para Distribuição Linux 

Este projeto é feito no Ubuntu.
Cheque sua distribuição e faça ajustes de acordo.

[Como checar versão do SO no Linux](https://www.cyberciti.biz/faq/how-to-check-os-version-in-linux-command-line/)

## Refatoração para scripts bash

Ao consertar os problemas de deprecate haviam muitos scripts bash, então foi criado um arquivo deste script para instalar a CLI, caminho: [./bin/install_terraform_cli](./bin/install_terraform_cli)

## Shebang

Shebang diz ao script bash qual programa interpretará o script.

Use este formato para bash
`#!/usr/bin/env bash`

## Considerações sobre execução do script

[Documentação Shebang](https://en.wikipedia.org/wiki/Shebang_(Unix))



Ao executar um script bash podemos usar o `./` para executá-lo.

ex: `./bin/install_terraform_cli`

Usando um script no .gitpod.yml é preciso apontar o script a um programa para interpretá-lo.
ex: `source ./bin/install_terraform_cli`

## Considerações das permissões do Linux

Pra deixar um arquivo executável (adicionar o X nas configurações dele) no nível de usuário:

```sh
chmod u+x ./bin/install_terraform_cli
```

Alternativamente:
```sh
chmod 744 ./bin/install_terraform_cli
```


https://en.wikipedia.org/wiki/Chmod


## Ciclo do Gitpod (Befire, Init, Command)

É preciso tomar cuidado ao usar o init porque não rodará se um workspace for reiniciado.

[Gitpod Lifecycle](https://www.gitpod.io/docs/configure/workspaces/tasks)