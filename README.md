# Sapphires-Redesign

## Project Overview:
This project is a redesign of a OSU CSE professor's webpage. The professor we chose was Dr. Venkatakrishnan.

## How to build the webpage (User instructions):
1. First you must have ruby, ruby on rails, and middleman. Middleman can be installed via ruby gems while ruby and ruby on rails were installed through the environment setup. 

2. Next you must clone this directory and open the terminal to the folder (when you run the command ls on linux, it should list the files you see in the repo). 

3. Once you're in the folder, run bundler install (path to gemfile) and it should install all the gems needed to run middleman build

4. Finally run middleman build. 

5. Once the build is complete, run middleman server to see the live view of the webpage.

## How the project works:
The team used a mix of ERb, markdown, html, css, and yml files to construct the final webpage.

The ERb files allowed us to put ruby code into the html pages. This was key to loading data from the yml files into the page. ERb allowed us to also create partial files which can used to modularize the html page. You can see how the page was modularize through the layout.erb. Some other things we used ERb for were creating tags on the final html page through conditional statements and generating images.

Files labeled with .html.erb are also a part of the modularization seen in the layout. Each part contains the core details of each page (i.e. home, research, students, etc). They are displayed via the yield keyword.

Our CSS file is loaded into the layout.erb via ruby inline code. This file controls the style for the whole webpage.

Markdown files (which is also this read me) help generate the Home page and Teaching page. This was done due to the ease of creating paragraph heavy pages.

Lastly. we used yml files to store links and text. This helped us make each html file more readible and allows for data to be used between pages without having to copy and paste data. It also allowed us to use ruby functions on data which helped generate the html page much more easily. Another benefit of having the data in it's own yml file allows for ease of updating pages as if the professor were to add or remove students, the yml file has to be updated but not the html page.