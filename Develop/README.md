# e-commerce backend app

## Licensing:
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)<br>
<h3>Apache 2.0</h3>
TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

    1. Definitions.
    
    "License" shall mean the terms and conditions for use, reproduction, and distribution as defined by Sections 1 through 9 of this document.
    
    "Licensor" shall mean the copyright owner or entity authorized by the copyright owner that is granting the License.


## Table of Contents
- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Contribution](#contribution)
- [Testing](#testing)
- [Additional Info](#additional-info)

## Description:
I wanted to make a backend app that furthered my understanding of MVC without the view. This includes creating a class/model and controllers/routes.
I built this app to better my understanding of the backend of applications and how servers, databases, routes all talk to each other.
This app gave me a better understanding of the backend of applications
I learned models, controllers, databases and how to interact with them

* Link to video of using app in insomnia 
https://drive.google.com/file/d/1ou4QVwnbSYBFBqUgAWdDeu1Ps2LPtlAq/view?usp=sharing

<img src="./img/terminal.png" alt="terminal interactions with insomnia while using app">

* routing
```
router.post('/', async (req, res) => {
  // create a new category
  try {
    const categoryData = await Category.create(req.body);
    res.status(200).json(categoryData);
  } catch (err) {
    res.status(400).json(err);
  }
});
```

* Modelling and creating relationships
```
// Categories have many Products
Category.hasMany(Product, {
  foreignKey: 'category_id',
})

// Products belongsTo Category
Product.belongsTo(Category, {
  foreignKey: 'category_id',
})
```

## Installation:
You must use an npm install to get the dependencies and use your database login information to correctly start and seed into the database.

## Usage:
You will need to run the database and seed into it via the terminal. To interact with the backend you will need to use insomnia or similar app.

## Contribution:
Contribute via pull requests on github

## Testing:
No tests for this project

## Additional Info
- Github: [stewsabatino](https://github.com/stewsabatino)
- Email: stewsabatino@gmail.com

  