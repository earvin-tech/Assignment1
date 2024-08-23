# Portfolio 

## Overview
This project is basic portfolio site about myself, Earvin Tumpao. This site will contain 5 webpages, the homepage, an About page, Skills page, Work page, and Contact page. Below will be details outlining all these different pages. 

This document will be updated as the project continues. 

## Homepage
The homepage is the main page the user will see when accessing the site. The header and footer of the hompage is the same on all other pages on the site.

### Header 
The header contains an icon and name which both link back to the homepage. It also contains a nav bar that has links to the other pages on the site. 

On mobile view the icon and name links will be centered on top of the nav bar. The nav bar will be spread out across the header evenly. On large screen sizes the nav bar will only stretch across the right side of the header and the icon and name links will be on the left side of the header but aligned on the same row as the nav bar.

### Footer 
The footer contains 3 icons which link to my social media pages, LinkedIn, Github, and Instagram. 

On the different screen sizes the social media links will be spread out differently: 

- Mobile view: Links are spread out with even space between. 
- Tablet view: Similar to the mobile view but links closer to center with space around the two outer links. 
- Desktop view: The links are much more centered but with a little space between the links.

### Main content of Homepage: Main Photo and site overview
The main content consists of a main photo of myself and a brief overview of the purpose and content of the website and it's pages.

On the mobile view the main photo and overview are aligned in a column and in a row on larger screen sizes.

Below is the HTML code and CSS styling for the homepage: 

```HTML 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Earvin Tumpao</title>
    <link rel="stylesheet" href="/styles/index.css">
    <link rel="stylesheet" href="/styles/home.css">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css" integrity="sha512-Kc323vGBEqzTmouAECnVceyQqyqdsSiqLQISBL29aUW4U/M7pSPA/gEUZQqv1cwx4OnYxTxve5UMg5GT6L4JJg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;1,600&display=swap" rel="stylesheet">

</head>
<body>
    <div class="main-body">
        <header>
            <div class="header-home-links">
                <a href="#" class="icon-link">
                    <img src="/images/iconPic2.png" alt="Icon Image">
                </a>
                <a href="#" class="name-link">
                    Earvin Tumpao
                </a>
            </div>
    
            <nav>
                <a href="pages/about.html">About</a>
                <a href="pages/skills.html">Skills</a>
                <a href="pages/work.html">Work</a>
                <a href="pages/contact.html">Contact</a>
            </nav>
        </header>
    
        <main>
            <h1>Earvin Tumpao's Portfolio</h1>
            <div class="homepage-div">
                
                
                <img src="images/mainPhoto.png" alt="Main Photo of Earvin Tumpao">
        
                <div class="main-text">
                    <p>Hi, my name is Earvin Tumpao and welcome to my portfolio site. Here you will find an outline of my skill and work so far as an aspiring web developer. Feel free to contact me for any queries and I'll be sure to get back to you as soon as possible.</p>
                </div>
            </div>
        </main>
        <footer>
            <a href="https://www.linkedin.com/in/earvin-tumpao-21640b31b" target="_blank">
                <i class="fa-brands fa-linkedin"></i>
            </a>
            <a href="https://github.com/earvin-tech" target="_blank" id="git-link">
                <i class="fa-brands fa-github"></i>
            </a>
            <a href="https://www.instagram.com/earvin_ktumpao?igsh=M3A4OGMycjYzYXB4" target="_blank">
                <i class="fa-brands fa-instagram"></i>
            </a>
        </footer>
    </div>
    

</body>
</html> 
```

```CSS 
:root {
    --header-footer-colour: #13293D;
    --background-colour: #4D7EA8; 
    --secondary-colour: #E8F1F2;
    --text-background: #CCAC8F;
    --border-colour: #FFD700;

    

}

body {
    margin: 0;
    max-width: 100vw;
    font-family: Barlow Condensed;
    font-size: auto;

}
.main-body {
    background-color: var(--background-colour);
    max-width: 100vw;
    min-height: 100vh;

    display: flex;
    flex-direction: column;
    justify-content: space-between;
}



header {
    max-width: 100vw;
    background-color: var(--header-footer-colour);

    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 1%;

}

.header-home-links {
    display: flex;
    margin-bottom: 5%;
}


.header-home-links img {
    width: 40px;
    border-radius: 50%;
    
    
    
} 

.icon-link {
    margin-right: 5px;
}

.name-link {
    color: var(--secondary-colour);
    font-size: 1.3rem;
    font-weight: 700;
    align-self: center;
    text-decoration: none;
}

nav {
    box-sizing: border-box;
    width: 100%;
    padding: 0% 1% 1%;
    
    
    display: flex;
    justify-content: space-between;
}

nav a {
    color: var(--secondary-colour);
    font-size: 1.2rem;
    text-decoration: none;
    padding: 0 1%;
    border-radius: 5px;
}




footer {
    box-sizing: border-box;
    max-width: 100vw;
    background-color: var(--header-footer-colour);
    padding: 1% 1%;

    display: flex;
    justify-content: space-between;
}

footer a {
    font-size: 2rem;
    color: var(--secondary-colour);
}

@media screen and (min-width: 768px) {
    header {
        flex-direction: row;
        justify-content: space-between;
    }

    nav {
        width: 40%;
    }

    .header-home-links {
        margin: 0;
        padding-bottom: 1% ;
        padding-left: 1%;

    }

    footer {
        justify-content: space-around;
    }
}

@media screen and (min-width: 1024px) {
    footer {
        justify-content: center;
    }

    #git-link {
        margin: 0 5%;
    }
}


``` 

```CSS
.homepage-div {
    display: flex;
    flex-direction: column;
    align-items: center;
}

main {
    display: flex;
    flex-direction: column;
}

main img {
    box-sizing: border-box;
    width: 300px;
    margin-bottom: 5%;
    border: 5px solid black;
    border-radius: 5px;

    transition: .5s;
}

main img:hover {
    transform: scale(1.1);
} 

h1 {
    text-align: center;
}

.main-text {
    box-sizing: border-box;
    width: 300px;
    border: 5px solid black; 
    border-radius: 5px;
    text-align: center;
    margin: 0 10% 10%;
    background-color: gray;
    font-size: 18px;
    padding: 2%;

    transition: .5s;
} 

.main-text:hover {
    transform: scale(1.1);
}

@media screen and (min-width: 768px) {
    .homepage-div {
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }

    main img {
        margin: 0;
        margin-right: 15%;
    }

    .main-text {
        margin: 0;
        height: 398.4px;

        display: flex;
        align-items: center;
    }

    main h1 {
        margin-bottom: 2.5%;
    }
}
```
Note: The main content styling of the homepage is in it's own seperate stylesheet.

## About Page

The About page outlines more about myself such as my hobbies and interests. It simply contains a photo and some text describing me.

### Main content of About Page: Photo and Overview
The photo and text overview are arranged in a column in when in mobile view and in a row in larger screen sizes. Both will also enlarge by 10% in size when hovering over them.

Below is the HTML and CSS code for the about page:

```HTML  
<main>
    <h1>About Me</h1>
    <div class="about-container">
        
        <div class="about-text">
            My name is Earvin Tumpao. I am a Filipino-Australian born and raised in the city of Melbourne. As an aspiring web developer I have decided to dedicate my time to learning the in's and out's of the industry and this page outlines my journey so far. From the basics of HTML and CSS I have done my absolute best to showcase my skills by building this website. <br><br>

            As a person I am someone who enjoys learning and experiencing new things, hence I have developed a hobby of travelling. I also like sports, mainly basketball and combat sports of any kind, making me a competitive person at times. If you were to ask me my favourite food I couldn't name just one, there's just too much to choose from. However desserts are something I can enjoy any time any where.
        </div>
        
        <section class="about-image">
            <img src="../images/aboutPhoto.png" alt="Picture of me, Earvin Tumpao">
            <figcaption>Me, travelling in Singapore</figcaption>
        </section>

    </div>
</main>
```

```CSS
h1 {
    text-align: center;
}


.about-text {
    box-sizing: border-box;
    background-color: gray;
    width: 70vw;
    max-height: 30vw;
    border: 5px solid black;
    border-radius: 5px;
    padding: 2%;
    overflow-y: auto;

    transition: .5s;
}

.about-text:hover {
    transform: scale(1.1);
}

.about-container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    row-gap: 100px;
    align-items: center;
    padding: 4%;
}

.about-container img {
    box-sizing: border-box;
    border: 5px solid black;
    width: 100%;
    border-radius: 5px;
}


.about-image {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 70vw;

    transition: .5s;

}

.about-image:hover {
    transform: scale(1.1);
}



@media screen and (min-width: 768px) {
.about-image {
    width: 30vw;
    order: -1;
}

.about-image img {
    box-sizing: border-box;
    width: 100%;
}

.about-text {
    width: 30vw;
    padding: 2%;
}

.about-container {
    box-sizing: border-box;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
}

}
```
## Skills Page
This page outlines my skills as a web developer. 

### Main content of Skills page: HTML, CSS, Wireframing 

The skills contains 3 sections outlining a skill in each, HTML, CSS and wireframing. In mobile view they are aligned in a column and in larger screen sizes all 3 are on a single row.

Below is the code for the skills page: 

```HTML
<main>
    <h1>Skills</h1>
    <div class="skill-container">
        <article>
            <h2>HTML</h2>
            <p>I am able to use HTML, a markup language to structure a webstite with features such as headings, images, and text. This web page you are viewing now is structured by HTML code I wrote.</p>
            <img src="../images/html.png" alt="Screenshot of some HTML for a project.">
        </article>

        <article class="css-skill-div">
            <h2>CSS</h2>
            <p>CSS allow me to style the HTML elements I create. I use CSS to style the colours, borders, font style and placement of elements on the page, with features such as flexbox.</p>
            <img src="../images/css.png" alt="Screenshot of some CSS of a project.">
        </article>
        
        <article>
            <h2>Wireframing</h2>
            <p>Wireframing allows proper planning of the placement and structure of web pages. This allows me to know what to code making the process of building a website much more efficient.</p>
            <img src="../images/wireframing.png" alt="Screenshot of wireframing for a project.">
        </article>
    </div>
</main>
```

```CSS
.skill-container {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
}

article {
    background-color: gray;
    width: 80%;
    border: 5px solid black;
    border-radius: 10px;

    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 5%;
    padding: 2.5%;
}


article img {
    width: 80%;
    border: 3px solid black;
    border-radius: 5px;
    
    transition: .7s;
}

article img:hover {
    transform: scale(2);
}


p {
    margin-block-start: 0;
}

@media screen and (min-width: 768px) {
    .skill-container {
        flex-direction: row;
        width: 80%;
        margin-left: auto;
        margin-right: auto;
    }

    article {
        width: 40%;
        min-height: 600px;

    }

    .css-skill-div {
        margin-left: 5%;
        margin-right: 5%;
    }

    img {
        margin-top: 20%;
    }
}
``` 
## Work Page
Work page is just placeholders for job positions. 

### Main content of work page: 
The main content is simply 4 divisions of text and headings aligned in a column. The page is the most simple of the pages as it is the same layout in all device screens. 

Below is the code for the work page: 

```HTML
<main>
    <h1>Work</h1>
    <div class="work-container">
        <article>
            <h3>Placeholder Position 1</h3>
            <h4>(Jun 2019 - May 2021)</h4>
            <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Recusandae cumque, incidunt reiciendis saepe quod dolor temporibus nobis animi qui dignissimos vitae quidem nostrum provident culpa quam esse quas quibusdam quos!</span> 
        </article>

        <article>
            <h3>Placeholder Position 2</h3>
            <h4>(Mar 2021 - Apr 2022)</h4>
            <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aut exercitationem cum fugiat tempora. Neque earum quos sint, similique aut nisi nihil voluptatibus alias eaque, pariatur eius. Libero optio perspiciatis illo.</span>
        </article>

        <article>
            <h3>Placeholder Position 3</h3>
            <h4>(Apr 2022 - Sep 2023)</h4>
            <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse facilis, incidunt quasi quis iste sint numquam eum vero maiores temporibus nemo ad dolorem consectetur ipsam beatae voluptate iure neque nobis!</span>
        </article>

        <article>
            <h3>Placeholder Position 4</h3>
            <h4>(Sep 2023 - current)</h4>
            <span>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quaerat voluptas placeat dolore quia, suscipit quae accusamus sapiente commodi incidunt consequatur perspiciatis a aliquam culpa consectetur modi numquam possimus debitis accusantium.</span>
        </article>
    </div>
</main>
```

```CSS  
.work-container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    min-height: 100%;
    margin-top: 5%;
    margin-bottom: 10%;
}

h3 {
    margin-block: 0;
    text-align: center;
}

h4 {
    text-align: center;
    margin-block: 0;
}

article {
    width: 60vw;
    background-color: gray;
    border: 5px solid black;
    border-radius: 5px; 
    padding: 2%;
    margin-bottom: 3%;
}
```

## Contact Page 

The contact page allows users to input their details for me to contact them if they wish.

### Main content of contact page: Contact Form

The form has inputs for a user's name, email, mobile and whatever enquiry they have. It also has a submit button (though it doesn't function). In mobile view the input and labels of the input are stacked in a column, in larger devices they are arranged in a row side by side.

Below is the code for the contact page: 

```HTML 
<main>
    <h1>Contact Me</h1>   
    <p>If you have any questions please feel free to contact me by filling out the form below:</p>
    
            <form action="" name="form">

            <div class="form-element">
                <label for="name">Name:</label>
                <input type="text" id="name">
            </div>

            <div class="form-element">
                <label for="email">Email:</label>
                <input type="text" id="email">
            </div>

            <div class="form-element">
                <label for="mobile">Mobile:</label>
                <input type="text" name="" id="mobile">
            </div>

            <div class="form-element bottom-form-element">
                <label for="enquiry">Enquiry:</label>
                <textarea name="" id="enquiry" rows="5"></textarea>
            </div>

            <div class="form-element">
                <button>Submit</button>
            </div>
        </form>
</main>
```

```CSS
p {
    margin-bottom: 8%;
    text-align: center;
    margin-left: 1%;
    margin-right: 1%;
}

form {
    background-color: gray;
    width: 50%;
    margin: 0 auto 5%;
    border: 5px solid black;
    border-radius: 5px;
    padding: 5% 0;
}

.form-element {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 5%;
}

.form-element input {
    width: 50%;
    border: 1px solid black;
    border-radius: 5px;
}

.form-element input:focus {
    box-shadow: 0px 1px 23px 6px rgba(0,0,0,0.66);
}

.form-element textarea {
    width: 50%;
    resize: vertical;
    border: 1px solid black;
    border-radius: 5px;
}

.form-element textarea:focus {
    box-shadow: 0px 1px 23px 6px rgba(0,0,0,0.66);

}

.form-element button {
    border: 1px solid black;
    border-radius: 5px;

    transition: .2s;

}

.form-element button:hover {
    background-color: rgb(46, 43, 43);
    color: white;
}

.bottom-form-element {
    margin-bottom: 15%;
}

@media screen and (min-width: 768px) {
    .form-element {
        flex-direction: row;
    }

    .form-element label {
        width: 12%;
        text-align: right;

    }

    .form-element input {
        margin-left: 2%;
        width: 80%;
    }

    .form-element textarea {
        margin-left: 2%;
        width: 80%;
    }

    button {
        margin: auto 
    }
}
```


