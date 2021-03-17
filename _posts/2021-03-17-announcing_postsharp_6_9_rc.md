---
layout: post 
comments: true
title: "Announcing PostSharp 6.9 RC: Visual&nbsp;Studio Tooling performance improvements"
date: 2021-03-17 09:00:00 +01:00
categories: [Announcement]
permalink: /post/postsharp-6-9-rc-visual-studio-tooling-performance-improvements.html
author: "Antonin Prochazka"
image: /assets/images/blog/2021-03-17-6-9-RC-announcement/6-9-RC-square.png
---
We are happy to announce that PostSharp 6.9 RC is available today. In this release, the performance of PostSharp Tools for Visual&nbsp;Studio has been improved.

This version is available for [download](https://www.postsharp.net/downloads/postsharp-6.9/v6.9.2) on our website and the packages for 6.9.2-rc are now available as prerelease on [NuGet](https://www.nuget.org/profiles/PostSharp).

PostSharp Tools for Visual&nbsp;Studio is a part of the PostSharp ecosystem since PostSharp 2.0, when we extended Visual&nbsp;Studio 2008 and 2010. That made projects enhanced by PostSharp more understandable, easier to debug and UI became available for application of aspects provided by the PostSharp Pattern Libraries. Since then, we’ve kept the pace with the development of Visual&nbsp;Studio itself and we’ve supported each succeeding Visual&nbsp;Studio version, incorporating many of the features that became available for the Visual&nbsp;Studio extensibility.

Support for a new Visual&nbsp;Studio version requires a certain amount of code refactoring and maintaining an abstraction layer that lets us keep the source code shared among the different extension versions as much as possible. Sometimes, this leads to having an obsolete code and suboptimal performance caused by use of legacy APIs.

In PostSharp 6.9, we've focused on code cleanup and performance optimization. Less time is required by the extension to obtain the information and to show all the important data about the source code. Additionally, it doesn't block the user interface more often than required by the Visual&nbsp;Studio Extensibility SDK. All that improves the overall user experience when developing PostSharp-enhanced projects.

Now let’s have a look at how exactly the PostSharp Tools for Visual&nbsp;Studio enrich the development experience and which questions about PostSharp-enhaced source code they answer.


## Which code elements are enhanced by PostSharp?

<img style="margin-right: 10px; margin-top: 0px; margin-left: 10px;" src="/assets/images/blog/2021-03-17-6-9-RC-announcement/01-adornments.png" alt="Each code element enhanced by PostSharp is underlined.">

Each code element enhanced by PostSharp is underlined.


## Which PostSharp aspects enhance my code and how?

<img style="margin-right: 10px; margin-top: 0px; margin-left: 10px;" src="/assets/images/blog/2021-03-17-6-9-RC-announcement/02-quick-info.png" alt="Aspects applied on code element are shown on mouse hover.">

Hovering the mouse over any of the code elements enhanced by PostSharp shows an information box. It shows which aspects enhance this particular code element, which effect they have on the code element, and how the aspects were applied. Additionally, all types listed in the information box provide links to their source code, where available.


## Which code elements are enhanced by a given PostSharp aspect and how?

<img style="margin-right: 10px; margin-top: 0px; margin-left: 10px;" src="/assets/images/blog/2021-03-17-6-9-RC-announcement/03-postsharp-explorer.png" alt="The PostSharp Explorer toolbox.">

The tooling comes with PostSharp Explorer toolbox consisting of three views. The first one shows the tree of all aspects used in the solution. Selecting one of the aspects shows a list of code elements that the aspect enhances in the second view. Selecting one of those code elements shows how the selected aspect enhances the selected code element in the third view. Double-clicking on the aspect, or on the code element navigates to its declaration in the source code, where available. More features can be found in the context menus. The PostSharp Explorer toolbox can be opened via the `(Extensions >) PostSharp > PostSharp Explorer` Visual&nbsp;Studio menu.


## How can a code element be enhanced by PostSharp?

<img style="margin-right: 10px; margin-top: 0px; margin-left: 10px;" src="/assets/images/blog/2021-03-17-6-9-RC-announcement/04-code-actions.png" alt="PostSharp code actions.">

Most of the aspects provided by the PostSharp Pattern Libraries, like Logging, Caching, Threading, and others, can be applied using the code actions menu. Select a code element in the source code and open the code actions menu, either by clicking on the light bulb or screwdriver icon next to the code line, or by pressing the ctrl+. shortcut. The menu contains code actions for applying aspects available for the selected code element. Selecting one of the aspect-related menu items shows a preview of how the aspect can be applied. Clicking on it automatically performs the code change. If the aspect requires any configuration or if required NuGet packages are not yet installed in the project, a wizard window pops up and it manages all the necessary steps. The list of aspects available in this menu can be configured via the `(Extensions >) PostSharp > Options > Code Actions` Visual&nbsp;Studio menu.


## How can a project or a solution be enhanced by PostSharp?

<img style="margin-right: 10px; margin-top: 0px; margin-left: 10px;" src="/assets/images/blog/2021-03-17-6-9-RC-announcement/05-solution-explorer.png" alt="Solution Explorer context menu items.">

In the project or solution context menu in the solution explorer, use the `Add > PostSharp policy` context menu item to apply an aspect to the whole project or solution. If PostSharp NuGet package is not yet installed in the project, it can be installed using the `Add PostSharp to project` context menu.


## Enhanced debugging experience

<img style="margin-right: 10px; margin-top: 0px; margin-left: 10px;" src="/assets/images/blog/2021-03-17-6-9-RC-announcement/06-debugging.png" alt="Enhanced debugging experience.">

Having the PostSharp Tools for Visual&nbsp;Studio installed allows to step into or over aspects and it improves the readability of the call stack shown in Visual&nbsp;Studio while debugging. The debugging experience can be customized via the `(Extensions >) PostSharp > Options > General > Debugging` Visual&nbsp;Studio menu.


## Setting PostSharp-specific project and solution properties

<img style="margin-right: 10px; margin-top: 0px; margin-left: 10px;" src="/assets/images/blog/2021-03-17-6-9-RC-announcement/07-project-properties.png" alt="PostSharp-scpecific project properties tab.">

PostSharp tab can be found in the project and solution properties windows allowing to adjust multiple PostSharp settings.


## Global PostSharp<br>and PostSharp Tools for Visual Studio<br>settings

<img style="margin-right: 10px; margin-top: 0px; margin-left: 10px;" src="/assets/images/blog/2021-03-17-6-9-RC-announcement/08-options.png" alt="PostSharp options window.">

Code Actions, License, Error Reporting, Customer Feedback, and other options can be configured via the `(Extensions >) PostSharp > Options` Visual&nbsp;Studio menu.


## Other features

<img style="margin-right: 10px; margin-top: 0px; margin-left: 10px;" src="/assets/images/blog/2021-03-17-6-9-RC-announcement/09-postsharp-menu.png" alt="PostSharp menu.">

More features, like learning and documentation resources, customer feedback and support, or solution-wide code enhancement metrics can be found in the `(Extensions >) PostSharp` Visual&nbsp;Studio menu.


## Summary

PostSharp Tools for Visual&nbsp;Studio improve the overall development experience when using&nbsp;PostSharp and Visual&nbsp;Studio for software development. It allows to better understand the&nbsp;PostSharp-enhanced source code, apply the PostSharp ready-made aspects automatically and&nbsp;it&nbsp;improves the debugging experience.

In PostSharp 6.9, the performance of the Visual&nbsp;Studio extension is improved significantly.

As always, it is a good time to update your VS extension and NuGet packages, and report any problem via our [support forum](https://support.postsharp.net/).  

Happy PostSharping!
