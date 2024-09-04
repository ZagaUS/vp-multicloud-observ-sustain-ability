statefulset.apps/airflow-airflow-postgresql
secret/airflow-postgresql
service/airflow-postgresql



deployment.apps/airflow
configmap/airflow-sso-config
configmap/sso-env-config
secret/dag-deployment
service/airflow
route.route.openshift.io/airflow






--------------

configmap/airflow-sso-config created
configmap/sso-env-config created

secret/airflow-postgresql created
secret/dag-deployment created

service/airflow created
service/airflow-postgresql created

deployment.apps/airflow created

statefulset.apps/airflow-airflow-postgresql created

route.route.openshift.io/airflow created

<!-- -------------------------------------------------------- -->

Init Containers

wait-for-airflow-migrations
quay.io/osclimate/airflow:2.7.3-omdingest-1.2.2

add-airflow-admin
quay.io/osclimate/airflow:2.7.3-omdingest-1.2.2

deploydagsfroms3
quay.io/osclimate/minioclient:1.7

<!-- -------------------------------------------------------- -->

Containers

airflow-web
quay.io/osclimate/airflow:2.7.3-omdingest-1.2.2

scheduler
quay.io/osclimate/airflow:2.7.3-omdingest-1.2.2

mc
quay.io/osclimate/minioclient:1.7