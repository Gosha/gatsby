---
title: Localization and Internationalization with Gatsby (i18n)
---

Serving users content in a way that is adapted to their language & culture is part of a great user experience. When you make an effort to adapt web content to a user's location, that practice is called internationalization (i18n).

In practice i18n involves translating text and formatting dates, numbers, and strings based on the user's detected location. For example, a date displayed for a user in the United States would follow the mm/dd/year date format, but for a user in the UK the date format would change to dd/mm/year.

This guide is a brief look at the options that exist for enhancing your Gatsby project for internationalization.

## Choosing a package

There are a few React i18n packages out there. Several options include [react-intl](https://github.com/yahoo/react-intl), the community [Gatsby plugin](https://www.npmjs.com/package/gatsby-plugin-i18n) and [react-i18next](https://github.com/i18next/react-i18next/). There are several factors to consider when choosing a package: Do you already use a similar package in another project? How well does the package meet the needs of your users? Are you or your team already familiar with a certain package? Is the package well documented and maintained?

### gatsby-plugin-i18n

This plugin helps you use `react-intl`, `i18next` or any other i18n library with Gatsby. This plugin does not translate or format your content, but rather it creates routes for each language, allowing Google to more easily find the correct version of your site, and if you need to, designate alternative UI layouts.

The naming format follows .**languageKey**.js for files and /**languageKey**/path/fileName for URLs.

**Example:**

File - src/pages/about.**en**.js

URL - /**en**/about

[gatsby-plugin-i18n on GitHub](https://github.com/angeloocana/gatsby-plugin-i18n)

### react-intl

React-intl is a part of the FormatJS set of i18n libraries and provides support for over 150+ languages. It builds on JavaScript's [Internationalization API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl) providing enhanced APIs and components. React-intl uses React context and HOCs (Higher Order Components) to provide translations allowing you to dynamically load language modules as you need them. There are also polyfill options available for older browsers that do not support the base JavaScript i18n API.

More detailed information about react-intl's [APIs](https://github.com/formatjs/react-intl/blob/master/docs/API.md) and [components](https://github.com/formatjs/react-intl/blob/master/docs/Components.md), including [demos](https://github.com/formatjs/react-intl/tree/master/examples), are available in the [documentation](https://github.com/formatjs/react-intl/tree/master/docs).

### react-i18next

React-i18next is an internationalization library built on the i18next framework. It uses components to make sure translations render correctly or to re-render your content when the user language changes.

React-i18next is more extensible than other options with a variety of plugins, utilities, and configurations. Common plugins allow for detecting a user's language or adding an additional layer of local caching. Other options include caching, a backend plugin to load translations from your server, or bundling translations with webpack.

This framework also has experimental support for the React suspense API and it supports a stable version of React hooks.

## Other resources

- [Building i18n with Gatsby](https://www.gatsbyjs.org/blog/2017-10-17-building-i18n-with-gatsby/)

- [Building Eviction Free NYC with GatsbyJS + Contentful](https://www.gatsbyjs.org/blog/2018-04-27-building-eviction-free-nyc-with-gatsbyjs-and-contentful/)

- [Gatsby i18n packages](https://www.gatsbyjs.org/packages/gatsby-plugin-i18n/?=i18)

- [Gatsby i18n articles](https://www.gatsbyjs.org/blog/tags/i-18-n/)

- [W3C's i18n resources](https://w3c.github.io/i18n-drafts/getting-started/contentdev.en#reference)
