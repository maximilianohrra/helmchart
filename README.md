With Helm installed in the local PC, you can use minikube to install a local chart.

$ helm create <chartname>

The "helm create" command is used to create a template for a Helm package, which is a tool for managing applications on Kubernetes. The template includes all the necessary files to create an application on a Kubernetes cluster, including a configuration file, a dependencies file, and a default values file for configuration parameters. When the "helm create" command is run, a folder with the specified name will be created containing all of these files.

$ "helm install --dry-run debug ."
The "helm install --dry-run debug" command installs a Helm package on a Kubernetes cluster, but in "dry-run" mode, meaning that no changes are made to the cluster. Instead, Helm generates and displays a representation of the final configuration that would be applied to the cluster if the command was run without the "dry-run" mode. The "debug" mode also enables debug output, providing additional information about how the command is being run. This command is useful for testing and debugging the configuration of a Helm package before permanently installing it on a cluster.

- values.yaml - 
In order to modify any option you could directly do it throw the "values.yaml" instead of hardcoding the deployment manually.

The "helm lint" command checks a Helm chart for formatting and syntax errors, and verifies that all the required fields are present. It is used to ensure that a chart is well-formed and ready to be installed on a Kubernetes cluster.

The "helm package + path" command is used to package a Helm chart into a format that can be shared and deployed. It creates a compressed archive (.tgz file) of the chart's source files, which can then be stored in a chart repository or shared directly with others. The resulting package can be installed on a Kubernetes cluster using the "helm install" command.

The "helm repo index" command generates an index file for a chart repository. It takes a directory that contains packaged charts as input and creates an index.yaml file that lists the charts and their versions. The index file is used by Helm to discover and install charts from the repository. The "helm repo index" command is typically used to create or update the index for a local chart repository that is served over HTTP. 

The "helm repo add <name> +URLgithubpages" command adds a Helm chart repository to the local list of Helm repositories. This allows Helm to discover and install charts from that repository using the "helm install" command. The "helm repo add" command takes as arguments the repository name and its URL. Once added, the repository can be used by Helm to discover and download charts.

Then you can check it with "helm search repo <name>"