## You don't need an ingress for this excercise

Use this basic load balancer instead:

```
apiVersion: v1
kind: Service
metadata:
  name: blog
spec:
  type: LoadBalancer
  selector:
    app: blog
  ports:
  - protocol: TCP
    port: 80
    targetPort: 2368
```

