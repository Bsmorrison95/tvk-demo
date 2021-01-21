# tvk-demo


OpenShift Demo Commands

** SHOW OPERATOR Deployed **

```
oc get pods -A | grep -i trilio
```
```
oc get crd | grep -i trilio
```


	## JUMP INTO NAMESPACE ##

oc project demosource

oc get all -n demosource -l app=k8s-demo-app

cat /SA/sampleApps/demoApp.yaml

	##### SHOW TARGET #####
cat /SA/backup/backuptarget.yaml

oc get target

	##### SHOW BACKUP PLAN #####
oc get backupplan

cat /SA/backup/backupplan.yaml
cat /SA/backup/retentionPolicy.yaml

    ##### SHOW BACKUPS ######
oc get backups --sort-by=status.completionTimestamp

	##### SHOW RESTORE #####
cat /SA/restore/demorestore.yaml

oc get all -n demotarget -l app=k8s-demo-app
