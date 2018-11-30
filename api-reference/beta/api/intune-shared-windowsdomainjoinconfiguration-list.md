---
title: Lista windowsDomainJoinConfigurations
description: Propiedades de la lista y relaciones de los objetos windowsDomainJoinConfiguration.
ms.openlocfilehash: b4708533f0f8c52a4ebc6f962db45f4f04f95d73
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086677"
---
# <a name="list-windowsdomainjoinconfigurations"></a><span data-ttu-id="db708-103">Lista windowsDomainJoinConfigurations</span><span class="sxs-lookup"><span data-stu-id="db708-103">List windowsDomainJoinConfigurations</span></span>

> <span data-ttu-id="db708-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="db708-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="db708-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="db708-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="db708-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="db708-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="db708-107">Propiedades de la lista y relaciones de los objetos [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="db708-107">List properties and relationships of the [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="db708-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="db708-108">Prerequisites</span></span>
<span data-ttu-id="db708-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="db708-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="db708-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="db708-111">Permission type</span></span>|<span data-ttu-id="db708-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="db708-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="db708-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="db708-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="db708-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="db708-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="db708-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="db708-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="db708-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="db708-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="db708-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="db708-117">Not supported.</span></span>|
|<span data-ttu-id="db708-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="db708-118">Application</span></span>|<span data-ttu-id="db708-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="db708-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="db708-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="db708-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="db708-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="db708-121">Request headers</span></span>
|<span data-ttu-id="db708-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db708-122">Header</span></span>|<span data-ttu-id="db708-123">Valor</span><span class="sxs-lookup"><span data-stu-id="db708-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="db708-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="db708-124">Authorization</span></span>|<span data-ttu-id="db708-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="db708-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="db708-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="db708-126">Accept</span></span>|<span data-ttu-id="db708-127">application/json</span><span class="sxs-lookup"><span data-stu-id="db708-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="db708-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="db708-128">Request body</span></span>
<span data-ttu-id="db708-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="db708-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="db708-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db708-130">Response</span></span>
<span data-ttu-id="db708-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="db708-131">If successful, this method returns a `200 OK` response code and a collection of [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="db708-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="db708-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="db708-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="db708-133">Request</span></span>
<span data-ttu-id="db708-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="db708-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="db708-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db708-135">Response</span></span>
<span data-ttu-id="db708-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="db708-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 760

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsDomainJoinConfiguration",
      "id": "40118d08-8d08-4011-088d-1140088d1140",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "computerNameStaticPrefix": "Computer Name Static Prefix value",
      "computerNameSuffixRandomCharCount": 1,
      "activeDirectoryDomainName": "Active Directory Domain Name value",
      "organizationalUnit": "Organizational Unit value"
    }
  ]
}
```



