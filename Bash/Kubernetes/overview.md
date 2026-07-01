# kubectl Commands

| Command                       | Description                      |
| ----------------------------- | -------------------------------- |
| `kubectl apply`               | Create or update resources       |
| `kubectl create`              | Create resources                 |
| `kubectl delete`              | Delete resources                 |
| `kubectl replace`             | Replace resources                |
| `kubectl patch`               | Patch resources                  |
| `kubectl edit`                | Edit resources                   |
| `kubectl get`                 | Display resources                |
| `kubectl describe`            | Show detailed information        |
| `kubectl explain`             | Display API documentation        |
| `kubectl api-resources`       | List resource types              |
| `kubectl api-versions`        | List API versions                |
| `kubectl cluster-info`        | Display cluster information      |
| `kubectl version`             | Show client/server version       |
| `kubectl config`              | Manage kubeconfig                |
| `kubectl auth`                | Authorization commands           |
| `kubectl certificate`         | Manage certificate requests      |
| `kubectl wait`                | Wait for conditions              |
| `kubectl label`               | Manage labels                    |
| `kubectl annotate`            | Manage annotations               |
| `kubectl taint`               | Manage node taints               |
| `kubectl cordon`              | Mark node unschedulable          |
| `kubectl uncordon`            | Mark node schedulable            |
| `kubectl drain`               | Safely evict workloads           |
| `kubectl rollout`             | Manage deployments               |
| `kubectl scale`               | Scale workloads                  |
| `kubectl autoscale`           | Create autoscalers               |
| `kubectl expose`              | Expose resource as Service       |
| `kubectl exec`                | Execute command inside container |
| `kubectl logs`                | Display container logs           |
| `kubectl cp`                  | Copy files                       |
| `kubectl attach`              | Attach to running process        |
| `kubectl port-forward`        | Forward local ports              |
| `kubectl proxy`               | Run Kubernetes proxy             |
| `kubectl top`                 | Display CPU and memory usage     |
| `kubectl diff`                | Compare manifests                |
| `kubectl apply --server-side` | Server-side apply                |
| `kubectl completion`          | Generate shell completion        |
| `kubectl plugin`              | Manage plugins                   |

---

# Common Resource Types

| Resource                  | Description                  |
| ------------------------- | ---------------------------- |
| `Pod`                     | Smallest deployable unit     |
| `Deployment`              | Stateless application        |
| `ReplicaSet`              | Maintain replica count       |
| `StatefulSet`             | Stateful applications        |
| `DaemonSet`               | One Pod per node             |
| `Job`                     | One-time workload            |
| `CronJob`                 | Scheduled workload           |
| `Service`                 | Network abstraction          |
| `Ingress`                 | HTTP routing                 |
| `NetworkPolicy`           | Network security             |
| `ConfigMap`               | Configuration storage        |
| `Secret`                  | Sensitive configuration      |
| `PersistentVolume`        | Physical storage             |
| `PersistentVolumeClaim`   | Storage request              |
| `StorageClass`            | Storage provisioning         |
| `Namespace`               | Resource isolation           |
| `Node`                    | Cluster machine              |
| `Event`                   | Cluster events               |
| `EndpointSlice`           | Service endpoints            |
| `HorizontalPodAutoscaler` | Automatic scaling            |
| `VerticalPodAutoscaler`   | Vertical scaling (extension) |
| `ResourceQuota`           | Namespace quotas             |
| `LimitRange`              | Resource limits              |
| `PriorityClass`           | Scheduling priority          |
| `RuntimeClass`            | Container runtime            |
| `Lease`                   | Leader election              |
| `ServiceAccount`          | Pod identity                 |
| `Role`                    | Namespace permissions        |
| `ClusterRole`             | Cluster permissions          |
| `RoleBinding`             | Assign namespace role        |
| `ClusterRoleBinding`      | Assign cluster role          |
| `CSIDriver`               | CSI driver                   |
| `CSIStorageCapacity`      | CSI capacity                 |
| `VolumeAttachment`        | Storage attachment           |

---

# kubectl create Subcommands

| Command                             | Description               |
| ----------------------------------- | ------------------------- |
| `kubectl create deployment`         | Create Deployment         |
| `kubectl create pod`                | Create Pod                |
| `kubectl create service`            | Create Service            |
| `kubectl create namespace`          | Create Namespace          |
| `kubectl create configmap`          | Create ConfigMap          |
| `kubectl create secret`             | Create Secret             |
| `kubectl create job`                | Create Job                |
| `kubectl create cronjob`            | Create CronJob            |
| `kubectl create ingress`            | Create Ingress            |
| `kubectl create quota`              | Create ResourceQuota      |
| `kubectl create role`               | Create Role               |
| `kubectl create rolebinding`        | Create RoleBinding        |
| `kubectl create clusterrole`        | Create ClusterRole        |
| `kubectl create clusterrolebinding` | Create ClusterRoleBinding |
| `kubectl create serviceaccount`     | Create ServiceAccount     |

---

# kubectl rollout Commands

| Command           | Description            |
| ----------------- | ---------------------- |
| `rollout status`  | Display rollout status |
| `rollout history` | Show rollout history   |
| `rollout undo`    | Roll back deployment   |
| `rollout restart` | Restart workload       |
| `rollout pause`   | Pause rollout          |
| `rollout resume`  | Resume rollout         |

---

# kubectl config Commands

| Command                  | Description                |
| ------------------------ | -------------------------- |
| `config current-context` | Show current context       |
| `config get-contexts`    | List contexts              |
| `config use-context`     | Switch context             |
| `config set-context`     | Create or modify context   |
| `config delete-context`  | Remove context             |
| `config rename-context`  | Rename context             |
| `config view`            | Show kubeconfig            |
| `config set-cluster`     | Configure cluster          |
| `config set-credentials` | Configure user             |
| `config unset`           | Remove configuration value |

---

# kubectl auth Commands

| Command          | Description       |
| ---------------- | ----------------- |
| `auth can-i`     | Check permissions |
| `auth reconcile` | Reconcile RBAC    |

---

# Common Output Formats

| Option              | Description        |
| ------------------- | ------------------ |
| `-o wide`           | Extended output    |
| `-o yaml`           | YAML output        |
| `-o json`           | JSON output        |
| `-o jsonpath`       | JSONPath output    |
| `-o custom-columns` | Custom columns     |
| `-o name`           | Resource names     |
| `-o go-template`    | Go template output |

---

# Label Selectors

| Selector          | Description       |
| ----------------- | ----------------- |
| `key=value`       | Exact match       |
| `key!=value`      | Not equal         |
| `key in (...)`    | Value in list     |
| `key notin (...)` | Value not in list |
| `key`             | Label exists      |
| `!key`            | Label missing     |

---

# Field Selectors

| Selector              | Description     |
| --------------------- | --------------- |
| `metadata.name=`      | Match name      |
| `metadata.namespace=` | Match namespace |
| `status.phase=`       | Pod phase       |
| `spec.nodeName=`      | Node assignment |
| `spec.restartPolicy=` | Restart policy  |

---

# Pod Spec Fields

| Field                           | Description               |
| ------------------------------- | ------------------------- |
| `containers`                    | Container list            |
| `initContainers`                | Initialization containers |
| `volumes`                       | Volumes                   |
| `restartPolicy`                 | Restart behavior          |
| `dnsPolicy`                     | DNS policy                |
| `nodeSelector`                  | Node selection            |
| `nodeName`                      | Fixed node                |
| `affinity`                      | Scheduling rules          |
| `tolerations`                   | Accept taints             |
| `priorityClassName`             | Scheduling priority       |
| `serviceAccountName`            | Service account           |
| `hostNetwork`                   | Host networking           |
| `hostPID`                       | Host PID namespace        |
| `hostIPC`                       | Host IPC namespace        |
| `securityContext`               | Pod security              |
| `terminationGracePeriodSeconds` | Shutdown timeout          |

---

# Container Fields

| Field             | Description           |
| ----------------- | --------------------- |
| `name`            | Container name        |
| `image`           | Container image       |
| `command`         | Startup command       |
| `args`            | Command arguments     |
| `env`             | Environment variables |
| `ports`           | Container ports       |
| `resources`       | CPU and memory        |
| `volumeMounts`    | Mounted volumes       |
| `livenessProbe`   | Health check          |
| `readinessProbe`  | Readiness check       |
| `startupProbe`    | Startup health check  |
| `securityContext` | Container security    |
| `workingDir`      | Working directory     |
| `stdin`           | Enable stdin          |
| `tty`             | Allocate TTY          |

---

# Volume Types

| Volume                  | Description        |
| ----------------------- | ------------------ |
| `emptyDir`              | Temporary storage  |
| `hostPath`              | Host directory     |
| `configMap`             | ConfigMap volume   |
| `secret`                | Secret volume      |
| `persistentVolumeClaim` | Persistent storage |
| `projected`             | Combined volume    |
| `downwardAPI`           | Pod metadata       |
| `nfs`                   | NFS storage        |
| `csi`                   | CSI storage        |
| `image`                 | OCI image volume   |

---

# Service Types

| Type           | Description         |
| -------------- | ------------------- |
| `ClusterIP`    | Internal service    |
| `NodePort`     | Expose node port    |
| `LoadBalancer` | Cloud load balancer |
| `ExternalName` | External DNS        |

---

# Deployment Strategy Types

| Strategy        | Description        |
| --------------- | ------------------ |
| `RollingUpdate` | Rolling deployment |
| `Recreate`      | Replace all Pods   |

---

# Restart Policies

| Policy      | Description        |
| ----------- | ------------------ |
| `Always`    | Always restart     |
| `OnFailure` | Restart on failure |
| `Never`     | Never restart      |

---

# Image Pull Policies

| Policy         | Description       |
| -------------- | ----------------- |
| `Always`       | Always pull image |
| `IfNotPresent` | Pull if missing   |
| `Never`        | Never pull        |

---

# Common kubectl Flags

| Flag               | Description                     |
| ------------------ | ------------------------------- |
| `-A`               | All namespaces                  |
| `-n`               | Namespace                       |
| `-f`               | Manifest file                   |
| `-l`               | Label selector                  |
| `--field-selector` | Field selector                  |
| `--watch`          | Watch changes                   |
| `--watch-only`     | Watch only                      |
| `--dry-run=client` | Client-side dry run             |
| `--dry-run=server` | Server-side dry run             |
| `--force`          | Force operation                 |
| `--grace-period`   | Shutdown grace period           |
| `--timeout`        | Timeout                         |
| `--selector`       | Label selector                  |
| `--all`            | All resources                   |
| `--recursive`      | Recursive processing            |
| `--validate`       | Validate manifests              |
| `--save-config`    | Save last applied configuration |
| `--context`        | Kubernetes context              |
| `--kubeconfig`     | Specify kubeconfig file         |

---

# Resource Management Fields

| Field                        | Description                  |
| ---------------------------- | ---------------------------- |
| `requests.cpu`               | Guaranteed CPU               |
| `requests.memory`            | Guaranteed memory            |
| `limits.cpu`                 | Maximum CPU                  |
| `limits.memory`              | Maximum memory               |
| `requests.ephemeral-storage` | Guaranteed ephemeral storage |
| `limits.ephemeral-storage`   | Maximum ephemeral storage    |

---

# Common API Groups

| API Group                      | Description                           |
| ------------------------------ | ------------------------------------- |
| `apps`                         | Deployments, StatefulSets, DaemonSets |
| `batch`                        | Jobs and CronJobs                     |
| `core`                         | Pods, Services, ConfigMaps, Secrets   |
| `networking.k8s.io`            | Ingress, NetworkPolicy                |
| `rbac.authorization.k8s.io`    | Roles and bindings                    |
| `storage.k8s.io`               | Storage classes and CSI               |
| `autoscaling`                  | HorizontalPodAutoscaler               |
| `coordination.k8s.io`          | Leases                                |
| `policy`                       | Pod disruption budgets                |
| `admissionregistration.k8s.io` | Admission webhooks                    |

---

# Common YAML Metadata Fields

| Field                  | Description       |
| ---------------------- | ----------------- |
| `apiVersion`           | API version       |
| `kind`                 | Resource type     |
| `metadata`             | Resource metadata |
| `metadata.name`        | Resource name     |
| `metadata.namespace`   | Namespace         |
| `metadata.labels`      | Labels            |
| `metadata.annotations` | Annotations       |
| `spec`                 | Desired state     |
| `status`               | Current state     |