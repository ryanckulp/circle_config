## Circle CI Config

1. inside Circle CI, [add a new project](https://circleci.com/add-projects)
2. navigate to project ENV (https://circleci.com/gh/your_username/your_repo/edit#env-vars)
3. click 'Add Variables' and add the following: `HEROKU_APP_NAME`, `HEROKU_API_KEY`
4. `HEROKU_APP_NAME` is whatever found inside `app-name-here.herokuapp.com`
5. `HEROKU_API_KEY` may be created via `$ heroku authorizations:create --description='App Name'`
6. add this repo's `config.yml` inside your Rails project: `.circleci/config.yml`
7. `$ git push` to build
