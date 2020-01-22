# Gatsby from Scratch

A basic Gatsby site create without the CLI.

## Gatsby plugins

### Helmet support

To use helmet.

    npm i gatsby-plugin-react-helmet react-helmet

Configuration in gatsby-config.js for helmet

<!-- prettier-ignore -->
    plugins: [
        `gatsby-plugin-react-helmet`,
    ]

To prevent the title from appear when opening in the background while using the gatsby-plugin-offline. Pass the `defer={false}` prop into the Helmet component.

    <Helmet title="something" defer={false}>

### Styled-component support

To use styled-components.

    npm i gatsby-plugin-styled-components styled-components babel-plugin-styled-components

Configuration in gatsby-config.js for styled-components

<!-- prettier-ignore -->
    plugins: [
        `gatsby-plugin-styled-components`,
    ]

### Offline support

To use offline support for generating a service worker

    npm i gatsby-plugin-offline

Configuration in gatsby-config.js for offline

<!-- prettier-ignore -->
    plugin: [
        `gatsby-plugin-offline`
    ]

### Markdown support

To use markdown

    npm i gatsby-plugin-mdx @mdx-js.mdx @mdx-js/react gatsby-source-filesystem

Configuration in gatsby-config.js for markdown

<!-- prettier-ignore -->
    plugins: [
        {
            resolve: `gatsby-plugin-mdx`,
            options: {
                extensions: [`.mdx`, `.md`]
            }
        },
        {
            resolve: `gatsby-source-filesystem`,
            options: {
                path: `${__dirname}/content`,
                name: `content`
            }
        }
    ]
