# Secured routes

1. Create the pod:

    ```
    oc apply -f pod.yml
    ```

1. Create the service:

    ```
    oc apply -f service.yml
    ```

    (You can also use `oc expose pod ...` to create the service)

1. Create the route:

    ```
    oc apply -f route.yml
    ```

    This is equivalent to running:

    ```
    oc create route edge darkhttpd --service darkhttpd
    ```

After the above, you can access the service at:

- https://darkhttpd-default.apps.cnv.massopen.cloud

(That's `<name>-<project>.apps.cnv.massopen.cloud`, so the hostname will
vary by project.)
