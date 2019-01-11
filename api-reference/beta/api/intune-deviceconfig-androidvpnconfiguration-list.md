---
title: Lista androidVpnConfigurations
description: Propiedades de la lista y relaciones de los objetos androidVpnConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4d4fbe96a6463e81d010af19295bb57b46c41c8c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833393"
---
# <a name="list-androidvpnconfigurations"></a><span data-ttu-id="001f4-103">Lista androidVpnConfigurations</span><span class="sxs-lookup"><span data-stu-id="001f4-103">List androidVpnConfigurations</span></span>

> <span data-ttu-id="001f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="001f4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="001f4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="001f4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="001f4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="001f4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="001f4-107">Propiedades de la lista y relaciones de los objetos [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="001f4-107">List properties and relationships of the [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="001f4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="001f4-108">Prerequisites</span></span>
<span data-ttu-id="001f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="001f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="001f4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="001f4-111">Permission type</span></span>|<span data-ttu-id="001f4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="001f4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="001f4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="001f4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="001f4-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="001f4-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="001f4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="001f4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="001f4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="001f4-116">Not supported.</span></span>|
|<span data-ttu-id="001f4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="001f4-117">Application</span></span>|<span data-ttu-id="001f4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="001f4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="001f4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="001f4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="001f4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="001f4-120">Request headers</span></span>
|<span data-ttu-id="001f4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="001f4-121">Header</span></span>|<span data-ttu-id="001f4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="001f4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="001f4-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="001f4-123">Authorization</span></span>|<span data-ttu-id="001f4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="001f4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="001f4-125">Accept</span><span class="sxs-lookup"><span data-stu-id="001f4-125">Accept</span></span>|<span data-ttu-id="001f4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="001f4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="001f4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="001f4-127">Request body</span></span>
<span data-ttu-id="001f4-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="001f4-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="001f4-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="001f4-129">Response</span></span>
<span data-ttu-id="001f4-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="001f4-130">If successful, this method returns a `200 OK` response code and a collection of [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="001f4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="001f4-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="001f4-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="001f4-132">Request</span></span>
<span data-ttu-id="001f4-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="001f4-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="001f4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="001f4-134">Response</span></span>
<span data-ttu-id="001f4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="001f4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1339

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidVpnConfiguration",
      "id": "d4c48852-8852-d4c4-5288-c4d45288c4d4",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "connectionName": "Connection Name value",
      "connectionType": "pulseSecure",
      "role": "Role value",
      "realm": "Realm value",
      "servers": [
        {
          "@odata.type": "microsoft.graph.vpnServer",
          "description": "Description value",
          "address": "Address value",
          "isDefaultServer": true
        }
      ],
      "fingerprint": "Fingerprint value",
      "customData": [
        {
          "@odata.type": "microsoft.graph.keyValue",
          "key": "Key value",
          "value": "Value value"
        }
      ],
      "customKeyValueData": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ],
      "authenticationMethod": "usernameAndPassword"
    }
  ]
}
```





