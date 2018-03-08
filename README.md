# Sage Business Cloud Ruby API Sample application

### FOR changes required for v3 please refer to the [v3 branch](https://github.com/Sage/sageone_api_ruby_sample/tree/v3)

##### Note: Request signing and noncing (the X-Signature and X-Nonce headers) is no longer checked in v3. The related code will soon be removed from this repo.

Sample application that integrates with Sage Business Cloud Accounting via the Sage API.

Authentication with Sage is handled in the [Controller](app/controllers/sage_one_controller.rb).

We use the [sageone_api_signer](https://github.com/Sage/sageone_api_signer) gem to sign our API requests.

## Run the app locally

Clone the repo:

`git clone git@github.com:Sage/sageone_api_ruby_sample.git`

Update the [config/sageone.yml](config/sageone.yml) file with your application's `client_id`, `client_secret`, `signing_secret` and `callback_url`.

Switch to the project directory, bundle and migrate the db:

```
cd sageone_api_ruby_sample
bundle install
bundle exec rake db:migrate
```

Start a local Rails server:

```
bundle exec rails s
```

You can now access the [home page](http://localhost:3000/), sign up, authorize and make an API call.
