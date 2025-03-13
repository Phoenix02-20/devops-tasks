Steps:
1. Create a secret which will take configurations from .docker/config.json file.
2. Add that secret in imagePullSecrets in values.yaml
3. Install the chart.
helm install releasename chartname
