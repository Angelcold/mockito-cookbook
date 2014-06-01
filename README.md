Mockito Cookbook Code Repository
=================================

This repository contains code present in my "Mockito Cookbook" by Packt Publishing.

The structure
-------------

### Project structure

It's a multimodule project where each module represents a particular chapter of the book

- chapter01
- chapter02
- ...
- chapter10
- common (classes used by all modules)
- common test (test classes used by all modules)

### Module structure
Each chapter contains the following package structure (example for chapter01):

```
chapter01
    src
        main
            java
                com
                    blogspot
                        toomuchcoding
                            chapter1
        test
            java
                com
                    blogspot
                        toomuchcoding
                            chapter1
```

The contents of chapters differ so in each "chapter" package (in the example above it's "chapter1" package)
you will have packags related to the given chapter in the book. To make it easier for you to find the desired
class I've named the chapter related packages in the following manner (example for Chapter 1):

```
_1_MockitoAnnotationsJunitRunner
_2_MockitoAnnotationsJunit
_3_MockitoAnnotationsTestNg
_4_MockitoGoodPractices
_5_AddingMockitoHintsToExceptionMessages
```

The prefix is given to sort packages in the order presented in the book. After the prefix you have the name of
the recipe inside the chapter. Now let's take a look at the structure of a recipe inside this code repository:

```
_4_MockitoGoodPractices
    assertj
        TaxFactorCalculatorTest.java
        TaxFactorCalculatorTestNgTest.java
    fancy
        assertj
            TaxFactorCalculatorTest.java
            TaxFactorCalculatorTestNgTest.java
        hamcrest
            TaxFactorCalculatorTest.java
            TaxFactorCalculatorTestNgTest.java
    hamcrest
        TaxFactorCalculatorTest.java
        TaxFactorCalculatorTestNgTest.java
```

In the book in the majority of examples I'm using [AssertJ](http://joel-costigliola.github.io/assertj/assertj-core.html)
for asserting objects. Since not everyone is using it and there are people who prefer to use Hamcrest that's why
you can find (almost in every recipe) two packages *assertj* and *hamcrest* where you can find the same examples
using two different libraries for assertions. The *fancy* package in the 1st chapter 4th recipe means that there
is an additional example in the book. It's related to a fancy way of creating code that's why the package is named
*fancy*. Inside that package yet again you have to approaches of asserting objects - with *assertj* and *hamcrest*.
Last but not least each of the tests (almost in every recipe) is written once for [JUnit](http://junit.org/)
and once for [TestNG](http://testng.org/doc/index.html).

How to build it
--------------

You can build the app using gradle

```bash
    ./gradlew build
```

or maven

```bash
   mvn clean install
```


Build status
--------------
[![Build Status](https://travis-ci.org/marcingrzejszczak/mockito-cookbook.svg?branch=master)](https://travis-ci.org/marcingrzejszczak/mockito-cookbook)

