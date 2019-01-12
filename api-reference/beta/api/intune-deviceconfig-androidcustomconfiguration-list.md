---
title: Enumerar androidCustomConfigurations
description: Enumere las propiedades y las relaciones de los objetos androidCustomConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6de2f726452d19bc2000fd691774f6659830f17e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919018"
---
# <a name="list-androidcustomconfigurations"></a><span data-ttu-id="84f05-103">Enumerar androidCustomConfigurations</span><span class="sxs-lookup"><span data-stu-id="84f05-103">List androidCustomConfigurations</span></span>

> <span data-ttu-id="84f05-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="84f05-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="84f05-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="84f05-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="84f05-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="84f05-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="84f05-107">Enumere las propiedades y las relaciones de los objetos [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="84f05-107">List properties and relationships of the [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="84f05-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="84f05-108">Prerequisites</span></span>
<span data-ttu-id="84f05-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="84f05-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="84f05-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="84f05-111">Permission type</span></span>|<span data-ttu-id="84f05-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="84f05-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="84f05-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="84f05-113">Delegated (work or school account)</span></span>|<span data-ttu-id="84f05-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="84f05-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="84f05-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="84f05-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="84f05-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84f05-116">Not supported.</span></span>|
|<span data-ttu-id="84f05-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="84f05-117">Application</span></span>|<span data-ttu-id="84f05-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84f05-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="84f05-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="84f05-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="84f05-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="84f05-120">Request headers</span></span>
|<span data-ttu-id="84f05-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84f05-121">Header</span></span>|<span data-ttu-id="84f05-122">Valor</span><span class="sxs-lookup"><span data-stu-id="84f05-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="84f05-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="84f05-123">Authorization</span></span>|<span data-ttu-id="84f05-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="84f05-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="84f05-125">Accept</span><span class="sxs-lookup"><span data-stu-id="84f05-125">Accept</span></span>|<span data-ttu-id="84f05-126">application/json</span><span class="sxs-lookup"><span data-stu-id="84f05-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="84f05-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="84f05-127">Request body</span></span>
<span data-ttu-id="84f05-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="84f05-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="84f05-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84f05-129">Response</span></span>
<span data-ttu-id="84f05-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="84f05-130">If successful, this method returns a `200 OK` response code and a collection of [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="84f05-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f05-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="84f05-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="84f05-132">Request</span></span>
<span data-ttu-id="84f05-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="84f05-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="84f05-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84f05-134">Response</span></span>
<span data-ttu-id="84f05-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="84f05-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 779

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidCustomConfiguration",
      "id": "619b5e6d-5e6d-619b-6d5e-9b616d5e9b61",
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





