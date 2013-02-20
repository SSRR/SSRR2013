# The SRRR website

The SSRR conference website is based on the Kitchensink Skeleton from [DocPad](https://github.com/bevry/docpad).

## Getting Started

1. [Install DocPad](https://github.com/bevry/docpad) if you want to generate a local version of the website on your machine

1. Clone the SSRR source repository on your computer and run the server


	``` bash
	git clone git://github.com/SSRR/SSRR2013.git
	```

1. If you want to have a local server on your computer, run the server :

	``` bash
	cd SSRR2013
	npm install
	docpad run
	```
 
1. [Open http://localhost:9778/](http://localhost:9778/)

1. Start hacking away by modifying the files in the `src` directory

1. Every time you want to commit your modifications on your local repository: 

	``` bash
	git add .
	git commit -m "Some useful comment"
	```
1. Push your modifications on the github repository:

	``` bash
	git pull
	git push
	```

## When you want to deploy your modifications on the SSRR website

1. To generate a static version of the website ready for deployment:

	``` bash
	docpad generate --env static
	```	

1. Copy the contents of out in the corresponding directory of the website

