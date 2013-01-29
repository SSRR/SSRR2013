# The SRRR website

The SSRR conference website is based on the Kitchensink Skeleton from [DocPad](https://github.com/bevry/docpad).

## Getting Started

1. [Install DocPad](https://github.com/bevry/docpad)

1. Clone the SSRR source repository and run the server

1. Clone the project and run the server

	``` bash
	git clone git://github.com/bevry/website.docpad.git
	cd website.docpad
	npm install
	coffee server.coffee
	```

1. [Open http://localhost:9778/](http://localhost:9778/)

1. Start hacking away by modifying the `src` directory

## When you want to deploy your modifications on the SSRR website

1. docpad generate -- env static

1. Copy the contents of out in the corresponding directory of the website

