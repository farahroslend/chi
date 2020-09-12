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


## Technologies Used

### Python and Django

### HTML

### CSS

## Testing

### Manual Testing
- Google Chrome Inspect Feature for each version 
- [HTML Validation](https://www.freeformatter.com/html-validator.html)
- [CSS Validation](https://jigsaw.w3.org/css-validator/)


## Deployment on Heroku

### Heroku Deployment Steps 

1. Go to the Heroku Website and create new app
2. Create requirements.txt and Procfile to tell heroku what is required to run the app
3. Login into Heroku Account via command line and add the newly created app
4. Go back to Heroku Website and in the settings tab click *Reveal Config Vars* and add IP and PORT vars from Project Config
5. Install [ClearDB](https://elements.heroku.com/addons/cleardb) and import local MySQL Database dump.sql
5. Restart all dynos
6. Finally do an initial git commit and push to heroku


## Acknowledgements
- [BoutiqueAdo Project by Code Institute](https://courses.codeinstitute.net/courses/course-v1:CodeInstitute+FSF_102+Q1_2020/courseware/4201818c00aa4ba3a0dae243725f6e32/d90bfac64e564b41a177b65c34a63502/?activate_block_id=block-v1%3ACodeInstitute%2BFSF_102%2BQ1_2020%2Btype%40sequential%2Bblock%40d90bfac64e564b41a177b65c34a63502) For all the apps in this website; modified html, css and json files to fit the requirements of the business logic.
- [BoutiqueAdo Project by Code Institute](https://github.com/Code-Institute-Submissions/Garathd-milestone-project-4) Heroku deploying documnetation