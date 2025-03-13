Steps:
1. Create secret for database credentials.
kubectl apply -f secret.yaml
2. Create PVC and PV for mysql and drupal.
kubectl apply -f pvc.yaml
3. Create deployment for mysql.
4. Add secrets as environment variables and pvc as volume claim.
5. Add service in same deployment file and give port as 3306.
kubectl apply -f mysql-deployment.yaml
6. Create deployment for drupal application.
7. Add init container:
        args: ['cp -r /var/www/html/sites/ /data/; chown www-data:www-data /data/ -R']
8. Add service to drupal. Keep service type as NodePort.
