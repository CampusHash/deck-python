title: Meet, Python!
content_class: flexbox vcenter centered

<img src="images/python.svg">

__World's easiest and arguably most powerful programming language.__

---

title: Who uses Python?
content_class: flexbox vcenter centered

<img src="images/whouses.png" style="width: 90%; height: 90%">

and many, many more. . .

---

title: Quick feature check
class: fill

- Very-high-level, __interpreted__, __loosely__ and __dynamically__ typed, object-oriented

- Clean, readable syntax

- Comfortable level of abstraction, automatic memory management

- Does __not__ force object orientation

- Extensive collection of standard modules, great community support

- Can be, and is, used for a large number of application types

- Easily extensible, plays nice with applications written in other programming languages

- Easy to learn, get started, and build things, has __common sense__

---

title: 
class: nobackground
content_class: flexbox vcenter centered

<img src="images/python.png" style="width: 100%; height: 100%">
<footer class="source">source: xkcd.com</footer>

This is a title with the event branding.

---

title: Common Sense?
class: fill

<pre class="prettyprint" data-lang="c++">
#include &lt;iostream&gt;
using namespace std; 
int main()
{
cout << "Hello, world!" << std::endl;
    return 0;
}
</pre>

<pre class="prettyprint" data-lang="java">
public class HelloWorld {
	public static void main(String [] args) {
		System.out.println("Hello, world!");
        }
}
</pre>

<div class="centered">How about, <strong>NO</strong>.</div>
---

title: Common Sense!
class: fill

<pre class="prettyprint" data-lang="python">
print "Hello, World!"
</pre>

<img src="images/troll-troll-face.svg" width=25% height=25% style="float: right">

- Clean, comprehensible syntax.
- No braces. Uses tab spaces as delimiters.

Impressed already?

---

title: Ready to hack?
class: nobackground
content_class: flexbox vcenter centered

<h3 style="font-size: 200%">Set up Python on your computer.<br>Fire up the interpreter.</h3>
<span class="blue2">
$ python
</span>
<br>or<br>
<span class="blue2">
Start > Python27 > IDLE
</span>
---
title: Look, we have a calculator!
class: fill

Your Python shell can be used to do some real quick calculations. Don't reach out for your calculator ever again.

<pre class="prettyprint" data-lang="python">
>>> 3 + 2
5
>>> 98 - 56
42
>>> (60 - 57) * 11
33
>>> (124 - 88) / 9
4
</pre>

Looks cool, huh?

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 400%" class="blue">Arithmetic</h1>

---

title: Operators, numbers and variables
class: fill

<pre class="prettyprint" data-lang="python">
>>> 57 / 8					# integer division by default
7
>>> 57.0 / 8				# coercion to float division
7.125
>>> PI = 3.14				# PI is a variable
>>> r = 2.5
>>> area = 2 * PI * r**2	# ** is used for exponentiation
>>> area
39.25
>>> x = 1
>>> y = z = 5				# multiple variable assignment
>>> X + y * z
Traceback (most recent call last):		# Drats! We have an error!
  File "&lt;input&gt;", line 1, in <module>
NameError: name 'X' is not defined		# variables are case-sensitive!
>>> x + y * z
26
</pre>

---

title: Imaginary numbers too!
class: fill

Complex numbers : <span class="blue">real + imag <span class="red">j</span></span>

<pre class="prettyprint" data-lang="python">
>>> z = 4 + 2j
>>> z
(4+2j)				# complex number tuple
>>> z.real			# property
4.0
>>> z.imag
2.0
>>> z.conjugate()	# method
(4-2j)
>>> abs(z)			# abs() is a built-in method in Python
5
</pre>
---
title: Some nifty functions
class: fill

<pre class="prettyprint" data-lang="python">
>>> x, y = 42, 6.9	# multiple inline assignments
>>> float(x)		# converts to floating point
42.0
>>> int(y)			# converts to an integer
6
>>> round(y)		# rounds off to the nearest integral number, returns a float
7.0
>>> long(x)			# converts to long int
42L
>>> max(x, y)
42
>>> min(x, y, 0, -3)
-3
</pre>

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 400%" class="green">Strings</h1>

---

title: Let's print something!
class: fill

<pre class="prettyprint" data-lang="python">
>>> 'CampusHash'
'CampusHash'
>>> "Hello, world!"
'Hello, world!'
>>> "And then everyone shouted, 'We love CampusHash!'"		# nested quotes
"And then everyone shouted, 'We love CampusHash!'"
>>> 'I said, "Well, that\'s great."'				# escaping with \
>>> person, emotion, thing = "Minions", "love", "banana"
>>> person+emotion+thing
'Minionslovebanana'
>>> person + ' ' + emotion + ' ' + thing + '.'
'Minions love banana.'
>>> thing * 5
'bananabananabananabananabanana'

</pre>

---

title: Let's 'print' something!
class: fill

<pre class="prettyprint" data-lang="python">
>>> print 'Gru'
Gru
>>> movie = 'Despicable Me'
>>> movie
'Despicable Me'
>>> print movie
Despicable Me		# no quotes!
</pre>

- print is not a function. It is an operator.
- Anything that you operate print on, will be printed to the standard output.

---

title: Anatomy of a String
class: nobackground
content_class: flexbox vcenter centered

<img src="images/string-slicing.png" style="height: 95%; width: 95%">
<footer>Tip : Google for 'Monty Python's Flying Circus'.</footer>

---

title: Not just your regular String
class: fill

- There is no <span class="red">char</span> in Python. Only <span class="green">str</span>.
- Strings are immutable, i. e., they cannot be changed.
- Strings support splicing.
- Lots of in-built methods and properties to operate on strings.

<pre class="prettyprint" data-lang="python">
>>> name = "Minion"
>>> name[3]
'i'
>>> name[3] = 'x'
Traceback (most recent call last):
  File "&lt;input&gt;", line 1, in <module>
TypeError: 'str' object does not support item assignment
>>> name[::-1]		# This one's magic!
'noiniM'

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 400%" class="blue">Data Structures: <span class="red">Lists</span></h1>

---

title:
class: fill
content_class: flexbox vcenter centered

<img src="images/lists.png" style="height: 50%; width: 50%">

<h1 style="font-size: 200%">List is a compund datatype.</h1>
It is analogous to an array.

---

title: Lists - Feature Check
class: fill

- Lists are collections of items (strings, integers, or even other lists).
- Each item in the list has an assigned index value.
- Lists are enclosed in [ ].
- Each item in a list is separated by a comma.
- Unlike strings, lists are mutable, which means they can be changed.

<pre class="prettyprint" data-lang="python">
>>> fruits = ['apple', 'banana', 'orange']
>>> fruits[0]
'apple'
>>> mix = ["1", "hello", 2, "world"]
>>> mix[-1]
'world'
</pre>

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 300%" class="blue">Data Structures: <span class="red">Dictionaries</span></h1>

---

title:
class: fill
content_class: flexbox vcenter centered

<img src="images/dictionary.gif" style="height: 100%; width: 100%">

<h1 style="font-size: 200%">Dictionaries are hash tables.</h1>

---

title: Dictionaries - Feature Check
class: fill

- Dictionaries are collections of items that have a "key" and a "value".

- Python dictionaries are also known as associative arrays or hash tables.

- They are just like lists, except instead of having an assigned index number,
you make up the index.

- Dictionaries are unordered, so the order that the keys are added doesn’t
necessarily reflect what order they may be reported back.

- Use {} curly brackets to construct the dictionary.

- Look up the value associated with a key using [].

- Provide a key and a value.

- A colon is placed between key and value (key:value). 

- Each key must be unique and each key can be in the dictionary only once.

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 300%" class="green2">Tuples and Sets</h1>

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 300%" class="yellow2">Functions</h1>

---

title:
class: fill
content_class: flexbox vcenter centered

<img src="images/phonecall.jpg" style="height: 100%; width: 100%">

<h1 style="font-size: 140%">A function is something you can call which performs an action and returns a value.</h1>

---

title: Function rules
class: fill

- A function in Python must be defined before it’s used.

- Create a function by using the keyword “def” followed by the functions name and
the parentheses (). 

- The function has to be named plus specify what parameter it has (if any).

- The keyword "def" is required and must be in lowercase.

- The name can be anything you like. 

- The end of the line has to end with a colon (:)

- The function often ends by returning a value using return.

- The code inside the function must be indented.

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 300%" class="gray3">Loops</h1>

---

title:
class: fill
content_class: flexbox vcenter centered

<img src="images/pypy.png" style="height: 100%; width: 100%">

<h1 style="font-size: 140%">Loops allow us to do similar things many times.</h1>

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 250%" class="blue2">Conditions and Comparisons</h1>

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 300%" class="red2">In-built Functions</h1>

---
title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 300%" class="black">Classes</h1>

---

title:
class: fill
content_class: flexbox vcenter centered

<img src="images/class.png" style="height: 100%; width: 100%">

<h1 style="font-size: 140%">Classes are definitions for objects.</h1>

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 300%" class="red">Object-orientation</h1>

---

title:
class: fill
content_class: flexbox vcenter centered

<img src="images/diamond.png" style="height: 75%; width: 75%">

<h1 style="font-size: 140%">Everything is an object in Python.</h1>

---

title:
class: nobackground
content_class: flexbox vcenter centered

<h1 style="font-size: 300%" class="black">Modules and Packages</h1>

---

title:
class: fill
content_class: flexbox vcenter centered

<img src="images/questions.jpg" style="height: 100%; width: 100%">

<h1 style="font-size: 400%">I <span class="red">&hearts;</span> questions!</h1>

