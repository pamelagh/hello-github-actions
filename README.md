## Welcome to "Hello World" with GitHub Actions

This course will walk you through writing your first action and using it with a workflow file. 

**Ready to get started? Navigate to the first issue.**

*** GitHub Actions *** 
They're a flexible way to automate nearly every aspect of  team's software workflow.
- Automated testing (CI)
- Continuous delivery and deployment
- Responding to workflow triggers using issues, @ mentions, labels, and more
- Triggering code reviews
- Managing branches
- Triaging issues and pull requests

*** Actions and Workflows ***
- The action.
- The workflow that uses the action(s).

A workflow can contain many actions. Each action has its own purpose.

- Types of Actions
Actions come in two types: container actions and JavaScript actions.

Docker container actions allow the environment to be packaged with the GitHub Actions code and can only execute in the GitHub-Hosted Linux environment.

JavaScript actions decouple the GitHub Actions code from the environment allowing faster execution but accepting greater dependency management responsibility.

*** Steps ***
1. Create action-a/Dockerfile:
FROM debian:9.5-slim

ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]

