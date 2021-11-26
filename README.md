# sync-public-images
Sync public images, e.g. *alpine*, *ubuntu*, *nginx* with org-local copy

DockerHub has a limit for anonymous access even for public images.

In our tests, we use such images very intensively.

The repo has daily GitHub workflow that synchronizes latest published DockerHub image with org-level cache.

E.g., instead of `ubuntu:latest` a test should use `ghcr.io/neuro-inc/ubuntu:latest`.

Cached images are public.

The following images are *cached*:

| DockerHub       | Neuro-inc cache                     |
|-----------------|-------------------------------------|
|alpine:latest    | ghcr.io/neuro-inc/alpine:latest     |
|nginx:latest     | ghcr.io/neuro-inc/nginx:latest      |
|ubuntu:latest    | ghcr.io/neuro-inc/ubuntu:latest     |

**N.B. Only 'latest' tags are cached by default, all other tags should be enumerated explicitly**
