# @charlietango/babel-preset-sx-prop

> A custom version of
> [@emotion/babel-preset-css-prop](https://github.com/emotion-js/emotion/tree/master/packages/babel-preset-css-prop)
> to use the JSX Pragma from [@charlietango/ui](https://github.com/charlie-tango/ui)

## Install

```bash
yarn add @charletango/babel-preset-sx-prop
```

## Usage

**.babelrc**

```json
{
  "presets": ["@charlietango/babel-preset-sx-prop"]
}
```

`@charlietango/babel-preset-sx-prop` includes the emotion plugin. The `babel-plugin-emotion` entry
should be removed from your config and any options moved to the preset. If you use
`@babel/preset-react` or `@babel/preset-typescript` ensure that `@charlietango/babel-preset-sx-prop`
is inserted after them in your babel config.

## Options

Options for both `babel-plugin-emotion` and `@babel/plugin-transform-react-jsx` are supported and
will be forwarded to their respective plugin.

> Refer to the plugin's documentation for full option documentation.
>
> - [`babel-plugin-emotion`](https://emotion.sh/docs/babel)
>
> - [`@babel/plugin-transform-react-jsx`](https://babeljs.io/docs/en/next/babel-plugin-transform-react-jsx)

You can opt into
[the new JSX runtimes](https://reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html)
by configuring this preset with `{ runtime: 'automatic' }`. Keep in mind that you have to use
compatible React version (`>=16.14.0`) to use this option and a compatible version of
`@emotion/core` (`>=10.1.0`).

### Examples

```json
{
  "presets": [
    "@emotion/babel-preset-css-prop",
    {
      "autoLabel": true,
      "labelFormat": "[local]",
      "useBuiltIns": false,
      "throwIfNamespace": true
    }
  ]
}
```

_Options set to default values for demonstration purposes._
