# sre-repo
https://github.com/settings/tokens
export GITHUB_TOKEN=<>
export GITHUB_USER=<>

  flux bootstrap github \
  --owner=$GITHUB_USER \
  --repository=sre-repo \
  --branch=main \
  --path=.\
  --personal

flux get kustomizations
# do manual edit to deployment
flux reconcile kustomization flux-system
# check the changes
# commit git changes 
