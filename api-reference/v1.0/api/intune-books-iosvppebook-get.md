---
title: Obtener iosVppEBook
description: Lea las propiedades y las relaciones del objeto iosVppEBook.
author: tfitzmac
ms.openlocfilehash: 96b3b5804950f4cb3a0d474f4926e62a5c386623
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334863"
---
# <a name="get-iosvppebook"></a><span data-ttu-id="c7255-103">Obtener iosVppEBook</span><span class="sxs-lookup"><span data-stu-id="c7255-103">Get iosVppEBook</span></span>

> <span data-ttu-id="c7255-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c7255-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c7255-105">Lea las propiedades y las relaciones del objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="c7255-105">Read properties and relationships of the [iosVppEBook](../resources/intune-books-iosvppebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c7255-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c7255-106">Prerequisites</span></span>
<span data-ttu-id="c7255-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7255-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7255-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7255-109">Permission type</span></span>|<span data-ttu-id="c7255-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7255-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7255-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7255-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c7255-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="c7255-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="c7255-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7255-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c7255-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7255-114">Not supported.</span></span>|
|<span data-ttu-id="c7255-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7255-115">Application</span></span>|<span data-ttu-id="c7255-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7255-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c7255-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7255-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c7255-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c7255-118">Optional query parameters</span></span>
<span data-ttu-id="c7255-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7255-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c7255-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7255-120">Request headers</span></span>
|<span data-ttu-id="c7255-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7255-121">Header</span></span>|<span data-ttu-id="c7255-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c7255-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c7255-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="c7255-123">Authorization</span></span>|<span data-ttu-id="c7255-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c7255-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c7255-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c7255-125">Accept</span></span>|<span data-ttu-id="c7255-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c7255-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7255-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7255-127">Request body</span></span>
<span data-ttu-id="c7255-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c7255-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c7255-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7255-129">Response</span></span>
<span data-ttu-id="c7255-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7255-130">If successful, this method returns a `200 OK` response code and [iosVppEBook](../resources/intune-books-iosvppebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7255-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7255-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="c7255-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7255-132">Request</span></span>
<span data-ttu-id="c7255-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7255-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}
```

### <a name="response"></a><span data-ttu-id="c7255-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7255-134">Response</span></span>
<span data-ttu-id="c7255-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7255-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1033

{
  "value": {
    "@odata.type": "#microsoft.graph.iosVppEBook",
    "id": "3b9f627e-627e-3b9f-7e62-9f3b7e629f3b",
    "displayName": "Display Name value",
    "description": "Description value",
    "publisher": "Publisher value",
    "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
    "largeCover": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    },
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "informationUrl": "https://example.com/informationUrl/",
    "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
    "vppTokenId": "9148ac60-ac60-9148-60ac-489160ac4891",
    "appleId": "Apple Id value",
    "vppOrganizationName": "Vpp Organization Name value",
    "genres": [
      "Genres value"
    ],
    "language": "Language value",
    "seller": "Seller value",
    "totalLicenseCount": 1,
    "usedLicenseCount": 0
  }
}
```



