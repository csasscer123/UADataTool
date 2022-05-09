# Urban Agriculture Data Tool
The Urban Agriculture Data Tool is a project that aims to centralize and display data on the small and medium-scale urban agriculture operations in Prince George’s County. It currently consists of a website that allows farm registration and allows users to search for farms based on certain search parameters. This website is hosted on heroku and can be accessed [here](https://team-go-green.herokuapp.com/). The data displayed on this website is stored on a MySQL database which is also hosted through Heroku using ClearDB

## Developer Manual
### How to Install the Application and all Node Module Dependencies
1. Clone the [Repository](https://github.com/KamranDjourshari24/490DataTool) via GitHub Desktop or the Terminal of your OS
2. Open the directory, where the repository is stored, in VSCode's Terminal or your OS's Terminal
3. Run ```npm install```

### How to Run the Application Locally
1. Open the directory, where the repository is stored, in VSCode's Terminal or your OS's terminal
2. Run ```npm start```
3. In your desired web browser, enter the following URL to view the Application: `http://localhost:3000/`

### API Endpoints
```/api/urbanfarms```
```/api/urbanfarms/:farm_name```
```/api/farms_products```
```/api/farms_products/:farm_name```
```/api/products```
```/api/owners```
```/api/thirdPartyAPI```



## Website
This website allows farms to register and create a customized profile that will display easily accessible information about their operation such as their location, what products they are producing and in what quantities, and a link to their website if they have one. This data is searchable based on the data in their profile and focuses on giving users a list of the farms closest to them meeting their search parameters. The website is built primarily through JavaScript, HTML, and CSS, and uses Bulma and Bootstrap frameworks. Maps are built using MapBox


### Home Page
This page is the first page that the user will land on. There is a slideshow at the top that cycles through different articles about urban agriculture, so a user who wants to learn more has access to resources that may be useful to them. Under this slideshow is the featured farms, which are a randomized set of 3 farms in order to give them exposure on the front page. Lastly, below that is the mission statement, which reflects the mission of the Prince George’s County University of Maryland Extension.


### Search Page
This page can be accessed by clicking “Search” on the navigation bar. It contains a map and search fields where a user can enter whatever they want to search for. Currently they can search by farm name, city, or zipcode, or all 3. Any field can be left out of the search if needed. Once the “Submit” button is pressed, farms will show up that match the search, and these farms will also show up on the map.

### Details
If a user were to click on “Learn more” on any of the farms, they will be taken to the details page of that farm. This page contains more information  about the farm not shown on the search page such as contact and product information. It also provides a gallery of images provided by the owner of the farms account. 

### Registration
The registration page allows for a user to potentially sign up for an account, where they will input information about their farm. This page as of right now allows for data to be inputted and sent to the database so the farm can show up on the website, but the account itself will not be created. 

### Profile
When a user is logged in, the profile will be where the user can see and edit their information. This page is similar to the details page and also leads to the inventory page.

### Inventory
This page acts as an inventory management system for the farm. Here they can edit the amount of the product they have in stock, how that product is measured, and if that product is in stock or not. 

### Contact Us
Here, a user can enter their contact information and put in a comment or concern. This will be sent to the email of whoever is managing the website so they can view user concerns/feedback.

## Database
The database used to hold information for this project is a MySQL relational database and is hosted on Heroku using ClearDB. This database is meant to contain data about each farm as well as the products that each farm provides.


### Features
The database contains 4 tables that hold information regarding farms on the website
* Urban_farms
    * Holds general information on the farm as a whole. Generally, this is information that is shown on the details page
* Owner
    * Holds information about the owner of the account including username and password
* Farms_products
    * Holds information about products on each farm
* Products
    * Holds information about all products that exist on the website

### Altering Data
Changing the data in the database should be done primarily on the website. However, if you need to go directly in the database to change any data, you can log in to the database on MySQL Workbench. Through the SQL programming language, one would be able to manipulate the data. However, these changes are permanent so please be very cautious with any changes. 

### Backing-up Data
Having a back-up of the data is important as a failsafe just in case anything goes wrong with the database. Backups should be made periodically as new data is added. Currently, the only way to back up the database is manually through MySQL.




