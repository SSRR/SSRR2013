# The SRRR website

The SSRR conference website is based on the Kitchensink Skeleton from [DocPad](https://github.com/bevry/docpad). DocPad is a static website generator based on JavaScript.
When the generation is done, you can move the resulting files to a web server (html and css files).

## Getting Started

1. [Install DocPad](https://github.com/bevry/docpad) if you want to generate a local version of the website on your machine

1. Configure correctly your email and name:

	``` bash
	git config --global user.name "Your Name"
	git config --global user.email "Your.Name@email.com"
	```

1. Clone the SSRR source repository on your computer


	``` bash
	git clone git@github.com:SSRR/SSRR2013.git
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
	
1. If you want to get the last version of the files on the server if someone else made a modifications:

	``` bash
	git pull
	```

## When you want to deploy your modifications on the SSRR website

1. To generate a static version of the website ready for deployment:

	``` bash
	docpad generate --env static
	```	

1. Copy the contents of out in the corresponding directory of the website

