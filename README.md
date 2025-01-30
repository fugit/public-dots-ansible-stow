# Dotfiles ansible

Dotfiles automation using ansible

## SSH Keys and GPG Keys

- need to copy ssh and gpg keys from existing source
- ssh-add for ssh keys
  ~/.ssh/id*rsa*{4096,}\_pw
- gpg --import for gpg key
  ~/gnupg/

## Packages

- No longer using debian on my desktops should remove or cleanup
  - Working on setting up unified packages debian and pacman.
    - 2.0+ should be able to use a the unified package system
    - [ansible-docs-package-module][ansible-docs-package-module]

## TODO

- Setup **bash-my-aws**, maybe use ansible clone repos instead of dotfiles for this
  - [github-bash-my-aws][github-bash-my-aws]
- DONE: **neovim plugins**: (lazyvim) figure out a good way to handle

## Arch Stuff

- cleanup pacman cache
  - [average-arch-cleanup] [average-arch-cleanup]
- tmpfs maybe switch to this or setup cleanup of /tmp/
  - one downside of /tmpfs is limited size ...
  - Also its already setup with btrfs :shrug:

## Notes

- run playbook

```bash
echo all
ansible-playbook setup.yml
echo "Only tag config"
ansible-playbook setup.yml --tag config
```

- **termite** not coppied over project dead... we moved to alacritty
- **alacritty** replaced with ghostty... very surprised but really enjoying it.
- **zathura** looks kind of cool

## Links

- [ansible-docs-package-module][ansible-docs-package-module]
- [average-arch-cleanup] [average-arch-cleanup]
- [github-bash-my-aws][github-bash-my-aws]

<!-- Identifiers, in alphabetical order -->

[ansible-docs-package-module]: https://docs.ansible.com/ansible/latest/collections/ansible/builtin/package_module.html#requirements
[github-bash-my-aws]: https://github.com/bash-my-aws/bash-my-aws
[average-arch-cleanup]: https://averagelinuxuser.com/clean-arch-linux/
