# kubernetes short cuts

List all the actions you can perform in a namespace  
```
$ kubectl auth can-i --list --namespace=
```

Perform an auth action as a specific service account  
```
$ kubectl auth can-i get pod --as system:serviceaccount:secure:unprivileged-service-account
```

List all SA that can...
```
$ kubectl who-can get secret cluster-admin-creds -n secure
```
