# Create a new application in ArgoCD

![Screenshot of a Argocd.](../.data/ArgoCD_summary.png)

## Add port forwarding

```
kubectl port-forward -n demo svc/ambassador 8088:80
```

## Download random png file

```
wget -O /tmp/g.png https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png
```

## Upload this file to the converter

```
curl -F 'image=@/tmp/g.png' localhost:8088/img/
```
You should observe something like this

![Screenshot of a MVP.](../.data/mvp.png)
