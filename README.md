# Experiment: Cluster bootstrapping using ArgoCD App of Apps and directory source

Assumption: Repo contains necessary charts and valuefiles, or valuefiles for charts in public Helm repos, or manifests.
Supposedly resonable for the cluster tooling repo.

Cons:

- ArgoCD application manifests in each directory
- Each ArgoCD application manifest contains links to this repository
- Too many copypasting when creating new app. Prone to errors. Fields are mostly the same as basedir, so templating might help a bit.
- Globs for inclusion and exlusion could be non obvious.

Pros:

- Easy to trigger update
