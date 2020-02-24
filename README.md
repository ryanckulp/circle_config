## Circle CI + Rails Config

1. inside Circle CI > your organization, click "New Project" then 'start build' to save it (build will fail)
2. navigate to project Environment Variables (eg: https://ui.circleci.com/settings/project/github/your_username/your_repo/environment-variables)
3. click 'Add Variables' and add the following: `HEROKU_APP_NAME`, `HEROKU_API_KEY`
4. `HEROKU_APP_NAME` is whatever found inside `app-name-here.herokuapp.com`
5. `HEROKU_API_KEY` may be created via `$ heroku authorizations:create --description='App Name'` (copy/paste the 'token' value)
6. add this repo's `config.yml` inside your Rails project: `.circleci/config.yml`
7. update Ruby version within the "Docker image", e.g. 2.6.1, inside your `config.yml`
8. `$ git push` to build the project on Circle CI
9. if tests pass, project will be deployed automatically to Heroku
