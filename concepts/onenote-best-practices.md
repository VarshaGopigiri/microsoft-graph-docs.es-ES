---
title: Procedimientos recomendados para trabajar con las API de OneNote en Microsoft Graph.
description: Este artículo proporciona recomendaciones para el trabajo con las API de OneNote en Microsoft Graph. Estas recomendaciones se basan en respuestas a preguntas comunes que se hacen en Stack Overflow y Twitter.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: 95c135ec405764a53f06fed2f9ac2dde6b4138bd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972253"
---
# <a name="best-practices-for-working-with-the-onenote-api-in-microsoft-graph"></a>Procedimientos recomendados para trabajar con las API de OneNote en Microsoft Graph.

Este artículo proporciona recomendaciones para el trabajo con las API de OneNote en Microsoft Graph. Estas recomendaciones se basan en respuestas a preguntas comunes que se hacen en Stack Overflow y Twitter.

## <a name="use-select-to-select-the-minimum-set-of-properties-you-need"></a>Use $select para seleccionar el conjunto mínimo de propiedades que necesita.

Cuando consulta un recurso (por ejemplo, las secciones dentro de un bloc de notas), realiza una solicitud similar a la siguiente.

```http
GET ~/notebooks/{id}/sections
```

Esto recupera todas las propiedades de las secciones. Pero puede que no necesite todas las propiedades. Puede usar el parámetro de consulta `$select` para que devuelva solo las propiedades que quiera, como se muestra en el siguiente ejemplo de consulta.

```http
GET ~/notebooks/{id}/sections?$select=id,displayName
```

El mismo enfoque se aplica a otras API de OneNote.

## <a name="use-expand-instead-of-making-multiple-api-calls"></a>Use $expand en lugar de realizar varias llamadas a la API.

Supongamos que quiere recuperar todos los grupos de sección, secciones y blocs de notas del usuario en una vista jerárquica. Pueden conseguirlo mediante el procedimiento siguiente:

* Llame a `GET ~/notebooks` para obtener la lista de blocs de notas.

* Para todos los blocs de notas recuperados, llame a `GET ~/notebooks/{notebookId}/sections` para recuperar la lista de secciones.

* Para todos los blocs de notas recuperados, llame a `GET ~/notebooks/{notebookId}/sectionGroups` para recuperar la lista de grupos de secciones.

* Opcionalmente, itere recursivamente por los grupos de sección.

Aunque esto funcionará (con algunos ciclos de ida y vuelta al servicios adicionales), un enfoque mejor es usar el parámetro de consulta `$expand`. 

```http
GET ~/notebooks?$expand=sections,sectionGroups($expand=sections)
```

Esto producirá los mismos resultados en un solo ciclo de ida y vuelta, con un mejor rendimiento.

## <a name="when-getting-all-pages-for-a-user-do-so-for-each-section-separately"></a>Cuando quiera obtener todas las páginas de un usuario, hágalo para cada sección por separado

Aunque Microsoft Graph expone un punto de conexión para recuperar todas las páginas, esta no es la mejor forma de obtener todas las páginas a las que tiene acceso el usuario. Cuando el usuario tiene demasiadas secciones, esto puede conducir a tiempos de espera o a un rendimiento incorrecto. Es mejor recorrer en iteración cada sección, y obtener las páginas para cada uno de ellos por separado.

Por ejemplo, en lugar de usar esta llamada (se pagina esta API, por lo que no podrá recuperar todas las páginas a la vez):

```http
GET ~/pages
```

Es mejor usar la siguiente llamada varias veces (especialmente si no necesita todas las secciones):

```http
GET ~/sections/{id}/pages
```

Si se obtienen los metadatos de la página, se anula el orden predeterminado de `lastModifiedDateTime`. Es más rápido obtener las páginas cuando hay que ordenarlas por `lastModifiedDateTime`. Para ello, puede ordenarlas por cualquier otra propiedad; por ejemplo:

```http
GET ~/sections/{id}/pages?$select=id,title,createdDateTime&$orderby=createdDateTime
```
