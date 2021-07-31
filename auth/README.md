Authentication service case:

![auth](auth.png)

The auth methodology it will be based on simple API setup:
```
gateway:
  routes:
  - name: "hello"
    path: "/hello/v1/sayHello"
    skipAuth: false
```

if skipeAuth is true, the GW virtual service will redirect to API, in
other case it will redirect to API-AUTH service that afterwards will redirect
to respective API