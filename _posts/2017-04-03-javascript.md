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

<b></b>
{% highlight javascript %}
{% endhighlight %}
