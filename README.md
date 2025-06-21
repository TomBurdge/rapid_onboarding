# Rapid Onboarding
Picture this:
* A junior platform engineer onboards to your team.
* The engineer is keen, and inexperienced. Enthusiastic to make commits, they clone some repositories and look to start making PRs in their first week. You love their enthusiasm!
* Almost immediately, the engineer runs into [dependency hell](https://en.wikipedia.org/wiki/Dependency_hell).
* The company firewall doesn't allow them to install [insert language here] (it's always the same story) and they are having trouble installing tools that the team uses for linting/formatting.
* Your junior engineer finishes their first few weeks a little deflated. They have enjoyed meeting the team, but their confidence is knocked by their local machine setup troubles. You know they will succeed, but you will need to allocate your time to getting them setup.

# The Solution
You can use [VSCode dev containers](https://code.visualstudio.com/docs/devcontainers/create-dev-container#_add-configuration-files-to-a-repository) to "use a Docker container as a full-featured development environment." Your next new joiner engineer:
* Installs docker & VSCode on their device.
* Clones one of the team's repositories.
* They open the repository in VSCode and runs: `F1`, and then selects `>Dev Containers: Rebuild Container`.
* Your new platform engineer has everything they need installed.

# Context
I  prefer to use [LazyVim](https://www.lazyvim.org/), both professionally and personally. However, this repository solves a real-world problem.

I have worked with many contractors (teams of >10 platform engineers), who work offshore and are required to develop on VMs for which the system PATH cannot be modified by the user. There are workarounds, which I will not outline because they are not at all secure. 

Developing on a secure (isolated Ubuntu image) docker container is not a workaround; it is a permanent fix for this problem. A developer with *any* level of confidence and experience can onboard quickly with a pre-specified VSCode devcontainer.

# Try it Out
If you have docker & VSCode already installed, then you can try out this repository's image setup at [this link](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/TomBurdge/rapid_onboarding.git).

# Roadmap
- [X] Add dev container + pre-commit file for a platform engineer's common stack: [terraform](https://github.com/hashicorp/terraform), [terragrunt](https://github.com/gruntwork-io/terragrunt), [pre-commit](https://github.com/pre-commit/pre-commit).
- [ ] Add dev container + pre-commit file for a python developer's stack: [UV](https://docs.astral.sh/uv/), pre-commit hooks for python.
- [ ] Add dev container + pre-commit file for a hybrid rust/python project developer's stack: UV, rust, clippy, pre-commit for rust & python.
