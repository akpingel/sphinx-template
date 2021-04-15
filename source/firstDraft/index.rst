History of C#
=============

C# was created by Microsoft. It was first developed in 2000 by Anders Hejlsberg
as a rival to Sun Microsystem's Java programming language. Microsoft had their
own implementation of Java. They tried to add language features to Java and Sun
said no. [#f5]_ Microsoft decided to abandon their Java product and create their own
which became known as C#. Understanding C# and its history helps determine its
relevance in today's world compared to other languages.

Microsoft's new language would go on to become one of the top languages used
by programmers.

    "One of the key differences between C# and these other languages,
    particularly Java, is that we tried to stay much closer to C++ in our
    design. C# borrows most of its operators, keywords, and statements directly
    from C++. But beyond these more traditional language issues, one of our key
    design goals was to make the C# language component-oriented, to add to the
    language itself all of the concepts that you need when you write components.
    Concepts such as properties, methods, events, attributes, and documentation
    are all first-class language constructs." [#f6]_

A key factor of C# is that it is strongly, dynamically typed. Being a strong
typed language means that any attempt to pass a wrong kind of parameter as an
argument will generate a compilation error. [#f6]_ For example, declaring an
integer and passing a string value such as "coding" will error. The graphic
below shows that JavaScript and C++ are some of the weaker typed
languages.

  .. figure:: dynamicStrong.png
    :width: 75%
    :align: center

    This figure shows whether programming languages are dynamic or static and
    strong or weak. [#f6]_

Dynamic means that rules are applied at runtime, compared to static languages
that apply their rules at compile time. [#f6]_ In the figure, Python and Clojure
are more dynamic than C#, but C# is more dynamic than Scala or C++.

C# is used for website development, applications, and games. The following are
examples of programs, applications, and games written in C#: [#f2]_

    * Microsoft Visual Studio - a development environment from Microsoft
    * Paint.NET - a graphics editor program for Microsoft Windows, developed
      on the .NET framework
    * Open Dental - dental practice management software written in C#
    * KeePass - a password safe primarily for Windows, built in C# and C++
    * Banshee - cross-platform media player written in C# and GTK
    * FlashDevelop - a development environment for development of Adobe Flash
      websites, web and desktop applications, and video games

To get to the advanced steps of creating an application or game, it is
important to start with the basics and learn the fundamentals of the
programming language.
C# 1.0
""""""

C# 1.0 was the first release of a new object-oriented language made by
Microsoft in 2002. There were a lot of similarities to Java. "As part of its
stated design goals, it sought to be a 'simple, modern, general-purpose object-
oriented language.'" [#f4]_

This new software originally only ran on Microsoft Windows, and only created
programs that ran on MS Windows. Within this first release, the major C#
features were:
classes, structs, interfaces, events, properties, delegates, operators and
expressions, statements, and attributes. Several key features that are used in
programming today, such as generics and LINQ, were not yet utilized in this
development language, but would be developed later on.

C# 2.0
""""""

C# 2.0 was released in 2005 with Visual Studio 2005. This version release
included new features and added improvements to existing features changing the
generic object-oriented language. "The first actual fundamental change that
took place in the language was the incorporation of Generics." [#f6]_ Generics
allows for code to be reused. For example, a ``List<T>`` is a generic
list class that could be used to create a list of integers, and also used to
create a list of strings. Without generics, programmers would need a list class
for every data type. The namespace ``System.Collection.Generic`` supports
this feature.

Another important feature in this release was iterators. "Iterators let you
examine all the items in a List \(or other Enumerable types\) with a foreach
loop. Having iterators as a first-class part of the language dramatically
enhanced readability of the language and people's ability to reason about the
code."  [#f4]_ C# still wasn't up to the capabilities of the Java language,
however, the new added features helped it attempt to catch up to current
popular programming languages.

C# 3.0
""""""

A major milestone of C# was in the 3.0 release in 2007 due to its establishment
of Lambda expressions, anonymous types and LINQ. Anonymous types allows objects
to be invoked with a new operator ``var``. This operator doesn't declare if the
object is an Int, String, Boolean, or an object of a class. This type is useful
when the programmer doesn't want all fields to be required. [#f6]_ For example,
for a person object, you might have their name and age, but not their date of
birth, so using an anonymous type allows you to not fill in that field, but
still have access to the methods, such as get_Age and get_Name.

Lambda expressions are anonymous functions, which is similar to Javascript in
style. The lambda operator ``=>`` divides the defined function into two parts:
the arguments to the left and the body to the right. [#f6]_ For example: if you
wanted to find if a number is divisible by 2 or 3 you could use the following
lambda expression:

  .. code-block:: c#

    x => ((x % 2) || (x % 3));

  ..


Lastly, Language-Integrated Query (LINQ) extends C#'s capabilities into
allowing for query expressions to be made. This allows the language to perform
SQL operations using C# syntax. These SQL-style queries are beneficial to
perform on collections. The following is an example using LINQ: [#f6]_

  .. code-block:: c#
     :linenos:

      // generate a few numbers
      var numbers = Enumerable.Range(50, 200);
      // use of LINQ to filter
      var selected = from n in numbers
        where n % 3 == 0 && n % 7 == 0
        select n;
      Console.WriteLine("Numbers divisible by 3 and 7 \n\r");
      // Now we use a lambda (Action) to print out results
      selected.ToList().ForEach(n => Console.WriteLine("Selected: {0} ", n));

If you were to run the above sample code, the following would be printed to the
console: [#f6]_

  .. figure:: linq_output.png
    :width: 300

    Output of LINQ sample code.

The features included in this released help label C# as a respected programming
language. [#f4]_

C# 4.0
""""""

The next release of C# in 2010, version 4.0 had some new
features, but none that compared to the previous release. The following
were included in this release: [#f6]_

 * Dynamic Binding
 * Named/optional arguments
 * Generic covariant and contravariant
 * Embedded interop types

Additionally, the dynamic keyword was introduced. "By using the dynamic keyword,
you can create constructs similar to dynamically typed languages like
JavaScript." [#f4]_  This means that you could create dynamic x = "a string" and
then add six to it and not have a compiler error because dynamic is assumed to
support any operation. Errors that occur from using the keyword dynamic will
be caught from the runtime and throw a runtime exception.

C# 5.0
""""""

C# 5.0 was released with Visual Studio 2012. The two main purposes of this
release were to incorporate ``async`` and ``await`` concepts for asynchronous
programming. "When these features came out in 2012, C# changed the game again
by baking asynchrony into the language as a first-class participant." [#f4]_
These two words go hand in hand. When the compiler sees the word ``async`` it
looks for the word ``await``.

Sample: [#f6]_

  .. code-block:: c#
    :linenos:

      static void Main(string[] args)
      {
        Console.WriteLine("SlowMethod started at...{0}",
          DateTime.Now.ToLongTimeString());
        SlowMethod();
        Console.WriteLine("Awaiting for SlowMethod...");
        Console.ReadLine();
      }
      static async Task SlowMethod()
      {
        // Simulation of slow method "Sleeping" the thread for 3 secs.
        await Task.Run(new Action(() => System.Threading.Thread.Sleep(3000)));
        Console.WriteLine("Finished at: {0}",
          DateTime.Now.ToLongTimeString());
        return;
      }

Output: [#f6]_

  .. figure:: awaitOutput.png
    :width: 75%

    Output of ``await`` function code.

Another smaller part of this release was caller info attributes. This
enhancement is beneficial for diagnostics and logging, but didn't have as big
of an impact as the ``async`` and ``await`` concepts.

C# 6.0
""""""

C# 6.0 was released with Visual Studio 2015. This release focused on smaller
aspects of the language rather than adding major new features. This allowed
the language to be more productive and make the code more readable. Additional
features include:

  * String interpolation
  * Exception filters
  * The nameof operator
  * The null-conditional operator
  * Auto-property initializer
  * Static using declarations
  * Expression bodied methods
  * Index initializer

Exception filters allows successful code to continue to run, and failed code
will throw an error message to tell you why the code won't work instead of
failing your program. You can also utilize to to do something else when the
failed code occurs.

This version release included Roslyn the compiler as a service which was written
in C#. [#f4]_ A compiler in the same language as your code allows new benefits
in the IDE for editing and compiling your code.


C# 7.0
""""""


C# 7.0 was released with Visual Studio 2017. The most important features of
this release include new support for tuples and deconstructions. You no longer
have to use the ``Tuple`` Class to declare tuples thanks to pattern matching,
the compiler can handle declarations that include a tuple syntax next to a var
definition. [#f6]_

  .. code-block:: c#

    (int n, string s) = ( 8, "coding" );

Function sample: [#f6]_

  .. code-block:: c#
    :linenos:

      static (int sum, int count) ProcessArray(List numbers)
      {
        var result = (sum:0 , count:0);
        numbers.ForEach(n =>
        {
          result.count++;
          result.sum += n;
        });
        return result;
      }

For this function, the return valid is a tuple. This allows a sum of numbers
and the count of the numbers being added to be calculated.

Deconstruction allows us to deconstruct/decompose an object into parts. The
``Deconstruct`` method must be defined to deconstruct and object. For example,
decomposing a DateTime Value declaration would look like this: [#f6]_

  .. code-block:: c#

    static void Deconstruct(this DateTime dt, out int hour, out int minute,
      out int second)
    {
      hour = dt.Hour;
      minute = dt.Minute;
      second = dt.Second;
    }

The following are point releases and the new features and enhancements
included in each version.


  C# 7.1

    * async Main method
    * default literal expressions
    * inferred tuple element names
    * pattern matching on generic type parameters

  C# 7.2

    * ``private protected`` access modifier
    * conditional ref expressions (``?:``)
    * leading underscores for numeric literals before printed digits

  C# 7.3

    * ability to test ``==`` and ``!=`` with tuple types
    * fixed statements can be used with any type that supports a pattern
    * additional generic constraints

C# 8.0
""""""

C# 8.0 targets .NET Core. Some features rely on new CLR capabilites, other on
library types added only in .NET Core C#. [#f4]_ The following are some of
the new features and enhancements to the language:

  * Readonly members
  * Default interface methods
  * Pattern matching enhancements
  * Nullable reference types
  * Stackalloc in nested expressions

C# 9.0
""""""

The newest version of C# is 9.0. It was released in 2020 and relies on and is
only compatible with .NET 5. "C# 9.0 focuses on features that support native
cloud applications, modern software engineering practices, and more concise
readable code. The biggest new features within this release are:

  * Top-level statements
  * Record types
  * Init-only setters
  * Enhancements to pattern matching
  * Function pointers

Top-level Statements
~~~~~~~~~~~~~~~~~~~~
Top-level statements was included in this release to reduce irrelevant code.
The previous version of a simple "Hello world!" program would be the following: [#f8]_

  .. code-block:: c#
    :linenos:

      using System;
      namespace HelloWorld
      {
        class Program
        {
          static void Main(string[] args)
          {
            Console.WriteLine("Hello World!");
          }
        }
      }

With the new release, this code would be simplified to:

  .. code-block:: c#

    using System;
    Console.WriteLine("Hello World!");

Only code that performs that action required is necessary with the new top-level
statements that replace the ``Main`` function in programs. Like the ``Main``
function, there can only be one top-level function within the program. If two
statements are included, the compiler will send an error.

Record Types
~~~~~~~~~~~~

Records provide a type declaration for an immutable reference type that uses
value semantics for equality. [#f8]_

  .. code-block:: c#
    :linenos:
    :emphasize-lines: 5

       public record Bank
       {
         public int AccountNum {get; init; }
         public string AccountName {get; init;}
         public Person(int num, string name) => (num, name) = (AccountNum, AccountNum);
       }

In this example, a Book type is created with two read-only properties
``AccountNum`` and ``AccountName``. The properties cannot be modified once it is
created which makes it immutable. To update a record, an existing object can be
copied and a new object can be created. Inheritance is supported by Records by
the following code:

  .. code-block:: c#
    :linenos:
    :emphasize-lines: 1,4,5

      public record SavingsAccount : Account
      {
        public int InterestRate { get; init}
        public SavingsAccount(int num, string name, int interest) : base
          (num, name) => InterestRate = interest;
      }

When a record type is defined, the compiler incorporates several other
methods: [#f8]_

  * Methods for value-baed equality comparisons
  * Override for ``GetHashCode``
  * ``Copy`` and ``Clone`` members
  * ``PrintMembers`` and ``ToString``
  * ``Deconstruct`` method

With record notion, objects are more like values and classes are enhanced to
have value like behavior rather than encapsulated identified entity. [#f9]_
Expressing record objects that are strings are easier. A record that is a
string type can be expressed using the following code to print out all its
attributes.

  .. code-block:: c#

    Console.WriteLine(person);

Init-only Setters
~~~~~~~~~~~~~~~~~

C# 9.0 allows you to create ``init`` accessors instead of ``set`` accessors.
This is like records where once it is set, the properties are read-only.

Example: [#f8]_

  .. code-block:: c#
    :linenos:
    :emphasize-lines: 3,4

      public struct Point
      {
        public double X {get; init;}
        public double Y {get; init;}
        public double Distance => Math.Sqrt(X * X + Y * Y);
      }

This example code can be initialized, but then cannot be modified until the
program has been run and completed.

  .. code-block:: c#
    :linenos:

      var pt = new Point { X = 3, Y = 4};
      // pt.X = 7; this would fail
      Console.WriteLine(pt.Distance);


Comparing C# to Other Languages
"""""""""""""""""""""""""""""""

C# was developed based with similar characteristics to Java in its first
release. Consider the following "Hello world!" example to see how the current
version of C# compares to other coding languages.

C#
~~

  .. code-block:: C#
    :linenos:

      namespace HelloWorld
      {
        class Hello {
          static void Main(string[] args)
          {
            System.Console.WriteLine("Hello World!");
          }
        }
      }

Java
~~~~

  .. code-block:: java
    :linenos:

      class HelloWorld {
        public static void main(String[] args) {
          System.out.println("Hello, World!");
        }
      }

Python
~~~~~~

  .. code-block:: python
    :linenos:

      print("Hello, World!)

C
~
  .. code-block:: c
    :linenos:

      #include <stdio.h>
      int main() {
        // printf() displays the string inside quotation
        printf("Hello, World!");
        return 0;
      }

Modern C#
"""""""""

C# is one of the top programming languages in the world today. As of 2017, 31%
of all developers were using C# regularly [#f2]_ and it is ranked 5th on the
Tiobe index behind C, Java, Python, and C++. [#f1]_

StackOverflow, a popular website for coding help, was built in C#. It also marks
C# as #4 in top tags and has over 1,466,151 questions asked. [#f7]_ Other
companies that use C# include: [#f3]_

    * JPMorgan Chase
    * FM Global
    * Salesforce
    * MUFG
    * Fiserv

Being one of the top languages, there are also thousands of job applications
that include the C# keyword in their job description on LinkedIn.

  .. figure:: jobSearchResults.png
    :width: 75%

    Figure taken from LinkenIn search results.
  ..

The possibilities of C# are endless. The language will continue to evolve as the
years go on and will remain prevalent in the coding world. Whether looking to
learn a new coding language or looking for a new job, C# shows opportunities
for people who are interested.



.. [#f1] C# Programming Language. TIOBE - The Software Quality Company.
         https://www.tiobe.com/tiobe-index/csharp/
.. [#f2] Everything you need to know about C#. Pluralsight.
         https://www.pluralsight.com/blog/software-development/everything-you-need-to-know-about-c-
.. [#f3] HG Insights (2021, March 2). Companies Using C#, Market Share,
         Customers and Competitors. https://discovery.hgdata.com/product/c-sharp
.. [#f4] Microsoft Contributors (2020, April 8). The History of C#. Microsoft.
         https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-version-history
.. [#f5] Mkhitaryan, Armina. (2017, October 13). Why is C# Among The Most
         Popular Programming Languages in The World? Medium.
.. [#f6] Posadas, Marino (2016). Mastering C# and .NET Framework. Packt
         Publishing.
.. [#f7] Tags. (n.d.). Stack Overflow. https://stackoverflow.com/tags
.. [#f8] Wagner, Bill (2020). Introducing C# 9.0. CODE Focus Magazine.
            https://www.codemag.com/Article/2010032/Introducing-C
.. [#f9] dotNET. (2020, November 12). What’s New in C#?
        https://www.youtube.com/watch?v=x3kWzPKoRXc&list=PLdo4fOcmZ0oVWop1HEOml\
        2OdqbDs6IlcI&index=6

