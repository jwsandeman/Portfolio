# Portfolio Website - Jason Sandeman

## Project Documentation 

### Important Links
- [Website]()
- [GitHub]()

### Project Description
The purpose of the portfolio is website is to showcase my skills as web professional to prospective employer and hopefully catch their attention with my design styling long enough that they stick around to learn more.

Ive taken the simple single page approach (even though theres actually 5 seperate html documents) so as to give it the feel of never leaving the home page. This was achieved by using CSS animation and flexbox to create the effect. Users will be able to navigate around my website using buttons to navigate to my about me section, portfolio, blog and the home page.

I have chosen to use SASS to help streamline my styling in a logical and efficient manner. I have also used a font combination of Raleway and Lusitana that i found on this [blog](https://inkbotdesign.com/font-combinations/).



My sitemap is as follows: 

![Sitemap](./docs/sitemap.png)

It's important when your building a site to keep in mind who the target audience will be. This is not only important for design decisions but it will also help you craft the overal tone and message that will be delivered when someone visits your site. 

My target audience will be a prospective employer with a strong background in software development, programming languages, industry standard tech stacks and design principles. They will have high expectations for a candidate to standout from the crowd with a professional and functional design that proves a hard work ethic and a genune passion for keeping up to date with the latest trends and technologies.

Before we start building the project id like to go over the tech stack that i used and the reasons why i chose each technology. 

- HTML - Ive chosen HTML not only because it is a reuqirement of my assignment but because it is stil a fast and effective way to design static website that look amazing. 

- CSS and SCSS - CSS is essential for any website to overlay desired styling, fonts, animations and colours. Ive also decided to use SCSS to help simplify the design process with variables and @mixins which i will go into more detail further on.

- GitHub Pages - I have chosen to host my portfolio site on GitHub pages because of how easy they have made the process. Also, its free.

### Project Build

First thing i did and i reccommend this to anyone starting a new project it to create a project dashboard where you can manage the project from start to finish. this can be done on your prefferred project management platform but some of the more popular ones are Trello, Notion and Asana just to mention a few. 

Next you need to look at your design brief and client/software requirements. This should be obvious but you need to write these down. You'll be surprised how many times you reference these whilst building your project. My design brief is an assignment so ive got plenty of information to reference.

Once you've set up your dashboard now its time to break the project down into manageable chunks. Start at the high level deliverables and work your way down to the smallest tasks. This can be time consuming but as Benjamin Franklin says "If you fail to plan, you are planning to fail."

Now that you have a plan its time to find some inspiration. This is one of the more enjoyable parts of starting a new project, where you get to dive head first into the depths of the bottomless internet and find sites and seigns that inspire you and that would fit the client design spec well.

Once you crawl out of the catacombs of the internet and have closed all of your tabs on all of your screens its time to start on the wireframe. This can be a simple(low-fidelity) or complicated(high-fidelity) approach, its up to you. I prefer to keep it simple at first by sketching it out roughly on the ipad and then ill move to a more concrete wirframe when im happy with the overall design.  

![Sketch](./docs/sketch.png)

![wireframe](./docs/wireframe.png)

Now that the wireframe is done it might actually be time to intitialise the project! Lets start in the terminal for now witht the following steps:

1. Make a new directory for the project and move into that directory

    `mkdir {project_name}`

    `cd {project_name}`

2. now let's initialise git in the project. Document control is essential - even when working on your own.
    `git init`

3. Now lets set up the directory with the intial folders and files

    `mkdir docs`

    `mkdir ppt`

    `mkdir src`

    `echo "# Portfolio Website - Jason Sandeman" >> README.md`

    `git log > gitlog.txt`

4. Now its time for our intial commit

    `git add .`

    `git commit -m "initial commit, added README/gitlog/sitemap, added project description and sitemap to README"`

5. Once thats done we can open the folder in VS code using the following command

    `code .`

6. Lets code! I'll start with the HTML pages first and then move onto the CSS. For the sake of time ill use some progress screenshots rather than explaining every step of the process. ALso i'll be sure to make regular commits and save my work!

