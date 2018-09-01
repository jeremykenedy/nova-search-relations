# Search relationships in Laravel Nova

This package allow you to include relationship columns into Laravel Nova search query.

## Screenshot

![screenshot of the search relations tool](./screenshot.png)

## Installation

```
composer require titasgailius/search-relations
```

Next, add `Titasgailius\SearchRelations\SearchesRelations` trait to your base resource class `App\Nova\Resource`
```php
use Titasgailius\SearchRelations\SearchesRelations;

abstract class Resource extends NovaResource
{
    use SearchesRelations;
```

## Usage

Simply add `public static $searchRelations` array to any of your Nova resources.
This array has a relationship name as a key and an array of columns to search for as a value.
```php
/**
 * The relationship columns that should be searched.
 *
 * @var array
 */
public static $searchRelations = [
    'user' => ['username', 'email'],
];
```
