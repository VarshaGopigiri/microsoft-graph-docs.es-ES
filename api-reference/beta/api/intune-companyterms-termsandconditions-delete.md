---
title: Eliminar termsAndConditions
description: Elimina un termsAndConditions.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d3e1584abe605f9f35cb29587ce59684fa2b2e12
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842325"
---
# <a name="delete-termsandconditions"></a><span data-ttu-id="9ba75-103">Eliminar termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="9ba75-103">Delete termsAndConditions</span></span>

> <span data-ttu-id="9ba75-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9ba75-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9ba75-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9ba75-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9ba75-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9ba75-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9ba75-107">Elimina un [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="9ba75-107">Deletes a [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9ba75-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9ba75-108">Prerequisites</span></span>
<span data-ttu-id="9ba75-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9ba75-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9ba75-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ba75-111">Permission type</span></span>|<span data-ttu-id="9ba75-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ba75-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9ba75-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ba75-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9ba75-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9ba75-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="9ba75-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ba75-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9ba75-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ba75-116">Not supported.</span></span>|
|<span data-ttu-id="9ba75-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ba75-117">Application</span></span>|<span data-ttu-id="9ba75-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ba75-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9ba75-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ba75-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/termsAndConditions/{termsAndConditionsId}
DELETE /deviceManagement/termsAndConditions/{termsAndConditionsId}/groupAssignments/{termsAndConditionsGroupAssignmentId}/termsAndConditions
DELETE /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}/termsAndConditions
```

## <a name="request-headers"></a><span data-ttu-id="9ba75-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ba75-120">Request headers</span></span>
|<span data-ttu-id="9ba75-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ba75-121">Header</span></span>|<span data-ttu-id="9ba75-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9ba75-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9ba75-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9ba75-123">Authorization</span></span>|<span data-ttu-id="9ba75-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9ba75-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9ba75-125">Accept</span><span class="sxs-lookup"><span data-stu-id="9ba75-125">Accept</span></span>|<span data-ttu-id="9ba75-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9ba75-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9ba75-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ba75-127">Request body</span></span>
<span data-ttu-id="9ba75-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9ba75-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9ba75-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ba75-129">Response</span></span>
<span data-ttu-id="9ba75-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="9ba75-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="9ba75-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ba75-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="9ba75-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ba75-132">Request</span></span>
<span data-ttu-id="9ba75-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ba75-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/termsAndConditions/{termsAndConditionsId}
```

### <a name="response"></a><span data-ttu-id="9ba75-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ba75-134">Response</span></span>
<span data-ttu-id="9ba75-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ba75-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





