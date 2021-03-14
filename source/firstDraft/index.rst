C# First Draft
==============

**Thesis:**
Understanding C# and its history to determine relevance in today's world
compared to other languages.


* Intro - Understanding C#

  * Where did C# originate from?

    * Created by Microsoft
    * Developed in 2000 by Anders Hejlsberg at Microsoft as a rival to Java [#f5]_
    * Created because Sun, (eventually bought by Oracle), did not want
      Microsoft to make changes to Java, so Microsoft decided to make it's own
      language instead. [#f5]_

  * QUOTE: "One of the key differences between C# and these other languages,
    particularly Java, is that we tried to stay much closer to C++ in our
    design. C# borrows most of its operators, keywords, and statements directly
    from C++. But beyond these more traditional language issues, one of our key
    design goals was to make the C# language component-oriented, to add to the
    language itself all of the concepts that you need when you write components.
    Concepts such as properties, methods, events, attributes, and documentation
    are all first-class language constructs." (page 54 from creator) [#f6]_

  * C# is strongly, dynamically typed

    * Include graphic from book that compares C# with other languages
      and compares dynamic/static and strong/weak [#f6]_ page 55

  * What is C# used for?

    * Website Development
    * Windows Application
    * Games

  * Example of programs and applications written in C# [#f2]_

    * Microsoft Visual Studio
    * Paint.NET
    * Open Dental
    * KeePass
    * Banshee
    * FlashDevelop

* Major Point 1 - History of C# [#f4]_


C# 1.0 was the first release of a new object-oriented language made by
Microsoft and if you used it for the first time, you would be able to tell the
similarities to Java. "As part of its
stated design goals, it sought to be a 'simple, modern, general-purpose object
oriented language.'" [#f4]_ This new software was greatly compatible with Windows
products, the same capability that many other Microsoft applications were
geared towards. Within this first release, the major C# features were: classes,
structs, interfaces, events, properties, delegates, operators and expressions,
statements, and attributes. Several key features that are used in programming
today were not yet utilized in this development language.

C# 2.0 was released in 2005 with Visual Studio 2005. This version release
included new features and added improvements to existing features changing the
generic object-oriented language. "The first actual fundamental change that
took place in the language was the incorporation of Generics." [#f6]_ Generics
allows for code to be reused. For example, a List<T> is a generic
List that can then be used for Ints or if the programmer changes
their mind, it can be used as a List of strings. Programmers can change what
is in the list without going back and changing the list type where it was first
defined. The namespace System.Collection.Generic supports this feature.
Another important feature in this release was iterators. "Iterators let you
examine all the items in a List \(or other Enumerable types\) with a foreach
loop. Having iterators as a first-class part of the language dramatically
enhanced readability of the language and people's ability to reason about the
code."  [#f4]_ C# still wasn't up to the capabilities of the Java language,
however, the new added features helped it attempt to catch up to current
favorite programming languages.

A major milestone of C# was in the 3.0 release in 2007 due to its establishment
of Lambda expressions, anonymous types and LINQ. Anonymous types allows objects
to be invoked with a new operator "var". This operator doesn't declare if the
object is an Int, String, Boolean, or an object of a class. This type is useful
when the programmer doesn't want all fields to be required. [#f6]_ For example,
for a person object, you might have their name and age, but not their date of
birth, so using an anonymous type allows you to not fill in that field, but
still have access to the methods get_Age and get_Name. Lambda expressions are
anonymous functions, which is similar to Javascript in style. The lambda
operator (=>) divides the defined function into two parts: the arguments to the
left and the body to the right. [#f6]_ For example: if you wanted to find if a
number is divisible by 2 or 3 you could use the following lambda expression:

  .. code-block:: c#

    x => ((x % 2) || (x % 3));

  ..


Lastly, Language-Integrated Query (LINQ) extends C#'s capabilities into
allowing for query expressions to be made. This allows the language to perform
SQL operations using C# syntax. These SQL-style queries were beneficial to
perform on collections. The following is an example using LINQ: [#f6]_

  .. code-block:: c#

    // generate a few numbers
    var numbers = Enumerable.Range(50, 200);
    // use of LINQ to filter
    var selected = from n in numbers
      where n % 3 == 0 && n % 7 == 0
      select n;
    Console.WriteLine("Numbers divisible by 3 and 7 \n\r");
    // Now we use a lambda (Action) to print out results
    selected.ToList().ForEach(n => Console.WriteLine("Selected: {0} ", n));

  ..

Output: [#f6]_

    * include the output of running the sample code above

The features included in this released help label C# as a respected programming
language. [#f4]_  The next release of C# in 2010, version 4.0 had some new
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

  * C# 1.0 [#f4]_
    * Major Features
    * Released with Visual Studio .Net 2002
    * Looked like Java
    * Started as a generic Object-Oriented (OO) Language
  * C# 2.0 [#f6]_

    * Released with Visual Studio 2005
    * Changed the generic OO Language

      * Quote - "C# version 2.0 brought iterators. To put it succinctly,
        iterators let you examine all the items in a List \(or other Enumerable
        types\) with a foreach loop. Having iterators as a first-class part of
        the language dramatically enhanced readability of the language and
        people's ability to reason about the code."  [#f4]_

    * C# still trying to catch up with Java

  * C# 3.0 --> this release included the release of Visual Studio 2008

    * Marked major growth in C#
    * Established C# as a respected programming language
    * LINQ
    * QUOTE: "C# 3.0 presented a revolutionary concept. C# 3.0 had begun to lay
      the groundwork for turning C# into a hybrid Object-Oriented / Functional
      language." [#f4]_

    * Could now write SQL-style queries to perform operations
    * Query and lambda expressions

  * C# 4.0

    * Released with Visual Studio 2010
    * Embedded interop types alleviated deployment pain
    * Optional parameters helped avoid method overloads
    * Introduction of the keyword dynamic

  * C# 5.0

    * Released with Visual Studio 2012
    * Async and await for asynchronous programming
    * Caller info attributes

* Major Point 2 - History of C# Versions 6.0 through 8.0 focused on smaller releases.

  * C# 6.0

    * Released with Visual Studio 2015
    * Moved towards smaller features that made C# more productive
    * This release made code more readable
    * Released Roslyn the compiler as a service

      * C# compiler now written in C# and the compiler can be utilized for
        programming efforts

  * C# 7.0

    * Released with Visual Studio 2017
    * New features with new capabilities that makes code even cleaner
    * .NET Core targets any operating system
    * Condensed the declaration of variables to use with the out keyword by
      allowing multiple return values via tuple

  * C# 7.1 through 7.3

    * 7.1 - async method
    * 7.2 - private protected access modifier, conditional of ref expressions
    * 7.3 - provides new features to support safe code and enhancements

  * C# 8.0

    * First major C# release that specifically targets .NET Core
    * Major Features
    * Default interface members require enhancements in the CLR
    * .NET Core Libraries

* Major Point 3 - Current Version of C# - 9.0 (references for step 3 [#f8]_ [#f9]_)

  * Date of release
  * What changed? [#f8]_

    * Part of .NET 5 - journey toward a single .NET ecosystem
    * Focus on modern workloads - applications and services being built today
    * Many C# 9.0 features rely on .NET 5.0

      * Focuses on features that support cloud applications, modern
        engineering practices, and more readable code

  * New features

    * Top-level statements - cleans up code [#f9]_

    * Include code sample of the changes [#f8]_


    * Before:

    .. code-block:: python

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

        ..

    * After:

    .. code-block:: python

        using System;
        Console.WriteLine("Hello World!");

    ..

    * Record types -> include sample code
    * Init-only setters -> include sample code
    * Enhancements to pattern matching
    * Function pointers

  * What's new? [#f9]_

    * Non-destructive mutation
    * Objects that are more like values
    * Done with record notion
    * Explain what it means to be a record
    * Show sample code of a person class

* Major Point 4 - Comparison to Other Languages and Example Applications

  * Java - include sample code to compare Hello World

    .. code-block:: python

        class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello, World!");
           }
        }

    ..

  * Python - include sample code to compare Hello World

    .. code-block:: python

        print("Hello, World!)

    ..

  * C ++

    .. code-block:: python

        #include <iostream>

        int main() {
        std::cout << "Hello World!";
        return 0;
        }

    ..

  * C

    .. code-block:: python

        #include <stdio.h>
        int main() {
           // printf() displays the string inside quotation
           printf("Hello, World!");
           return 0;
        }

    ..

  * Another point??




* Conclusion - C# in today's world

  * How often is C# being used?

    * As of 2017, 31% of all developers were using C# regularly [#f2]_

  * Are there jobs available?

    * C# in the United States - 49,697 Results on Linkedin
    * possibly include screenshot of search results

  * Tiobe index

    * C# is ranked 5th on the Tiobe index behind C, Java, Python, and C++
    * 4.44% in ratings
    * Same ranking as January and this time last year [#f1]_

  * StackOverflow

    * 1,466,151 questions asked
    * #4 in top tags [#f7]_
    * StackOverflow was built in C#

  * Companies that use C# [#f3]_

    * JPMorgan Chase
    * FM Global
    * Salesforce
    * MUFG
    * Fiserv


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
         https://medium.com/sololearn/why-is-c-among-the-most-popular-programmin
         g-languages-in-the-world-ccf26824ffcb#:~:text=C%23%20is%20an%20In%2DDem
         and%20Skill&text=Today%2C%20it%20is%20the%204th,more%20than%201.1%20million%20topics.
.. [#f6] Posadas, Marino (2016). Mastering C# and .NET Framework. Packt
         Publishing. http://simpson.idm.oclc.org/login?url=https://search.ebsco
         host.com/login.aspx?direct=true&db=nlebk&AN=1440572&site=ehost-live&sc
         ope=site&ebv=EB&ppid=pp_Cover
.. [#f7] Tags. (n.d.). Stack Overflow. https://stackoverflow.com/tags
.. [#f8] Wagner, Bill (2020). Introducing C# 9.0. CODE Focus Magazine.
            https://www.codemag.com/Article/2010032/Introducing-C
.. [#f9] dotNET. (2020, November 12). What’s New in C#?
        https://www.youtube.com/watch?v=x3kWzPKoRXc&list=PLdo4fOcmZ0oVWop1HEOml\
        2OdqbDs6IlcI&index=6

