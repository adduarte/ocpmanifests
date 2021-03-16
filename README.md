# ocpmanifests
Collection of useful manifests

The manifests in this repository are to be added to the appropriate directories during openshift cluster deployment. 
See https://docs.openshift.com/container-platform/4.6/installing/install_config/installing-customizing.html for more details. 

To use
Execute in the following oreder: 
```
openshift-install create instacll-config
openshift-install create manifests

# move the desired new manifest to the openshift/ directory 

openshift-install create ignition-config

# check results by greping the bootstrap.ign for the name of the manifests

 python3 -mjson.tool  bootstrap.ign  | grep 99 

# proceed with installation

openshift-install cluster create --log-level=debug
