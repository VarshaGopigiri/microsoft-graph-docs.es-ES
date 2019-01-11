---
title: tipo de recurso bookingStaffMember
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 382da1b0710b691a6563a40c03ed62397262911d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884458"
---
# <a name="bookingstaffmember-resource-type"></a>tipo de recurso bookingStaffMember

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa a un miembro del personal que proporciona servicios en un [bookingBusiness](bookingbusiness.md).

Los miembros del personal pueden formar parte del inquilino de Office 355 donde está configurado el negocio de reserva, o bien pueden usar servicios de correo electrónico de otros proveedores de correo electrónico.

Cuando las citas de reserva, la API de reservas tiene en cuenta la siguiente configuración para determinar la disponibilidad de un miembro del personal: 

1. De forma predeterminada, las horas de operación de la empresa (la propiedad **businessHours** de la entidad [bookingBusiness](bookingbusiness.md) ) representa la disponibilidad general de los empleados.
2. Si **useBusinessHours** es false, horas de trabajo específicos de los empleados (**workingHours** (propiedad) de la entidad **bookingStaffmember** ) representa la disponibilidad general de dicho miembro.
3. Si **availabilityIsAffectedByPersonalCalendar** es true, a continuación, la API de reservas tendría en primer lugar buscar generalmente disponibles de las horas de los empleados (según determine #1 o 2 #) y comprobar la disponibilidad durante las horas de personal de los empleados calendario, antes de realizar una reserva.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Miembros del personal de lista](../api/bookingbusiness-list-staffmembers.md) | colección de [bookingStaffMember](bookingstaffmember.md) | Para obtener una lista de objetos de **bookingStaffMember** en el especificado [bookingbusiness](../resources/bookingbusiness.md). |
|[Crear bookingStaff](../api/bookingbusiness-post-staffmembers.md) | colección de [bookingStaffMember](bookingstaffmember.md) | Crear un nuevo **bookingStaffMember** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado. |
|[Obtener bookingStaffMember](../api/bookingstaffmember-get.md) | [bookingStaffMember](bookingstaffmember.md) |Obtener las propiedades y relaciones de un **bookingStaffMember** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.|
|[Update](../api/bookingstaffmember-update.md) | [bookingStaffMember](bookingstaffmember.md)    |Actualizar las propiedades de un **bookingStaffMember** en la [bookingbusiness](../resources/bookingbusiness.md)de especificado.|
|[Delete](../api/bookingstaffmember-delete.md) | Ninguno |Eliminar a un miembro del personal en el especificado [bookingbusiness](../resources/bookingbusiness.md). |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|availabilityIsAffectedByPersonalCalendar|Booleano|True significa que si el miembro del personal es un usuario de Office 365, la API de reservas debería comprobar disponibilidad de los empleados en su calendario personal en Office 365, antes de realizar una reserva. |
|colorIndex|Int32|Identifica un color para representar al miembro del personal. El color se corresponde con la paleta de colores en la página de **Detalles del personal** en la aplicación de reservas.|
|displayName|Cadena|El nombre del miembro del personal, tal como se muestra a los clientes. Necesario.|
|emailAddress|Cadena|La dirección de correo electrónico del miembro del personal. Esto puede ser en el mismo arrendatario de Office 365 como la empresa o en un dominio de correo electrónico diferentes. Se puede usar esta dirección de correo electrónico si la propiedad **sendConfirmationsToOwner** está establecida en true en la directiva de programación de la empresa. Necesario.|
|id|Cadena| El identificador del miembro del personal, en un formato GUID. Solo lectura.|
|role|string| La función del miembro del personal de la empresa. Los valores posibles son: `guest`, `administrator`, `viewer` y `externalGuest`. Necesario.|
|useBusinessHours|Booleano|True significa que la disponibilidad de los empleados es como especificado en la propiedad **businessHours** de la empresa. False significa que la disponibilidad está determinada por el valor de la propiedad **workingHours** de los empleados.|
|workingHours|colección de [bookingWorkHours](bookingworkhours.md)|El intervalo de horas de cada día de la semana en los que el miembro del personal está disponible para reserva. De forma predeterminada, se inicializan para ser la misma que la propiedad **businessHours** de la empresa.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingStaffMember"
}-->

```json
{
  "availabilityIsAffectedByPersonalCalendar": true,
  "colorIndex": 1024,
  "displayName": "String",
  "emailAddress": "String",
  "id": "String (identifier)",
  "role": "string",
  "useBusinessHours": true,
  "workingHours": [{"@odata.type": "microsoft.graph.bookingWorkHours"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingStaffMember resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
