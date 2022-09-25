[![npm version](https://badge.fury.io/js/directus-extension-computed-interface.svg)](https://badge.fury.io/js/directus-extension-computed-interface)

# Introduction
A [Directus](https://github.com/directus/directus) extension for previewing HTML rendering. I designed this primarily to test thumbnail designs in projects for clients. Hopefully this will be useful to other people!

It's currently a very hacky solution, but it works. If there's a better of way doing it, please let me know!

It's based on the [Computed Interface plugin](https://github.com/rezo-labs/directus-extension-computed-interface) by Rezo Labs.

# Installation
```
npm i directus-extension-live-preview
```

# Get Started
1. Go to **Settings**, create a new field with type string or number.
2. In the **Interface** panel, choose **Live Preview** interface. There are 2 options:
    1. **Template**: Similar to M2M interface, determine what HTML is used. Templating similiar to Twig is used for defined fields in the table. 
    2. **Display Only**: Tick this for it to work.

# Using Variables in your HTML

You can use variables in your HTML. The variables are the fields in the table. For example, if you a field called `name`, you can use `{{name}}` in your HTML.

```html
<h1>{{name}}</h1>
```

## Examples


# Limitation
- Cannot parse literal strings (`{{ 's' }}`).
- Cannot use relational fields (`{{ user.name }}`).
