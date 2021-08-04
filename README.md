# Helm deployment action

This actions deploys you Helm Chart to K8s cluster

## Inputs

## `IMAGE_TAG`
**Required** The tag of the docker image. Default `""`.

## `IMAGE`
**Required** The Docker image (without tag). Default `""`.

## `HELM_CHART_PATH`
**Optional** Path to Helm Chart. Default `"chart/"`.

## `DIFFERENT_REPO_CHART`
**Optional** If the Helm Chart is in different repository and needs to be cloned. Default `"false"`.

## `CHART_REPO`
**Optional** Helm Chart git repo. Default `""`.

## `CHART_REPO_SSH_KEY`
**Optional** SSH key to clone Helm Chart git repository. Default `""`.

## `USE_DEFAULT_VALUE_GENERATOR`
**Optional** Generates values.yaml based on IMAGE and IMAGE_TAG. Default `true`.

## `CHART_VALUES_PATH`
**Optional** Values file path for Helm Chart. Default `"values-default.yaml"`.

## `UPDATE_CHART_FILE`
**Optional** Updates chart.yaml file with new version. Default `false`.

## `HELM_RELEASE_NAME`
**Required** Name of the Helm release. Default `""`.

## `HELM_RELEASE_NAMESPACE`
**Optional** Namespace in which you want to deploy application. Default `"default"`.

## `HELM_DEPLOY_WAIT_TIMEOUT`
**Optional** Timeout for waiting deploying to become ready. Default `"180"`.

## `PRINT_LOGS_AND_DESCRIPTION`
**Optional** Print logs and description if deployment has been failed. Default `"true"`.

## `USING_GKE_CLUSTER`
**Optional** Set true if you're deploying to GKE. Default `false`.

## `GKE_CLUSTER_NAME`
**Optional** GKE cluster name. Default `""`.

## `GKE_LOCATION`
**Optional** GKE cluster location. Default `""`.

## `GKE_CREDENTIALS`
**Optional** GKE cluster SA key. Default `""`.

## `USING_EKS_CLUSTER`
**Optional** Set true if you're deploying to EKS. Default `false`.

## `EKS_CLUSTER_NAME`
**Optional** EKS cluster name. Default `""`.

## `EKS_LOCATION`
**Optional** EKS cluster location. Default `""`.

## `AWS_ACCESS_KEY_ID`
**Optional** AWS access key id. Default `""`.

## `AWS_SECRET_ACCESS_KEY`
**Optional** AWS access key. Default `""`.

## Outputs

## `time`

The time we greeted you.

## Example usage

uses: rserag/helm-deploy-action@v0.1
with:
  who-to-greet: 'Mona the Octocat'