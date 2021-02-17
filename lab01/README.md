## Lab 01 - Ping 


## Como usar
Para configurar os nodes, primeiro é preciso subir o docker-compose:  
`docker-compose up -d`

## Via comando ad-hoc 
Dentro do diretório `lab01`:   
`ansible nodes -m ping` (para usar o grupo específico de hosts nodes)   
`ansible all -m ping` (para usar todos os hosts disponíveis no inventário)

Para executar de forma explícita mostrando a referência ao inventário (`hosts`), executar assim:   
`ansible nodes -i all -m ping` ou `ansible nodes -i hosts -m ping` 

## Via playbook
Dentro do diretório `lab01`:   
`ansible-playbook playbook.yml`

Para executar de forma explícita mostrando a referência ao inventário (`hosts`), executar assim:   
`ansible-playbook -i hosts playbook.yml`

