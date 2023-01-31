# Quickstart

This section assumes you have [installed](install.md) CodeHerald on at least one account.

## Activate Webhooks

By default, CodeHerald does not activate webhooks in your repositories (1), but
you can choose to enable them when you click "Edit" (2).

![Screenshot of repository list](images/quickstart/repository-list.png ':size=600x237')

In the details view - click "Enable" next to the webhook url. Technically, you
could set-up webhook with that url on any repository as long as the repository
url in the form matches, but this feature is still in progress.

![Screenshot of webhook enablement](images/quickstart/enable-webhook.png ':size=600x283')

Once that's done, the "Active" row should show a green check mark.

We are now ready to create the first rule.

## Create Rule

### Rule Name

The first rule will be something relatively simple - post a comment, when all
the checkboxes are ticked. Therefore:

* Set **Rule Name** to something suitable, like "*Label checklist complete*".
* Leave **Object Type** as "*Issue*".

![New rule name](images/quickstart/new-rule-name.png ':size=600x213')

Now, let's add some conditions. CodeHerald literally listens to Github Webhooks,
so you could, in theory, work out which condition fields mean which webhook
fields. Leave **Match** as "*All Conditions*", and let's add a couple of conditions:

### Conditions

* **First**, this rule should trigger when issue is edited. Set **Field** to "*Action*", **Condition** to "*one of*" and **Value** to "*edited*". See more about values below.
* **Second**, this rule should trigger when all the checkboxes are ticked in the Issue description. Set **Field** to "*Description*", **Condition** to "*wildcard*", and **Value** to `*[*] [[]x[]] Checklist is done*`. See more about wildcards below.
* **Third**, this rule should only trigger when the original Issue description did not have the checkbox, otherwise this rule would trigger every time any change is made after the checkbox is ticked. Set **Field** to "*Description (original)*", **Condition** to "*wildcard*", and **Value** to `*[*] [[] []] Checklist is done*`. Note the different field name and the space instead of `x` in the value.

![New rule conditions](images/quickstart/new-rule-conditions.png ':size=600x251')

?> **On values**. Values are processed as JSON, with two exceptions: first, if value cannot be parsed - it is interpreted as a single string; second, JSON objects (`{}`) are not allowed. So for example, if you wanted to provide a list of values you could write `["opened", "edited", "closed"]`

?> **On wildcards**. Wildcards are interpreted using a glob pattern, so standard rules apply. `*` matches everything, `?` matches a single character, `[seq]` matches any character in `seq` and `[!seq]` matches any character not in `seq`. To escape any of the `*?[]` characters, you put them between `[]`. So the example used earlier `*[*] [[]x[]] Checklist is done*` would match `* [x] Checklist is done`.


### Actions

* Set **Action** to "*Post Comment*" and **Text** to "*Congratulations, your first rule succeeded!*"
* Hit **Save**

![New rule actions](images/quickstart/new-rule-actions.png ':size=600x150')

## See It In Action

Create issue and make sure to include a line `* [ ] Checklist is done`, hit "**Submit new issue.**"

![Create issue](images/quickstart/create-issue.png ':size=600x270')

Next up, tick the checkbox in issue description and within seconds you should
see a comment pop-up. That's CodeHerald!

![CodeHerald](images/quickstart/codeheral-in-action.png ':size=600x294')
