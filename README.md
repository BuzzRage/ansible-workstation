# ansible-workstation
An workstation installed and configured with Ansible.

## Installation
1. Change your ansible password in `.vault_pass` ( default : "password" )
2. Change remote users password in `inventories/group_vars/workstations/secrets.yaml`:
  - ̀`ansible-vault decrypt inventories/group_vars/workstations/secrets.yaml`
  - ̀modify `ssh_passwd_pcX` value ( default : "passwdpcX" )
  - ̀`ansible-vault encrypt inventories/group_vars/workstations/secrets.yaml`
3. Check user used with `ansible-playbook playbook/check-user.yml --limit pc1`
4. Run the playbook : `ansible-playbook playbook/setup-zsh.yml` (you may add `--ask-become-pass` if you don't want to use the one stored in the vaulted file)

TODO:
- ansibliser .zshrc ( omz + theme powerlevel10k)
- kde plasma config + raccourcis clavier
- pref thunderbird / firefox avec comptes
- keepass
- stocker donnée sensibles dans un .env ou autre vaulté
- liste des package / appimage à installer (client element, client nextcloud etc..)
- config session / images fond grub / animation lancement etc..
- Faire un profil "perso" et un profile "pro" pour différentier les configs et les personnalisations
