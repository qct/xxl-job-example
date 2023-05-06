## SQL scripts
`curl -sL https://raw.githubusercontent.com/xuxueli/xxl-job/master/doc/db/tables_xxl_job.sql > sql/tables_xxl_job.sql`

## Run xxl-job admin
`docker-compose up -d`

```
NAME                IMAGE                         COMMAND                  SERVICE             CREATED             STATUS              PORTS
xxl_job_admin       xuxueli/xxl-job-admin:2.4.0   "sh -c 'java -jar $J…"   admin               37 minutes ago      Up 37 minutes       0.0.0.0:7070->8080/tcp
xxl_job_db          mysql:8                       "docker-entrypoint.s…"   mysql               37 minutes ago      Up 37 minutes       33060/tcp, 0.0.0.0:13306->3306/tcp
```

## Run xxl-job executor
`mvn spring-boot:run`

## Add an executor
admin: http://localhost:7070/xxl-job-admin

user/pwd: admin/123456

AppName: xxl-job-example-executor	

## Add a task and run it
tasks defined in `com.xxl.job.executor.jobhandler.SampleXxlJob`

* demoJobHandler
* shardingJobHandler
* commandJobHandler
* httpJobHandler
* demoJobHandler2
