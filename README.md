# Instructions
## Ref: https://django-storages.readthedocs.io/en/latest/backends/gcloud.html
* Create bucket on gcp
* Get google service account
* Add role to be storage admin
* Create key as json
* Put file in project (jorworajak-c4ed4262f353.json)
* pip install django-storages[google]
* Add following settings

```
from google.oauth2 import service_account
GS_CREDENTIALS = service_account.Credentials.from_service_account_file(
    os.path.join(BASE_DIR, 'jorworajak-c4ed4262f353.json')
)

DEFAULT_FILE_STORAGE = 'storages.backends.gcloud.GoogleCloudStorage'
STATICFILES_STORAGE = 'storages.backends.gcloud.GoogleCloudStorage'
GS_BUCKET_NAME = 'bucket-name'
```
