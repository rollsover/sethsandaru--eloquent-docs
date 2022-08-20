# Eloquent phpDoc Generators

Quickly generate the phpDoc for your Eloquent Model. Make your Eloquent super friendly with IDEs (eg PHPStorm).

And maintaining the phpDoc of your models don't have to be a pain in the ass, should be:

- Fun
- Fast
- Reliable

And, welcome to Eloquent phpDoc Generator, which going to help you to achive the 3 points above 🎉

## Requirements
- PHP 8+ (yes it is 2022, PHP8 is superfast)
- Laravel 9 (tested)
- Laravel 8 (untested but very likely work without any issues)

## Install
Install as dev-dependencies is enough, since you are only going to use this command on `local/development` env.

```bash
composer require sethphat/eloquent-docs --dev
```

Laravel auto-discovery will automatically do the magic for you. So you don't have to worry 😉.

## Use the command

```bash
php artisan eloquent:phpdoc App\Models\User # view only
php artisan eloquent:phpdoc App\Models\User --write # view & write to file
```

Result:

<details>

```bash
====== Start PHPDOC scope of App\Models\User
/**
* Table: users
*
* === Columns ===
* @property int $id
* @property string $name
* @property string $email
* @property \Carbon\Carbon|null|null $email_verified_at
* @property string $password
* @property string|null $remember_token
* @property \Carbon\Carbon|null $created_at
* @property \Carbon\Carbon|null $updated_at
*
* === Relationships ===
* @property-read \App\Models\Emails[]|\Illuminate\Support\Collection|null $emails
* @property-read \App\Models\UserDetails|null $userDetail
*
* === Accessors/Attributes ===
* @property-read string $full_name
* @property-read string $is_admin
* @property-read string $user_type
* @property-read int $total_salary
* @property-read mixed $levels
* @property-read mixed $first_name
* @property-read mixed $last_name
*/
====== End PHPDOC scope of App\Models\User
Wrote phpDoc scope to /<my-path>/app/Models/User.php
Thank you for using SethPhat/EloquentDocs!
```

</details>

Note: if you haven't installed `doctrine/dbal` as your dev-dependency, 
then once you trigger the command for the first time, it will help you to install the needful dependency

## Release logs
- v1.0.0
  - First version
  - View & Update phpDoc for a single Model at a time
- v1.1.0 (planned)
  - Bulk replace by namespace

## Contribute to the library

Feel free to fork this library and sending a PR here.

Note: all the contributions need to follow PSR-12 and add unit testing.

## LICENSE

MIT License

## 