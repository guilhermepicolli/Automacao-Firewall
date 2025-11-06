# Automação de Regras de Firewall com AWX

Este projeto automatiza a criação de objetos e aplicação de regras nos firewalls Juniper SRX e Checkpoint R82 usando Ansible AWX.

## Componentes

- `inventory.yml`: inventário com IPs e credenciais
- `playbook_srx.yml`: aplica regras no Juniper SRX via SSH
- `playbook_checkpoint.yml`: aplica regras no Checkpoint via API REST
- `templates/`: regras padrão para Linux e Windows

## Como usar no AWX

1. Importe este projeto como fonte Git
2. Crie credenciais para SRX e Checkpoint
3. Crie templates de job com variáveis:
   - `nome_objeto`
   - `novo_ip`
4. Execute via GUI e acompanhe os logs
