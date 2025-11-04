# ansible-ha-streamdeck
Ansible playbook to set up a device for use with the Home Assistant Stream Deck addon

## About the Stream Deck Addon
See [home-assistant-streamdeck-yaml](https://github.com/basnijholt/home-assistant-streamdeck-yaml) for more information

## Installation
1. Edit `inventory.yaml` and set the IP address of your device (e.g. Raspberry Pi)
2. Create a file called `credentials.txt` and enter your SSH password
3. Run `ansible-playbook -u [your SSH username] -i inventory.yaml --become-password-file credentials.txt --connection-password-file credentials.txt main.yaml`