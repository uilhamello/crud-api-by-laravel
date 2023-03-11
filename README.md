API is the acronym for application programming interface, a software intermediary that allows two applications to talk to each other. APIs are an accessible way to extract and share data within and across organizations.

web programming languages have features to ease the mundane processes of creating an API, as well as frameworks that make that job even easier.

In this repository we will use Laravel 8, a PHP framework.

We are going to create a application that manages products in stock:

Create product;
Update product;
Delete product;


For this we gonna following these steps:

Creation Product Model;

Creation Product Controller;

creation of Routes;

Tests;

Let's get to work at! :star_struck:


Laravel cames with a command-line interface called Artisan, witch makes easy to creates the project structure. Let's use it to create our Model, Migration and Controller.

Criando Model, Migration and Controller by Artisan

```php
php artisan make:model Product -mc --api
```

The above command has create three file for us:


Product.php




