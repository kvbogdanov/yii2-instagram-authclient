# yii2-instagram-authclient

This extension adds Instagram OAuth2 supporting for [yii2-authclient](https://github.com/yiisoft/yii2-authclient).

## Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist kvbogdanov/yii2-instagram-authclient "*"
```

or add

```json
"kvbogdanov/yii2-instagram-authclient": "*"
```

to the `require` section of your composer.json.

## Usage

You must read the yii2-authclient [docs](https://github.com/yiisoft/yii2/blob/master/docs/guide/security-auth-clients.md)

Register your application [in Instagram](http://instagram.com/developer/clients/register)

and add the Instagram client to your auth clients.

```php
'components' => [
    'authClientCollection' => [
        'class' => 'yii\authclient\Collection',
        'clients' => [
            'instagram' => [
                'class' => 'kvbogdanov\authclient\Instagram',
                'clientId' => 'instagram_client_id',
                'clientSecret' => 'instagram_client_secret',
            ],
            // other clients
        ],
    ],
    // ...
 ]
 ```
