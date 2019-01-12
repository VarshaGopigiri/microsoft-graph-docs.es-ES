---
title: Obtener managedEBook
description: Lea las propiedades y las relaciones del objeto managedEBook.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 88ebfec3265f467fb3441b6c0d0e9753b489b3c2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950154"
---
# <a name="get-managedebook"></a><span data-ttu-id="bafcc-103">Obtener managedEBook</span><span class="sxs-lookup"><span data-stu-id="bafcc-103">Get managedEBook</span></span>

> <span data-ttu-id="bafcc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bafcc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bafcc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bafcc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bafcc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bafcc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bafcc-107">Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune-books-managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="bafcc-107">Read properties and relationships of the [managedEBook](../resources/intune-books-managedebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bafcc-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bafcc-108">Prerequisites</span></span>
<span data-ttu-id="bafcc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bafcc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bafcc-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bafcc-111">Permission type</span></span>|<span data-ttu-id="bafcc-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bafcc-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bafcc-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bafcc-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bafcc-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="bafcc-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="bafcc-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bafcc-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bafcc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bafcc-116">Not supported.</span></span>|
|<span data-ttu-id="bafcc-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bafcc-117">Application</span></span>|<span data-ttu-id="bafcc-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bafcc-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bafcc-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bafcc-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="bafcc-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bafcc-120">Optional query parameters</span></span>
<span data-ttu-id="bafcc-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bafcc-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bafcc-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bafcc-122">Request headers</span></span>
|<span data-ttu-id="bafcc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bafcc-123">Header</span></span>|<span data-ttu-id="bafcc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bafcc-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bafcc-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="bafcc-125">Authorization</span></span>|<span data-ttu-id="bafcc-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bafcc-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bafcc-127">Accept</span><span class="sxs-lookup"><span data-stu-id="bafcc-127">Accept</span></span>|<span data-ttu-id="bafcc-128">application/json</span><span class="sxs-lookup"><span data-stu-id="bafcc-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bafcc-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bafcc-129">Request body</span></span>
<span data-ttu-id="bafcc-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bafcc-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bafcc-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bafcc-131">Response</span></span>
<span data-ttu-id="bafcc-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedEBook](../resources/intune-books-managedebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bafcc-132">If successful, this method returns a `200 OK` response code and [managedEBook](../resources/intune-books-managedebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bafcc-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bafcc-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="bafcc-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bafcc-134">Request</span></span>
<span data-ttu-id="bafcc-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bafcc-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}
```

### <a name="response"></a><span data-ttu-id="bafcc-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bafcc-136">Response</span></span>
<span data-ttu-id="bafcc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bafcc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 712

{
  "value": {
    "@odata.type": "#microsoft.graph.managedEBook",
    "id": "1fbd3558-3558-1fbd-5835-bd1f5835bd1f",
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
    "privacyInformationUrl": "https://example.com/privacyInformationUrl/"
  }
}
```





