# ansible-ha-streamdeck
Ansible playbook to set up a device for use with the Home Assistant Stream Deck addon

## About the Stream Deck Addon
See [home-assistant-streamdeck-yaml](https://github.com/basnijholt/home-assistant-streamdeck-yaml) for more information

## Installation
1. Edit `inventory.yaml` and set the IP address of your device
2. Create a file called `credentials.txt` and enter your SSH password
3. Edit `files/.env.example.j2` and fill out your details as appropriate. Be careful of `wss` vs `ws` when using a Nabu Casa URL vs. a local IP address 
4. Run `ansible-playbook -u [your SSH username] -i inventory.yaml --become-password-file credentials.txt --connection-password-file credentials.txt main.yaml`