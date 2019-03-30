# DataTable for laravel-admin

**Add advanced interaction controls to your HTML tables** the free & easy way.

#### ScreenShot

<img src="https://user-images.githubusercontent.com/2421068/55276143-0e4ae800-532b-11e9-8031-48d5a575f221.png">

#### Install

```bash
composer install jxlwqq/data-table
php artisan vendor:publish --tag=laravel-admin-data-table
```

## Configurations

Add `extensions` option in your `config/admin.php` configuration file:

```php
'extensions' => [
    'data-table' => [
        // If the value is set to false, this extension will be disabled
        'enable' => true
    ]
]
```

#### Use

```php
use Jxlwqq\DataTable;

// table
$headers = ['Id', 'Email', 'Name', 'Company'];
$rows = [
    [1, 'labore21@yahoo.com', 'Ms. Clotilde Gibson', 'Goodwin-Watsica'],
    [2, 'omnis.in@hotmail.com', 'Allie Kuhic', 'Murphy, Koepp and Morar'],
    [3, 'quia65@hotmail.com', 'Prof. Drew Heller', 'Kihn LLC'],
    [4, 'xet@yahoo.com', 'William Koss', 'Becker-Raynor'],
    [5, 'ipsa.aut@gmail.com', 'Ms. Antonietta Kozey Jr.'],
];

$style = ['table-bordered','table-hover', 'table-striped'];

$optionss = [
    'paging' => true,
    'lengthChange' => false,
    'searching' => false,
    'ordering' => true,
    'info' => true,
    'autoWidth' => false
];

$dataTable = new DataTable($headers, $rows, $style, $options);

echo $dataTable->render();
```

## More resources

[Awesome Laravel-admin](https://github.com/jxlwqq/awesome-laravel-admin)

## License

Licensed under [The MIT License (MIT)](LICENSE).