## Code Institute Data Centric Development Milestone Project
# Vegan Minus Gluten
Vegan Minus Gluten is an online cookbook where users can browse recipes and registered users can submit, edit and delete recipes they have posted. Clean and simple - without unnecesarry long essays about inpiration etc. Catered to host plant-based gluten-free recipes.

![site logo](https://res.cloudinary.com/www-madine-se/image/upload/v1595172156/vegansite/readme/bannerreadme_detb2e.jpg)

[Visit deployed site](https://vegan-gluten.herokuapp.com)

## Table of Contents

- [**Demo**](#Demo)
- [**UI/UX**](#UI/UX)
  - [Project goals](#Project-goals)
  - [User Stories](#User-Stories)
  - [Developer goals](#Developer-goals)
  - [Design](#Design)
    - [Research](#Research)
    - [Wireframes](#Wireframes)
    - [Color Palette](#Color-Palette)
  - [Defensive design](#Defensive-design)
- [**Features**](#Features)
    - [Notes](#Notes)
    - [Existing features](#Existing-features)
    - [Future features](#Future-features)
- [**Information Architecture**](#Information-Architecture)
- [**Technologies used**](#Technologies-used)
- [**Testing**](#Testing)
    - [Validators and linters](#Validators-and-linters)
    - [Manual testing](#Testing)
    - [Errors](#Errors)
- [**Deployment**](#Deployment)
- [**Credits**](#Deployment)
    - [Code](#Code)
    - [Images](#Images)
- [**Acknowledgements**](#Acknowledgements)
- [**Disclaimer**](#Disclaimer)

## Demo

![demo2](https://res.cloudinary.com/www-madine-se/image/upload/v1595203055/vegansite/readme/ezgif.com-crop-4_xi2tc7.gif)


[Video link](https://res.cloudinary.com/www-madine-se/video/upload/v1595200322/vegansite/readme/demovegan_gyowyo.mp4)

## UI/UX
### Project goals
Vegan Minus gluten is milestone project for Code Institute Data Centric Development module. The goal of this project is to create, store, edit and delete recipes (CRUD). Target audience for this project is people that are gluten allergic/intolerant or are simply interested in gluten-free and vegan cooking. My goal was to create online cookbook without any unnecesarry long descriptions - only straight-to-the-point recipes. A secondary goal is to sell a theoretical physical cookbook by scattering ads across the site.

### User Stories

As a User I would like to:
- [x] Access the site from both mobile devices and desktop browsers.
- [x] Be able to register to have my own profile.
- [x] Be able to browse and navigate information easily.
- [x] Be able to search recipes by ingredients or name etc.
- [x] Browse recipes by category
- [x] Submit my own recipes
- [x] Subscribe for a newsletter if I do not wish to Sign Up
- [x] Sign up or Sign in with user friendly form
- [x] Edit and delete my own recipes, without others tampering with my submitted recipes.
- [x] Get feedback for submitting/editing/logging in/logging out
- [x] Access a list of all recipes
- [x] Get error messages in case user has done something wrong or there is an issue with database.

As an admin I would like to do all of the above plus:
- [x] Be able to access, edit and delete ALL recipes from admin profile

### Developer goals

 * Provide a simple, easy to use online cookbook where user can browse, post, edit and delete recipes, filter them by categories, search by text, subscribe and have profile.
 * By practice learn Jinja templating, Python, non-relational database MongoDb 
 * Improve Bootstrap and JavaScript knowledge.
 * Learn to use Heroku Pages

### Design

![Demo Picture](https://res.cloudinary.com/www-madine-se/image/upload/c_scale,w_2144/v1595199372/vegansite/readme/demostatic_elwtwp.jpg)

Main inspiration for the page design comes from [Cookie and Kate](https://cookieandkate.com) site and the idea to create it specifically vegan + gluten-free comes from my friends asking for recipe ideas.

I chose to override all B4 round corners on images, forms and buttons to suit my design. I chose calm and neutral colors because the colors of recipe images are very vibrant and all over the spectrum. 

To build the design of the page I used Bootstrap 4, FontAwesome, Adobe Illustrator and Adobe Photoshop. 

To design page [logo](https://res.cloudinary.com/www-madine-se/image/upload/v1592952530/vegansite/Screenshot_2020-06-24_at_00.47.43_upejzd.png) and favicon I used Adobe Illustrator. 

I used Adobe Photoshop to create cookbook ( [1](https://res.cloudinary.com/www-madine-se/image/upload/v1594563548/vegansite/cookbook_dkpywm.jpg), [2](https://res.cloudinary.com/www-madine-se/image/upload/v1595090139/vegansite/book_banner_vj3xtf.jpg) )  design and photoshopped that onto images of books. For the index page jumbotron I had to extend and adjust the background for the text over it to fit nicely ([original](https://www.crowdedkitchen.com/spring-vegetable-frittata-vegan/) vs my [jumbotron](https://res.cloudinary.com/www-madine-se/image/upload/v1594225831/vegansite/Vegan-Frittata__rxd4dw.png)).


 Fonts used: [Dazzle Unicase](https://fonts.adobe.com/fonts/dazzle-unicase), [Playfair Display](https://fonts.adobe.com/fonts/playfair), [Linotype Didot](https://fonts.adobe.com/fonts/linotype-didot), [Arimo](https://fonts.adobe.com/fonts/arimo) imported from Adobe Fonts.

#### Research

I browsed many other online recipe sites to gain insight on how pages are created, their functionality and the way information is displayed and organised. Personally I find it irritating to have to scroll through pages on pages of text and photos only to get to recipe ingredients and instructions, therefore this is a subjective take on a recipe site. I observed that my friends feel the same way and decided to make a minimalistic site.

#### Wireframes

After browsing lots of recipe sites I had a very clear idea of what I wanted the site to look and created wireframes with Adobe XD directly. 

Initial wireframes for [homepage](https://res.cloudinary.com/www-madine-se/image/upload/v1595196757/vegansite/readme/initial%20mockups/Web_1920_1_sqlmhn.png), [recipe](https://res.cloudinary.com/www-madine-se/image/upload/v1595196757/vegansite/readme/initial%20mockups/Web_1920_3_hevjef.png), [form](https://res.cloudinary.com/www-madine-se/image/upload/v1595196756/vegansite/readme/initial%20mockups/Web_1920_4_jrd626.png),[recipe list](https://res.cloudinary.com/www-madine-se/image/upload/v1595196756/vegansite/readme/initial%20mockups/Web_1920_2_ifp82a.png). At first I had come up with a different name, but after some googling I found that that site  with same name already exists.

I realised that making forms with those fields would be too time consuming so I simplified.

During development I simplified even more. I viewed mockup as a guide and did not stick to it to the pixel as I did not find it necessary. There is too little difference (3 columns become 2 for example) between desktop and tablet version therefore I omitted making tablet wireframes, shop page wireframes, signup page (same template, different input fields) and profile page (just a list of images with titles).

Index page

<img width="90%" src="https://res.cloudinary.com/www-madine-se/image/upload/c_scale,w_1260/v1595196813/vegansite/readme/final%20mockups/Web_1920_1_2x_aiydsy.png"> 


  Wireframes for:
 [search results](https://res.cloudinary.com/www-madine-se/image/upload/v1595196812/vegansite/readme/final%20mockups/Web_1920_6_rpgg2q.png), [recipe list](https://res.cloudinary.com/www-madine-se/image/upload/v1595196812/vegansite/readme/final%20mockups/Web_1920_2_iwbsbx.png), [single recipe](https://res.cloudinary.com/www-madine-se/image/upload/v1595196812/vegansite/readme/final%20mockups/Web_1920_3_l4lgig.png), [login](https://res.cloudinary.com/www-madine-se/image/upload/v1595196812/vegansite/readme/final%20mockups/Web_1920_5_kwgbqu.png), [recipe form](https://res.cloudinary.com/www-madine-se/image/upload/v1595196812/vegansite/readme/final%20mockups/Web_1920_4_e6iufv.png).
  

  Mobile: 

<img width="50%" src="https://res.cloudinary.com/www-madine-se/image/upload/v1595196811/vegansite/readme/final%20mockups/iPhone_XR-XS_Max_1_2x_e8m5td.png"> 

Footer:

<img width="50%" src="https://res.cloudinary.com/www-madine-se/image/upload/v1595196811/vegansite/readme/final%20mockups/iPhone_XR-XS_Max_2_2x_vpm1ye.png"> 

[Toggled navbar](https://res.cloudinary.com/www-madine-se/image/upload/v1595196811/vegansite/readme/final%20mockups/iPhone_XR-XS_Max_3_2x_j8xizg.png)

As I mentioned above, I did not find the need to create extensive wireframes/mockups, because the design follows the same pattern.

#### Color Palette

I kept the color pallette very simple and clean because the content of the page is inevitably very colorful.

![Color Palette](https://res.cloudinary.com/www-madine-se/image/upload/v1594581862/vegansite/palette-2_bhhqtr.png)

For the navigation, all larger text I used black, Jet grey for secondary information and paragraphs, platinum light grey for background and moss green for accents.

Images I used for design (not recipes) are mostly from Pexels and follow similar convention - neutral background and with fresh, clean coloured food. I used more vibrant greens and ochre tones to energize the page appearance. 

Red is used for warning messages in Login and Signup pages.

### Defensive design

* User is not able to break the site by clicking buttons out of the expected order.
* All forms handle empty input fields by warning the user and not permitting recipe submission.
* Navigating between pages via the back/forward buttons does not break the site. 
* User errors do not cause database errors
* User is given feedback for actions/errors


## Features
### Notes
* Admin features will not be available publicly for security reasons. Admin is able to browse, edit and delete all recipes.
* I had accidentaly commited MongoDB URI - fixed and changed password.
* I did not find the need to use more JavaScript for this project, except I would like to implement dynamic input fields but that is a future feature.

### Existing features

- [x] Search: users are able to search for recipes by username, title or any other text. If no results are found message "No results found. Please try again".
- [x] Sorting by category by clicking navigation links.
- [x] Acess Shop page with in Navbar or Footer
- [x] Index page greets the user with an inspiring jumbotron
- [x] Ads for shop are scattered across the pages
- [x] Index page features curated recipes
- [x] Signup
- [x] Login
- [x] Sign up for a weekly newsletter
- [x] Access to user profile with all users recipes
- [x] If user has not posted anything yet, the page title reads "Nothing here yet" and has "SUMBIT RECIPE" button. 
- [x] Whenever user has logged in user is greeted with a 5 second flash welcome message
- [x] When user is first registerd user is greeted with 5 second "Signup Successful" flashed message.
- [x] Profile page displays username in banner
- [x] Thank you page with a "Back Home" button that appears after user has edited or submitted a recipe
- [x] Only registered and logged in users allowed to sumbit/edit and delete recipes.
- [x] Only user that posted the recipe or admin can delete and/or edit it.
- [x] Social icons with links in the page footer
- [x] Recipes displayed in list have title, description, cooking time and user information
- [x] Single recipe page have full recipe information, the date and time it was first created, image and list.
- [x] Single recipe page displays tips only if they have been defined. All other fields are required.
- [x] Submit recipe and edit recipe forms have clear instructions and character limits for certain fields. 
- [x] If password is too short or email is invalid etc tooltip appears
- [x] Favicon
- [x] Bootstrap input field validation

### Future features

- [ ] Pagination
- [ ] Google login 
- [ ] Lazy loading images 
- [ ] Prevent duplicate subscribers
- [ ] "Remember me" signup checkbox
- [ ] Edit user profiles
- [ ] User profiles with description, avatar, post list
- [ ] Ability to click on other user profiles and see recipes they posted
- [ ] Page loading animation
- [ ] Third party search engine
- [ ] Subscription letters
- [ ] Filter emails so that there are no duplicates for subscription letters
- [ ] Admin console
 - [ ] Contact form and admin to be able to see all recieved messages directly in the admin console
- [ ] Recipe image url validation
- [ ] Admin recipe review to either accept or reject recipe for it to be public.
- [ ] More categories
- [ ] Admin able to add/edit/delete categories
- [ ] Sort recipes by tag, cousine, cook or prep time, even more specific dietary needs
- [ ] Nutrition calculations
- [ ] Server side credential validation
- [ ] SSL certificate
- [ ] Recipe Comments

### Information Architecture
MongoDB Atlas is used for storing data for this web site.

Current schema: 

![Schema](https://res.cloudinary.com/www-madine-se/image/upload/v1595169619/vegansite/readme/Screenshot_2020-07-19_at_16.40.03_qdsabq.png)

Other file versions - 
[.txt](https://res.cloudinary.com/www-madine-se/raw/upload/v1595169852/vegansite/readme/schema_eqzj7h.txt),
[.pdf](https://res.cloudinary.com/www-madine-se/image/upload/v1595169899/vegansite/readme/QuickDBD-Free_Diagram_bfo0kv.pdf).

And what it [should be ](https://res.cloudinary.com/www-madine-se/image/upload/v1595169338/vegansite/readme/Screenshot_2020-07-19_at_16.16.21_lccftm.png)in a real world project.

For the needs of this website I did not find the need to use other data types in MongoDB. In a real world application I would add image file uploads, dynamic input fields and rich text editing.

Subscriber collection is currently not connected to anything else because that is a future feature.

## Technologies used

Below are a list of the programming languages, technologies, frameworks and resources used for this website.

* HTML5
* CSS3
* jQuery
* Python 3.8.2
    * Flask
    * Jinja 
    * Werkzeug security
* MongoDB and MongoDB Compass
* Bootstrap CDN
* Visual Studio Code
    * Live Server Extension
    * Color Picker Extension
    * Markdown Preview Extension
* Git & GitHub.com
* Heroku.com pages
* Markdown
* FontAwesome.com
* Google Fonts
* Adobe Fonts
* Google Chrome Developer tools
* Firefox Developer tools
* Safari Web Inspector
* Adobe Suite CC
* Cloudinary.com to store all images
* Favicon.io convert favicon
* EZGIF to convert demo video to gif

## Testing
Devices and platforms used for testing:

* Iphone X 
    - Safari
    - Chrome
    - Brave
* Ipad Pro 12.9" 2018
    - Safari 
    - Chrome
* MacBook Pro 13" MacOS Catalina
    - Safari 
    - Chrome
    - Firefox
* MacBook Pro 13" Windows 10
    - Chrome
    - Firefox
    - Microsoft Edge
* OnePlus 5T
    - Firefox
    - Chrome
* Windows 7
    - Chrome
    - Firefox
* Huawei P20 Pro
    - Chrome

### Validators and linters

* [W3C HTML Validator](https://validator.w3.org/#validate_by_input) Passed tests without issues
* [W3C CSS Validator](https://jigsaw.w3.org/css-validator/#validate_by_input)
Passed tests without issues
* CSS Lint VSCode extension
* [JSHint](https://jshint.com) Passed tests without issues
* JSHint VSCode extension
* [PEP8](http://pep8online.com) and AUTOPEP8. Online PEP8 warns about lines being too long but when I attempted to fix that, AUTOPEP8 would break the code, otherwise no issues.

### Manual testing

I extensively tested the page on laptop, mobile and iPad Pro 13" tablet after every major development test. I use VSCode Live Sever extension and autosave to speed up the process, force refreshed the page in Chrome, Firefox and used Private Window on Safari.

Extensively used Crome Developer tools to test form submissions through network tab etc.

Used lots of `print()` to test python code.

1. Visiting page
    * Test if navigation bar works correctly on phone, tablet and desktop browsers
    * Test if page is responsive at all sizes
    * Test footer social icon links (links open homepages in a new window)
    * Attempt accessing non-existant endpoints:

        <img src="https://res.cloudinary.com/www-madine-se/image/upload/v1595190178/vegansite/readme/Screenshot_2020-07-19_at_22.22.51_w6ow8y.png" alt="404 error" width="400"/>

        Correctly returns 404.html with access to go back to homepage
    * Verify that shop page looks as it should.
    * Press Subscribe for newsletter button - redirects to footer form
    * Try submitting empty form or invalid email (shows tooltip "Enter an email adress")
2. Sign Up
    * Try registering with empty form/inputs (shows tooltip "Fill out this field")
    * Try to register with invalid email ("Enter an email adress")
    * Attempt to use username/password that is too long or too short ("Match the requested format!")
3. Login 
    * Try using empty form (shows tooltip "Fill out this field")
    * Try to use not existing or wrong credentials ("Incorrect Username and/or Password!")
4. Submit recipe
    * Go to the "Submit Recipe" page
    * Try to submit empty form and verify that no recipe has been added to any category page.
    * Try to submit filled out form and verify that fields appear correctly, there is no missing information
    * Try to submit recipe with empty fields
5. Edit recipe
    * Try to submit recipe with empty fields
    * Test edit button, submit edit button
    * Check if changes have been made and displayed correctly
6. Delete recipe
    * Visit recently posted recipe and try the Delete button
    * Delete button opens a modal:

    <img src="https://res.cloudinary.com/www-madine-se/image/upload/v1595189947/vegansite/readme/Screenshot_2020-07-19_at_22.18.56_kmxqv1.png" alt="delete button" width="400"/>

    * Test cancel button 
    * Test delete button 
    * Verify that recipe has been deleted
7. Logout
    * Log out
    * Test accessing pages available only for logged in users e.g. profile page or thank you page (Wraps redirects to Login page)
8. Search
    * Search a recipe by ingredient or title 
    * If no recipes are found, user is notified "No results found. Please try again"

    Note: search does not return results for words like "and", "if", "other", "after"

I wanted to try PyTest automated testing, got sample to run and work but decided not to write tests due to time constraints.

### Errors

Most of the errors I encountered along the way were simply syntax mistakes.

Something I had done or installed had set .vscode/launch.json to `"--no-debugger"` that set flask to production mode. Fixed that by commenting out that line. 

These are current issues:

* In profile page viewed from [Safari](https://res.cloudinary.com/www-madine-se/image/upload/v1595179660/vegansite/readme/Screenshot_2020-07-19_at_19.27.33_tvrhjr.png) some CSS does not apply, but is not important enough to correct right now.  Correct styling from [Chrome](https://res.cloudinary.com/www-madine-se/image/upload/v1595179678/vegansite/readme/Screenshot_2020-07-19_at_19.27.23_t5uuet.png)
* When searching for recipe title "Easy Baked Beans", search returns not the most relevant results. I would use a third party search engine for the next project.
* Is it a bug or feature?! When searching for words like "and, or, if" etc search returns no results. 
* Images don't load smoothly and at the same time, because they come from many different sources. I would like to use lazy loading (didn't have the time).
* After submitting recipe and using browser back button and forward, same recipe can be submitted several times.

* Bootstrap tooltip from mobile Safari on Iphone X

    <img src="https://res.cloudinary.com/www-madine-se/image/upload/v1595190726/vegansite/readme/IMG_2972_mim2tv.png" alt="broken" width="400"/> 

I did not change styling of that and it displays correctly on all other browser/device.

* If image is posted with broken link, it looks exacly like that - broken and sad:

    <img src="https://res.cloudinary.com/www-madine-se/image/upload/v1595188923/vegansite/readme/Screenshot_2020-07-19_at_22.01.56_rzvsbf.png" alt="broken" width="300"/>

I would have liked to implement submission verification and/or have a placeholder image instead.

## Deployment

This project can be ran locally by following the following steps: 
(Steps may differ in GitPod/Windows/Linux. I used Visual Studio Code on MacOS)

Create a free account on Cloudinary.com download my media or create your own.

Visit this [repository link](https://github.com/sabinemm/recipe-site-ms3.git) and click on the Clone or Download button to copy the link provided.

![clone](https://res.cloudinary.com/www-madine-se/image/upload/v1594582454/vegansite/Screenshot_2020-07-12_at_21.33.47_k4rvyg.png)

In your IDE, open a Terminal window and change to the directory where you want to clone this [repository](https://github.com/sabinemm/recipe-site-ms3.git) and type:

for macOS:
```
$ cd /Users/user/my_project
```
for Windows:
```
$ cd C:/Users/user/my_project
```
and type:
```
$ git init
```

```
$ git clone https://github.com/sabinemm/recipe-site-ms3.git
```
After pressing Enter the project will be created and cloned locally.

(Alternatively you can download the zipped file, decompress it and use your IDE of choice to access it.)

Create a free account on MongoDb and reproduce the 4 collections as described [here](#Information-Architecture).

Make sure to upgrade PIP. 
```
$ pip install -U pip 
```

Install all dependencies
```
$ pip3 install -r requirements.txt
```
Activate virtual environment 
```
$ source env/bin/activate
```
Create .env file with following data
```
MONGO_URI=mongodb+srv://...
SECRET_KEY=superdupersecretkey
```
Add your .env file to .gitignore

In the last line of app.py file change from `debug=False` to `debug=True`

You will then be able to run the app locally by typing `python app.py` or  `flask run`. 

### Heroku

Heroku was chosen as the deployment platform for this project. The steps to deploy the local app to Heroku were as follow:

In Heroku, create an app. The app must have a unique name.

Link that app to the GitHub repository by going to the "Deploy" tab in the main app menu.

In the Settings tab, add the corresponding Config Variables as present in local development:

```
MONGO_URI mongodb+srv://...
IP 0.0.0.0
PORT 5000
SECRET_KEY superdupersecretkey
```

Created "Procfile" by typing:
```
$ echo web: python app.py > Procfile
```
Push repo to Heroku
```
$ git push heroku master
```
After these steps the app is live and running remotely in Heroku's servers.

## Credits
### Code
* [Datetime](https://www.programiz.com/python-programming/datetime/current-datetime) (submission date and time)

* [Login](https://startbootstrap.com/snippets/login/), [Login2](https://realpython.com/introduction-to-flask-part-2-creating-a-login-page/),  
[Sign up](https://github.com/TravelTimN/flask-task-manager-project/blob/master/app.py), [Password Hash](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-v-user-logins), [How to store passwords securely using Werkzeug](https://techmonger.github.io/4/secure-passwords-werkzeug/)

* [Flash](https://pythonprogramming.net/flash-flask-tutorial/), [Dissapearing message](https://stackoverflow.com/questions/1911290/make-div-text-disappear-after-5-seconds-using-jquery), [Message flashing](https://flask.palletsprojects.com/en/1.1.x/patterns/flashing/)

* [Back to top](http://www.voidynullness.net/blog/2015/05/29/jquery-smooth-scrolling-floating-scroll-to-top-button/)

* [Overlay title](https://www.w3schools.com/howto/howto_css_image_overlay_title.asp)

* And loads of tiny snippets from Stack Overflow,  Google, MongoDB documentation, W3Schools and CSS Tricks

### Images

* Backgrounds: [Vegetable fritatta](https://www.crowdedkitchen.com/spring-vegetable-frittata-vegan/), [Thyme](https://www.pexels.com/photo/close-up-photo-of-thyme-leaves-4113901/), [Almonds](https://www.pexels.com/photo/white-table-with-tasty-scattered-almonds-4033328/), [Papaya](https://www.pexels.com/photo/sliced-lemon-and-black-berries-on-white-surface-4113798/), [Asparagus](https://www.pexels.com/photo/fresh-ripe-asparagus-pods-in-bunch-4033003/)

* Ad: [Book](https://unsplash.com/photos/CXYPfveiuis), [Oranges](https://unsplash.com/photos/S3_D7Q9vz0Y), [Book 2](https://www.pexels.com/photo/white-book-near-food-on-plate-2237798/)

* [Demo](https://www.freepik.com/free-psd/set-digital-devices-screen-mockup_3766951.htm#query=mockup-computer&position=0) for video and [Static](https://www.freepik.com/free-photo/laptop-coffee-cup-mobile-phone-cake-white-background_3317839.htm#page=1&query=mockup)

* Recipes: [Melon Smoothie](https://www.pexels.com/photo/photo-of-glasses-near-sliced-melon-4051452/)

### Content 

* [Terms](https://www.termsandconditionsgenerator.com/)
* Recipes taken from various websites, some of them linked in the Tips section.

## Acknowledgements
A thanks to my mentor [Maranatha Ilesanmi](https://github.com/mbilesanmi), Code Institute Tutor support (especially [
Tim Nelson](https://github.com/TravelTimN) for login and tips), Slack, my friend Reinis for explaining Python and debugging to me

## Disclaimer

If there are any issues with copyright of content, please contact me. I will fix that as soon as possible. 

This project is for educational purposes only.

Sabine Madara 

2020

[Back to top ↑](#Vegan-Minus-Gluten)