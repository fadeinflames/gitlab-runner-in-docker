# gitlab-remote-runner

Allows you create and use your own private GitLab CI/CD runner, which can for example have access to docker, private environment variables, etc.

  * git clone https://github.com/fadeinflames/gitlab-runner runner
  * Get the token from your project CICD settings page: `https://gitlab.com/<PROJECT_NAME>/settings/ci_cd`
  * Start runner using `./start.runner`
  * Execute `docker exec -ti runner gitlab-runner register –leave-runner` to gather runner`s token from console output
  * Enter token obtained
  * Enter any tags (required, for example: docker)
  * Enter any image (dind usually required)
  * Copy runner`s token generated
  * Go again to CICD settings `https://gitlab.com/<PROJECT_NAME>/settings/ci_cd`
  * Your runner will be registered where
  * Go to your runner and copy runner`s token from there
  * Add token to `./gitlab-runner.toml` (instead of 123)
  * Rerun `./start-runner`
