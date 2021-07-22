---
layout: post 
comments: true
title: "Announcing PostSharp \"Caravela\" Preview 2 (0.3.5)"
date: 2021-01-25 15:30:00 +02:00
categories: ["Announcement", "Caravela"]
permalink: /post/announcing-caravela-preview-2.html
author: "Gael Fraiteur"
image: /assets/images/blog/2021-01-25-caravela-announcement/Project Caravela 1.png
tag: featured
---

> __TLDR__: We've made it! The Roslyn-based "Caravela" can now implement INotifyPropertyChanged and aspect-oriented way and you can [try it in your browser](https://try.postsharp.net/#inpc). But watch out! You can run with a knife that's in preview, but not in production code.

If you haven't heard from us for three months, it's because we have been badly hit by the COVID/lockdown mess in April. We're now working with a smaller team, have more energy than _ever_, and we have chosen to focus it on our top priority: code, not words.

Today, we're excited to announce the second preview of PostSharp "Caravela", our new Roslyn-based meta-programming framework for aspect-oriented programming, code generation and code validation. PostSharp "Caravela" is to become the successor of the MSIL-based PostSharp Framework and PostSharp SDK.

Whereas the first preview, announced six months ago, was merely a proof of concept, the current preview is built on the final architecture of the product. It implements the most useful aspect-oriented features and a large part of the C# language. As an early preview, however, it is still unsuitable for production use. The most noticeable gap is the lack of support for async methods and the poor handling of warnings, including nullability warnings. Caravela still does not cover all the features of the "old" PostSharp, so if you're excited to port your aspects to the new stack &ndash; wait.

That said, Caravela is already a wonderful playground. It already implements a load of feature. For examples and demos, follow the links below.

## Aspect-oriented features

- [An innovative C#-based template language](https://doc.postsharp.net/caravela/aspects/templates) that allow you to mix meta expressions and statements (such as compile-time loops) with run-time code;
- [Overriding existing methods, fields, properties, events (add/remove)](https://doc.postsharp.net/caravela/aspects/simple-aspects/simple-aspects);
- [Introducing new methods, fields, properties or events into an existing type](https://doc.postsharp.net/caravela/aspects/advising/introducing-members);
- [Implementing new interfaces in an existing type](https://doc.postsharp.net/caravela/aspects/advising/implementing-interfaces);
- Mixing of all of the above in a single aspect &mdash; _YES!_ we now do INotifyPropertyChanged ([try it in your browser!](https://try.postsharp.net/#inpc));
- [Reporting and suppressing diagnostics from your aspects](https://doc.postsharp.net/caravela/aspects/diagnostics)
- [Support for several aspects on the same declaration](https://doc.postsharp.net/caravela/aspects/ordering)

## Design-time features

- Creating [live templates](https://doc.postsharp.net/caravela/aspects/creating-live-template), i.e. complex code transformations, like aspects, but that are executed from the lightbulb menu in the editor and applied to your source code.
- Syntax highlighting of aspects ([Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=PostSharpTechnologies.caravela) required).

## Testing

  -  A dedicated xUnit-based [testing framework](https://doc.postsharp.net/caravela/aspects/testing/testing) for aspects.

## Documentation
  
- [try.postsharp.net](https://try.postsharp.net/), an online tool to try Caravela without installing it on your machine (a fork of try.dot.net)
- A dozen of open-source [samples](https://github.com/postsharp/Caravela.Samples)
- A reasonably complete [online documentation](https://doc.postsharp.net/caravela) with code snippets that can be executed and edited online thanks to [try.postsharp.net](https://try.postsharp.net/),
[automatically and comprehensively tested](https://github.com/postsharp/Caravela/tree/master/code/Caravela.Documentation.SampleCode.AspectFramework);

## Summary

We have reached an important milestone with PostSharp "Caravela". We are now working on stabilizing the product and continuing to build the most important features. Until it's done, we will continue focusing and code instead of words.

For feedback and questions, please use our [GitHub discussion board](https://github.com/postsharp/Caravela/discussions).

Happy PostSharping!

-gael
