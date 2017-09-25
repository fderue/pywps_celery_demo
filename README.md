# pywps_celery_demo
Show how to use Pywps (with feature pywps-scheduler-extension ) with a task queue manager such as Celery.
Run this request multiple time consecutively: 
```
http://localhost:5000/wps?service=wps&request=Execute&version=1.0.0&identifier=sleep&datainputs=delay=10&storeExecuteResponse=true&status=true
```
This process sleep for 10 seconds, so if you monitor the workers with Celery-Flowers, you will observe that two workers handling those processes.
