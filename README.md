# Nicola's New Portfolio Website

Project and development of my new Portfolio Website using Bootstrap.

## About Me 
Born and raised in Italy, I moved to the UK in 2015. I have always been interested in new technologies and IT, as I studied IT in my A levels back in Italy. After 5 years working in content management for a website, I decided to make the step of learning Front-End Development thanks to the edX course, and on this page I want to showcase not only my progress as a student but also a journey that hopefully will lead to new exciting projects in this field.

## Usage

You can visit the Horiseon website by clicking [HERE](https://nikola84ca.github.io/bootstrap-portfolio/). There you can navigate though the website using the top navication links that will redirect you to the relative portion of the website.

## Installation
First, make sure that Git and Git Bash are installed on your system. To download this project on your machine click [HERE](https://github.com/Nikola84ca/bootstrap-portfolio) to go to the repository on GitHub. Click on the green CODE botton, and copy the link of the repository. In your machine, open gitBash and create a new folder where you will clone the project using the command below

```bash
Git mkdir your-project-folder
```
navigate inside the new folder, and clone the project files with the following comands

```bash
cd your-project-folder
Git clone url-copied-on-repository
git pull
```

Open your editor with the command

```bash
code .
```

alternatively download the zip file in GitHub after pressing the Code button, unzip it and copy it in your project folder. Navigate to the folder using the cd command on gitbash and lounch your editor as shown above with code .

## Website Description 

The website is a single page that consists of these elements, listed from top to bottom.

* An Header where we find my name and includes an improved navigation bar, with a structured list of links and dropdown menu links, pointing to specific sections of the page, and an external link.
* A big background image, the hero banner with a specific headline.
* A Work section, where I highlight the main project with a big picture, and four more project sit below. All picture of the project have a nice hover effect that remove the overlay color once hovering with the mouse. All project sections have a title, description and a call-to-action button that serves as a link to the specific webpage of the relative project.
* An About Me section, containing a small picture of me and a short intro/bio.
* A Skills section where I explore my goals during this bootcamp and all the skills and tools I am learning.
* An improved Contact Me section with phone number, email, gitHub profile and website.

Here is a gif animation of the final result, you can compare it with the previous portfolio website by clicking [HERE](https://nikola84ca.github.io/my-portfolio/).

![Gif animation of the webpage](/assets/images/01-portfolio-website-view.gif)

As you can see, I reorganized the content putting the most important assets, my projects, right after the hero banner jumbotron, and organizing the contacts and skills after in a more tidy and structured way. The contact section now is more functional with a dedicated nav bar, buttons with overlay and shadow effects and a handy button to go back to the top of the page.

## My Process

* The first thing I did was designing a new, clearer structure of containers to have a clear idea of how to organize all the content. I started by analysing my previous portfolio, created with flex-boxes, and spotting all the possible improvement I could implement. The use of Bootstrap components has been fundamental to speed up the process and allow me to have a much more tidy, responsive and fast webpage. The first thing to do I did in the html file was to connect my project to Bootstrap through the relative html, Css and JavaScript links.

* Starting from the top of the page, the Header, I decided to opt for a much better nav bar, that can offer many more options, and a clearer and more interactive and intuitive approach to comply with the UI and UX guidelines. Here is an animation of the navigation menu at the top of the page and its functionality:

![Gif animation of the header nav bar, when clicked they will redirect the user to the relative sections of the webpage and external links](/assets/images/02-portfolio-nav-menu.gif)

For the work section I decided to include a dropdown menu, that serves as direct access to the specific project, and also a link to my GitHub profile. Here is a snippet of the HTML structure and its Relative CSS styling code for this nav bar:

```HTML
<nav class="navbar navbar-expand-lg bg-body-tertiary customNav">
    <div class="container-fluid content">
        <a class="navbar-brand" href="#">NICOLA'S PORTFOLIO</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
              </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item dropdown">
                 <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                          WORK
                        </a>
                  <ul class="dropdown-menu">
                 <li><a class="dropdown-item" href="#workTitle">All Projects</a></li>
                 <li><hr class="dropdown-divider"></li>
                 <li><a class="dropdown-item" href="#project1">Horiseon</a></li>
                <li><hr class="dropdown-divider"></li>
                <li><a class="dropdown-item" href="https://github.com/Nikola84ca">GitHub Profile</a></li>
              </ul>
             </li>
          <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#aboutTitle">ABOUT</a>
             </li>
         </ul>
        </div>
  </div>
</nav>

```

For this example I removed some of the links, but it is evident the Bootstrap structure of classes that allows me to identify, and style each component of the menu, from the dropdown button, to every single link and divider. Here is what I did with my custom CSS to override the Bootstrap predefined style.

```CSS

.customNav {
    position: fixed;
    width: 100%;
    background-color: rgb(128, 123, 123);
    background-size: cover;
    z-index: 10;
    background:linear-gradient(0deg, rgba(134, 94, 118, 0.3), rgba(85, 80, 83, 0.3));
    background-size:cover;
  }
  .navbar-nav {
    margin-left: auto;
    margin-right: 0 !important;
  }
  .navbar-brand {
    margin-left: 10px;
  
  }
  .nav-item {
    margin: 0px 15px;
  }

  /* Navigation dropdown menu */
  .dropdown-menu {
    background-color: rgb(128, 123, 123)!important;
    min-height:100%;
    background-size: cover;
  }

  .dropdown-item:focus, .dropdown-item:hover {
    background-color: rgb(182, 180, 180);

      color: rgb(253, 251, 251);
      text-decoration: none;   
  }
  
  .navCTA {
    font-size: 15px;
  }

```

* As requested the new website should maintain some of the features of the previous project, so I decided to keep a similar structure of the work section, showing the main project in a bigger area, and the following four order in two smaller rows. Each project now has a bigger picture compare to the previous project, and a project title, description and a dedicated button to redirect to the specific website. I achieved this using cards, ordered with a grid structure. Just like the previous portfolio, every card has an overlay that fades once hovered with the mouse, and also a button with an hover effect, that changes colour of the background and text once pressed. Here is a gif showing this functionality:

![Gif animation of the projects section, when passing the mouse on them the overlay color fades, and the background picture is fully visible, plus animation of the buttons.](/assets/images/03-portfolio-projects-cards-hover.gif)

This is how I achieved this result with CSS:

```CSS

.card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5); 
  opacity: 1;
  transition: opacity 0.3s ease; /* This adds a transition for smooth visibility change */
  pointer-events: none; /* Ensures the overlay doesn't interfere with mouse events */
}

.card:hover::before {
  opacity: 0; /* When hovering, the overlay becomes transparent */
}
```

* I moved the About Me section below the projects, and added also a Skills section including some of the skills I am learning during the Front End Development Course.

* At the bottom of the page, where the footer sits I decided to implement a much more functional Contact section, that includes my email, phone number and other links. I also added a "Back to the Top of the page" button to make it easier for the users to go back to the top of the page. As specified in the requirements, I implemented all the links as buttons, with an overlay effect that changes when hovered, showing a shadow on the hovered button. Once clicked the button will change colour and the relative text will change as well. Here is a gif animation of the final result:

![Gif animation of the Contacts nav bar at the bottom of the page.](/assets/images/04-portfolio-contacts-nav-menu.gif)

This is the CSS I wrote to make the shadow effect during the hover of a speficic link:

```CSS
footer a:link, a:visited {
  background-color: rgb(160, 159, 159);
  color: black;
  border: 1px solid rgb(62, 62, 65);
  padding: 20px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}

footer a:hover {
  background-color: rgb(122, 122, 122);
  color: rgb(255, 255, 255)!important;
  box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24),0 17px 50px 0 rgba(0,0,0,0.19);
}

```


* Lastly, I made sure that the website is much more responsive for mobile view compared to the previous project, the menu and dropmenu keep their functionality, as all the other bootstrap components. Here is a gif animation of the final result on mobile view:

![Gif animation of the mobile view of the website.](/assets/images/05-portfolio-mobile-view.gif)

The content is align in colums and all the functionality of links and hover effects are working. 


## Credits

I would like to thank all the teachers and TA of the EdX bootcamp for all the content provided. I would like to credit [w3 schools](https://www.w3schools.com/html/html5_semantic_elements.asp) for the useful content responsive layouts, and the staff at [Bootstrap](https://getbootstrap.com/docs/5.0/layout/grid/) for the useful tools provided.

## Project Status and Upcoming Improvements

Although the website is optimized for desktop view and mobile view, it is still not responsive for tablet and other screen sizes. The next steps to offer a more accessible and performant user experience is to work on the CSS of the website in order to make the website even more responsive and easy to navigate on all other devices as well. A new design, using a Grid structure will be a possible approach to this next step.

## Collaborations and Contributions

I welcome all the brilliant coders out there to join me in this project. Join effort can result in a fundamental learning experience for a beginner coder like me, so feel free to reach out with tips and advice. If you want to contribute to this project, pull requests are welcome, but if you want to make major changes, please open an issue first so that we can discuss what you would like to change. You can contact me on my GitHub profile [HERE](https://github.com/Nikola84ca) and visit this project repository by clicking [HERE](https://github.com/Nikola84ca/bootstrap-portfolio).

[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](code_of_conduct.md)

## License

[MIT](https://choosealicense.com/licenses/mit/)