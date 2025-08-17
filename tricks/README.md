# Tricks

## Imperative commands

> dry-run 

If you simply want to test your command , use the --dry-run=client option. This will not create the resource

> -o yaml: This will output the resource definition in YAML format on screen.

$ kubectl run nginx --image=nginx --dry-run=client -o yaml

kubectl create deployment --image=nginx nginx --dry-run -o yaml

kubectl create deployment --image=nginx nginx --dry-run -o yaml > nginx-deployment.yml

## Formatting
**kubectl [command] [TYPE] [NAME] -o **

> - -o json Output a JSON formatted API object.
> - -o name Print only the resource name and nothing else.
> - -o wide Output in the plain-text format with any additional information.
> - -o yaml Output a YAML formatted API object.

## Logs

> watch

kubectl -n elastic exec -it app -- cat /var/log/messages

kubectl logs app -n elastic

## Edit existing pod

kubectl edit pod

## Replace (recreate)

> recreate pod

kubectl replace --force -f /tmp/manifest.yml

## Selectors

> show

kubectl get pods --selector dev=test

kubectl get pods --selector dev=test,dep=finance --no-headers
