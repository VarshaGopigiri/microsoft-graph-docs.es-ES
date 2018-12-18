---
title: Obtener termsAndConditionsAssignment
description: Lea las propiedades y las relaciones del objeto termsAndConditionsAssignment.
author: tfitzmac
ms.openlocfilehash: e2fc025eca77abb3951c4453adf8644a5a0ffc9a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27335780"
---
# <a name="get-termsandconditionsassignment"></a><span data-ttu-id="37e03-103">Obtener termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="37e03-103">Get termsAndConditionsAssignment</span></span>

> <span data-ttu-id="37e03-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37e03-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37e03-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37e03-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="37e03-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="37e03-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="37e03-107">Lea las propiedades y las relaciones del objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="37e03-107">Read properties and relationships of the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="37e03-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="37e03-108">Prerequisites</span></span>
<span data-ttu-id="37e03-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37e03-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37e03-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37e03-111">Permission type</span></span>|<span data-ttu-id="37e03-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37e03-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="37e03-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37e03-113">Delegated (work or school account)</span></span>|<span data-ttu-id="37e03-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="37e03-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="37e03-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37e03-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="37e03-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37e03-116">Not supported.</span></span>|
|<span data-ttu-id="37e03-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37e03-117">Application</span></span>|<span data-ttu-id="37e03-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37e03-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="37e03-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37e03-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="37e03-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="37e03-120">Optional query parameters</span></span>
<span data-ttu-id="37e03-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37e03-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="37e03-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37e03-122">Request headers</span></span>
|<span data-ttu-id="37e03-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37e03-123">Header</span></span>|<span data-ttu-id="37e03-124">Valor</span><span class="sxs-lookup"><span data-stu-id="37e03-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="37e03-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="37e03-125">Authorization</span></span>|<span data-ttu-id="37e03-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="37e03-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="37e03-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="37e03-127">Accept</span></span>|<span data-ttu-id="37e03-128">application/json</span><span class="sxs-lookup"><span data-stu-id="37e03-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="37e03-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37e03-129">Request body</span></span>
<span data-ttu-id="37e03-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="37e03-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="37e03-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37e03-131">Response</span></span>
<span data-ttu-id="37e03-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37e03-132">If successful, this method returns a `200 OK` response code and [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="37e03-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37e03-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="37e03-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37e03-134">Request</span></span>
<span data-ttu-id="37e03-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37e03-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
```

### <a name="response"></a><span data-ttu-id="37e03-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37e03-136">Response</span></span>
<span data-ttu-id="37e03-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="37e03-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 246

{
  "value": {
    "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
    "id": "64c1a196-a196-64c1-96a1-c16496a1c164",
    "target": {
      "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
    }
  }
}
```





