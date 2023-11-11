# gatsby5-dev-container

TODO: 
- install sshagent openssh-ssh-agent service
- vscode prettier and eslint

AVSCode dev container useful for Gatsby.js v5 dev. 

Supports developing npm linked local plugins by mounting the /workspace in a docker volume. This improves performance anbut also allows you to install multiple git repos side by side. This allows you to use `npm link` to develop a local, external Gatsby plugin.

Core compenents (can be easily changed on your copy):

- Node 18.18 bookworm
- gatsby-cli 5 CHANGED: install this as a dev dep in each sub project
- netlify-cli CHANGED: ...

See .devcontainer/devcontainer.json for a list of VSCode plugins that are installed.

// repoen in container -> Dev Container: Gatsby5-Dev-Container

git install each project you want to work on in parallel

// Create file:
// my.code-workspace
{
    "folders": [
        {
            "name": "edpike365-blog",
            "path": "edpike365-blog"
        },
        {
            "name": "gatsby-head-style-boss",
            "path": "gatsby-head-style-boss"
        },
        {
            "name": "gatsby-plugin-tester",
            "path": "gatsby-plugin-tester"
        }
    ],

}

An "Open Workspace" button should appear in the editor pane. Click it and the container will reopen.

It will say "Opening remote container" in the lower left corner, but its just reopening your current container, but now each project you defined will have its own "workspace" sub folder with a radio button icon. Each folder's .vscode folder and settings.json file will be honored. VSCode Plugins like prettier will read configs for each project.

