**Currently in development**
Development page for the Calendar ProcessWire module. This documentation will 
probably not match PHP Docs in source. 

## Creating the calendar
To create a calendar, simply create a new calendar from the Calendar 
class. Takes no argument.

```php
// Create a calendar
$calendar = new Calendar();
```

## Methods

### Calendar::render()
Renders the calendar. Of course, make sure you have passed all your 
events before calling the render method, otherwise the calendar will be blank.

```php
// Render a calendar for the current month
$calendar->render();
```
```php
// Create a calendar for July 2038
$calendar->render("2038-10-01");

// same as (day isn't required)...
$calendar = new Calendar("2038-10");
```

### Calendar::addEvent()
Adds an event to the calendar.

*... fill this*

### Calendar::addSpecialDay()
Allows you to set a class or background on a given day.

Can be passed a date and class.

Optionally, an array with additional parameters can be used. Supported parameters are:
- "date" -- Formatted as "Y-m-d";
- "class" -- A string containing one or multiple classes, separated by a space;
- "style" -- A string containing css styling, inline

```php
// Using parameters...
$calendar->addSpecialDay("2015-01-21","my-class");
```
```php
// Using an array...
$calendar->addSpecialDay(array(
    "date"=>"2015-01-20",
	"class"=>"my-class"
	"background"=>"#DDDDDD"
	));
```

## Styling
Todo...
Apart from custom classes and styles defined in code, these are available by default.

.calendar - Calendar container, use to set width




## Example usage
```php

// Create calendar
$calendar = new Calendar();

// add special days and events
$calendar->addSpecialDay("2015-01-01");
$calendar->addSpecialDay("2015-01-02");

$calendar->addEvent("2015-01-15", "Ev1");
$calendar->addEvent("2015-01-15", "Ev2");

// render!
echo $calendar->render();
```
