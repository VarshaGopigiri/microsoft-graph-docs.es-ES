---
title: Enumerar androidStoreApps
description: Enumere las propiedades y las relaciones de los objetos androidStoreApp.
author: tfitzmac
ms.openlocfilehash: 0f3e1b0ca33d6995cd8dbdc30207395e5f5075a6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330936"
---
# <a name="list-androidstoreapps"></a><span data-ttu-id="05cc3-103">Enumerar androidStoreApps</span><span class="sxs-lookup"><span data-stu-id="05cc3-103">List androidStoreApps</span></span>

> <span data-ttu-id="05cc3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="05cc3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="05cc3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="05cc3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="05cc3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="05cc3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="05cc3-107">Enumere las propiedades y las relaciones de los objetos [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="05cc3-107">List properties and relationships of the [androidStoreApp](../resources/intune-apps-androidstoreapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="05cc3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="05cc3-108">Prerequisites</span></span>
<span data-ttu-id="05cc3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="05cc3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="05cc3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05cc3-111">Permission type</span></span>|<span data-ttu-id="05cc3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05cc3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="05cc3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05cc3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="05cc3-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="05cc3-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="05cc3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05cc3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="05cc3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05cc3-116">Not supported.</span></span>|
|<span data-ttu-id="05cc3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05cc3-117">Application</span></span>|<span data-ttu-id="05cc3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05cc3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="05cc3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05cc3-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="05cc3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="05cc3-120">Request headers</span></span>
|<span data-ttu-id="05cc3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05cc3-121">Header</span></span>|<span data-ttu-id="05cc3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="05cc3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="05cc3-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="05cc3-123">Authorization</span></span>|<span data-ttu-id="05cc3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="05cc3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="05cc3-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="05cc3-125">Accept</span></span>|<span data-ttu-id="05cc3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="05cc3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="05cc3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05cc3-127">Request body</span></span>
<span data-ttu-id="05cc3-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="05cc3-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="05cc3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05cc3-129">Response</span></span>
<span data-ttu-id="05cc3-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [androidStoreApp](../resources/intune-apps-androidstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05cc3-130">If successful, this method returns a `200 OK` response code and a collection of [androidStoreApp](../resources/intune-apps-androidstoreapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="05cc3-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05cc3-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="05cc3-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="05cc3-132">Request</span></span>
<span data-ttu-id="05cc3-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="05cc3-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="05cc3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05cc3-134">Response</span></span>
<span data-ttu-id="05cc3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="05cc3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1483

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidStoreApp",
      "id": "1f2b7654-7654-1f2b-5476-2b1f54762b1f",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisher": "Publisher value",
      "largeIcon": {
        "@odata.type": "microsoft.graph.mimeContent",
        "type": "Type value",
        "value": "dmFsdWU="
      },
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "isFeatured": true,
      "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
      "informationUrl": "https://example.com/informationUrl/",
      "owner": "Owner value",
      "developer": "Developer value",
      "notes": "Notes value",
      "uploadState": 11,
      "publishingState": "processing",
      "packageId": "Package Id value",
      "appIdentifier": "App Identifier value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "minimumSupportedOperatingSystem": {
        "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
        "v4_0": true,
        "v4_0_3": true,
        "v4_1": true,
        "v4_2": true,
        "v4_3": true,
        "v4_4": true,
        "v5_0": true,
        "v5_1": true,
        "v6_0": true,
        "v7_0": true,
        "v7_1": true,
        "v8_0": true,
        "v8_1": true,
        "v9_0": true
      }
    }
  ]
}
```





