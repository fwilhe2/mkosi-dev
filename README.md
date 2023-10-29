# mkosi-dev
lima-based development environment for images based on [mkosi](https://github.com/systemd/mkosi)

This is to be used with the [VS Code SSH Remote plugin](https://code.visualstudio.com/docs/remote/ssh)

```bash
limactl create --name mkosi-dev mkosi-dev.yaml
limactl start mkosi-dev
less +F ${LIMA_HOME:-$HOME/.lima}/mkosi-dev/serial*.log
echo "Include ${LIMA_HOME:-$HOME/.lima}/mkosi-dev/ssh.config" >> ~/.ssh/config
limactl shell mkosi-dev
```

Connect to vs code ssh remote plugin via name 'lima-mkosi-dev'

## Using with lima

Download images

```
gh run download --name fedora-image-x86-64
gh run download --name fedora-image-arm64

gh run download --name debian-image-x86-64
gh run download --name debian-image-arm64
```

Create vm

```
limactl create --name fedora fedora.yaml

limactl create --name debian debian.yaml
```