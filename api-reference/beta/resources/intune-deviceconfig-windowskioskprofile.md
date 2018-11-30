---
title: tipo de recurso windowsKioskProfile
description: Todavía no documentado
ms.openlocfilehash: 074c6caa9b632016f092f67192064ae18e9dcce3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084934"
---
# <a name="windowskioskprofile-resource-type"></a><span data-ttu-id="f6336-103">tipo de recurso windowsKioskProfile</span><span class="sxs-lookup"><span data-stu-id="f6336-103">windowsKioskProfile resource type</span></span>

> <span data-ttu-id="f6336-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f6336-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f6336-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f6336-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f6336-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6336-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6336-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f6336-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="f6336-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6336-108">Properties</span></span>
|<span data-ttu-id="f6336-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6336-109">Property</span></span>|<span data-ttu-id="f6336-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6336-110">Type</span></span>|<span data-ttu-id="f6336-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6336-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f6336-112">ID de perfil</span><span class="sxs-lookup"><span data-stu-id="f6336-112">profileId</span></span>|<span data-ttu-id="f6336-113">String</span><span class="sxs-lookup"><span data-stu-id="f6336-113">String</span></span>|<span data-ttu-id="f6336-114">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f6336-114">Key of the entity.</span></span>|
|<span data-ttu-id="f6336-115">nombre del perfil</span><span class="sxs-lookup"><span data-stu-id="f6336-115">profileName</span></span>|<span data-ttu-id="f6336-116">String</span><span class="sxs-lookup"><span data-stu-id="f6336-116">String</span></span>|<span data-ttu-id="f6336-117">Esto es un nombre descriptivo usado para identificar un grupo de aplicaciones, el diseño de estas aplicaciones en el menú Inicio y los usuarios a quienes se asigna esta configuración de quiosco.</span><span class="sxs-lookup"><span data-stu-id="f6336-117">This is a friendly name used to identify a group of applications, the layout of these apps on the start menu and the users to whom this kiosk configuration is assigned.</span></span>|
|<span data-ttu-id="f6336-118">appConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6336-118">appConfiguration</span></span>|[<span data-ttu-id="f6336-119">windowsKioskAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6336-119">windowsKioskAppConfiguration</span></span>](../resources/intune-deviceconfig-windowskioskappconfiguration.md)|<span data-ttu-id="f6336-120">La configuración de aplicación que se usará para esta configuración de quiosco.</span><span class="sxs-lookup"><span data-stu-id="f6336-120">The App configuration that will be used for this kiosk configuration.</span></span>|
|<span data-ttu-id="f6336-121">userAccountsConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6336-121">userAccountsConfiguration</span></span>|<span data-ttu-id="f6336-122">colección de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="f6336-122">[windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md) collection</span></span>|<span data-ttu-id="f6336-123">Las cuentas de usuario que se bloqueará a esta configuración de quiosco.</span><span class="sxs-lookup"><span data-stu-id="f6336-123">The user accounts that will be locked to this kiosk configuration.</span></span> <span data-ttu-id="f6336-124">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="f6336-124">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f6336-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f6336-125">Relationships</span></span>
<span data-ttu-id="f6336-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f6336-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f6336-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f6336-127">JSON Representation</span></span>
<span data-ttu-id="f6336-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f6336-128">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskProfile",
  "profileId": "String",
  "profileName": "String",
  "appConfiguration": {
    "@odata.type": "microsoft.graph.windowsKioskMultipleApps",
    "apps": [
      {
        "@odata.type": "microsoft.graph.windowsKioskUWPApp",
        "startLayoutTileSize": "String",
        "name": "String",
        "appUserModelId": "String",
        "appId": "String",
        "containedAppId": "String"
      }
    ],
    "showTaskBar": true,
    "disallowDesktopApps": true,
    "startMenuLayoutXml": "binary"
  },
  "userAccountsConfiguration": [
    {
      "@odata.type": "microsoft.graph.windowsKioskVisitor"
    }
  ]
}
```




