
# Introduction to Xamarin 

## What is Xamarin?

-  Xamarin is a cross-platform toolkit that allows you to develop an app that would be compatible across different operating systems, such as your android, windows or iOS, without having you to code for the same app, 3 times. 

- When using Xamarin, you will be coding in two languages, XAML and C# using Visual Studio as your integrated development environment, also known as an IDE.
 
- XAML is an XML based language, that gives you the ability to declare the user interface elements, which is the visual appearance of your app. C# is the language that you use to develop your code-behind. 

- The code behind is what determines how the user interface behaves, for example what happens after you touch an icon. 

- Before we begin, you should also know that in the industry, there are many large companies that uses Xamarin for their app development, such as Slack, Kellogg’s, FoxSports, jetBlue and Alaska Airlines, just to name a few. So learning how to use Xamarin specifically Xamarin Forms, is really really useful. 


## MVVM Pattern

-   When making applications, you will be introduced to the MVVM Pattern. MVVM stands for Model–view–viewmodel. 

- It is a standardized structure of how you should format your Xamarin code. Just like when writing essays you have a writing structure, for coding, it is just the same. 

- You normally enforce patterns such as MVVM when writing code for large projects to make it easy to maintain and understandable. 


## Sharing Code Options 

- There are 3 methods available between cross platform applications, and today we will be going through 2 of the main ones: PCL and SL. We recommend using PCL or portable class library as the code is cleaner and hence more readable.

- So, the main difference between PCL and SAP is how we deal with platform-specific
code:

    - PCL: Using the Device class
    - SAP: Using preprocessor directives (#if, #elif, #endif)

## Shared Project

- Shared Libraries uses the Shared Asset Project type to organize your source code, and uses compiler directives to manage platform-specific requirements. This means that you can create classes as per usual, but if you want to perform something platform specific, you would have to implement a compiler directive around the code. 

- Universal windows applications use shared forms which is the default, as it allows you to write code for windows desktop and applications. 

- Overall, it can be useful, however it can be limited and is normally used for coding small apps, backward compatibility reasons or prototyping, which is why we normally recommend using portable class libraries. 

## Portable Class Library

- Portable Class Libraries targets the platforms you wish to support, and uses Interfaces to provide platform-specific functionality.

- It is a great way to write code once that can be used on multiple platforms, and can be easily maintained and tested. When you write a PCL you don’t need to insert compiler directives to switch the code depending on each platform. 
You only need to select which platforms you will support then starting coding. Portable Libraries like .NET Standard or Profile Based, are the recommended method when coding for a cross-platform mobile application. 


- There are some great benefits for using PCL’s to summarise 
    - Easier unit testing
    - Easier to read code
    - Greater Portability
    - Better implementations of code




