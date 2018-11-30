---
title: Revisa el acceso de Azure AD
description: Puede usar AD Azure tener acceso a las revisiones para configurar revisiones de acceso única o recurrente para la certificación de derechos de acceso del usuario.
ms.openlocfilehash: 33722c68429729e3996ad289d07146c95ee219ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087665"
---
# <a name="azure-ad-access-reviews"></a>Revisa el acceso de Azure AD

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede usar [AD Azure access revisa](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-azure-ad-controls-access-reviews-overview) para configurar única o periódica access revisa para certificación de derechos de acceso del usuario.

Revisa los escenarios típicos del cliente para el acceso de pertenencias a grupos y acceso a las aplicaciones son:
   
- Los clientes pueden revisar y certifica el acceso de usuarios invitado mediante el uso de revisiones de acceso de su acceso a las aplicaciones y la pertenencia a grupos. Los revisores pueden utilizar los conocimientos que se proporcionan con eficacia decidir si los invitados deben tengan un acceso continuado.
      
- Los clientes pueden revisar y certifica el acceso de los empleados a las aplicaciones y pertenencias a grupos con acceso a las revisiones.
   
- Los clientes pueden recopilar acceso a controles de revisión en los programas que son relevantes para su organización realizar el seguimiento de revisiones para cumplimiento de normas o aplicaciones sensibles de riesgo.

También es una capacidad relacionada para clientes revisar y certifica las asignaciones de roles de usuarios administrativos que se asignan a funciones de Azure AD como administrador Global o Azure roles de suscripción.  Esta capacidad se incluye en [la administración de identidades AD con privilegios de Azure](privilegedidentitymanagement-root.md).

Tenga en cuenta que la característica de revisiones de access, incluida la API, se incluye en Azure AD Premium P2. 

## <a name="methods"></a>Métodos

Ésta es la lista de los métodos proporcionados por Azure AD tener acceso a las revisiones.  

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener accessReview](../api/accessreview-get.md) |   [accessReview](accessreview.md) |   Obtenga una revisión de access con un identificador específico. |
|[Crear accessReview](../api/accessreview-create.md) | [accessReview](accessreview.md) |   Crear un nuevo accessReview. |
|[Eliminar accessReview](../api/accessreview-delete.md) | Ninguna.   | Eliminar un accessReview. |
|[Actualizar accessReview](../api/accessreview-update.md) | [accessReview](accessreview.md) | Actualizar un accessReview. |
|[Revisores accessReview de lista](../api/accessreview-listreviewers.md) |      colección de [IdentidadDeUsuario](useridentity.md)| Obtenga los revisores de un accessReview. |
|[Agregar revisor accessReview](../api/accessreview-addreviewer.md) |      Ninguna.   |   Agregar un revisor a una accessReview. |
|[Quitar accessReview revisor](../api/accessreview-removereviewer.md) | Ninguna.  |   Quitar un revisor de un accessReview. |
|[Lista decisiones de accessReview](../api/accessreview-listdecisions.md) |      colección de [accessReviewDecision](accessreviewdecision.md)| Obtenga las decisiones de un accessReview.|
|[Mis decisiones accessReview de lista](../api/accessreview-listmydecisions.md) |     colección de [accessReviewDecision](accessreviewdecision.md)| Como revisor, obtener Mis decisiones de un accessReview.|
|[Enviar aviso de accessReview](../api/accessreview-sendreminder.md) |        Ninguna.   |   Enviar un aviso a los revisores de un accessReview. |
|[Detener accessReview](../api/accessreview-stop.md) |     Ninguna.   |   Detener una accessReview. |
|[Restablecer las decisiones de accessReview](../api/accessreview-reset.md) |     Ninguna.   |   Restablecer las decisiones en un accessReview en curso.|
|[Aplicar decisiones accessReview](../api/accessreview-apply.md) |     Ninguna.   |   Se aplican las decisiones de un accessReview completado.|
|[Lista businessFlowTemplates](../api/businessflowtemplate-list.md) | colección de [businessFlowTemplate](businessflowtemplate.md)| Obtener las plantillas de flujo de negocio adecuados tener acceso a las revisiones.|
|[Creación de programa](../api/program-create.md) |   [programa](program.md)   |   Crear un nuevo programa.|
|[Eliminar programa](../api/program-delete.md) |   Ninguna.   |   Eliminar un programa.|
|[Programas de lista](../api/program-list.md) |  colección de [programa](program.md)|   Obtener una colección de todos los programas.|
|[ProgramControls de lista de un programa](../api/program-listcontrols.md) |      colección de [programControl](programcontrol.md)| Obtener una colección de los controles de un programa.|
|[Programa de actualización](../api/program-update.md) |   [programa](program.md)|  Actualizar un programa.|
|[Crear programControl](../api/programcontrol-create.md) |     [programControl](programcontrol.md) |   Agregar un programControl a un programa.|
|[Eliminar programControl](../api/programcontrol-delete.md) |     Ninguna.   |   Quitar un programControl de un programa.|
|[Lista programControls](../api/programcontrol-list.md) | colección de [programControl](programcontrol.md)| Controles de lista a través de todos los programas en el inquilino.|
|[Lista programControlTypes](../api/programcontroltype-list.md) | colección de [programControlType](programcontroltype.md)| Lista de tipos de control de programa. |


## <a name="see-also"></a>Vea también

- [Revisa cómo un administrador puede administrar el acceso de usuarios con acceso de Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-azure-ad-controls-manage-user-access-with-access-reviews)
- [Revisa cómo un administrador puede administrar el acceso de invitado con acceso de Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-azure-ad-controls-manage-guest-access-with-access-reviews)
- [Cómo un administrador puede administrar programas y controles para Azure AD obtener acceso a las revisiones](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-azure-ad-controls-manage-programs-controls)


<!-- {
  "type": "#page.annotation",
  "description": "Service root",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
