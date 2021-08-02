So to use Scrapy for scraping a website, I have taken following steps:
- Create a virtual environment using anaconda prompt: 
	conda create -n yourenvname python=x.x anaconda

- Switch to the new environment created by activating it:
	conda activate yourenvname
	* In case I want to deactivate after, I wrote:
	conda deactivate

- Thereafter, I created a folder in which the project will be stored and then I used cd in shell prompt to 
  go to this folder

- In order to use scrapy, I needed to create first its project by using the following code:
	scrapy startproject projectname .
	* it is a period at the end not a stop point.

- Using for example a text editor (VSCode in my case), we can access the folder named "spiders" and then inside we have
  to create the spider class that will scrape the website (in my case the spider class name is quotes_spider.py).

- Still anaconda prompt heading to this folder, I accessed the scrapy shell by using:
	scrapy shell
	* In case we want to scrape a website, we need to write:
		scrapy shell "your_URL"

- Finally to scrape a website and store the results in a file (.json, .xml, or .csv), we need first to use cd to go to the 
  folder "spiders" and then run this command:
	scrapy runspider yourspiderclassname -o yourFileName.xml
