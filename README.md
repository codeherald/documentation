# Welcome to CodeHerald

CodeHerald is like “if-this-then-that” for GitHub. It listens to events in your
GitHub repositories and triggers actions, based on the rules you create.

## How does it work?

1. Sign-up on CodeHerald with your GitHub account and select repositories
   to integrate with.
2. Enable webhooks in those repositories.
3. Create rules that trigger actions when events match given conditions.

That's it! CodeHerald will tirelessly apply your rules to all future events.

## Why would I use it?

Undoubtedly the first thought that comes to mind is "what about GitHub Actions?"
Indeed, GitHub Actions is great at executing scripts and it can listen to
webhooks too. However, it comes with some limitations:

1. They have to be written in YAML. YAML event matching is limited to certain
   actions. Beyond that, conditions use either template language or have to be
   coded. This can be fiddly, especially if the goal is to set-up sometihng
   quick. CodeHerald’s goal is to provide a platform to simplify this process.
2. It is easy to accidentally, or intentionally, remove, break, or stop a GitHub
   Action from executing in a pull request. CodeHerald will trigger an action as
   long as webhooks are set-up, regardless if the code changed or not (in fact,
   CodeHerald does not have access to code content at all!)
3. GitHub Actions have to be duplicated in each repository you work with.
   CodeHerald can have one rule that services events from multiple repositories.

Finally, CodeHerald is an MVP and an experiment, looking for its place under the
sun. If you're not ready to try it out, but think "Oh, I'd use this only if ..."
I would love to know the end of that sentence at julius {at} codeherald.com

## Next Steps

* Sign-up and [install](install.md) CodeHerald in your account.
* Setup your first rule by following the [quickstart](quickstart.md).
