---
title: tipo de recurso bookingBusiness
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 0ea11dcd16a129e6d6648be4b09435c5c052de9e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086756"
---
# <a name="bookingbusiness-resource-type"></a>tipo de recurso bookingBusiness

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.
 
Representa una empresa en Microsoft Bookings. Esto es el objeto de nivel superior de la API de reservas de Microsoft. Contiene información de la empresa y los objetos de negocio relacionados, como las citas, los clientes, servicios y los miembros del personal.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista bookingBusinesses](../api/bookingbusiness-list.md) | colección de [bookingBusiness](bookingbusiness.md) |Obtener una colección de objetos de bookingbusiness en el inquilino. |
|[Crear bookingBusiness](../api/bookingbusiness-post-bookingbusinesses.md) | [bookingBusiness](bookingbusiness.md) | Crear un nuevo negocio de Microsoft Bookings. |
|[Obtener bookingBusiness](../api/bookingbusiness-get.md) | [bookingBusiness](bookingbusiness.md) |Leer las propiedades y las relaciones del objeto bookingBusiness.|
|[Update](../api/bookingbusiness-update.md) | [bookingBusiness](bookingbusiness.md) |Actualizar las propiedades de un objeto **bookingBusiness** . |
|[Delete](../api/bookingbusiness-delete.md) | Ninguno |Eliminar un objeto **bookingBusiness** . |
|[Crear bookingAppointment](../api/bookingbusiness-post-appointments.md) |[bookingAppointment](bookingappointment.md)| Crear un nuevo bookingAppointment por la publicación de la colección de citas.|
|[Citas de lista](../api/bookingbusiness-list-appointments.md) |colección de [bookingAppointment](bookingappointment.md)| Obtener una colección de objetos bookingAppointment.|
|[Crear bookingCustomer](../api/bookingbusiness-post-customers.md) |[bookingCustomer](bookingcustomer.md)| Crear un nuevo bookingCustomer por la publicación de la colección de los clientes.|
|[Clientes de la lista](../api/bookingbusiness-list-customers.md) |colección de [bookingCustomer](bookingcustomer.md)| Obtener una colección de objetos bookingCustomer.|
|[Crear bookingService](../api/bookingbusiness-post-services.md) |[bookingService](bookingservice.md)| Crear un nuevo bookingService por la publicación de la colección de servicios.|
|[Servicios de la lista](../api/bookingbusiness-list-services.md) |colección de [bookingService](bookingservice.md)| Obtener una colección de objetos bookingService.|
|[Crear bookingStaffMember](../api/bookingbusiness-post-staffmembers.md) |[bookingStaffMember](bookingstaffmember.md)| Crear un nuevo bookingStaffMember por la publicación de la colección staffMembers.|
|[Lista staffMembers](../api/bookingbusiness-list-staffmembers.md) |colección de [bookingStaffMember](bookingstaffmember.md)| Obtener una colección de objetos bookingStaffMember.|
|[Lista de calendarView](../api/bookingbusiness-list-calendarview.md)|colección de [bookingAppointment](bookingappointment.md)|Obtener la colección de objetos **bookingAppointment** que se produce en el intervalo de fechas especificado.|
|[publicar](../api/bookingbusiness-publish.md)|Ninguno|Ponga la página programación de este negocio a disposición de los clientes externos. Establezca la propiedad **isPublished** en true y la propiedad **publicUrl** a la dirección URL de la página de programación.|
|[Cancelar la publicación](../api/bookingbusiness-unpublish.md)|Ninguno| Hacer que la página programación de esta empresa no está disponible para los clientes externos. Establezca la propiedad **isPublished** en false y la propiedad **publicUrl** en null.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|address|[physicalAddress](physicaladdress.md)|La dirección de la empresa. La propiedad **address** , junto con el **teléfono** y **webSiteUrl**, aparecen en el pie de página de un página de programación de negocio.|
|businessHours|colección de [bookingWorkHours](bookingworkhours.md)|Las horas de operación para la empresa.|
|businessType|String|El tipo de negocio.|
|defaultCurrencyIso|String|El código para la moneda que la empresa opera en Microsoft Bookings.|
|displayName|String|El nombre de la empresa, las interfaces con los clientes. Este nombre aparece en la parte superior de la página de programación de empresa.|
|email|String|La dirección de correo electrónico para el negocio.|
|id|String|Un identificador de programación único para el negocio. Solo lectura.|
|isPublished|Booleano|La página de programación se realizó disponible para los clientes externos. Use las acciones de **Publicar** y **Cancelar la publicación** para establecer esta propiedad. Solo lectura.|
|phone|String|El número de teléfono para el negocio. La propiedad de **teléfono** , junto con la **dirección** y **webSiteUrl**, aparecen en el pie de página de un página de programación de negocio.|
|publicUrl|String|La dirección URL de la página de programación, que se establece después de [Publicar](../api/bookingbusiness-publish.md) o [Cancelar la publicación de](../api/bookingbusiness-unpublish.md) la página. Solo lectura.|
|schedulingPolicy|[bookingSchedulingPolicy](bookingschedulingpolicy.md)|Especifica cómo se pueden crear reservas para este negocio.|
|webSiteUrl|String|La dirección URL del sitio web de negocio. La propiedad **webSiteUrl** , junto con la **dirección**, **teléfono**, aparecen en el pie de página de una página de programación de negocio.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|appointments|colección de [bookingAppointment](bookingappointment.md)| Todas las citas de esta empresa. Solo lectura. Admite valores NULL.|
|calendarView|colección de [bookingAppointment](bookingappointment.md)| El conjunto de citas de esta empresa en un intervalo de fechas especificado. Solo lectura. Admite valores NULL.|
|clientes|colección de [bookingCustomer](bookingcustomer.md)| Todos los clientes de este negocio. Solo lectura. Admite valores NULL.|
|servicios|colección de [bookingService](bookingservice.md)| Todos los servicios ofrecidos por esta empresa. Solo lectura. Admite valores NULL.|
|staffMembers|colección de [bookingStaffMember](bookingstaffmember.md)| Todos los personal miembros que proporcionan servicios en este negocio. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Esta es una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingBusiness"
}-->

```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "businessHours": [{"@odata.type": "microsoft.graph.bookingWorkHours"}],
  "businessType": "String",
  "defaultCurrencyIso": "String",
  "displayName": "String",
  "email": "String",
  "id": "String (identifier)",
  "isPublished": true,
  "phone": "String",
  "publicUrl": "String",
  "schedulingPolicy": {"@odata.type": "microsoft.graph.bookingSchedulingPolicy"},
  "webSiteUrl": "String"
}

```

## <a name="see-also"></a>Vea también


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingBusiness resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->