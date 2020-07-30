---
title : "Why not Automation" 
description : "" 
weight : 8011 
toc : false
type: docs
url: /java/gettingstarted/why+not+automation/
---

# Aspose.Diagram for Java : Why not Automation


Why are Aspose APIs a much better option than Microsoft Office Automation?

There are two questions that we hear most often here at Aspose:

1.  **Do your products require Microsoft Office to be installed in order for them to run?**  
    The simple answer is no. Aspose APIs are totally independent and are not affiliated with, nor authorized, sponsored, or otherwise approved by Microsoft Corporation.
2.  **Why should we use Aspose products rather than utilizing Microsoft Office automation?**  
    The shortest answer we could give is that there are many reasons, with the main one being that Microsoft themselves strongly recommends against Office automation from software solutions: [Considerations for server-side Automation of Office](https://support.microsoft.com/en-us/help/257757/considerations-for-server-side-automation-of-office).

There are several reasons why Aspose APIs are a better alternative to automation. Some of the key reasons are:

*   [Security](https://docs2.aspose.com/diagram/java/gettingstarted/why+not+automation)
*   [Stability](https://docs2.aspose.com/diagram/java/gettingstarted/why+not+automation)
*   [Scalability/Speed](https://docs2.aspose.com/diagram/java/gettingstarted/why+not+automation)
*   [Price](https://docs2.aspose.com/diagram/java/gettingstarted/why+not+automation)
*   [Features](https://docs2.aspose.com/diagram/java/gettingstarted/why+not+automation)

The key points are described below. Also, be sure to visit the links at the end of this section.

### Security

The following is a direct quote from the above-referenced Microsoft article: *"Office Applications were never intended for use server-side, and therefore do not take into consideration the security problems that are faced by distributed components. Office does not authenticate incoming requests, and does not protect you from unintentionally running macros, or starting another server that might run macros, from your server-side code. Do not open files that are uploaded to the server from an anonymous Web! Based on the security settings that were last set, the server can run macros under an Administrator or System context with full privileges and compromise your network! In addition, Office uses many client-side components (such as Simple MAPI, WinInet, and MSDAIPP) that can cache client authentication information in order to speed up processing. If Office is being automated server-side, one instance may service more than one client, and because authentication information has been cached for that session, it is possible that one client can use the cached credentials of another client, and thereby gain non-granted access permissions by impersonating other users."*

Aspose products are very secure. Aspose APIs run in the same user context as all .NET and Java applications. Therefore, Aspose APIs do not pose a potential risk to vital system resources. Furthermore, when a document is opened by an Aspose API, macros are not automatically run. Aspose APIs were built with the goal of allowing developers to create, manipulate and save Office files. None of the risks associated with the Microsoft Office package are inherent to Aspose APIs.

### Stability

The following is a direct quote from the above referenced Microsoft article: *"Office 2000, Office XP, and Office 2003 use Microsoft Windows Installer (MSI) technology to make installation and self-repair easier for an end user. MSI introduces the concept of "install on first use", which allows features to be dynamically installed or configured at runtime (for the system, or more often for a particular user). In a server-side environment this both slows down performance and increases the likelihood that a dialog box may appear that asks for the user to approve the install or provide an appropriate install disk. Although it is designed to increase the resiliency of Office as an end-user product, Office's implementation of MSI capabilities is counterproductive in a server-side environment. Furthermore, the stability of Office in general cannot be assured when run server-side because it has not been designed or tested for this type of use. Using Office as a service component on a network server may reduce the stability of that machine and as a consequence your network as a whole. If you plan to automate Office server-side, attempt to isolate the program to a dedicated computer that cannot affect critical functions, and that can be restarted as needed."*

Since Aspose APIs are packaged into a single library, there will never be a need to install any additional parts or pieces for them to function. Aspose APIs are utilized by various applications and there is no portion of the API code designed to wait on a human response. Aspose APIs have been thoroughly tested. Aspose APIs are used by companies such as IBM , Hilton , Reader's Digest, Bank of America and many more.

### Scalability/Speed

The following is a direct quote from the above referenced Microsoft article: *"Server-side components need to be highly reentrant, multi-threaded COM components with minimum overhead and high throughput for multiple clients. Office Applications are in almost all respects the exact opposite. They are non-reentrant, STA-based Automation servers that are designed to provide diverse but resource-intensive functionality for a single client. They offer little scalability as a server-side solution, and have fixed limits to important elements, such as memory, which cannot be changed through configuration. More importantly, they use global resources (such as memory mapped files, global add-ins or templates, and shared Automation servers), which can limit the number of instances that can run concurrently and lead to race conditions if they are configured in a multi-client environment. Developers who plan to run more than one instance of any Office Application at the same time need to consider "pooling" or serializing access to the Office Application to avoid potential deadlocks or data corruption."*

Aspose APIs are highly scalable and lightning fast. Office applications were not designed to be simultaneously used by hundreds and thousands of users; however, Aspose APIs are designed for just that. Our APIs are a true solution and perform flawlessly whether on a single server powering a single application or on a load balanced web farm powering an enterprise wide application.

### Price

When an application utilizes Microsoft Office automation, a copy of Microsoft Office must be purchased for each machine that runs the application. There are many times that an application may need to create or manipulate an office file, but does not require the user to have Office. Aspose offers a very [cost effective](https://purchase.aspose.com/), royalty free, redistribution license that will allow deployment to an unlimited number of users with no licensing worries.

When creating web based applications it is important to know that Microsoft Office automation components are not priced nor licensed for server side solutions; therefore, there is no good, licensing solution for deploying web applications that utilize the Microsoft Office components. Aspose offers a very cost effective solution for server based applications as well.

### Features

Aspose components provide everything needed for managing Office files, plus much, much more. They are designed with the philosophy of allowing developers to accomplish the greatest results with the least amount of work. Unlike Office automation, Aspose components provide many powerful, time-saving functions. For instance, [Aspose.Diagram](https://repository.aspose.com/repo/com/aspose/aspose-diagram/) offers developers the ability to export from a **DataTable** or **DataView** directly into an Excel File. [Every component](https://products.aspose.com/total) in the Aspose family offers their own set of unique, powerful features.

The best part of purchasing an Aspose API or a API suite is having access to our development teams. Our development teams realize that if there is a feature that your company needs, more than likely other companies will need it as well. While not every feature request can be added, our teams try to be very open-minded and flexible when providing assistance. That mindset is what has helped Aspose APIs to become as powerful as they are. If there are additional features that you need from Office automation objects, your chances of having them added are very, very low.

### Conclusion

This article has covered the key points as to why Aspose APIs are a better choice than Office automation. All of the different Aspose APIs offer a risk free, no obligation [evaluation version](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-diagram). We encourage you to take advantage of that evaluation in order to see what Aspose can do for your applications.

For more information, please navigate to this Internet article:

*   [Considerations for Server-Side Automation of Office](https://support.microsoft.com/en-us/help/257757/considerations-for-server-side-automation-of-office)

## Attachments:

![](https://docs2.aspose.com/diagram/java/images/icons/bullet_blue.gif) [Aspose-Diagram-for-Java.png](https://docs2.aspose.com/diagram/java/attachments/18612326/18808841.png) (image/png)  

