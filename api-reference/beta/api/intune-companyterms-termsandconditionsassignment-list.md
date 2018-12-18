---
title: Enumerar termsAndConditionsAssignments
description: Enumere las propiedades y las relaciones de los objetos termsAndConditionsAssignment.
author: tfitzmac
ms.openlocfilehash: 8f32698a82447e18b6086f565e0acf2f07055662
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340239"
---
# <a name="list-termsandconditionsassignments"></a><span data-ttu-id="e1a11-103">Enumerar termsAndConditionsAssignments</span><span class="sxs-lookup"><span data-stu-id="e1a11-103">List termsAndConditionsAssignments</span></span>

> <span data-ttu-id="e1a11-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e1a11-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e1a11-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e1a11-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e1a11-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e1a11-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e1a11-107">Enumere las propiedades y las relaciones de los objetos [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e1a11-107">List properties and relationships of the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e1a11-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e1a11-108">Prerequisites</span></span>
<span data-ttu-id="e1a11-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1a11-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e1a11-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1a11-111">Permission type</span></span>|<span data-ttu-id="e1a11-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1a11-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e1a11-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1a11-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e1a11-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="e1a11-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="e1a11-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1a11-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e1a11-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1a11-116">Not supported.</span></span>|
|<span data-ttu-id="e1a11-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1a11-117">Application</span></span>|<span data-ttu-id="e1a11-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1a11-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e1a11-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e1a11-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="e1a11-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1a11-120">Request headers</span></span>
|<span data-ttu-id="e1a11-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1a11-121">Header</span></span>|<span data-ttu-id="e1a11-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e1a11-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e1a11-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e1a11-123">Authorization</span></span>|<span data-ttu-id="e1a11-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e1a11-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e1a11-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e1a11-125">Accept</span></span>|<span data-ttu-id="e1a11-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e1a11-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e1a11-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e1a11-127">Request body</span></span>
<span data-ttu-id="e1a11-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e1a11-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e1a11-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1a11-129">Response</span></span>
<span data-ttu-id="e1a11-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1a11-130">If successful, this method returns a `200 OK` response code and a collection of [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e1a11-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1a11-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="e1a11-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1a11-132">Request</span></span>
<span data-ttu-id="e1a11-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e1a11-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments
```

### <a name="response"></a><span data-ttu-id="e1a11-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1a11-134">Response</span></span>
<span data-ttu-id="e1a11-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e1a11-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 270

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
      "id": "64c1a196-a196-64c1-96a1-c16496a1c164",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```





