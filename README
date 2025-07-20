Local development environment setup:
```
sudo apt install -y uv
uv venv
source .venv/bin/activate
uv pip install ansible
up pip install passlib # for creating password hashes
```

Remote machine setup
All we need is a plain, freshly installed debian server. The only requirements are:

- installer user with sudo privileges
- ssh server up and running
    - ssh public key authentication enabled for install user
- python3 installed

## SSH
SSH gets hardened automatically so that only public key authenticaion is allowed

## User settings
### User password
Generate a new password with `ansible all -i localhost, -m debug -a "msg={{ 'mypassword' | password_hash('sha512', 'mysecretsalt') }}"`
Paste the hash into the host_vars file of the remote client.
