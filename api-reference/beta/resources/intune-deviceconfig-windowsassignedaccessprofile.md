---
title: tipo de recurso windowsAssignedAccessProfile
description: Perfil de acceso asignado para Windows.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 893e81e544286c6877b9443d96f610acb939e934
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972855"
---
# <a name="windowsassignedaccessprofile-resource-type"></a>tipo de recurso windowsAssignedAccessProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Perfil de acceso asignado para Windows.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista windowsAssignedAccessProfiles](../api/intune-deviceconfig-windowsassignedaccessprofile-list.md)|colección de [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md)|Propiedades de la lista y relaciones de los objetos [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) .|
|[Obtener windowsAssignedAccessProfile](../api/intune-deviceconfig-windowsassignedaccessprofile-get.md)|[windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md)|Leer las propiedades y las relaciones del objeto [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) .|
|[Crear windowsAssignedAccessProfile](../api/intune-deviceconfig-windowsassignedaccessprofile-create.md)|[windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md)|Crear un nuevo objeto [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) .|
|[Eliminar windowsAssignedAccessProfile](../api/intune-deviceconfig-windowsassignedaccessprofile-delete.md)|Ninguno|Elimina un [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md).|
|[Actualizar windowsAssignedAccessProfile](../api/intune-deviceconfig-windowsassignedaccessprofile-update.md)|[windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md)|Actualizar las propiedades de un objeto [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|nombre del perfil|Cadena|Esto es un nombre descriptivo usado para identificar un grupo de aplicaciones, el diseño de estas aplicaciones en el menú Inicio y los usuarios a quienes se asigna esta configuración de quiosco.|
|showTaskBar|Booleano|Esta opción le permite al administrador especificar si se muestra la barra de tareas o no.|
|appUserModelIds|Colección String|Estos son el único almacén de aplicaciones de Windows que estará disponible para iniciar desde el menú Inicio.|
|desktopAppPaths|Colección String|Estas son las rutas de acceso de las aplicaciones de escritorio que estará disponible en el menú Inicio y las aplicaciones sólo el usuario podrá iniciar.|
|cuentas de usuario|Colección String|Las cuentas de usuario que se bloqueará a esta configuración de quiosco.|
|startMenuLayoutXml|Binario|Permite a los administradores invalidar el diseño de inicio predeterminado y se evita que el usuario que lo modifique.Para modificar el diseño, se especifica un archivo XML basado en el esquema de modificación del diseño. XML debe estar en formato binario.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsAssignedAccessProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsAssignedAccessProfile",
  "id": "String (identifier)",
  "profileName": "String",
  "showTaskBar": true,
  "appUserModelIds": [
    "String"
  ],
  "desktopAppPaths": [
    "String"
  ],
  "userAccounts": [
    "String"
  ],
  "startMenuLayoutXml": "binary"
}
```





