# dump_db

**Dump postgres db in k8s pods**

    kubectl exec -it <pod_name> -n <namespace> -- /bin/bash
    pg_dump -U <username> -h localhost -d <database_name> > /tmp/db_dump.sql
    kubectl cp <namespace>/<pod_name>:/tmp/db_dump.sql /path/to/local/destination/db_dump.sql
