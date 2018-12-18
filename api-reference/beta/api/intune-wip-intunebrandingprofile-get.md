---
title: Obtener intuneBrandingProfile
description: Leer las propiedades y las relaciones del objeto intuneBrandingProfile.
author: tfitzmac
ms.openlocfilehash: 2c90dc24f85f6c259c48cdf0ba2e431ef5c8c55a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27333575"
---
# <a name="get-intunebrandingprofile"></a><span data-ttu-id="dca39-103">Obtener intuneBrandingProfile</span><span class="sxs-lookup"><span data-stu-id="dca39-103">Get intuneBrandingProfile</span></span>

> <span data-ttu-id="dca39-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dca39-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dca39-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dca39-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="dca39-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dca39-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dca39-107">Leer las propiedades y las relaciones del objeto [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="dca39-107">Read properties and relationships of the [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dca39-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dca39-108">Prerequisites</span></span>
<span data-ttu-id="dca39-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dca39-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dca39-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dca39-111">Permission type</span></span>|<span data-ttu-id="dca39-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dca39-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dca39-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dca39-113">Delegated (work or school account)</span></span>|<span data-ttu-id="dca39-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="dca39-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="dca39-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dca39-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dca39-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dca39-116">Not supported.</span></span>|
|<span data-ttu-id="dca39-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dca39-117">Application</span></span>|<span data-ttu-id="dca39-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dca39-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dca39-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dca39-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/intuneBrandingProfiles/{intuneBrandingProfileId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="dca39-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="dca39-120">Optional query parameters</span></span>
<span data-ttu-id="dca39-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dca39-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="dca39-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dca39-122">Request headers</span></span>
|<span data-ttu-id="dca39-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dca39-123">Header</span></span>|<span data-ttu-id="dca39-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dca39-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dca39-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="dca39-125">Authorization</span></span>|<span data-ttu-id="dca39-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dca39-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dca39-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="dca39-127">Accept</span></span>|<span data-ttu-id="dca39-128">application/json</span><span class="sxs-lookup"><span data-stu-id="dca39-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dca39-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dca39-129">Request body</span></span>
<span data-ttu-id="dca39-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dca39-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dca39-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dca39-131">Response</span></span>
<span data-ttu-id="dca39-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dca39-132">If successful, this method returns a `200 OK` response code and [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dca39-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dca39-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="dca39-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dca39-134">Request</span></span>
<span data-ttu-id="dca39-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dca39-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/intuneBrandingProfiles/{intuneBrandingProfileId}
```

### <a name="response"></a><span data-ttu-id="dca39-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dca39-136">Response</span></span>
<span data-ttu-id="dca39-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dca39-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1472

{
  "value": {
    "@odata.type": "#microsoft.graph.intuneBrandingProfile",
    "id": "fcd6136c-136c-fcd6-6c13-d6fc6c13d6fc",
    "profileName": "Profile Name value",
    "profileDescription": "Profile Description value",
    "isDefaultProfile": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "contactITName": "Contact ITName value",
    "contactITPhoneNumber": "Contact ITPhone Number value",
    "contactITEmailAddress": "Contact ITEmail Address value",
    "contactITNotes": "Contact ITNotes value",
    "privacyUrl": "https://example.com/privacyUrl/",
    "onlineSupportSiteUrl": "https://example.com/onlineSupportSiteUrl/",
    "onlineSupportSiteName": "Online Support Site Name value",
    "themeColor": {
      "@odata.type": "microsoft.graph.rgbColor",
      "r": 1,
      "g": 1,
      "b": 1
    },
    "showLogo": true,
    "showDisplayNameNextToLogo": true,
    "themeColorLogo": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    },
    "lightBackgroundLogo": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    },
    "landingPageCustomizedImage": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    }
  }
}
```





