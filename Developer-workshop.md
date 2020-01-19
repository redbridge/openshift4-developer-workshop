# Workshop Örebro

## Utvecklar-Workshop

### Mål

Kunna bygga och deploya containers i Openshift. Skapa och bygga pipelines med Openshift pipelines

### Innehåll

#### Docker

* Vad är en container?
* Vad är docker?
* Dockerfile
* Image registry
* Bygg, push & pull


#### Openshift

* Hur fungerar det?
* Kubelang: pod, service, route, secret, configmap, deployment

#### Openshift Console

* Navigera
* Skapa app

#### Openshift cli (oc)

* Använda, skapa app.
* Yaml

#### Openshift pipelines

* Install:

```yaml
apiVersion: operators.coreos.com/v1alpha1
kind: Subscription
metadata:
  name: openshift-pipelines-operator
  namespace: openshift-operators
spec:
  channel: dev-preview
  installPlanApproval: Automatic
  name: openshift-pipelines-operator
  source: community-operators
  sourceNamespace: openshift-marketplace
  startingCSV: openshift-pipelines-operator.v0.8.2
```

[tkn cli](https://github.com/tektoncd/cli#installing-tkn)
[openshift-pipelines](https://github.com/openshift/pipelines-tutorial)

##### Create a pipeline

1. Create a namespace
2. Create PipelineResources (imagerepo, gitrepo) (https://github.com/tektoncd/pipeline/blob/master/examples/taskruns/git-ssh-creds.yaml
)
