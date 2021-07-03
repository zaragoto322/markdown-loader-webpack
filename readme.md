# Markdown Loader

It's a markdown loader for webpack using markdown-it


## Installation

```bash
npm install --save-dev markdown-loader-webpack
```

## Usage

```bash
const path = require('path')
const HtmlWebpackPlugin = require('html-webpack-plugin')

module.exports = {
	entry: {
		index: './src/js/index.js'
	},
	module: {
		rules: [
			{
				test: /\.md$/,
				use: [
				{
					loader: 'html-loader'
				},
				{
					loader: 'markdown-loader-webpack',
					options: {
                        html: true
                    }
				}],
			},
		]
	},

	plugins: [
		new HtmlWebpackPlugin({
			filename: 'index.html',
			template: 'src/views/index.html',
			title: 'example'
		}),
	]
}
```