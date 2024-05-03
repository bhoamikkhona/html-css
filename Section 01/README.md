# Section 01: Introduction

**About:** In this section, we go over a high-level overview of what is web development. Along with that we set up our code editor (Visual Studio Code), and build our very first webpage. We also get some of the cour materials and understand how to take this course and how to get help in case we need it.

## Lessons Learned

- A High-Level Overview of Web Development
  - Frontend vs. Backend Development
    - Let's say that we are trying to access a webpage in our browser at omnifood.dev (a website that we will build in this course).
    - What happens as we try to access this page is that our browser will send a request to the server where this page is hosted on the internet.
      - Each and every website is stored on something called a server, which is basically a computer that is connected to the internet and is able to receive requests like the one we are talking about.
    - When we browse to a certain website, our web browser will send a request to the server where the website is stored (where it is hosted).
    - When the server receives the request, it will take all the files that make up the website and send them back to the browser. So, we say that the server sends a response to the browser, which essentially contains all of these files that the website is made of.
    - The files that the server sends have the extensions of `.html`, `.css`, and `.js` and from these extensions, you can tell that these files are of HTML, CSS, and JavaScript. These are precisely the three languages that browsers can understand.
    - This means that all of the code that makes up a website needs to be written in HTML, CSS, and JavaScript because they are essentially the 3 core technologies that any browser can understand.
    - Once the browser receives these HTML, CSS, and JavaScript files from the service response, it will take the code and based on it, the browser will render the website that we are trying to access.
    - With this, you should have a basic understanding of what actually happens when we browse a website along with the technologies that we use to build any website.
    - The process of writing HTML, CSS, and JavaScript code that the browser can understand is the process that we call front-end web development.
    - Front-end web development means writing the code that is displayed in a browser - basically the front-end of a website. In fact, this is essentially what we are going to learn in this course, or at least the very fundamentals of front-end development, which is learning HTML and CSS.
    - **NOTE:** Whenever the files that make up the website are simply stored on the web server and are then sent to the browser as they are, we say that we have a <ins>static website</ins>.
    - Now let's talk about backend development. This time, let's try to understand what happens when we try to access a website like udemy.com.
    - The first step is that a request is sent to the web server where udemy.com is hosted.
    - Why is udemy.com so different from a static website such as omnifood.dev?
    - A static website is completely different from a complex site like udemy.com because there is a lot of content that is always chaning in websites like udemy.com, for example, there are always new courses and new reviews being added to the site, new ratings, and course length are calculated and whole lot of other things.
    - So, in order to make this work, udemy.com needs a whole application running on a server and they also need a big database, which basically contains all the courses, and all the reviews, all the users and really all the content that is being displayed on their website.
    - To do all that, front-end technologies like HTML and CSS are simply not enough. Basically, with what you will learn in this course, you are not going to be able to build something like udemy.com.
    - To write applications that are actually executed on web servers, developers use some kind of backend language like Node.js, PHP, or Python. These languages take the data out of a database and assemble that data into final files that will then be sent to the browser as the response; and this whole process is called back-end development because this is basically the invisible part of a website i.e. its back-end.
    - In this situation, we say that we have a dynamic website because the website is dynamically assembled from different pieces on the server and that happens each time that someone visits the website.
    - Returning to the example of udemy.com - each time you visit udemy.com, a new version of the website is going to be generated from their database and sent to your browser.
    - On the other hand, if udemy was a static website, then the website files would already be sitting on the server just waiting for someone to access them.
    - That is the big difference between static and dynamic. In static, the files are already done and in dynamic, they first need to be generated by an application that is running on the server.
    - The rest of the process is the same as before. So, the files from backend are then ready to be sent to the browser as a response, which will then be converted to the final website like the udemy.com.
- This is a very high-level overview. The key takeways from this should be:
  - What are static websites
  - What are dynamic websites
  - What is front-end
  - What is back-end
  - What is browser
  - What is server
- The 3 Languages of the front-end
  - HTML
    - HTML is responsible for the content of the page i.e. the text, images, buttons, etc.
    - All the content that you see on a webpage is always written inside a an HTML file.
  - CSS
    - CSS is responsible for the presentation of that content i.e. for styling and laying out elements on the webpage.
  - JavaScript
    - JavaScript is the acutal programming language of the front-end. It allows us to add dynamic and interactive effects to webpages.
    - We can also use it to manipulate the content or the CSS, to load data from web servers, and even to build entire front-end applications which we then call web applications.

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)