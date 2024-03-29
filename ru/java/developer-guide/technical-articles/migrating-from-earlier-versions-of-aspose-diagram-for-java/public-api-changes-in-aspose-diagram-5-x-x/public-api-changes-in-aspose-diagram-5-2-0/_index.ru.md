﻿---
title: Общедоступный API Изменения в Aspose.Diagram 5.2.0
type: docs
weight: 50
url: /ru/java/public-api-changes-in-aspose-diagram-5-2-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 2.3.0 до 5.2.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
### **Укажите расположение шрифтов**
В класс TimeLineHelper добавлен новый метод setFontDirs. Это позволяет разработчикам указывать расположение своих собственных или сторонних папок со шрифтами. Пользователи могут ознакомиться с примером раздела об этой функции: [Как указать расположение шрифтов TrueType]### **Изменение внешнего вида формы типа соединителя**
Разработчики теперь могут программно управлять внешним видом формы типа соединителя. Подробнее об этой функции см. в следующем разделе справки: [Установить внешний вид формы типа соединителя в Visio].### **Обновить вехи на временной шкале**
Добавлен новый метод refreshTimeLine в классе TimeLineHelper. В следующем разделе справки показано, как разработчики могут обновлять вехи на временной шкале: [Обновить вехи на временной шкале в Visio]### **Установка имени принтера и документа**
Мы добавили еще один метод печати в класс Diagram, который отправляет задания на печать на принтер. Он принимает имя принтера и документа в качестве параметров.
