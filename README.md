# SSHD

[![Docker Repository on Quay.io](https://quay.io/repository/macropin/sshd/status "Docker Repository on Quay.io")](https://quay.io/repository/macropin/sshd)

Minimal Alpine Linux Docker container with `sshd` exposed and `rsync` installed.

Set the Docker Environment variable AUTHORIZED_KEYS to the keys (separated by comma) you want to grant access.

Optionally mount a custom sshd config at `/etc/ssh/`.

## Usage Example

```
docker run -E AUTHORIZED_KEYS="<key_1>,<key_2> -d -p 2222:22 -v /secrets/id_rsa.pub:/root/.ssh/authorized_keys:ro -v /mnt/data/:/data/ quay.io/macropin/sshd
````
