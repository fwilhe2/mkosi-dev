# dev
lima-based development environment

This is to be used with the [VS Code SSH Remote plugin](https://code.visualstudio.com/docs/remote/ssh)

```bash
limactl create --name dev dev.yaml
limactl start dev
less +F ${LIMA_HOME:-$HOME/.lima}/dev/serial*.log
echo "Include ${LIMA_HOME:-$HOME/.lima}/dev/ssh.config" >> ~/.ssh/config
limactl shell dev
```

Connect to vs code ssh remote plugin via name 'lima-dev'
