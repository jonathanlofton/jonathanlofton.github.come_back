---
layout: post
title:  "Javascript Notes # 1"
date:   2017-04-01
---

You can print out things using `console.log()`

An example could be:

{% highlight javascript %}
  console.log( 2 * 5 )
  // => 10
{% endhighlight %}

{% highlight javascript %}
// An example of `if` statements.
if ( video_game_collection.length > 30) {
    console.log("Wow, I'm Jealous!");
}
else
{
  console.log("Wow, do you not know what steam is?")
}

confirm("Using confirm will make a pop up box appear.")

"wonderful day".substring(3,7); // will print "derf"

// Creating a variable is similar to a method in ruby it takes the form like this
var variableName = function (name) {
  console.log("This code will be executed automatically, " name " ."")
}

variableName("Jonathan")
 => "This code will be executed automatically, Jonathan."

{% endhighlight %}


<b>Scope:</b> if var is used outside a function, that variable has a global scope. If var is used inside a function, that variable has a local scope.

{% highlight javascript %}
// to set a global variable
var globalVar = "This is a global string";

var foo = function() {
  console.log(globalVar);
};
{% endhighlight %}

<b>For Loops</b>

{% highlight javascript %}
// general syntax for a javascript for loop
for (var i = 1; i < 11; i = i + 1) {
	console.log(i);
}
{% endhighlight %}

<b>Arrays</b>
{% highlight javascript %}
var arrayName = [1,2,3,4]

// pull an element out of an array like ruby
arrayName[0] == 1
{% endhighlight %}

<b>Switch Statement</b>

Switch statements will allow you to not have to write a ton of 'else if' statements.

{% highlight javascript %}
var color = prompt("What's your favorite primary color?","Type your favorite color here");

switch(color) {
  case 'red':
    console.log("Red's a good color!");
    break;
  case 'blue':
    console.log("That's my favorite color, too!");
    break;
  case 'yellow':
    console.log("Errthand yella!");
    break;

  default:
    console.log("I don't think that's a primary color!");
}

{% endhighlight %}


<b>Objects</b>

Using objects allows us to put our information and functions that use that information in that same place.
{% highlight javascript %}
var phonebookEntry = {};

phonebookEntry.name = 'Oxnard Montalvo';
phonebookEntry.number = '(555) 555-5555';
phonebookEntry.phone = function() {
  console.log('Calling ' + this.name + ' at ' + this.number + '...');
};

//add additional keys like this
myObj["name"] = "Charlie";
myObj.name = "Charlie";

phonebookEntry.phone();



//

var friends = {
    bill: {
        firstName: "Bill",
        lastName: "Hicks",
        number: 814-234-5555,
        address: ['blah', 23]
    },
    steve: {
        firstName: "Steve",
        lastName: "Hicks",
        number: 814-234-5555,
        address: ['blah', 23]
    },
    };



var list = function (friends) {
    for (var key in friends ) {
        console.log(key)
    }
}
{% endhighlight %}


<b>Methods</b>

Methods can be used to change object property values, and they can be used to perform calculations based on object properties.

{% highlight javascript %}
var bob = new Object();
bob.age = 17;
// this time we have added a method, setAge
bob.setAge = function (newAge){
  bob.age = newAge;
};

bob.getYearOfBirth = function () {
  return 2014 - bob.age;
};
console.log(bob.getYearOfBirth());

// You can create a constructor for objects like so...
function Person(name,age) {
  this.name = name;
  this.age = age;
}

// Let's make bob and susan again, using our constructor
var bob = new Person("Bob Smith", 30);
var susan = new Person("Susan Jordan", 25);

// include methods in your objects
function Rectangle(height, width) {
  this.height = height;
  this.width = width;
  this.calcArea = function() {
      return this.height * this.width;
  };
  // put our perimeter function here!
  this.calcPerimeter = function() {
        return (this.height + this.width) * 2   
  }
}

var rex = new Rectangle(7,3);
var area = rex.calcArea();
var perimeter = rex.calcPerimeter();
{% endhighlight %}
