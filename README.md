# Example Streamlit App


## GCR Build and deploy

Command to build the application.
```
gcloud builds submit --tag gcr.io/<ProjectID>/<AppName>  --project=<ProjectID>
```

Command to deploy the application
```
gcloud run deploy --image gcr.io/<ProjectID>/<AppName> --platform managed  --project=<ProjectID> --allow-unauthenticated
```

Example: 
```
gcloud builds submit --tag gcr.io/mohammad-sandbox-345817/example-streamlit  --project=mohammad-sandbox-345817 --timeout="20m"

gcloud run deploy --image gcr.io/mohammad-sandbox-345817/example-streamlit --platform managed  --project=mohammad-sandbox-345817 --allow-unauthenticated
```