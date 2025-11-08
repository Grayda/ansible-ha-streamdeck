# ansible-ha-streamdeck
Ansible playbook to set up a device for use with the Home Assistant Stream Deck addon

## About the Stream Deck Addon
See [home-assistant-streamdeck-yaml](https://github.com/basnijholt/home-assistant-streamdeck-yaml) for more information

## Installation
1. Install Ansible. Instructions can be found on the [Ansible website](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#pipx-install)
2. Edit `inventory.yaml` and set the IP address of your device
3. Create a file called `credentials.txt` and enter your SSH password. This is optional, but you'll need to modify the `ansible-playbook` command in step 6
4. Edit `files/.env.example.j2` and fill out your details as appropriate. Be careful of `wss` vs `ws` when using a Nabu Casa URL vs. a local IP address
5. Edit `files/configuration.yaml.j2` and add in your button / dial definitions. See [the documentation](https://github.com/basnijholt/home-assistant-streamdeck-yaml) for info
6. Run `ansible-playbook -u [your SSH username] -i inventory.yaml --become-password-file credentials.txt --connection-password-file credentials.txt main.yaml`
