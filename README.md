# 4th Milestone Project

This a fullstack website for a fitness and wellbeing ecommerce webshop. Clients will be able to browse from a list or search for an item from a host of products being sold in this website.


## UX and Features

User stories:

- To view all products, and their details (product description, price, rating)
- To view products by price, categories, rating and the number of results
- To add some products and scale by quantity, to purchase into a virtual bag prior checking out and paying
- To search for relevant product by a keyword in the search bar (to be matched to the product description) and the number of results
- To add some products to purchase into a virtual bag prior checking out and paying
- To know the total amount price of items added into bag
- To register as a new user on the website, to access secret recipes for fitness and wellbeing as well as motivational quotes 
- Sign in/out as a registered user
- To proceed to check out and key in card details to make the purchase 


## Features Left to Implement
- To access secret recipes for fitness and wellbeing as well as motivational quotes (apps in development)
- To proceed to check out and key in card details to make the purchase (app in development)

## Design

### Front-End

My design inspiration was essentially a YouTube and Facebook hybrid. I also took a little inspiration from Reddit with the Up Votes and Down Votes as I like it better than like and dislike. I like the layout of how YouTube presents its videos. I just modified it slightly to show 3 videos per row instead of 4 on the large resolution screen devices and then just show one video per row on smaller resolution devices. I have a few small very basic sketches as I more or less knew in my head how I wanted the site to look. I did my sketches using [Adobe XD](https://www.adobe.com/uk/products/xd.html?sdid=88X75SKR&mv=search&ef_id=CjwKCAiAqt7jBRAcEiwAof2uKyYmJoV3wlWgAtyiwwWG5Q9ndPqtJejDidjgRFtcyOti86rbwX6lkhoCu8IQAvD_BwE:g:s&s_kwcid=AL!3085!3!315413032962!e!!g!!adobe%20xd). Screenshots can be found in the [mockups folder](https://github.com/Garathd/milestone-project-4/tree/master/mockups).

I was considering also doing some mobile resolution mockups but its more or less the same except for the mobile menu and the fact that instead of having 3 videos per row in the All Videos/ My Videos pages it just has one video per row.

***Login/Register Pages***
These pages are more or less the same design wise. If there is an issue with either login or registration then a brief information message should appear on the screen. New users will be directed to a welcome page.

***Welcome Page***
The welcome page appears to the new users and users who have no videos saved on their profile. This page explains how the site works and explains the various buttons. This is also the help page

***All Videos Page***
This page displays all the users’ videos except for the videos of the user that is signed in. Users are redirected to this page when they sign in and if they have existing videos on their profile or else click the logo when they are signed in. On this page you can repost videos as well as vote on videos. Videos can be ordered by user or by category.

***My Videos Page***
Also known as the profile page. This page lets you delete, edit and view your videos. This page also shows reposted videos. Videos can be ordered by category and status (original or reposted). The My Videos and the All Videos pages have more or less an identical design except for a few different options on videos.

***New Video / Edit Video Page***
These pages have identical design. The edit video pages text fields are populated with data from a chosen video and in the new video page the text fields are blank


### Back-End (Django Database)

My backend consists of a relatively simple MySQL database. For testing and Development I use the local [Cloud 9](https://aws.amazon.com/cloud9/?origin=c9io) Database and then for the live version I use the [ClearDB](https://elements.heroku.com/addons/cleardb) heroku add on. The databases can be set in the applications db.py file with options for local or remote databases.

My Database consists of 4 tables:

- ***users***
- ***videos***
- ***categories***
- ***votes***

I had to set ``` ON DELETE CASCASE ``` on the *video id* FOREIGN KEY on the ***votes*** table that REFERENCES the *video id* PRIMARY KEY on the ***videos*** table. This was to ensure that if a video got deleted than all corresponding vote data would be deleted 


The dump file for my database can be viewed [here](https://github.com/Garathd/milestone-project-4/blob/master/dump.sql)

### The ER Diagram for my database:

![alt text](https://github.com/Garathd/milestone-project-4/blob/master/images/ER-Diagram.png)






## Technologies Used

### Python and Django

Flask is the Python Framework I’m using for this application

### HTML

I'm using SCSS to build my css style sheets and probably a little unconventionally I'm using [Materialize](https://materializecss.com/) and also [Bootstrap 4](https://getbootstrap.com/). To be honest though it doesn't seem to have any adverse effects and over all looks better and is more responsive and visually pleasing out of the box when used together than individually. It was initially a mistake on my part but ended up looking pretty good. I also did a little research and decided to use the two of them after reading this [article](https://stackoverflow.com/questions/28613848/is-it-possible-to-integrate-materializecss-into-bootstrap). I also tried Material Design for bootstrap but wasn't happy with the way it looked

### CSS

I have only used minimal JQuery. I have used it for the scroll to top button, the mobile menu and for select options for the forms in materialize.

### Javascript

Using Gulp to watch out for SCSS changes and converting SCSS to CSS


## Testing

### Manual Testing

For manual testing I have tested on the following browsers. *Firefox*, *Chrome*, *Edge* and *IE11*. I had to add some css fixes for both Microsoft Browsers.

I used an Alcatel U5 for mobile phone resolution testing and a Dell Inspiron 5567 for all other testing.

After running each possible scenario multiple times, going over each feature, user stories and client requirements I then validated my HTML and CSS using the following:

- [HTML Validation](https://www.freeformatter.com/html-validator.html)
- [CSS Validation](https://jigsaw.w3.org/css-validator/)



### Unit Testing



## Deployment

During development, all code was written in Cloud 9 and updates were saved and tested locally. Throughout the process I used [GitHub](https://github.com/Garathd/milestone-project-4) to keep track of changes and to maintain version control in my code base.

The development version of my application is on GitHub and I push this code using *git push origin master* and the code is run and tested on Cloud 9 before being updated to heroku

The production version of my application is deployed to heroku and I push this code using *git push heroku master* and the live application can be found [here](https://milestone-project-4.herokuapp.com/).


### Heroku Deployment Steps

1. Go to the Heroku Website and create new app
2. Create requirements.txt and Procfile to tell heroku what is required to run the app
3. Login into Heroku Account via command line and add the newly created app
4. Go back to Heroku Website and in the settings tab click *Reveal Config Vars* and add IP and PORT vars from Project Config
5. Install [ClearDB](https://elements.heroku.com/addons/cleardb) and import local MySQL Database dump.sql
5. Restart all dynos
6. Finally do an initial git commit and push to heroku


## Acknowledgements

- [ER Diagram Generator](https://app.sqldbm.com)
- [ClearDB](https://elements.heroku.com/addons/cleardb)
- [Adobe XD](https://www.adobe.com/uk/products/xd.html?sdid=88X75SKR&mv=search&ef_id=CjwKCAiAqt7jBRAcEiwAof2uKyYmJoV3wlWgAtyiwwWG5Q9ndPqtJejDidjgRFtcyOti86rbwX6lkhoCu8IQAvD_BwE:g:s&s_kwcid=AL!3085!3!315413032962!e!!g!!adobe%20xd)