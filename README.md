
# Laravel API Docs Generator

This Laravel package provides an API Documentation generator based upon your Routes and Controller Method DocBlocks.

- `apidocs:generate api/v1`


######NOTES:

You must prefix your route with an API Version.  i.e. 'api/v1

    Route::group(['prefix' => 'api/v1'], function(){

    });

#####DocBlock Example
    /**
    * Display the specified resource.
    * GET /user/{id}
    *
    * @param  int  $id  The id of the User
    * @return Response
    */
    public function show($id)
    {
    // Display User
    }

## Installation

#### Laravel 4.2 and Below

Begin by installing this package through Composer. Edit your project's `composer.json` file to require `f2m2/apidocs`.

    "require-dev": {
    "f2m2/apidocs": "~1.0"
    }

Next, update Composer from the Terminal:

composer update --dev

Once the packaage has installed, the final step is to add the service provider. Open `app/config/app.php`, and add a new item to the providers array.

    'F2m2\Apidocs\ApidocsServiceProvider',

Run the `artisan` command from the Terminal to see the new `apidocs` command.

    php artisan apidocs:generate


Create a copy of the API Docs Config by running this `artisan` command:

    php artisan config:publish f2m2/apidocs


License
-------

See [LICENSE](LICENSE) file.

