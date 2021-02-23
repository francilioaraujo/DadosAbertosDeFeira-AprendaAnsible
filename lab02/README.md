## Lab 02 - Instalação do apache

## Estrutura do diretório
```
.
├── README.md
├── ansible.cfg
├── hosts
└── playbook.yml

0 directories, 4 files
```
## Como funciona
Esse playbook realiza as seguintes tarefas:   
1. Realiza um apt-get update nas máquinas alvos
2. Verifica a máquina tem o apache2 instalado, senão instala
3. Verifica se o serviço apache2 está iniciado, senão inicia

Módulos usados:
#### [apt](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_module.html): 
usado para realizar operações do gerenciador de pacotes apt
#### [service](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/service_module.html): 
usado para realizar operações com serviços na máquina


## Executando

Para executar, dentro do diretório `lab02`:   
`ansible-playbook playbook.yml`
