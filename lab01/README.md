# Lab 01 - Ping

## Requisitos

- [ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- [docker](https://docs.docker.com/engine/install/)
- [docker-compose](https://docs.docker.com/compose/install/)

## Como usar

Para configurar os nodes, primeiro é preciso subir o docker-compose:  

`docker-compose up -d`

Note que os contêineres têm nomes similares a IPs. Isto foi feito para simular o acesso com SSH.

No arquivo `ansible.cfg` há algumas configurações para facilitar o lab.

## Via comando ad-hoc

Dentro do diretório `lab01`:
`ansible web -m ping` (para usar o grupo específico de hosts web)
`ansible all -m ping` (para usar todos os hosts disponíveis no inventário)

Para executar de forma explícita mostrando a referência ao inventário (`hosts`), executar assim:
`ansible nodes -i all -m ping` ou `ansible web -i hosts -m ping`

Exercícios sugeridos:

- [Exercício 1.2](https://ansible.github.io/workshops/exercises/ansible_rhel/1.2-adhoc/README.pt-br.html)

Obs: Os exercícios pedirão para modificar o arquivo de inventário. É aconselhado não modificá-lo. A execução dos comandos ansible deve prosseguir normalmente no ambiente do lab.

## Via playbook

Dentro do diretório `lab01`:
`ansible-playbook playbook.yml`

Para executar de forma explícita mostrando a referência ao inventário (`hosts`), executar assim:
`ansible-playbook -i hosts playbook.yml`
