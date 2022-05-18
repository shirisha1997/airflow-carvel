# Apache Airflow package

Apache Airflow is a tool to express and execute workflows as directed acyclic graphs (DAGs). It includes utilities to schedule tasks, monitor task progress and handle task dependencies.

## Airflow common parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
auth.password|Password to access web UI|string|""|

## Airflow web parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
web.image.registry|Airflow image registry|string|docker.io|
web.image.repository|Airflow image repository|string|bitnami/airflow|
web.image.pullPolicy|Airflow image pull policy|string|IfNotPresent|
web.containerPorts.http|Airflow web HTTP container port|integer|8080|
web.replicaCount|Number of Airflow web replicas|integer|1|
web.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|180|
web.livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|20|
web.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|5|
web.livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|6|
web.livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
web.readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|30|
web.readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|10|
web.readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|5|
web.readinessProbe.failureThreshold|Failure threshold for readinessProbe|integer|6|
web.readinessProbe.successThreshold|Success threshold for readinessProbe|integer|1|
web.startupProbe.enabled|Enable startupProbe on Airflow web containers|string|FALSE|
web.startupProbe.initialDelaySeconds|Initial delay seconds for startupProbe|integer|60|
web.startupProbe.periodSeconds|Period seconds for startupProbe|integer|10|
web.startupProbe.timeoutSeconds|Timeout seconds for startupProbe|integer|1|
web.startupProbe.failureThreshold|Failure threshold for startupProbe|integer|15|
web.startupProbe.successThreshold|Success threshold for startupProbe|integer|1|
web.podSecurityContext.fsGroup|Set Airflow web pod's Security Context fsGroup|integer|1001|
web.containerSecurityContext.runAsUser|Set Airflow web containers' Security Context runAsUser|integer|1001|
web.containerSecurityContext.runAsNonRoot|Set Airflow web containers' Security Context runAsNonRoot|string|TRUE|

## Airflow scheduler parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
scheduler.image.registry|Airflow Scheduler image registry|string|docker.io|
scheduler.image.repository|Airflow Scheduler image repository|string|bitnami/airflow-scheduler|
scheduler.image.pullPolicy|Airflow Scheduler image pull policy|string|IfNotPresent|
scheduler.image.pullSecrets|Airflow Scheduler image pull secrets|string|[]|
scheduler.replicaCount|Number of scheduler replicas|integer|1|
scheduler.podSecurityContext.fsGroup|Set Airflow scheduler pod's Security Context fsGroup|integer|1001|
scheduler.containerSecurityContext.runAsUser|Set Airflow scheduler containers' Security Context runAsUser|integer|1001|
scheduler.containerSecurityContext.runAsNonRoot|Set Airflow scheduler containers' Security Context runAsNonRoot|string|TRUE|

## Airflow worker parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
worker.image.registry|Airflow Worker image registry|string|docker.io|
worker.image.repository|Airflow Worker image repository|string|bitnami/airflow-worker|
worker.image.pullPolicy|Airflow Worker image pull policy|string|IfNotPresent|
worker.containerPorts.http|Airflow worker HTTP container port|integer|8793|
worker.replicaCount|Number of Airflow worker replicas|integer|1|
worker.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|180|
worker.livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|20|
worker.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|5|
worker.livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|6|
worker.livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
worker.readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|30|
worker.readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|10|
worker.readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|5|
worker.readinessProbe.failureThreshold|Failure threshold for readinessProbe|integer|6|
worker.readinessProbe.successThreshold|Success threshold for readinessProbe|integer|1|
worker.startupProbe.enabled|Enable startupProbe on Airflow worker containers|string|FALSE|
worker.startupProbe.initialDelaySeconds|Initial delay seconds for startupProbe|integer|60|
worker.startupProbe.periodSeconds|Period seconds for startupProbe|integer|10|
worker.startupProbe.timeoutSeconds|Timeout seconds for startupProbe|integer|1|
worker.startupProbe.failureThreshold|Failure threshold for startupProbe|integer|15|
worker.startupProbe.successThreshold|Success threshold for startupProbe|integer|1|
worker.podSecurityContext.fsGroup|Set Airflow worker pod's Security Context fsGroup|integer|1001|
worker.containerSecurityContext.runAsUser|Set Airflow worker containers' Security Context runAsUser|integer|1001|
worker.containerSecurityContext.runAsNonRoot|Set Airflow worker containers' Security Context runAsNonRoot|string|TRUE|
worker.autoscaling.enabled|Whether enable horizontal pod autoscaler|string|FALSE|
worker.autoscaling.minReplicas|Configure a minimum amount of pods|integer|1|
worker.autoscaling.maxReplicas|Configure a maximum amount of pods|integer|3|

## Traffic Exposure Parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
service.type|Airflow service type|string|ClusterIP|
service.ports.http|Airflow service HTTP port|integer|8080|
ingress.enabled|Enable ingress record generation for Airflow|string|FALSE|

## Other Parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
serviceAccount.name|The name of the ServiceAccount to use.|string|""|
serviceAccount.automountServiceAccountToken|Allows auto mount of ServiceAccountToken on the serviceAccount created|string|TRUE|

## Airflow metrics parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
metrics.serviceMonitor.enabled|if true, creates a Prometheus Operator ServiceMonitor (requires metrics.enabled to be true)|string|FALSE|

## Airflow database parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
postgresql.auth.password|Password for the custom user to create|string|""|
redis.auth.password|Redis password|string|""|
