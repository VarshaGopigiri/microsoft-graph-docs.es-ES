---
title: Lista windowsUniversalAppXContainedApps
description: Propiedades de la lista y relaciones de los objetos windowsUniversalAppXContainedApp.
ms.openlocfilehash: cfe51a97e09f446cb8241f739f5339e88c1041f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089521"
---
# <a name="list-windowsuniversalappxcontainedapps"></a><span data-ttu-id="cfec6-103">Lista windowsUniversalAppXContainedApps</span><span class="sxs-lookup"><span data-stu-id="cfec6-103">List windowsUniversalAppXContainedApps</span></span>

> <span data-ttu-id="cfec6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cfec6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cfec6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cfec6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cfec6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cfec6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cfec6-107">Propiedades de la lista y relaciones de los objetos [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md) .</span><span class="sxs-lookup"><span data-stu-id="cfec6-107">List properties and relationships of the [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cfec6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cfec6-108">Prerequisites</span></span>
<span data-ttu-id="cfec6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cfec6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cfec6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cfec6-111">Permission type</span></span>|<span data-ttu-id="cfec6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cfec6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cfec6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cfec6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cfec6-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="cfec6-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="cfec6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cfec6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cfec6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cfec6-116">Not supported.</span></span>|
|<span data-ttu-id="cfec6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cfec6-117">Application</span></span>|<span data-ttu-id="cfec6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cfec6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cfec6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cfec6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps
GET /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.microsoftStoreForBusinessApp/containedApps
GET /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.windowsUniversalAppX/committedContainedApps
```

## <a name="request-headers"></a><span data-ttu-id="cfec6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cfec6-120">Request headers</span></span>
|<span data-ttu-id="cfec6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfec6-121">Header</span></span>|<span data-ttu-id="cfec6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cfec6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cfec6-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="cfec6-123">Authorization</span></span>|<span data-ttu-id="cfec6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cfec6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cfec6-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cfec6-125">Accept</span></span>|<span data-ttu-id="cfec6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cfec6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cfec6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cfec6-127">Request body</span></span>
<span data-ttu-id="cfec6-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cfec6-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cfec6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cfec6-129">Response</span></span>
<span data-ttu-id="cfec6-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cfec6-130">If successful, this method returns a `200 OK` response code and a collection of [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cfec6-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cfec6-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="cfec6-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cfec6-132">Request</span></span>
<span data-ttu-id="cfec6-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cfec6-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps
```

### <a name="response"></a><span data-ttu-id="cfec6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cfec6-134">Response</span></span>
<span data-ttu-id="cfec6-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cfec6-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 216

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsUniversalAppXContainedApp",
      "id": "2d03284a-284a-2d03-4a28-032d4a28032d",
      "appUserModelId": "App User Model Id value"
    }
  ]
}
```




