Yii2 validators
===============================================

Collection of useful validators for Yii Framework 2.0

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist yii2mod/yii2-validators "*"
```

or add

```
"yii2mod/yii2-validators": "*"
```

to the require section of your `composer.json` file.

Usage
-----
* **Credit Card Validator**
```php
    public function rules()
    {
        return [
            [['creditCard'], \yii2mod\validators\ECCValidator::className()],
        ];
    }
```

*  **Yii2 phone validator is a validator uses phone number util to validate and format the phone number attribute of model.**
```php
    public function rules()
    {
        return [
            [['phone'], \yii2mod\validators\PhoneValidator::className(), 'country' => 'US'], // OR
            [['phone'], \yii2mod\validators\PhoneValidator::className(), 'countryAttribute' => 'country'], // OR
            [['phone'], \yii2mod\validators\PhoneValidator::className(), 'countryCodeAttribute' => 'countryCode'], 
        ];
    }
```

