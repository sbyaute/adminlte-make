# AdminLTEMaker bundle for Symfony  5

This repository contains AdminLTEMaker bundle which helps you create controller skeletons and templates based on [AdminLTE bundle](https://github.com/kevinpapst/AdminLTEBundle) and [DataTables bundle](https://github.com/omines/datatables-bundle).

Fork from [Pretorien / AdminLTEMaker](https://github.com/pretorien/adminlte-maker) 

Add : 
- Personal templates
- Delete method with token and modal
- Modal option to create CRUD with modal


### Minimum requirements

- Symfony 5.0
- PHP 7.2
- Twig 2.0
- [AdminLTE bundle](https://github.com/kevinpapst/AdminLTEBundle)
- [DataTables bundle](https://github.com/omines/datatables-bundle)

## Installation with Composer

Installation using composer :

```bash
   composer require sbyaute/adminlte-maker
```

Then, enable the bundle by adding it to the list of registered bundles in the `config/bundles.php` file of your project:

```php
<?php

return [
    // ...
    Sbyaute\AdminLTEMakerBundle\AdminLTEMakerBundle::class => ['all' => true],
];
```

## Usage

This bundle provides several commands under the make: namespace. List them all executing this command:

```sh
php bin/console list make:adminlte

make:adminlte:controller  Creates a new controller class
make:adminlte:crud        Creates AdminLTE CRUD for Doctrine entity class
make:adminlte:crudmodal   Creates AdminLTE CRUD (modal mode) for Doctrine entity class
```

## Configuration

This bundle doesn't require any configuration. But, you can configure the base layout and several parameters :

```sh
php bin/console config:dump admin_lte_make

admin_lte_make:
    base_layout:          '@AdminLTE/layout/default-layout.html.twig'
    skeleton_dir:         .../src/DependencyInjection/../Resources/skeleton/
    datatable:
        cdn_css:              'https://cdn.datatables.net/v/dt/jq-3.2.1/dt-1.10.16/datatables.min.css'
        cdn_js:               'https://cdn.datatables.net/v/dt/jq-3.2.1/dt-1.10.16/datatables.min.js'

```

## License and contributors

Published under the MIT, read the [LICENSE](LICENSE) file for more information.