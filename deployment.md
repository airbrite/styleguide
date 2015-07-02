# Deployment Guidelines

## Production

This is where money is handled and real businesses are run.
Do not make this a test environment, do your testing elsewhere.

Anything in the `master` branch **can and will** be deployed to Production.

### Tests

All tests (both unit and integration) should be passing.
See individual project README files for instructions on how to run tests.

Generally, unit tests are automatically run on branches
so you just have to worry about integration tests.

## Staging

All projects have a staging environment.
If you have the standard heroku setup and configured your gitconfig,
it's simply `git push staging [yourbranch]:master`.

Click around and do a spot check on staging before deploying to production.
Integration tests make this step very quick since you can rely on them to catch most things.

## Sandbox

Used by third parties for their own testing and experiments.

**Mirrors Production**

## Canary

Lives on Heroku and serves as a multi-purpose testing area for branches.

Integration tests will use Canary for remote testing,
so make sure you push to canary if you use Browserstack for integration tests.

### Fridays

Try not to deploy on a Friday.

In the unlikely event that the deploy introduces a bug,
it may not be discovered until the weekend.

**We do not like working on the weekend.**
