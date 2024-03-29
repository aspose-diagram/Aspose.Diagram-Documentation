﻿---
title: Открыть документ Visio программно
linktitle: Открыть документ Visio
type: docs
weight: 20
url: /ru/java/open-visio-document/
description: На этой странице описывается, как открыть документ Visio с нуля с помощью библиотеки Aspose.Diagram.
---
## **Чтение существующего чертежа Visio**
Aspose.Diagram API поддерживает создание новых диаграмм Visio с нуля и последующее сохранение в любом поддерживаемом формате файла. Разработчики также могут загрузить существующий Visio diagram для модификации, добавления или обработки.
### **Чтение Diagram**
Используя Aspose.Diagram API, разработчики могут загружать все поддерживаемые форматы файлов Visio. Доступные конструкторы класса Diagram позволяют это сделать, и они принимают допустимую строку пути к файлу или файловый поток исходного файла Visio.

Поддерживаются следующие читаемые форматы файлов:
**VSDX, VSD, VSDM, ВСС, VSSM, VSSX, VTX, VDX, VDW, VST, VSTX, VSTM и VSX**

Конструкторы класса diagram также предлагают необязательный параметр, определяющий LoadFileFormat или LoadOptions. Это информация о предварительной загрузке, которую разработчики могут передавать по телефону Aspose.Diagram API. Мы рекомендуем передавать реалистичную информацию для достижения идеальной производительности.
#### **Чтение Diagram Пример программирования**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ReadVisioDiagram-ReadVisioDiagram.java" >}}
