# Steps

## Adicionar os IPs das instâncias no arquivo de hosts

```bash
✗ sudo /bin/sh -c 'echo "[instances]" >> /etc/ansible/hosts "\n""ec2-user@ec2-44-214-42-148.compute-1.amazonaws.com" >> /etc/ansible/hosts "\n""ec2-user@ec2-3-239-203-125.compute-1.amazonaws.com" >> /etc/ansible/hosts'
```

## Visualizar o arquivo de hosts

```bash
✗ cat /etc/ansible/hosts

[instances] 
ec2-user@ec2-44-214-42-148.compute-1.amazonaws.com 
ec2-user@ec2-3-239-203-125.compute-1.amazonaws.com

```

## Verificar comunicação do ansible com as instâncias 

```bash
✗ ansible -m ping all

[WARNING]: Platform linux on host ec2-user@ec2-44-214-42-148.compute-1.amazonaws.com is using the discovered Python interpreter at /usr/bin/python3, but future installation of another
Python interpreter could change this. See https://docs.ansible.com/ansible/2.9/reference_appendices/interpreter_discovery.html for more information.
ec2-user@ec2-44-214-42-148.compute-1.amazonaws.com | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "ping": "pong"
}
[WARNING]: Platform linux on host ec2-user@ec2-3-239-203-125.compute-1.amazonaws.com is using the discovered Python interpreter at /usr/bin/python3, but future installation of another
Python interpreter could change this. See https://docs.ansible.com/ansible/2.9/reference_appendices/interpreter_discovery.html for more information.
ec2-user@ec2-3-239-203-125.compute-1.amazonaws.com | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "ping": "pong"
}
```
