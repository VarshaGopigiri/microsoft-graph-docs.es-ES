---
title: Enumerar windowsPhone81CustomConfigurations
description: Enumere las propiedades y las relaciones de los objetos windowsPhone81CustomConfiguration.
ms.openlocfilehash: 9aae2a0b7e98bded001b1889f304a2f2b8c0a285
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087136"
---
# <a name="list-windowsphone81customconfigurations"></a><span data-ttu-id="f77ef-103">Enumerar windowsPhone81CustomConfigurations</span><span class="sxs-lookup"><span data-stu-id="f77ef-103">List windowsPhone81CustomConfigurations</span></span>

> <span data-ttu-id="f77ef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f77ef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f77ef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f77ef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f77ef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f77ef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f77ef-107">Enumere las propiedades y las relaciones de los objetos [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f77ef-107">List properties and relationships of the [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f77ef-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f77ef-108">Prerequisites</span></span>
<span data-ttu-id="f77ef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f77ef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f77ef-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f77ef-111">Permission type</span></span>|<span data-ttu-id="f77ef-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f77ef-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f77ef-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f77ef-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f77ef-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f77ef-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f77ef-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f77ef-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f77ef-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f77ef-116">Not supported.</span></span>|
|<span data-ttu-id="f77ef-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f77ef-117">Application</span></span>|<span data-ttu-id="f77ef-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f77ef-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f77ef-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f77ef-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="f77ef-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f77ef-120">Request headers</span></span>
|<span data-ttu-id="f77ef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f77ef-121">Header</span></span>|<span data-ttu-id="f77ef-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f77ef-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f77ef-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f77ef-123">Authorization</span></span>|<span data-ttu-id="f77ef-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f77ef-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f77ef-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f77ef-125">Accept</span></span>|<span data-ttu-id="f77ef-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f77ef-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f77ef-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f77ef-127">Request body</span></span>
<span data-ttu-id="f77ef-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f77ef-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f77ef-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f77ef-129">Response</span></span>
<span data-ttu-id="f77ef-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f77ef-130">If successful, this method returns a `200 OK` response code and a collection of [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f77ef-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f77ef-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f77ef-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f77ef-132">Request</span></span>
<span data-ttu-id="f77ef-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f77ef-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="f77ef-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f77ef-134">Response</span></span>
<span data-ttu-id="f77ef-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f77ef-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 786

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsPhone81CustomConfiguration",
      "id": "0d98693c-693c-0d98-3c69-980d3c69980d",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "omaSettings": [
        {
          "@odata.type": "microsoft.graph.omaSettingInteger",
          "displayName": "Display Name value",
          "description": "Description value",
          "omaUri": "Oma Uri value",
          "value": 5
        }
      ]
    }
  ]
}
```




