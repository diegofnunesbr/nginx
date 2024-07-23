# Nginx

### Instalar o Nginx no Kubernetes:

- `git clone git@github.com:diegofnunesbr/nginx.git`
- `cd nginx`
- `helm install --create-namespace nginx -n nginx .`

### Configurar o Nginx no arquivo hosts do Windows:

- `sudo tee -a /mnt/c/Windows/System32/drivers/etc/hosts <<< "$(ifconfig eth0 | grep 'inet ' | awk '{print $2}') nginx.local"`

### Remover o Nginx no Kubernetes:

- `helm uninstall nginx -n nginx`
