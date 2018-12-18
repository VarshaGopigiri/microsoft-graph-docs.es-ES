---
title: tipo de recurso iosSingleSignOnSettings
description: configuración de autenticación de Kerberos para el inicio de sesión único de iOS
author: tfitzmac
ms.openlocfilehash: 6bde13865c1d6b34c433a92005681b247b99d984
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347372"
---
# <a name="iossinglesignonsettings-resource-type"></a><span data-ttu-id="51a08-103">tipo de recurso iosSingleSignOnSettings</span><span class="sxs-lookup"><span data-stu-id="51a08-103">iosSingleSignOnSettings resource type</span></span>

> <span data-ttu-id="51a08-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="51a08-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="51a08-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="51a08-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="51a08-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="51a08-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="51a08-107">configuración de autenticación de Kerberos para el inicio de sesión único de iOS</span><span class="sxs-lookup"><span data-stu-id="51a08-107">iOS Kerberos authentication settings for single sign-on</span></span>
## <a name="properties"></a><span data-ttu-id="51a08-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51a08-108">Properties</span></span>
|<span data-ttu-id="51a08-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51a08-109">Property</span></span>|<span data-ttu-id="51a08-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="51a08-110">Type</span></span>|<span data-ttu-id="51a08-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="51a08-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="51a08-112">allowedAppsList</span><span class="sxs-lookup"><span data-stu-id="51a08-112">allowedAppsList</span></span>|<span data-ttu-id="51a08-113">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="51a08-113">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="51a08-114">Lista de identificadores de aplicación que tienen permiso para utilizar este inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="51a08-114">List of app identifiers that are allowed to use this login.</span></span> <span data-ttu-id="51a08-115">Si se omite este campo, el inicio de sesión se aplica a todas las aplicaciones en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51a08-115">If this field is omitted, the login applies to all applications on the device.</span></span> <span data-ttu-id="51a08-116">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="51a08-116">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="51a08-117">allowedUrls</span><span class="sxs-lookup"><span data-stu-id="51a08-117">allowedUrls</span></span>|<span data-ttu-id="51a08-118">Colección String</span><span class="sxs-lookup"><span data-stu-id="51a08-118">String collection</span></span>|<span data-ttu-id="51a08-119">Lista de direcciones URL de HTTP que se debe coincidir con el fin de utilizar este inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="51a08-119">List of HTTP URLs that must be matched in order to use this login.</span></span> <span data-ttu-id="51a08-120">Con iOS 9.0 o posterior, se puede usar un carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="51a08-120">With iOS 9.0 or later, a wildcard characters may be used.</span></span>|
|<span data-ttu-id="51a08-121">displayName</span><span class="sxs-lookup"><span data-stu-id="51a08-121">displayName</span></span>|<span data-ttu-id="51a08-122">String</span><span class="sxs-lookup"><span data-stu-id="51a08-122">String</span></span>|<span data-ttu-id="51a08-123">El nombre para mostrar de la configuración de inicio de sesión que se muestra en el dispositivo receptor.</span><span class="sxs-lookup"><span data-stu-id="51a08-123">The display name of login settings shown on the receiving device.</span></span>|
|<span data-ttu-id="51a08-124">kerberosPrincipalName</span><span class="sxs-lookup"><span data-stu-id="51a08-124">kerberosPrincipalName</span></span>|<span data-ttu-id="51a08-125">String</span><span class="sxs-lookup"><span data-stu-id="51a08-125">String</span></span>|<span data-ttu-id="51a08-126">Un nombre principal de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="51a08-126">A Kerberos principal name.</span></span> <span data-ttu-id="51a08-127">Si no se proporciona, el usuario se le pida durante la instalación del perfil.</span><span class="sxs-lookup"><span data-stu-id="51a08-127">If not provided, the user is prompted for one during profile installation.</span></span>|
|<span data-ttu-id="51a08-128">kerberosRealm</span><span class="sxs-lookup"><span data-stu-id="51a08-128">kerberosRealm</span></span>|<span data-ttu-id="51a08-129">String</span><span class="sxs-lookup"><span data-stu-id="51a08-129">String</span></span>|<span data-ttu-id="51a08-130">Un nombre de territorio Kerberos.</span><span class="sxs-lookup"><span data-stu-id="51a08-130">A Kerberos realm name.</span></span> <span data-ttu-id="51a08-131">Distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="51a08-131">Case sensitive.</span></span>|

## <a name="relationships"></a><span data-ttu-id="51a08-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="51a08-132">Relationships</span></span>
<span data-ttu-id="51a08-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="51a08-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="51a08-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="51a08-134">JSON Representation</span></span>
<span data-ttu-id="51a08-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="51a08-135">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosSingleSignOnSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosSingleSignOnSettings",
  "allowedAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "allowedUrls": [
    "String"
  ],
  "displayName": "String",
  "kerberosPrincipalName": "String",
  "kerberosRealm": "String"
}
```





