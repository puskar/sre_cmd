# sre_cmd

*NAME*

`sre.py` - `sre.py` provides several commands to manage aspects of a Kubenetes cluster

*INSTALL*

1. Copy the script to your local machine and run `chmod +x sre.py`
2. Make sure the `kubectl` command is installed and in your `$PATH`
To get `kubectl`, please see https://kubernetes.io/docs/tasks/tools/

*USAGE*

The `sre.py` command provides a CLI to perform the following actions on a Kubernetes instance:

`sre list` - lists deployments in a namespace

Supported arguments:

`--namespace` - specifies the namespace to examine. If omitted, will list all deployments in all namespaces

Note: the `--namespace` argument works with all commands

`sre scale` - Scales a deployment to the desired number of replicas

Supported arguments:

`–-replicas` - number of replicas

`–-deployment` - deployment name

`--namespace` - scale deployment in a specific namespace, otherwise it will try to look for the deployment in all namespaces

`sre info` - Prints info on the deployment (you can choose what info you would like exactly to output)

Supported arguments:

`-–deployment` - deployment name

`–-namespace` - prints info on the deployment in the given namespace, otherwise it will print info on the first deployment found
