﻿---
title: Общедоступный API Изменения в Aspose.Diagram 4.2.0
type: docs
weight: 30
url: /ru/net/public-api-changes-in-aspose-diagram-4-2-0/
---
{{% alert color="primary" %}} 

В этом документе описаны изменения в Aspose.Diagram API с версии 4.1.0 до 4.2.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные общедоступные методы, но и описание любых изменений в поведении за кулисами в Aspose.Diagram.

{{% /alert %}} 
## **Добавляет два метода GetMasterByName и IsExist в MasterCollection.**
Теперь разработчики могут склеивать групповые фигуры внутри контейнера. Также этот релиз позволяет получить Мастер по его имени и проверить наличие Мастера по его имени. Вы можете просмотреть примеры тем, посвященных этим функциям: [Получить мастер-объект из Visio], [Проверить наличие мастера в чертеже Visio]## **Добавляет метод GlueShapesInContainer на страницу**
Раньше он отлично работал с разгруппированными фигурами. Тем не менее, в групповых формах много точек, это не было так хорошо поддержано. Теперь мы добавили поддержку групповых фигур. См. пример темы об этой функции: [Форма группы приклеивания внутри контейнера]