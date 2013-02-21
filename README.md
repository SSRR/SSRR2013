# The SRRR website

The SSRR conference website is based on the Kitchensink Skeleton from [DocPad](https://github.com/bevry/docpad). DocPad is a static website generator based on JavaScript.
When the generation is done, you can move the resulting files to a web server (html and css files).

There is 2 github repositories:

* one containing the source file of the website : [https://github.com/SSRR/SSRR2013](https://github.com/SSRR/SSRR2013)
* one containing only HTML and CSS generated files: [https://github.com/SSRR/ssrr.github.com](https://github.com/SSRR/ssrr.github.com)

## Getting Started

1. [Install DocPad](https://github.com/bevry/docpad) if you want to generate a local version of the website on your machine

1. Install the following Docpad plugins needed by SSRR website:
	``` bash
  	npm install --save docpad-plugin-eco
  	npm install --save docpad-plugin-coffeescript
  	npm install --save docpad-plugin-marked
	npm install --save docpad-plugin-stylus
	npm install --save docpad-plugin-less
  	npm install --save docpad-plugin-haml
	npm install --save docpad-plugin-js2coffee
	npm install --save docpad-plugin-coffeekup
	npm install --save docpad-plugin-html2coffee
	```

1. Configure correctly your email and name for git:

	``` bash
	git config --global user.name "Your Name"
	git config --global user.email "Your.Name@email.com"
	```

1. Clone the SSRR source repository on your computer:


	``` bash
	git clone git@github.com:SSRR/SSRR2013.git
	```

1. The SSRR website is available on another github repository. In order to clone this repository:

	``` bash
	git clone git@github.com:SSRR/ssrr.github.com.git
	```

## When you want to test the webpages locally on your machine

1. If you want to run a local server on your computer that will regenerate the webpages at every modifications:

	``` bash
	cd SSRR2013
	docpad run
	```
 
1. [Open http://localhost:9778/](http://localhost:9778/)

1. Start hacking away by modifying the files in the `src` directory. All the pages are in the SSRR2013/src/documents/pages/ directory. Only the index.html (entry of the website) is under SSRR2013/src/

2. Files with .md extension are text files based on [Markdown](http://daringfireball.net/projects/markdown/syntax) markup.


1. Every time you want to commit your modifications on your local repository: 

	``` bash
	git add .
	git commit -m "Some useful comment"
	```
1. Push your modifications on the github repository:

	``` bash
	git push origin master
	```
	
1. If you want to get the last version of the files on the server if someone else made a modification:

	``` bash
	git pull
	```

## When you want to deploy your modifications on the SSRR website


1. To generate a static version of the website ready for deployment:

	``` bash
	docpad generate --env static
	```	

1. Copy the contents of out directory containing the generated files in the corresponding directory of the website:

	``` bash
	cp -r out/ ../ssrr.github.com/
	```
	
2. Commit & push the generated files on the server

	``` bash
	git add .
	git commit -m "Meaninfull comment"
	git push origin master
	```

3. Have a look at the new website: [http://ssrr.github.com/](http://ssrr.github.com/)



