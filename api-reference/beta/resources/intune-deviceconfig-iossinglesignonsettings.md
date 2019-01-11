---
title: tipo de recurso iosSingleSignOnSettings
description: configuración de autenticación de Kerberos para el inicio de sesión único de iOS
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 17c2e100f9762334173ca6ca7049d1e5933f8616
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841065"
---
# <a name="iossinglesignonsettings-resource-type"></a><span data-ttu-id="956b7-103">tipo de recurso iosSingleSignOnSettings</span><span class="sxs-lookup"><span data-stu-id="956b7-103">iosSingleSignOnSettings resource type</span></span>

> <span data-ttu-id="956b7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="956b7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="956b7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="956b7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="956b7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="956b7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="956b7-107">configuración de autenticación de Kerberos para el inicio de sesión único de iOS</span><span class="sxs-lookup"><span data-stu-id="956b7-107">iOS Kerberos authentication settings for single sign-on</span></span>
## <a name="properties"></a><span data-ttu-id="956b7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="956b7-108">Properties</span></span>
|<span data-ttu-id="956b7-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="956b7-109">Property</span></span>|<span data-ttu-id="956b7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="956b7-110">Type</span></span>|<span data-ttu-id="956b7-111">Description</span><span class="sxs-lookup"><span data-stu-id="956b7-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="956b7-112">allowedAppsList</span><span class="sxs-lookup"><span data-stu-id="956b7-112">allowedAppsList</span></span>|<span data-ttu-id="956b7-113">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="956b7-113">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="956b7-114">Lista de identificadores de aplicación que tienen permiso para utilizar este inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="956b7-114">List of app identifiers that are allowed to use this login.</span></span> <span data-ttu-id="956b7-115">Si se omite este campo, el inicio de sesión se aplica a todas las aplicaciones en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="956b7-115">If this field is omitted, the login applies to all applications on the device.</span></span> <span data-ttu-id="956b7-116">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="956b7-116">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="956b7-117">allowedUrls</span><span class="sxs-lookup"><span data-stu-id="956b7-117">allowedUrls</span></span>|<span data-ttu-id="956b7-118">Colección String</span><span class="sxs-lookup"><span data-stu-id="956b7-118">String collection</span></span>|<span data-ttu-id="956b7-119">Lista de direcciones URL de HTTP que se debe coincidir con el fin de utilizar este inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="956b7-119">List of HTTP URLs that must be matched in order to use this login.</span></span> <span data-ttu-id="956b7-120">Con iOS 9.0 o posterior, se puede usar un carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="956b7-120">With iOS 9.0 or later, a wildcard characters may be used.</span></span>|
|<span data-ttu-id="956b7-121">displayName</span><span class="sxs-lookup"><span data-stu-id="956b7-121">displayName</span></span>|<span data-ttu-id="956b7-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="956b7-122">String</span></span>|<span data-ttu-id="956b7-123">El nombre para mostrar de la configuración de inicio de sesión que se muestra en el dispositivo receptor.</span><span class="sxs-lookup"><span data-stu-id="956b7-123">The display name of login settings shown on the receiving device.</span></span>|
|<span data-ttu-id="956b7-124">kerberosPrincipalName</span><span class="sxs-lookup"><span data-stu-id="956b7-124">kerberosPrincipalName</span></span>|<span data-ttu-id="956b7-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="956b7-125">String</span></span>|<span data-ttu-id="956b7-126">Un nombre principal de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="956b7-126">A Kerberos principal name.</span></span> <span data-ttu-id="956b7-127">Si no se proporciona, el usuario se le pida durante la instalación del perfil.</span><span class="sxs-lookup"><span data-stu-id="956b7-127">If not provided, the user is prompted for one during profile installation.</span></span>|
|<span data-ttu-id="956b7-128">kerberosRealm</span><span class="sxs-lookup"><span data-stu-id="956b7-128">kerberosRealm</span></span>|<span data-ttu-id="956b7-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="956b7-129">String</span></span>|<span data-ttu-id="956b7-130">Un nombre de territorio Kerberos.</span><span class="sxs-lookup"><span data-stu-id="956b7-130">A Kerberos realm name.</span></span> <span data-ttu-id="956b7-131">Distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="956b7-131">Case sensitive.</span></span>|

## <a name="relationships"></a><span data-ttu-id="956b7-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="956b7-132">Relationships</span></span>
<span data-ttu-id="956b7-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="956b7-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="956b7-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="956b7-134">JSON Representation</span></span>
<span data-ttu-id="956b7-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="956b7-135">Here is a JSON representation of the resource.</span></span>
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





