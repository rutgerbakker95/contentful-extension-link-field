# contentful-extension-link-field

> Link Field extension for Contentful

This Contentful extension creates a special link field, that lets the user choose between an internal link (to another entry) or an external link (to a specific URL).

The field value is an object. For internal links, it looks like this:

```json
{
  "linkTitle": "",
  "linkType": "internal",
  "entry": {}
}
```

The `entry` property includes all fields and metadata.

For external links, it looks like this:

```json
{
  "linkTitle": "",
  "linkType": "external",
  "url": "https://example.com"
}
```

## Installation

In your Contentful space, go to Settings > Extensions, then select Add Extension > Install from GitHub. In the dialog that opens, paste this URL: `https://github.com/ueno-llc/contentful-extension-link-field/blob/master/extension.json`

## Usage

To add a link field, create a JSON Object field, and under the Appearance tab, select "Link Field".

## Local Development

To test the extension locally, you need a Contentful space to install it in.

```bash
# Clone and install
git clone https://github.com/ueno-llc/contentful-extension-link-field
cd contentful-extension-link-field
yarn install

# Log in to Contentful and install test extension into a space
npm run login
npm run configure

# Compile extension
yarn start
```

Before you commit your changes, run `npm run build`. Contentful loads the extension code directly from GitHub, so the file `build/index.html` needs to be up to date.

## License

MIT &copy; [Ueno](https://ueno.co)
