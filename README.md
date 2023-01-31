# Welcome to CodeHerald

CodeHerald listens to events in your Github repositories and triggers actions
and integrations, based on the rules you have set up. Or, as a friend put it,
"it's an if-this-then-that for Github."

## How does it work?

1. You sign-up on CodeHerald with your Github account and select repositories
   you want to integrate with.
2. You enable webhooks in some or all of those repositories.
3. You create rules to trigger actions that help you save time.

That's it! CodeHerald will trigger rules whenever an event matches a rule.

## Why would I use it?

Undoubtedly the first thought that comes to mind is "what about Github Actions?"
Indeed, Github Actions (and Workflows) is great at executing scripts and it can
listen to webhooks too. However, it comes with some limitations:

1. They have to be written in YAML. YAML event matching is limited to certain
   actions. Beyond that, conditions use either template language or have to be
   coded. This can be fiddly, especially if the goal is to set-up sometihng
   quick. CodeHerald goal is to provide a platform to simplify this process.
2. It is easy to accidentally, or intentionally, remove, break, or stop a Github
   Action from executing in a pull request. CodeHerald will trigger an action as
   long as webhooks are set-up, regardless if the code changed or not (in fact,
   CodeHerald does not have access to code content at all!)
3. Github Actions have to be duplicated in each repository you work with.
   CodeHerald can have one rule that services events from multiple repositories.

Finally, CodeHerald is an MVP and an experiment, looking for its place under the
sun. If you're not ready to try it out, but think "Oh, I'd use this only if ..."
I would love to know the end of that sentence at julius {at} codeherald.com

## Next Steps

* Sign-up and [install](install.md) CodeHerald in your account.
* Setup your first rule by following the [quickstart](quickstart.md).
