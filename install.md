# Install CodeHerald

To sign-up on CodeHerald you need to have a GitHub account and that's it. Press
"Log in with GitHub" button. It is used for both - sign-up and sign-in.

![Screenshot showing Login with GitHub](images/install/login-with-github.png)

GitHub Apps require you to give two sets of permissions: for user (what the app
can do on behalf of the user) and app (what the app can do itself). If this is
the first time installing CodeHerald - you will see the screen to authorize user
permissions first. As shown in the screenshot - the only _User_ level permission
CodeHerald needs is an email address.

![Screenshot showing user authorization](images/install/authorize.png ':size=400x515')

## Choose Account

Next step, GitHub will ask you to choose an account where to install CodeHerald
\- the GitHub App. You can install CodeHerald to more than one account by
visiting CodeHerald settings later. Meanwhile, this is how the sign-up flow
looks like:

![Screenshot showing account choice](images/install/choose-account.png ':size=400x394')

## Choose Repositories

CodeHerald will only be able to listen to events and execute actions on
repositories that you explicitly give permissions to. You can choose to either
allow (1) all repository access, or (2) pick and choose specific repositories
yourself.

![Screenshot showing repository selection](images/install/select-repositories.png ':size=400x380')

## Review Permissions

CodeHerald does not ask for more permissions than it needs to right now. If
permissions will change in the future, GitHub will explicitly ask you to approve
the changes. Meanwhile, CodeHerald needs permissions to add webhooks and execute
actions, issues and pull requests. Checks and security events are needed for
upcoming features, and metadata is a mandatory permission.

![Screenshot of permission request](images/install/permissions.png ':size=400x232')

## Install & Authorize

That's it for the first time, click "Install & Authorize" and you will be
redirected back to CodeHerald. CodeHerald needs a minute to setup the
repositories, so while that is happening. Start reading the
[quickstart](quickstart.md).


## Next Steps

* Go through the [quickstart](quickstart.md) guide.
