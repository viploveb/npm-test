# @cloud/backups




> This file is generated by [argodocs](https://github.com/atlanhq/argodocs). Please do not edit.

|Name|Kind|Version|Entrypoint Template|
|----|----|----|----|
|cloud-backups|WorkflowTemplate|argoproj.io/v1alpha1|main|


## Templates

A list of all the templates present in the Workflow Template

|Name|Type|Line Number|
|----|----|----|
|[main](#main)|`DAG`|18|

---

### main

Type: `DAG`


- Inputs
    - Parameters
        - `git-kube-secret-name`
        - `git-kube-ssh-key`
        - `branch`
        - `backup-filename`
- Tasks
    - `redis`
        - Template: `cloud-redis-backup::redis-backup`
    - `postgres`
        - Template: `cloud-postgres-backup::postgres-backup`
    - `cassandra`
        - Template: `cloud-cassandra-backup::main`
    - `elasticsearch-atlas`
        - Template: `cloud-elasticsearch-backup::main`
    - `elasticsearch-logging`
        - Template: `cloud-elasticsearch-backup::main`
    - `prometheus-backup`
        - Template: `cloud-prometheus-backup::prometheus-backup`

