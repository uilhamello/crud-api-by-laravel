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

1 - First Step

Criando Model, Migration and Controller by Artisan

```php
php artisan make:model Product -mc --api
```

The above command has create three file for us:

Product Model File
app/Models/
Product.php

This is the file that create a object to relate with the database table Product, that one we are going at the next step.

Product Migration File
/database/migrations
[current datatime]_create_products_table.php

This file is going to create a object map of Product Table.
In this file we are going to work soon, to genarate the table Product on are database.

Product Controller File
/app/Http/ProductController
Here is where we are going to fill with the actions for each route

Great! Until now we just have to execute one command-line and it has done a big percent of our job.


2 - Second Step

Creating the routes:

Open the file routes/api.php. 
Here is where we are going to create the routes to access the Controller Methods.

For routes:

GET /api/index = it will acess the ProductController index()
POST /api/store = it will access the ProductController store()
GET /api/show/{id} = it will access the ProductController show(Product id)
PUT /api/update/{id} = it will acess the ProductController update(Product id)
DELETE /api/destroy/{id} = it will acess the ProductController destroy(Product id)

Since we are creating inside the api.php, it understand that our route has the 'api/' prefixed to the method on our route, so we don't need to add it, just the name after "api/".

Creating the routs on api.php:


Product.index =  Display a listing of the resource.
´´´php
Route::get('index', [ProductController::class, 'index']);
´´´

Product.store =  Store a newly created resource in storage.
´´´php
Route::post('store', [ProductController::class, 'store']);
´´´

Product.show = Display the specified resource.
´´´php
Route::post('show/{id}', [ProductController::class, 'show']);
´´´

Product.update = update the specified resouce in storage.
´´´php
Route::post('store/{id}', [ProductController::class, 'store']);
´´´
