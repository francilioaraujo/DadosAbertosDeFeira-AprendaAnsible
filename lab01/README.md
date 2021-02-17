## Lab 01 - Ping 


## Como usar
Para configurar os nodes, primeiro é preciso subir o docker-compose:  
`docker-compose up -d`

## Via comando ad-hoc   
`ansible nodes -m ping` (para usar o grupo específico de hosts nodes)   
`ansible all -m ping` (para usar todos os hosts disponíveis no inventário)

## Via playbook
`ansible-playbook playbook.yml`
