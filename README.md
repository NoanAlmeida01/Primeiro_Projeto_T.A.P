Provisionemanto de uma infraestrutura para desenvolvimento web em python usando django_framework, e com um servidor web ativo.

O Provisionamento da instância EC2 da Amazon foi feito no Terraform e o gerenciamento de tarefas foi feino no Ansible.

A ami é um ubuntu server 20.04 lts.

Com o Ansible foi instalado o python3, virtualenv, djangoframework e iniciado o servidor.

Faça as alterações no arquivo main.tf para ficar de acordo com as suas especificidades, depois va até a pasta IaC e digite: terraform apply 
Após ter subido a instância, confira se aparece corretamente na AWS console.

Para executar as tarefas na instância vá até o arquivo hosts.yml e coloque o ip público da sua instância ec2, depois execute o playbook do Ansible na pasta IaC com o comando: ansible-playbook playbook.yml -u ubuntu --private-key [sua chave.pem na AWS] -i hosts

Por último digite no browser o ip público da sua instancia com a porta 8000 ao final depois de dois pontos, ex: 0.0.0.0:8000
