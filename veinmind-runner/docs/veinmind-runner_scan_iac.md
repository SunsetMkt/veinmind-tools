## veinmind-runner scan iac

Scan iac

### Synopsis

Scan iac from multi source, include host/git/kubernetes

```
veinmind-runner scan iac [flags] target
```

### Examples

```

1. scan host iac (current directory)
veinmind-runner scan iac host:./

2. scan github kubernetes-sigs/kustomize repo iac
veinmind-runner scan iac git:https://github.com/kubernetes-sigs/kustomize.git

3. scan kubernetes pod iac
veinmind-runner scan iac --kubeconfig admin.yaml kubernetes:pod

```

### Options

```
  -h, --help                help for iac
      --iac-type string     dedicate iac type for iac files
  -k, --kubeconfig string   k8s config file
  -n, --namespace string    k8s resource namespace (default "all")
      --proxy string        proxy to git like: https://xxxxx or socks5://xxxx
      --sshkey string       auth to git if use by ssh proto
```

### Options inherited from parent commands

```
  -e, --exit-code int   exit-code when veinmind-runner find security issues
  -g, --glob string     specifies the pattern of plugin file to find
      --insecure-skip   skip tls config
  -o, --output string   output filepath of report (default "report.json")
      --threads int     threads for scan action (default 5)
```

### SEE ALSO

* [veinmind-runner scan](veinmind-runner_scan.md)	 - Scan cloud native objects security, include image/container/iac

###### Auto generated by spf13/cobra on 18-Jan-2023