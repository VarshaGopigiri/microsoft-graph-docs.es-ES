---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: PersonOrGroupColumn
ms.openlocfilehash: 715c6ca22957cbd951784e6cf32edf2bf47f1098
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="personorgroupcolumn-resource-type"></a>Tipo de recurso PersonOrGroupColumn

El recurso **personOrGroupColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de columna representan una persona o un grupo seleccionados del directorio.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **personOrGroupColumn**.
<!-- { "blockType": "resource", "@type": "microsoft.graph.personOrGroupColumn", "@property.aka": "chooseFromType=format" } -->

```json
{
  "allowMultipleSelection": true,
  "displayAs": "account | contentType | created | department | ...",
  "chooseFromType": "peopleAndGroups | peopleOnly"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad              | Tipo    | Descripción
|:---------------------------|:--------|:--------------------------------------
| **allowMultipleSelection** | boolean | Indica si se pueden seleccionar varios valores desde el origen.
| **displayAs**              | string  | Cómo mostrar la información sobre la persona o el grupo elegido. Véalo a continuación.
| **chooseFromType**         | string  | Si quiere permitir la selección solo de personas, o de personas y grupos. Debe ser `peopleAndGroups` o `peopleOnly`.

## <a name="displayas-values"></a>Valores displayAs

| Valor displayAs               | Descripción
|:------------------------------|:-----------------------
| **account**                   | La cadena de notificación codificada de SharePoint sin formato de la persona o el grupo (por ejemplo, i:0#.f|pertenencia|jane@contoso.com).
| **department**                | Departamento de la persona o el grupo.
| **firstName**                 | Nombre de la persona.
| **id**                        | Identificador de la persona o el grupo en el directorio.
| **lastName**                  | Apellido de la persona.
| **mobilePhone**               | Número de teléfono móvil de la persona.
| **name**                      | Nombre de la persona.
| **nameWithPictureAndDetails** | Nombre de la persona junto con su imagen y detalles adicionales.
| **nameWithPresence**          | Valor predeterminado. Nombre de la persona con un icono de indicador de presencia (disponible/ocupado/etc.).
| **office**                    | Número de la oficina de la persona.
| **pictureOnly36x36**          | Imagen de la persona, delimitado por un cuadrado de 36x36 píxeles.
| **pictureOnly48x48**          | Imagen de la persona, delimitado por un cuadrado de 48x48 píxeles.
| **pictureOnly72x72**          | Imagen de la persona, delimitado por un cuadrado de 72x72 píxeles.
| **sipAddress**                | Dirección SIP de la persona.
| **title**                     | Puesto de la persona en la organización.
| **userName**                  | Nombre de usuario de la persona o el grupo.
| **workEmail**                 | Dirección de correo electrónico de la persona o el grupo.
| **workPhone**                 | Número de teléfono del trabajo de la persona.

Nota: Se pueden devolver tipos DisplayAs adicionales.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/PersonOrGroupColumn"
} -->
