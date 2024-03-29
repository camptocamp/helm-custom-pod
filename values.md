# HELM custom Pod configuration

## Properties

- **`common`**
- **`global`** _(object)_
  - **`image`**: Refer to _[#/definitions/globalImage](#definitions/globalImage)_.
  - **`configMapNameOverride`**: Refer to _[#/definitions/configMapNameOverride](#definitions/configMapNameOverride)_.
  - **`revisionHistoryLimit`** _(integer)_: The number of old history to keep to allow rollback.
- **`nameOverride`**: Refer to _[#/definitions/nameOverride](#definitions/nameOverride)_.
- **`fullnameOverride`**: Refer to _[#/definitions/fullnameOverride](#definitions/fullnameOverride)_.
- **`serviceName`**: Refer to _[#/definitions/serviceName](#definitions/serviceName)_.
- **`releaseTrunc`**: Refer to _[#/definitions/releaseTrunc](#definitions/releaseTrunc)_.
- **`prefixTrunc`**: Refer to _[#/definitions/prefixTrunc](#definitions/prefixTrunc)_.
- **`metadata`** _(boolean)_: Create a ConfigMap to expose some metadata about the chart.
- **`ingress`** _(object)_: Cannot contain additional properties.
  - **`enabled`** _(boolean)_: Enable the Ingress.
  - **`nameOverride`**: Refer to _[#/definitions/nameOverride](#definitions/nameOverride)_.
  - **`fullnameOverride`**: Refer to _[#/definitions/fullnameOverride](#definitions/fullnameOverride)_.
  - **`serviceName`**: Refer to _[#/definitions/serviceName](#definitions/serviceName)_.
  - **`labels`**: Refer to _[#/definitions/labels](#definitions/labels)_.
  - **`annotations`**: Refer to _[#/definitions/annotations](#definitions/annotations)_.
  - **`podLabels`**: Refer to _[#/definitions/podLabels](#definitions/podLabels)_.
  - **`podAnnotations`**: Refer to _[#/definitions/podAnnotations](#definitions/podAnnotations)_.
  - **`resources`**: Refer to _[#/definitions/resources](#definitions/resources)_.
  - **`affinity`**: Refer to _[#/definitions/affinity](#definitions/affinity)_.
  - **`nodeSelector`**: Refer to _[#/definitions/nodeSelector](#definitions/nodeSelector)_.
  - **`hostGroups`** _(object)_: Can contain additional properties.
    - **Additional properties** _(object)_: Cannot contain additional properties.
      - **`hosts`** _(array)_
        - **Items** _(string)_
      - **`tls`** _(object)_: Cannot contain additional properties.
        - **`enabled`** _(boolean)_: Enable TLS.
        - **`secretName`** _(string)_: The name of the Secret.
- **`serviceAccount`**: Refer to _[#/definitions/serviceAccount](#definitions/serviceAccount)_.
- **`securityContext`**: Refer to _[#/definitions/securityContext](#definitions/securityContext)_.
- **`podSecurityContext`**: Refer to _[#/definitions/podSecurityContext](#definitions/podSecurityContext)_.
- **`affinity`**: Refer to _[#/definitions/affinity](#definitions/affinity)_.
- **`tolerations`**: Refer to _[#/definitions/tolerations](#definitions/tolerations)_.
- **`services`** _(object)_: Can contain additional properties.
  - **Additional properties** _(object)_: Cannot contain additional properties.
    - **`enabled`** _(boolean)_: Enable this service.
    - **`type`** _(string)_: The type of the service. Must be one of: `["Deployment", "StatefulSet", "Job"]`. Default: `"Deployment"`.
    - **`name`** _(string)_: The name of the service.
    - **`nameOverride`**: Refer to _[#/definitions/nameOverride](#definitions/nameOverride)_.
    - **`labels`**: Refer to _[#/definitions/labels](#definitions/labels)_.
    - **`annotations`**: Refer to _[#/definitions/annotations](#definitions/annotations)_.
    - **`podLabels`**: Refer to _[#/definitions/podLabels](#definitions/podLabels)_.
    - **`podAnnotations`**: Refer to _[#/definitions/podAnnotations](#definitions/podAnnotations)_.
    - **`serviceName`**: Refer to _[#/definitions/serviceName](#definitions/serviceName)_.
    - **`resources`**: Refer to _[#/definitions/resources](#definitions/resources)_.
    - **`releaseTrunc`**: Refer to _[#/definitions/releaseTrunc](#definitions/releaseTrunc)_.
    - **`prefixTrunc`**: Refer to _[#/definitions/prefixTrunc](#definitions/prefixTrunc)_.
    - **`affinity`**: Refer to _[#/definitions/affinity](#definitions/affinity)_.
    - **`nodeSelector`**: Refer to _[#/definitions/nodeSelector](#definitions/nodeSelector)_.
    - **`replicaCount`** _(integer)_: The number of replicas.
    - **`maxFailedIndexes`** _(integer)_: The maximum number of failed indexes.
    - **`parallelism`** _(integer)_: The number of parallel jobs.
    - **`backoffLimitPerIndex`** _(integer)_: The number of backoff limit per index.
    - **`completionMode`** _(string)_: The completion mode of the job. Must be one of: `["Indexed", "NonIndexed"]`.
    - **`completions`** _(integer)_: The number of completions.
    - **`minReadySeconds`** _(integer)_: The minimum number of seconds for the Pod to be ready.
    - **`persistentVolumeClaimRetentionPolicy`** _(object)_: The persistent volume claim retention policy.
    - **`replicas`** _(integer)_: The number of replicas.
    - **`paused`** _(boolean)_: Pause the deployment.
    - **`progressDeadlineSeconds`** _(integer)_: The number of seconds for the deployment to be ready.
    - **`strategy`** _(object)_: The deployment strategy. Cannot contain additional properties.
      - **`type`** _(string)_: The type of the strategy.
      - **`rollingUpdate`** _(object)_: The rolling update strategy.
    - **`suspend`** _(boolean)_: Suspend the job.
    - **`template`** _(boolean)_: Create the service keys in the self ConfigMap even if the service is disabled.
    - **`ttlSecondsAfterFinished`** _(integer)_: The number of seconds before the job is deleted.
    - **`backoffLimit`** _(integer)_: The number of backoff limit.
    - **`podReplacementPolicy`** _(string)_: The Pod replacement policy.
    - **`restartPolicy`** _(string)_: The Pod restart policy.
    - **`podFailurePolicy`** _(object)_: The Pod failure policy.
    - **`activeDeadlineSeconds`** _(integer)_: The number of seconds before the job is deleted.
    - **`ordinals`** _(object)_: The ordinals of the stateful set.
    - **`podManagementPolicy`** _(string)_: The Pod management policy. Must be one of: `["OrderedReady", "Parallel"]`.
    - **`updateStrategy`** _(object)_: The update strategy.
    - **`volumeClaimTemplates`** _(array)_: The volume claim templates, the key is the name of the volume claim template.
    - **`volumes`** _(object)_: The volumes configuration, the key is the name of the volume.
    - **`initContainers`** _(object)_: The initialization containers configuration. Can contain additional properties.
      - **Additional properties** _(object)_: Cannot contain additional properties.
        - **`image`**: Refer to _[#/definitions/image](#definitions/image)_.
        - **`env`**: Refer to _[#/definitions/env](#definitions/env)_.
        - **`resources`**: Refer to _[#/definitions/resources](#definitions/resources)_.
        - **`command`**: Refer to _[#/definitions/command](#definitions/command)_.
        - **`args`**: Refer to _[#/definitions/args](#definitions/args)_.
        - **`volumeMounts`**: Refer to _[#/definitions/volumeMounts](#definitions/volumeMounts)_.
        - **`volumeDevices`**: Refer to _[#/definitions/volumeDevices](#definitions/volumeDevices)_.
    - **`containers`** _(object)_: The containers configuration. Can contain additional properties.
      - **Additional properties** _(object)_: Cannot contain additional properties.
        - **`image`**: Refer to _[#/definitions/image](#definitions/image)_.
        - **`env`**: Refer to _[#/definitions/env](#definitions/env)_.
        - **`resources`**: Refer to _[#/definitions/resources](#definitions/resources)_.
        - **`command`**: Refer to _[#/definitions/command](#definitions/command)_.
        - **`args`**: Refer to _[#/definitions/args](#definitions/args)_.
        - **`volumeMounts`**: Refer to _[#/definitions/volumeMounts](#definitions/volumeMounts)_.
        - **`volumeDevices`**: Refer to _[#/definitions/volumeDevices](#definitions/volumeDevices)_.
        - **`ports`** _(object)_: The ports, key is the name of the port.
        - **`livenessProbe`** _(object)_
        - **`readinessProbe`** _(object)_
        - **`startupProbe`** _(object)_
    - **`ingress`** _(object)_: Cannot contain additional properties.
      - **`enabled`** _(boolean)_: Enable the ingress for this service.
      - **`path`** _(string)_: The path of the ingress.
    - **`service`** _(object)_: The Kubernetes service configuration. Cannot contain additional properties.
      - **`name`** _(string)_: The name of the service.
      - **`type`** _(string)_: The type of the service. Default: `"ClusterIP"`.
      - **`servicePort`** _(integer)_: The port of the service. Default: `80`.
      - **`labels`**: Refer to _[#/definitions/labels](#definitions/labels)_.
      - **`annotations`**: Refer to _[#/definitions/annotations](#definitions/annotations)_.
      - **`ports`** _(array)_
    - **`podMonitor`** _(object)_: The Prometheus Pod monitor configuration. Cannot contain additional properties.
      - **`enabled`** _(boolean)_: Enable the Pod monitor for this service.
      - **`endpoint`** _(object)_: The endpoint of the Pod monitor.

## Definitions

- <a id="definitions/nameOverride"></a>**`nameOverride`** _(string)_: [helm-common] Override the name.
- <a id="definitions/fullnameOverride"></a>**`fullnameOverride`** _(string)_: [helm-common] Override the fullname.
- <a id="definitions/releaseTrunc"></a>**`releaseTrunc`** _(integer)_: [helm-common] The release trunk length. Default: `20`.
- <a id="definitions/prefixTrunc"></a>**`prefixTrunc`** _(integer)_: [helm-common] The prefix trunk length (release and chart name). Default: `40`.
- <a id="definitions/serviceAccount"></a>**`serviceAccount`** _(object)_: [helm-common] Service account configuration. Cannot contain additional properties.
  - **`create`** _(boolean)_: Create a service account.
  - **`name`** _(string)_: Name of the service account.
- <a id="definitions/podSecurityContext"></a>**`podSecurityContext`** _(object)_: [helm-common] Pod security context.
- <a id="definitions/securityContext"></a>**`securityContext`** _(object)_: [helm-common] Container security context.
- <a id="definitions/globalImage"></a>**`globalImage`** _(object)_: [helm-common] global image configuration. Cannot contain additional properties.
  - **`pullPolicy`** _(string)_: Image pull policy.
  - **`pullSecrets`** _(array)_: Image pull secrets.
- <a id="definitions/configMapNameOverride"></a>**`configMapNameOverride`** _(object)_: [helm-common] global: Used to be able to globally override the name of the ConfigMap. Can contain additional properties.
  - **Additional properties** _(string)_
- <a id="definitions/labels"></a>**`labels`** _(object)_: [helm-common] Pod labels. Can contain additional properties.
  - **Additional properties** _(string)_
- <a id="definitions/annotations"></a>**`annotations`** _(object)_: [helm-common] Pod annotations. Can contain additional properties.
  - **Additional properties** _(string)_
- <a id="definitions/podLabels"></a>**`podLabels`** _(object)_: [helm-common] Labels used only in the Pod definition. Can contain additional properties.
  - **Additional properties** _(string)_
- <a id="definitions/podAnnotations"></a>**`podAnnotations`** _(object)_: [helm-common] Annotations used only in the Pod definition. Can contain additional properties.
  - **Additional properties** _(string)_
- <a id="definitions/serviceName"></a>**`serviceName`** _(string)_: [helm-common] The name of the service (not Kubernetes service), this will postfix the name.
- <a id="definitions/affinity"></a>**`affinity`** _(object)_: [helm-common] Pod: The used affinity.
- <a id="definitions/tolerations"></a>**`tolerations`** _(array)_: [helm-common] Pod: Tolerations.
- <a id="definitions/nodeSelector"></a>**`nodeSelector`** _(object)_: [helm-common] Pod: Node selector.
- <a id="definitions/image"></a>**`image`** _(object)_: [helm-common] Container: Image configuration.
  - ## **Any of**
    -
  - **`repository`** _(string, required)_: Image repository.
  - **`tag`** _(string)_: Image tag, used if the sha is not defined.
  - **`sha`** _(['null', 'string'])_: Image sha.
- <a id="definitions/env"></a>**`env`** _(object)_: [helm-common] Container: Environment variables. Can contain additional properties.
  - **Additional properties**
    - **One of**
      - _object_
        - **`type`** _(string, required)_: Disable the environment variable. Must be one of: `["none"]`.
      - _object_
        - **`type`** _(string)_: Environment variable from a direct value. Must be one of: `["value"]`. Default: `"value"`.
        - **`order`** _(integer)_: Order of the environment variable. Must be one of: `[0, 1]`. Default: `0`.
        - **`value`** _(string, required)_: Value of the environment variable.
      - _object_
        - **`type`** _(string, required)_: Environment variable from a ConfigMap or a Secret. Must be one of: `["configMap", "secret"]`.
        - **`order`** _(integer)_: Order of the environment variable. Must be one of: `[0, 1]`. Default: `0`.
        - **`name`** _(string, required)_: Name of the ConfigMap or Secret, if 'self', same name as the service.
        - **`key`** _(string, required)_: Key of the ConfigMap or Secret.
      - _object_
        - **`type`** _(string, required)_: Free field type for an environment variable.
        - **`order`** _(integer)_: Order of the environment variable. Must be one of: `[0, 1]`. Default: `0`.
        - **`valueFrom`** _(object, required)_
- <a id="definitions/resources"></a>**`resources`** _(object)_: [helm-common] Container: The container resources.
- <a id="definitions/command"></a>**`command`** _(array)_: Container: The container command.
  - **Items** _(string)_
- <a id="definitions/args"></a>**`args`** _(array)_: Container: The container arguments.
  - **Items** _(string)_
- <a id="definitions/volumeMounts"></a>**`volumeMounts`** _(object)_: Container: Volume mounts, the key is the mountPath of the volume.
- <a id="definitions/volumeDevices"></a>**`volumeDevices`** _(object)_: Container: Volume devices, the key is the devicePath of the volume.
