---
title: Administrar sesiones y persistencia Excel con Microsoft Graph
description: Si la aplicación necesita hacer más de una o dos llamadas a la API de Excel, debería crear una sesión y pasar el identificador de sesión con cada solicitud. La presencia de un identificador de sesión en las solicitudes asegura que usa la API de Excel de la manera más eficiente posible.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 151119a2a2861b64db126c8f49d0b916a6f563e8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921692"
---
# <a name="manage-sessions-and-persistence-in-excel-with-microsoft-graph"></a>Administrar sesiones y persistencia Excel con Microsoft Graph

Si la aplicación necesita hacer más de una o dos llamadas a la API de Excel, debería crear una sesión y pasar el identificador de sesión con cada solicitud. La presencia de un identificador de sesión en las solicitudes asegura que usa la API de Excel de la manera más eficiente posible.

Se puede llamar a las API de Excel de tres modos:

1. **Sesión persistente** Todos los cambios realizados en el libro son persistentes (se guardan) en el libro. Esta es la forma más eficaz y que ofrece un mejor rendimiento para usar la API de Excel.
2. **Sesión no persistente** Los cambios realizados por la API no se guardan en la ubicación de origen. En su lugar, el servidor backend de Excel conserva una copia temporal del archivo que refleja los cambios realizados durante esa sesión API en concreto. Cuando expira la sesión de Excel, se pierden los cambios. Este modo es útil para aplicaciones que necesitan realizar análisis u obtener los resultados de un cálculo de una imagen de gráfico, pero no necesitan afectar al estado de documento.
3. **Sin sesión** Las llamadas a la API no pasan un identificador de sesión. Los servidores de Excel deben buscar la copia del servidor del libro para cada operación. No es una forma eficaz para llamar a la API de Excel, pero es adecuada para hacer ciertos tipos de solicitudes aisladas.

Para representar la sesión en la API, utilice el encabezado `workbook-session-id: {session-id}`.

>**Nota:** El encabezado de sesión no es necesario para que funcione una API de Excel. Sin embargo, recomendamos que utilice el encabezado de sesión para mejorar el rendimiento. Si no utiliza un encabezado de sesión, los cambios realizados durante la llamada API _sí_ persisten en el archivo.  

## <a name="next-step"></a>Paso siguiente
Para obtener información sobre cómo crear y usar sesiones, consulte el [tema de referencia sobre creación de sesiones](/graph/api/workbook-createsession?view=graph-rest-1.0).

## <a name="see-also"></a>Vea también
* [Escribir en un libro de Excel con Microsoft Graph](excel-write-to-workbook.md)
* [Usar funciones de libro en Excel con Microsoft Graph](excel-use-functions.md)
* [Actualizar el formato de un rango en Excel con Microsoft Graph](excel-update-range-format.md)
* [Mostrar una imagen de gráfico de Excel con Microsoft Graph](excel-display-chart-image.md)
* [Usar la API de REST de Excel](/graph/api/resources/excel?view=graph-rest-1.0)
