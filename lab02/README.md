# Lab 02 - Instalação do apache

## Estrutura do diretório

```bash
.
├── README.md
├── ansible.cfg
├── hosts
└── playbook.yml

0 directories, 4 files
```

## Como funciona

Esse playbook executa a instalação e configuração do apache no grupo de hosts `[apache]` (é possível ver no arquivo `hosts`), tarefas executadas:

1. Realiza um apt-get update
2. Verifica se tem o apache2 instalado, senão instala
3. Verifica se o serviço apache2 está iniciado, senão inicia

Para verificar se está funcionando, abrir no navegador: <http://localhost>

Módulos usados:

- [apt](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_module.html): usado para realizar operações do gerenciador de pacotes apt
- [service](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/service_module.html): usado para realizar operações com serviços na máquina

## Executando

Para executar, dentro do diretório `lab02`:
`ansible-playbook playbook.yml`

## Resumo

Com esse lab foram exercitados os conceitos:

- uso do módulo apt
- uso do módulo service
