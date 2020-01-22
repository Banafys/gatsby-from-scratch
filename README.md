# Gatsby from Scratch

A basic Gatsby site create without the CLI.

## Gatsby plugins

### Markdown support

To use markdown

> npm i gatsby-plugin-mdx @mdx-js.mdx @mdx-js/react gatsby-source-filesystem

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

### Styled-component support

To use styled-components.

> npm i gatsby-plugin-styled-components styled-components babel-plugin-styled-components

Configuration in gatsby-config.js for styled-components

<!-- prettier-ignore -->
    plugins: [
        `gatsby-plugin-styled-components`,
    ]
