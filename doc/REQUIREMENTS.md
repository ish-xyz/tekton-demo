High level:

- All pipeline configuration stored as code
- Deployment tool configuration stored as code (JCasC, etc)
- Templated/Templateable deployment pipelines so we don’t have to duplicate the same steps in multiple repositories
- Support variables (pass in clustername, environment, etc) so we can use the same pipeline for each environment
- Phoenix deployment tool (you can kill it at any moment, and redeploy it’ll come back up in exactly the same state)
- Supports trunk based development and git tagging
- Supports splitting CI and CD
- References to artifacts are passed to CD stages, never the actual artefact


Create helm chart from manifest
Configure prometheus ?
Configure LDAP on NGINX ? 
Configure pipelines:
    deploy with cloudbuild