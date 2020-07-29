# Ansible Role for your Dotfiles repo

An Ansible role to get your dotfiles repo to your system.

## Usage

I assume you have already setup [Ansible](https://ansible.com) and your [Ansible playbook](https://docs.ansible.com/ansible/latest/user_guide/playbooks.html) with the [best practices](https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html#directory-layout) in mind.

Go to your playbook root directory and run

```bash
git submodule add https://github.com/ansible-roles-group/ansible-role-dotfiles roles/dotfiles
```

This will add the role to your git project structure. You now have to add it to your playbooks role section (checkout the [official docs](https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html) if you don't know what I'm talking about). It will look something like this:

```yaml
---

- name: Setup basic stuff for all devices
  hosts: all
  roles:
    - dotfiles
```

To get your dotfiles via this role execute your whole playbook or use one of the [tags](#Tags) provided by this role.

Checkout the [Ansible Roles Group / Ansible Arch Linux Playbook](https://github.com/ansible-roles-group/ansible-arch-linux-playbook) for a complete example setup.

## Tags

In this role the following tags are included.

- dotfiles

Checkout my [Gist - Advanced Ansible task tagging](https://gist.github.com/BennyLi/060ecf3bead4ac007bf3752280cc9e17) for more information on why my tags look like this.

# Buy me a cup of tea 🍵

If you like my work feel free to bring some love back. 

- Give this repo a ⭐
- Follow me on [GitHub](https://github.com/BennyLi) or [Twitter](https://twitter.com/BennyLindemann)
- Drop some 💰 via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=L5FWZYAM5Y5A4&source=url)