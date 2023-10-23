# gatsby5-dev-container

AVSCode dev container useful for Gatsby.js v5 dev. 

Supports developing npm linked local plugins by mounting the /workspace in a docker volume. This improves performance anbut also allows you to install multiple git repos side by side. This allows you to use `npm link` to develop a local, external Gatsby plugin.

Core compenents (can be easily changed on your copy):

- Node 18.18 bookworm
- gatsby-cli 5
- netlify-cli

See devcontainer.json for a list of VSCode plugins that are installed.
