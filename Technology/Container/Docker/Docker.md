Docker is controlled by a `root-owned Unit socket`:

```bash
/var/run/docker.sock
```

```bash
srw-rw---- root docker /var/run/docker.sock
```

#tech #container