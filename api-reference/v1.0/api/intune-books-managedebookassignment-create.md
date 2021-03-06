---
title: Crear managedEBookAssignment
description: Cree un objeto managedEBookAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4756c95fb9ebba3125c3a3dbbbdb82ec7d76c111
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967444"
---
# <a name="create-managedebookassignment"></a>Crear managedEBookAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Cree un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementApps.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto managedEBookAssignment.

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedEBookAssignment.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|El destino de la asignación para el libro electrónico.|
|installIntent|[installIntent](../resources/intune-shared-installintent.md)|El objetivo de instalación para el libro electrónico. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
Content-type: application/json
Content-length: 194

{
  "@odata.type": "#microsoft.graph.managedEBookAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 243

{
  "@odata.type": "#microsoft.graph.managedEBookAssignment",
  "id": "ae8b0d27-0d27-ae8b-270d-8bae270d8bae",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```



