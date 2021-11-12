## Source Code

View the source code on GitHub [here](https://github.com/jwsandeman/JasonSandeman_T1A2).

## Project Description

The purpose of the portfolio is website is to showcase my skills as a web professional to prospective employers and hopefully catch their attention long enough that they stick around to learn more.

### Target Audience

- It's important when your building a site to keep in mind who the target audience will be. This is not only important for design decisions but it will also help you craft the overal tone and message that will be delivered when someone visits your site.

- My target audience will be a prospective employer with a strong background in software development, programming languages, industry standard tech stacks and design principles. They will have high expectations for a candidate to standout from the crowd with a professional and functional design that proves a hard work ethic and a genune passion for keeping up to date with the latest trends and technologies.

### Design Mentality

- Ive taken the simple single page approach (even though theres actually 5 seperate html documents) so as to give it the feel of never leaving the home page. This was achieved by using flexbox and CSS animation to create the effect.

- Users will be able to navigate around my website using 4 buttons which will navigate to my 'about me', 'portfolio, blog and the home page.

- I have chosen to use SCSS to help with streamlining the styling in a logical and efficient manner.

---

## Design Process & Decisions

### Project Management Dashboard

- First thing i did and i reccommend this to anyone starting a new project it to create a project dashboard where you can manage the project from start to finish. I used Notion to create mine however this can be done on your prefferred project management platform of choice. Some of the more popular ones are Trello, Notion and Asana just to mention a few. Here is a link to my project on [Notion](https://jwsandeman.notion.site/T1A2-Portfolio-Website-82cb51ae84d149038dfa7b5ee00ab4c0)

### Software Requirements

- Next i checked the design brief and client/software requirements. This should be obvious but you need to write these down, preferably in your project dashboard. You'll be surprised how many times you reference these whilst building your project. My design brief is an assignment so ive got plenty of information to reference.

### Sitemap

- Now that you know your software requirements, its time for a sitemap.

  ![Sitemap](./sitemap.png)

### Planning

- Now that my dashboard is set up its time to break the project down into manageable chunks. Starting at the high level deliverables and working my way down to the smallest tasks. This can be time consuming but as Benjamin Franklin says "If you fail to plan, you are planning to fail."

### Inspiration/Mood Board

- Now that I have a plan its time to find some inspiration. This is one of the more enjoyable parts of starting a new project, where you get to dive head first into the depths of the bottomless internet and find sites that inspire you and that would fit the client design spec well. A word of warning - don't spend too much time on this. Set a time limit and stick to it, otherwise inspiration turns into procrastination (speaking from personal experience).

- I ended up settling for a design with a particular aesthetic that would give the whole site a ‘business card’ feel to it. I wanted a clean and effective user interface without too much information overload in order to reduce friction. I also wanted a bit of animation to help enhance the user experience. I used material design for all my sizing (4px/8px increments).

### Design Decisions

Desktop:

- I wanted fixed buttons that stayed in the same place to give the website a single page feel.
- I wanted to steer away from traditional single column scrolling where possible (except blog posts) to maintain the business card effect
- I wanted the ‘about me’ page to have a series of tiles addressing my skills/experience/interest/hobbies etc.

Mobile/Tablet:

- I kept the same basic layout with a similar design aesthetic.
- Optimised the design for single column layout.
- I kept the single page layout for home, blog and projects.
- About me and blog posts were single column scrolling

### Wireframe

- Once I crawled out of the catacombs of the internet and closed all of my tabs on all of my screens it was time to start on the wireframe. This can be a simple(low-fidelity) or complicated(high-fidelity) approach, its up to you. I prefer to keep it simple at first by sketching it out roughly on the ipad and then ill move to a more concrete wirframe when im happy with the overall design. You can access my wireframes [here](https://whimsical.com/portfolio-wireframe-FrwWza12S3iqTH7YrLgS8G@3CRerdhrAw8V6w9PrpoRpqSq). ![Sketch](./sketch.png) ![Wireframes](./wireframes.png) ![Desktop Wireframe](./dwireframe.png) ![Tablet Wireframe](./twireframe.png) ![Mobile wireframe](./mwireframe.png)

---

## Initialise The Project

Now that we are clear on our project requirements it is time to intitialise the project! Lets open the terminal (we will move to VS code later) and perform the following steps:

1. Make a new directory for the project and move into that directory

   `mkdir JasonSandeman_T1A2`

   `cd JasonSandeman_T1A2`

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

5. Create a new repository in GitHub

6. Follow GitHubs commands to link your local directory with your remote GitHub repository

   `git remote add origin git@github.com:jwsandeman/JasonSandeman_T1A2.git`

   `git branch -M main`

   `git push -u origin main`

7. Once thats done we can open the folder in VS code using the following command

   `code .`

8. Lets code! I'll start with the HTML pages first and then move onto the CSS. For the sake of time ill skip straight to the completed screenshots. Also be sure to make regular commits and save your work!

---

## Development

### Desktop

- Built the fixed navigation and footer to achieve desired aesthetic.
- Built the main card that would be used on each page using flexbox.
- Built the tiles on the about page.
- Added blog and projects page.
- Styled each page.
- Added slideshow to blog and projects which prevented the need for page scrolling.
- Built blog post layout.
- Converted styling to mobile and tablet.

### Mobile

- I opted for a standard nav bar at the top for tablet and a pop-down hamburger menu for mobile.
- I removed the card effect for tablet and mobile and just used a basic column layout.
- I kept the same slideshow component for the blog and projects page which also worked well on mobile.
- The blog posts kept the same column layout.

---

## Tech Stack

I'd like to go over the tech stack that i used and the reasons why i chose each technology.

### Project Management

- To keep myself organised and accountable i used **_Notion_**. Its a hybrid between trello, google docs, quip and has handy tools like kanban boards, lists, calendars, gant charts, tables/databases and is basically my one stop shop for organising my entire life.

### Time Management

- I use 2 techniques to help stay on track. The 1st tool is the **_pomodoro technique_** which i think most people have heard of, if not google it.

- The second tool i use is a free phone app called **_Structured_** which lets you break up your day into single manageble task that you can set a time limit on. As the day progresses structured counts down each task and gives you a great visual on how much time you have left on your current task until the next task begins. Simple but very very effective.

### Code Editor

- **_Visual Studio Code_** is my favourite code editor. The amount of helpful extensions alone are enough to justify this over other IDE's for me. Live server, Prettier and Bracket Pair Colouriser being some of my favourites. I also like the layout and the collaboration tools, and I don't think i could go back to an IDE that doesnt have an in-built terminal.

### Markdown

- I used markdown to create this README which i then converted into html and injected straight into my blog post which was really helpful as it maintained markdown formatting and save me a lot of double handling.

### HTML

- Ive chosen **_HTML_** not only because it is a reuqirement of my assignment but because it is stil a fast and effective way to design static websites that look amazing.

### CSS

- **_CSS_** is essential for any website to overlay desired styling, fonts, animations and colours. I also intended to use **_SCSS_** to help simplify the design process with variables, @mixins and nesting. However i was a litlle late converting it to SCSS and essentially ran out of time to convert it before i had to hand in my assignment. I was close though.. i added all of the mixins and variables to my CSS file (commented out) in preperation for easier converting. I'll probably convert it at a later date.

### Javascript (... I know, I know. I said only HTML & CSS)

- So i almost built this portfolio website using only HTML and CSS but let's be honest who doesnt enjoy a quick script here and there. I used 2 seperate scripts in order to make 2 different components work. 1 was for the Markdown -> HTML converter script and the other was for the slideshow component on the blog and projects page.

### Version Control

- For version control i am using **_Git_** and my source code is available on **_GitHub_**.

### Hosting

- I have chosen to host my portfolio site on **_Netlfiy_** because of how easy they have made the process. I can deploy production changes using git in the terminal in VS Code, it's dead simple. Also, its free.

### Security

- I used **_Subresource Integrity_** as reccommended by Coder Academy

---

## Components and Features

Now lets talk about what components and features i used in my design.

### Responsive Design

- I designed this website with responsive layouts in mind. When the screen size changes, the layout and typography is optimised for the current screen size. I have used 3 main media breakpoints - Desktop(>1200px), Tablet(600-1200px) and Mobile(<600px).

### Site Navigation

Header/Navigation - will be simple and effective whilst utilising brand colours to minimise friction.

- Desktop - I have used 4 buttons placed in eah corner of the web page to allow users to navigate around my portfolio. When a user hovers over one of the buttons the icon will rotate and dislay the link description

- Tablet - Using a centred navigation bar at the top of each page.

- Mobile - I have opted for the tradtional burger menu at the top of the screen to diplay the navigation menu.

### Footer

- Desktop/Mobile - Simple footer at the bottom of every page with a link to attribution for the tools i used on this site.

### Main Card Theme

- Desktop - I am using a business card style to display all of my information in. This shows that i understand flexbox and will capture the users attention with a central focus point on the page.

- Mobile - I used a single vertical column scrolling layout for the mobile as the card theme would not work as well on smaller screens.

### About Me Card

- Desktop - I used a grid styled approach for the 'about me' section. This shows off important information and stats that i want to user to be able to ascertain at a glance.

- Mobile - I used the single vertical scrolling column layout here.

### Tiles

- Desktop/Mobile - will provide short and concise summaries in individual cards on the about page.

### Slideshow

- Desktop/Mobile - will help the user navigate blog posts and projects without leaving the page whilst offering a preview image and description.

### Blog Card

- Desktop - Here i used a split row layout on the card so as to give a preview of the blog image and the content contained in the blog. The whole card is a link to the associated blog post.

- Mobile - I used a smaller version of the card to give a preview of the image and the article. These previews are in a single vertical scrolling column layout.

### Portfolio Card

- Desktop - I used vertical column layout so that you can see the screenshots preview of each website i have worked on. I also included a small horizontal information bar at the bottom. This bottom bar has a link to the associated website.

- Mobile - I used a smaller version of the card to give a preview of the website and the information bar. These previews are in a single vertical scrolling column layout.

### Blog Post

- Desktop/Mobile - I used a vertical scrolling column with an image as the post header. Then you have the post meta data and tags followed by the heading and publish date. After that the user can read the blog post by scrolling down the page.

---

## Screenshots

Heres a few of the screenshots of the finished product. The rest are in the docs folder.

Desktop screenshots:

![Home Page](./dhomecompleted.png)![About Page](./daboutcompleted.png)![Projects Page](./dprojectscompleted.png)![Blog Page](./dblogcompleted.png)![Post Page](./dpostcompleted.png)

Tablet screenshots:

![Projects Page](./tprojectscompleted.png)![Post Page](./tpostcompletedtop.png)![About Page](./taboutcompleted.png)

Mobile screenshots:

![Home Page](./mhomecompleted.png)![Post Page](./mpostcompletedbody.png)![About Page](./maboutcompleted.png)![Mobile Menu](./mmenu.png)

---

## Attribution

### Font/Typography

- I have used a font combination of Raleway and Lusitana that i found on this [blog](https://inkbotdesign.com/font-combinations/).

### Color Palette

- The Colour pallet i have chosen came from [Coolors](https://coolors.co/eae4e9-fff1e6-fde2e4-fad2e1-e2ece9-bee1e6-f0efeb-dfe7fd-cddafd) and is as follows: ![Colour Palette](./colourpalette.png)

### Icons

- For my icons i used [Font Awesome](https://fontawesome.com/).

### Images

- I created most of my images in Canva and my profile pic was taken by a friend of mine named James Stocks who gave me the image to use freely. His portflio can be found [here](https://jamesstocks.myportfolio.com/).

### Markdown -> HTML converter

- I used a markdown converter script in the header to insert my markdown file directly into this blog post. This saved me a ton of time as i already had a correctly formatted markdown file with my blog post written on it. If your reading the markdown file instead of the website, you can see the end result [here](https://festive-aryabhata-690f3c.netlify.app/post1.html).

  Here is the ISC License attribution:

  ISC License

  Copyright (c) 2021, Jason Lee <jason@zerodevx.com> (jason@zerodevx.com)

  Permission to use, copy, modify, and/or distribute this software for any
  purpose with or without fee is hereby granted, provided that the above
  copyright notice and this permission notice appear in all copies.

  THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
  WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
  ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
  WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
  ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
  OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.

### Mobile Navigation Bar/Burger Menu

- I used a html/css navigation bar called 'CSS Flexbox Based Responsive Navigation' by [Mehmet Burak Erman](https://codepen.io/mburakerman) which i found [here](https://codepen.io/mburakerman/pen/QpGpQZ). It was fairly simple to implement then it just needed a few styling adjustments. It is under the MIT licence.

  Copyright 2017 Mehmet Burak Erma

  Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE

### Slideshow Component on Blog and Projects pages.

- I used slideshow from [w3schools.com](https://www.w3schools.com/howto/tryit.asp?filename=tryhow_js_slideshow). It involved HTML, CSS and a small Javascript script.

### Text/icon background gradients

- For the gradient i used an example from Sarah L. Fossheim's blog [post](https://fossheim.io/writing/posts/css-text-gradient/)

---

## Challenges

- Juggling work and family commitments.
- Being over ambitious with the design and trying to figure out how to code it.
- The desktop navigation button css animation was very time consuming.
- The slideshow css was hard to get right.
- The icons had a weird glitch where they would randomly not show up on different devices/browsers.
- The desktop design proved very difficult to convert to mobile later. I found the design would behave - differently on my iphone and ipad than it did in the google chrome device toolbar.
- I had to opt for a simpler mobile design than i had originally intended.
- I pretty much had to start again with the mobile cards which caused breaking changes.
- In future i will definitely be starting with mobile first and expanding from there.

## Favourite Parts

- When my css worked.
- Getting the desktop navigation buttons working correctly was a big win.
- Getting the slideshow working properly was another big win.
- The end result - I’m really happy with how the desktop site turned out especially the blog posts.

---

Thankyou for taking the time to read this. I put a lot of effort into it an i hope it has helped you in some way.
