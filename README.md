
# Book store api
 An online bookstore system to provide users with an enhanced shopping experience using JWT

 A online bookstore system with having these key features

 1.User Registration and Authentication:
 The singleton design pattern is a creational pattern that ensures that only one instance of a class can be created and provides a global point of access to that instance. The purpose of this pattern is to guarantee that a class has only one instance and to provide a way to access it.define a MySingleton class that uses a static instance property to ensure that only one instance of the class can be created. If the instance doesn’t already exist, the constructor creates it and sets the instance property to the new instance.


 2.Book Catalog Management
our code runs on different devices and depending on the device type we want to use class that supports particular capabilities. This is the place where we take advantage of factory design pattern.

const mongoose = require('mongoose')

class Books {
	static saved() { return "hello "; }
}
	
const schema = new mongoose.Schema();
schema.loadClass(books);
 

const book = require('../models/Book');
const savedbook = book.saved();

 ![Car and Driver Class Diagram](https://github.com/nike541/bookstoreapi/assets/70380310/2e969ed3-d9f8-4c61-a4c3-fb5a65e0350d)


 3.Shopping Cart
The Command Pattern involves creating objects that represent actions or operations, allowing you to separate the execution of these actions from their implementation. This pattern promotes the decoupling of the object that invokes the action from the object that performs it.By using the Command Pattern, we can easily extend the class's functionality without modifying its implementation, adhering to the Open/Closed Principle.


 4.Order Management
user wants to order online and get it delivered and the service running at the backend needs to handle the various stages that can be there during the entire process from order initiation and order placing to the final delivery of the order.

5.Payment Integration
 To integrate a payment gateway into your application. The payment gateway has its own set of APIs and interfaces, but your application has its own structure and set of APIs. To integrate the payment gateway into your application, you can use the adapter pattern.
 you need to create an adapter class that will convert the interface of the payment gateway into the interface that your application expects. The adapter class has a method called processPayment that takes the payment amount as an argument and converts it into the payment details that the payment gateway expects. The adapter class then calls the payment gateway's charge method with the payment details and returns the result.

6. Advanced Search and Filtering: Search and filter options are available in api where url will be in given format api/books?genre=<name> ,  api/books?new=true . In this way you can search the data in apis and render data to frontend

   
## Tech Stack
**Server:** Node, Express, postman ,Docker


## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`MONGO_URL` = mongodb+srv://nikhilprakash1911:12345@cluster0.2r6luje.mongodb.net/

`PASS_SEC` = nikhi

`JWT_SEC` = nikhi

`STRIPE_KEY`=sk_test_51Np5kDSIBvoqIWAZhBECxfX7FtH6l3nn2Mdto5MVGp6bWS5xjwLg0RrUVAiufFb6H3xs1nO55aUCO1OTEOooS2jw00WUz9xpnj


## Deployment

To deploy this project run
git clone the repo
add .env file

run the docker composefile

```bash
  docker compose up
```


## Documentation

postman collection is here 

Here is the testing document ,reponses are not documented

## 🔗 Links
[postman-collection](https://documenter.getpostman.com/view/29652722/2s9YC2zZK6)



## Run Locally

Clone the project

```bash
  git clone https://link-to-project
```

Go to the project directory

```bash
  cd my-project
```

Install dependencies

```bash
  npm install
```

*add .env file


Start the server

```bash
  npm start
```


## Optimizations can be made
Incorporate Natural language processing
Natural Language Processing (NLP) is a layer of AI search. It focuses on understanding the complexity of human language by adding structure and meaning to unstructured data. In the context of e-commerce search, NLP helps extract the necessary information to provide the most suitable products to the input queries.

Search filters are a powerful tool for searchers to streamline product discovery. By selecting specific filters, customers can tailor their search to their preferences, making it easier for them to find the products that meet their needs
## API Reference

#### POST register

```http
  POST /api/auth/register
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `name` | `string`    | **Required**.  |
   `email` | `string`  | **Required**.  |
 ` password` | `string`  | **Required**.  |


#### POST login

```http
  POST /api/auth/login
```
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `name` | `string`    | **Required**.  |
   `email` | `string`  | **Required**.  |
 ` password` | `string`  | **Required**.  |

Takes two numbers and returns the sum.

