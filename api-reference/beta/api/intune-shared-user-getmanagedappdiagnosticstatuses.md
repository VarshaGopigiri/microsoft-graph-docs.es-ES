---
title: Función getManagedAppDiagnosticStatuses
description: Obtiene estados de validación de diagnósticos de un usuario determinado.
ms.openlocfilehash: bbbb399ef26c38972f989c2e1129fe61baffa0fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089664"
---
# <a name="getmanagedappdiagnosticstatuses-function"></a><span data-ttu-id="90853-103">Función getManagedAppDiagnosticStatuses</span><span class="sxs-lookup"><span data-stu-id="90853-103">getManagedAppDiagnosticStatuses function</span></span>

> <span data-ttu-id="90853-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90853-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90853-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90853-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="90853-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="90853-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="90853-107">Obtiene estados de validación de diagnósticos de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="90853-107">Gets diagnostics validation status for a given user.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="90853-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="90853-108">Prerequisites</span></span>
<span data-ttu-id="90853-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90853-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90853-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90853-111">Permission type</span></span>|<span data-ttu-id="90853-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90853-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="90853-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90853-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="90853-114">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="90853-114">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="90853-115">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="90853-115">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="90853-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90853-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="90853-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90853-117">Not supported.</span></span>|
|<span data-ttu-id="90853-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90853-118">Application</span></span>|<span data-ttu-id="90853-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90853-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="90853-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90853-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/getManagedAppDiagnosticStatuses
```

## <a name="request-headers"></a><span data-ttu-id="90853-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90853-121">Request headers</span></span>
|<span data-ttu-id="90853-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90853-122">Header</span></span>|<span data-ttu-id="90853-123">Valor</span><span class="sxs-lookup"><span data-stu-id="90853-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="90853-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="90853-124">Authorization</span></span>|<span data-ttu-id="90853-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="90853-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="90853-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="90853-126">Accept</span></span>|<span data-ttu-id="90853-127">application/json</span><span class="sxs-lookup"><span data-stu-id="90853-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="90853-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90853-128">Request body</span></span>
<span data-ttu-id="90853-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="90853-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="90853-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90853-130">Response</span></span>
<span data-ttu-id="90853-131">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección [managedAppDiagnosticStatus](../resources/intune-mam-managedappdiagnosticstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90853-131">If successful, this function returns a `200 OK` response code and a [managedAppDiagnosticStatus](../resources/intune-mam-managedappdiagnosticstatus.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90853-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90853-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="90853-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90853-133">Request</span></span>
<span data-ttu-id="90853-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90853-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/users/{usersId}/getManagedAppDiagnosticStatuses
```

### <a name="response"></a><span data-ttu-id="90853-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90853-135">Response</span></span>
<span data-ttu-id="90853-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90853-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 249

{
  "value": [
    {
      "@odata.type": "microsoft.graph.managedAppDiagnosticStatus",
      "validationName": "Validation Name value",
      "state": "State value",
      "mitigationInstruction": "Mitigation Instruction value"
    }
  ]
}
```






