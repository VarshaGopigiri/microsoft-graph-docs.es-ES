---
title: tipo de recurso agreementAcceptance
description: Representa el estado actual de un usuario dentro de ámbito de condiciones personalizable de una compañía de uso con tecnología de Azure Active Directory (AD Azure).
ms.openlocfilehash: 23221fe88a65b003c8d26aca99eaf1f03d935722
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083147"
---
# <a name="agreementacceptance-resource-type"></a><span data-ttu-id="2bd8c-103">tipo de recurso agreementAcceptance</span><span class="sxs-lookup"><span data-stu-id="2bd8c-103">agreementAcceptance resource type</span></span>

> <span data-ttu-id="2bd8c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2bd8c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2bd8c-106">Representa el estado actual de un usuario dentro de ámbito de condiciones personalizable de una compañía de uso con tecnología de Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="2bd8c-106">Represents the current status of a user within scope of a company's customizable terms of use powered by Azure Active Directory (Azure AD).</span></span>

<!--
## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [Get agreementAcceptance](../api/agreementacceptance-get.md) | [agreementAcceptance](agreementacceptance.md) | Read properties and relationships of agreementAcceptance object. |
| [Update](../api/agreementacceptance-update.md) | [agreementAcceptance](agreementacceptance.md) | Update an **agreementAcceptance** object. |
| [Delete](../api/agreementacceptance-delete.md) | None | Delete an **agreementAcceptance** object. |
-->

## <a name="properties"></a><span data-ttu-id="2bd8c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2bd8c-107">Properties</span></span>
| <span data-ttu-id="2bd8c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2bd8c-108">Property</span></span>     | <span data-ttu-id="2bd8c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bd8c-109">Type</span></span>        | <span data-ttu-id="2bd8c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bd8c-110">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="2bd8c-111">agreementFileId</span><span class="sxs-lookup"><span data-stu-id="2bd8c-111">agreementFileId</span></span>|<span data-ttu-id="2bd8c-112">String</span><span class="sxs-lookup"><span data-stu-id="2bd8c-112">String</span></span>|<span data-ttu-id="2bd8c-113">Identificador del archivo de contrato aceptado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-113">ID of the agreement file accepted by the user.</span></span>|
|<span data-ttu-id="2bd8c-114">agreementId</span><span class="sxs-lookup"><span data-stu-id="2bd8c-114">agreementId</span></span>|<span data-ttu-id="2bd8c-115">String</span><span class="sxs-lookup"><span data-stu-id="2bd8c-115">String</span></span>|<span data-ttu-id="2bd8c-116">Identificador del contrato.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-116">ID of the agreement.</span></span>|
|<span data-ttu-id="2bd8c-117">id</span><span class="sxs-lookup"><span data-stu-id="2bd8c-117">id</span></span>|<span data-ttu-id="2bd8c-118">String</span><span class="sxs-lookup"><span data-stu-id="2bd8c-118">String</span></span>| <span data-ttu-id="2bd8c-119">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-119">Read-only.</span></span>|
|<span data-ttu-id="2bd8c-120">recordedDateTime</span><span class="sxs-lookup"><span data-stu-id="2bd8c-120">recordedDateTime</span></span>|<span data-ttu-id="2bd8c-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2bd8c-121">DateTimeOffset</span></span>|<span data-ttu-id="2bd8c-p102">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="2bd8c-p102">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="2bd8c-124">estado</span><span class="sxs-lookup"><span data-stu-id="2bd8c-124">state</span></span>|<span data-ttu-id="2bd8c-125">string</span><span class="sxs-lookup"><span data-stu-id="2bd8c-125">string</span></span>| <span data-ttu-id="2bd8c-126">Los valores posibles son: `accepted` y `declined`.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-126">Possible values are: `accepted`, `declined`.</span></span>|
|<span data-ttu-id="2bd8c-127">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="2bd8c-127">userDisplayName</span></span>|<span data-ttu-id="2bd8c-128">String</span><span class="sxs-lookup"><span data-stu-id="2bd8c-128">String</span></span>|<span data-ttu-id="2bd8c-129">Nombre para mostrar del usuario cuando se registró la aceptación.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-129">Display name of the user when the acceptance was recorded.</span></span>|
|<span data-ttu-id="2bd8c-130">userEmail</span><span class="sxs-lookup"><span data-stu-id="2bd8c-130">userEmail</span></span>|<span data-ttu-id="2bd8c-131">String</span><span class="sxs-lookup"><span data-stu-id="2bd8c-131">String</span></span>|<span data-ttu-id="2bd8c-132">Correo electrónico del usuario cuando se registró la aceptación.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-132">Email of the user when the acceptance was recorded.</span></span>|
|<span data-ttu-id="2bd8c-133">userId</span><span class="sxs-lookup"><span data-stu-id="2bd8c-133">userId</span></span>|<span data-ttu-id="2bd8c-134">String</span><span class="sxs-lookup"><span data-stu-id="2bd8c-134">String</span></span>|<span data-ttu-id="2bd8c-135">Identificador del usuario que ha aceptado el contrato.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-135">ID of the user who accepted the agreement.</span></span>|
|<span data-ttu-id="2bd8c-136">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2bd8c-136">userPrincipalName</span></span>|<span data-ttu-id="2bd8c-137">String</span><span class="sxs-lookup"><span data-stu-id="2bd8c-137">String</span></span>|<span data-ttu-id="2bd8c-138">UPN del usuario cuando se registró la aceptación.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-138">UPN of the user when the acceptance was recorded.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2bd8c-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2bd8c-139">Relationships</span></span>
<span data-ttu-id="2bd8c-140">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2bd8c-140">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="2bd8c-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2bd8c-141">JSON representation</span></span>

<span data-ttu-id="2bd8c-142">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2bd8c-142">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreementAcceptance"
}-->

```json
{
  "agreementFileId": "String",
  "agreementId": "String",
  "id": "String (identifier)",
  "recordedDateTime": "String (timestamp)",
  "state": "string",
  "userDisplayName": "String",
  "userEmail": "String",
  "userId": "String",
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "agreementAcceptance resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
