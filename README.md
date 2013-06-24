# Laravel-Bundle-Constant #
=======================

Prepare constant options for select drop down for date, month and year in Laravel. Many times we may need to put in the drop down for date, month and year in a select option. This is a helper to produce the options with jus a line of code. 


## Configuration ##

Place this bundle in the bundles directory. Then config the constant bundle in the bundles.php.

```php
'constant' => array('auto' => true),
```

## Usage ##

###### Constant::day(); ######

```php
{{ Form::select('date', Constant::day()); }}
// <select name='date'> 
// <option value="01">01</option>
// ...
// </select>
```

###### #Constant::month(); ######

```php
{{ Form::select('month', Constant::month()); }}
// <select name='month'> 
// <option value="1">Jan</option>
// ...
// </select>
```

###### #Constant::month_alpha(); ######

```php
{{ Form::select('month', Constant::month_alpha()); }}
// <select name='month'> 
// <option value="Jan">Jan</option>
// ...
// </select>
```

###### #Constant::month_numbers(); ######

```php
{{ Form::select('month', Constant::month_numbers()); }}
// <select name='month'> 
// <option value="01">01</option>
// ...
// </select>
```

###### #Constant::month_numbers(); 

```php
{{ Form::select('year', Constant::year()); }}
// <select name='year'> 
// <option value="2010">2010</option>
// ...
// </select>
```

By default, you will have 3 options in the year option. 

```php
<selectname="year">
	<option value="2011">2011</option>
	<option value="2012">2012</option>
	<option value="2013">2013</option>
</select>
```

You can specify the number of options you want (going backward).
```php
{{ Form::select('year', Constant::year(10)); }}
// This year is 2013. 10 options from 2013, the drop down will begin with 2004.
// <select name='year'> 
// <option value="2004">2004</option>
// ...
// <option value="2013">2013</option>
// </select>
```

