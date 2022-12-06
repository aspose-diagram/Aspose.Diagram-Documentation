---
title: Общедоступный API Изменения в Aspose.Diagram 5.7.0
type: docs
weight: 30
url: /ru/net/public-api-changes-in-aspose-diagram-5-7-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 5.6.0 до 5.7.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Установите строки шаблона даты на временной шкале**
В класс TimelineHelper добавлены новые свойства DateFormatStringForBE и DateFormatStringForIntm. Примеры кодов:

**C#**

{{< highlight "java" >}}

 // set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd";

// set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd";

{{< /highlight >}}

**ВБ**

{{< highlight "java" >}}

 ' set DateFormat String for start and finish of timeline shape

timelineHelper.DateFormatStringForBE = "yyyy-MM-dd"

' set DateFormat String for intm of timeline shape

timelineHelper.DateFormatStringForIntm = "yyyy-MM-dd"

{{< /highlight >}}
