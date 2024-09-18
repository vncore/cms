<p align="center">
    <img src="https://vncore.net/logo.png" width="150">
</p>
<p align="center">Free CMS source code built with Laravel for your system<br>
    <code><b>composer create-project vncore/cms</b></code></p>


<p align="center">
<a href="https://packagist.org/packages/vncore/cms"><img src="https://poser.pugx.org/vncore/cms/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/vncore/cms"><img src="https://poser.pugx.org/vncore/cms/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/vncore/cms"><img src="https://poser.pugx.org/vncore/cms/license.svg" alt="License"></a>
</p>

## About Vncore CMS
- Vncore CMS makes it easy for you to build a website for your business. 
- Vncore CMS is a complete system, combining `Vncore/front` and `Vncore/core`.

**What can Vncore CMS do?**

- Fully inherits the power and convenience of `Vncore/core`.
- Plugins will be continuously updated.
- Vncore is FREE

**And more:**

- Vncore builds a large, open ecosystem (plugin, template), helping users quickly build CMS, PMO, eCommerce, etc., according to your needs.

<p align="center">
    <img src="https://vncore.net/images/vncore-screen.jpg" width="100%">
</p>

## Laravel core:

Vncore 1.x

> Core laravel framework 11.x 


## Website structure using Vncore

    Website-folder/
    |
    ├── app
    │     └── Vncore
    │           ├── Core(+) //Customize controller core
    │           ├── Blocks(+)
    │           ├── Helpers(+)
    │           ├── Templates(+)
    │           └── Plugins(+)
    ├── public
    │     └── Vncore
    │           ├── Admin(+)
    │           ├── Templates(+)
    │           └── Plugins(+)
    ├── resources
    │            └── views/vendor
    │                           └── vncore-admin(+) //Customize view admin
    ├── vendor
    │     └── vncore/core
    ├── .env
    └──...

## Support the project
Support this project :stuck_out_tongue_winking_eye: :pray:
<p align="center">
    <a href="https://www.paypal.me/LeLanh" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-green.svg" data-origin="https://img.shields.io/badge/Donate-PayPal-green.svg" alt="PayPal Me"></a>
</p>

## Quick Installation Guide

**Initialize vncore cms**

  Run the command: 
  >`php artisan vncore:install`


## Useful information:

**To view Vncore version**

>`php artisan vncore:info`

**Update vncore**

Update the package using the command: 
>`composer update vncore/core`

Then, run the command: 

>`php artisan vncore:update`

**To create a plugin:**

>`php artisan vncore:make plugin  --name=PluginName`

To create a zip file plugin:

>`php artisan vncore:make plugin  --name=PluginName --download=1`

**To create a template:**

>`php artisan vncore:make template  --name=TemplateName`

To create a zip file template:

>`php artisan vncore:make template  --name=TemplateName --download=1`

## Customize

**Customize vncore-config and functions**

>`php artisan vncore:customize config`

**Customize view admin**

>`php artisan vncore:customize view`

**Overwrite vncore_* helper functions**

>Step 1: Use the command `php artisan vncore:customize config` to copy the file `app/config/vncore_functions_except.php`

>Step 2: Add the list of functions you want to override to `vncore_functions_except.php`

>Step 3: Create a new function in the `app/Vncore/Helpers folder`

**Overwrite vncore controller files**

>Step 1: Copy the controller files you want to override in vendor/vncore/core/src/Admin/Controllers -> app/Vncore/Core/Admin/Controllers

>Step 2: Change `namespace Vncore\Core\Admin\Controllers` to `namespace App\Vncore\Core\Admin\Controllers`

**Overwrite vncore API controller files**

>Step 1: Copy the controller files you want to override in vendor vendor/vncore/core/src/Api/Controllers ->  app/Vncore/Core/Api/Controllers

>Step 2: Change `namespace Vncore\Core\Api\Controllers` to `namespace App\Vncore\Core\Api\Controllers`

## Add route

Use prefix and middleware constants `VNCORE_ADMIN_PREFIX`, `VNCORE_ADMIN_MIDDLEWARE` in route declaration.

References: https://github.com/vncore/core/blob/master/src/Admin/routes.php



## Environment variables in .env file

**Quickly disable Vncore and plugins**
> `VNCORE_ACTIVE=1` // To disable, set value 0

**Disable APIs**
> `VNCORE_API_MODE=1` // To disable, set value 0

**Data table prefixes**
> `VNCORE_DB_PREFIX=vncore_` //Cannot change after install vncore

**Path prefix to admin**
> `VNCORE_ADMIN_PREFIX=vncore_admin`

