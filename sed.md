# sed

Replace `1Gi` with `10Gi` only lines that contain __storage__:
```
sed -i '/storage/ s/1Gi/10Gi/g' az-pvc.yml
```

Add text in line 5:
```
sed -i '5i\  namespace: sigma' az-pvc.yml
```

Delete line 5:
```
sed -i '5d' az-pvc.yml
```

