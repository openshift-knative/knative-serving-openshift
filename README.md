# knative-serving-openshift

A platform-specific operator for OpenShift to be deployed with the
primary knative-serving operator

## Running e2e tests

Ensure KUBECONFIG refers to a valid OpenShift cluster with
maistra/istio installed, and then run:

```
kubectl apply -f https://raw.githubusercontent.com/openshift-knative/serverless-operator/release-1.3/serving/operator/deploy/crds/serving_v1alpha1_knativeserving_crd.yaml
kubectl apply -f https://raw.githubusercontent.com/knative/serving-operator/master/config/300-serving-v1alpha1-knativeserving-crd.yaml
operator-sdk test local ./test/e2e/ --namespace default 
```
