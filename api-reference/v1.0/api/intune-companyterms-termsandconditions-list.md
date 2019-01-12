---
title: Enumerar termsAndConditionses
description: Enumere las propiedades y las relaciones de los objetos termsAndConditions.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4fe09d858f0dea587c122663ce16639e20b65672
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976971"
---
# <a name="list-termsandconditionses"></a><span data-ttu-id="75396-103">Enumerar termsAndConditionses</span><span class="sxs-lookup"><span data-stu-id="75396-103">List termsAndConditionses</span></span>

> <span data-ttu-id="75396-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="75396-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="75396-105">Enumere las propiedades y las relaciones de los objetos [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="75396-105">List properties and relationships of the [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="75396-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="75396-106">Prerequisites</span></span>
<span data-ttu-id="75396-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="75396-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="75396-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="75396-109">Permission type</span></span>|<span data-ttu-id="75396-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="75396-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="75396-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="75396-111">Delegated (work or school account)</span></span>|<span data-ttu-id="75396-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="75396-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="75396-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="75396-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="75396-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75396-114">Not supported.</span></span>|
|<span data-ttu-id="75396-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="75396-115">Application</span></span>|<span data-ttu-id="75396-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75396-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="75396-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="75396-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/termsAndConditions
```

## <a name="request-headers"></a><span data-ttu-id="75396-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="75396-118">Request headers</span></span>
|<span data-ttu-id="75396-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75396-119">Header</span></span>|<span data-ttu-id="75396-120">Valor</span><span class="sxs-lookup"><span data-stu-id="75396-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="75396-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="75396-121">Authorization</span></span>|<span data-ttu-id="75396-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="75396-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="75396-123">Accept</span><span class="sxs-lookup"><span data-stu-id="75396-123">Accept</span></span>|<span data-ttu-id="75396-124">application/json</span><span class="sxs-lookup"><span data-stu-id="75396-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="75396-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="75396-125">Request body</span></span>
<span data-ttu-id="75396-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="75396-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="75396-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75396-127">Response</span></span>
<span data-ttu-id="75396-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75396-128">If successful, this method returns a `200 OK` response code and a collection of [termsAndConditions](../resources/intune-companyterms-termsandconditions.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="75396-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="75396-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="75396-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="75396-130">Request</span></span>
<span data-ttu-id="75396-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="75396-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions
```

### <a name="response"></a><span data-ttu-id="75396-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75396-132">Response</span></span>
<span data-ttu-id="75396-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="75396-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 518

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.termsAndConditions",
      "id": "eefc80cf-80cf-eefc-cf80-fceecf80fcee",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "displayName": "Display Name value",
      "description": "Description value",
      "title": "Title value",
      "bodyText": "Body Text value",
      "acceptanceStatement": "Acceptance Statement value",
      "version": 7
    }
  ]
}
```



