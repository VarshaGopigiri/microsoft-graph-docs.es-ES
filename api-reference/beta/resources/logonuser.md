---
title: tipo de recurso de logonUser
description: Contiene información de estado sobre el usuario ha iniciado sesión en este host
localization_priority: Normal
ms.openlocfilehash: 3b7862555c62eb16aaceaa53d4df58541426e08a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855597"
---
# <a name="logonuser-resource-type"></a><span data-ttu-id="f71c5-103">tipo de recurso de logonUser</span><span class="sxs-lookup"><span data-stu-id="f71c5-103">logonUser resource type</span></span>

<span data-ttu-id="f71c5-104">Contiene información de estado sobre el usuario ha iniciado sesión en este host</span><span class="sxs-lookup"><span data-stu-id="f71c5-104">Contains stateful information about the logged on user on this host</span></span>

## <a name="properties"></a><span data-ttu-id="f71c5-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f71c5-105">Properties</span></span>

| <span data-ttu-id="f71c5-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f71c5-106">Property</span></span>   | <span data-ttu-id="f71c5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f71c5-107">Type</span></span> |<span data-ttu-id="f71c5-108">Description</span><span class="sxs-lookup"><span data-stu-id="f71c5-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f71c5-109">accountDomain</span><span class="sxs-lookup"><span data-stu-id="f71c5-109">accountDomain</span></span>|<span data-ttu-id="f71c5-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="f71c5-110">String</span></span>|<span data-ttu-id="f71c5-111">Dominio de la cuenta de usuario que se usa para el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="f71c5-111">Domain of user account used to logon.</span></span>|
|<span data-ttu-id="f71c5-112">accountName</span><span class="sxs-lookup"><span data-stu-id="f71c5-112">accountName</span></span>|<span data-ttu-id="f71c5-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="f71c5-113">String</span></span>|<span data-ttu-id="f71c5-114">Nombre de cuenta de la cuenta de usuario que se usa para el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="f71c5-114">Account name of user account used to logon.</span></span>|
|<span data-ttu-id="f71c5-115">accountType</span><span class="sxs-lookup"><span data-stu-id="f71c5-115">accountType</span></span>|<span data-ttu-id="f71c5-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="f71c5-116">String</span></span>|<span data-ttu-id="f71c5-117">Tipo de cuenta de usuario, por definición de Windows.</span><span class="sxs-lookup"><span data-stu-id="f71c5-117">User Account type, per Windows definition.</span></span> <span data-ttu-id="f71c5-118">Los valores posibles son: `unknown`, `standard`, `power` y `administrator`.</span><span class="sxs-lookup"><span data-stu-id="f71c5-118">Possible values are: `unknown`, `standard`, `power`, `administrator`.</span></span>|
|<span data-ttu-id="f71c5-119">firstSeenDateTime</span><span class="sxs-lookup"><span data-stu-id="f71c5-119">firstSeenDateTime</span></span>|<span data-ttu-id="f71c5-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f71c5-120">DateTimeOffset</span></span>|<span data-ttu-id="f71c5-121">Fecha y hora en que se produjo el inicio de sesión más antigua por esta cuenta de usuario (período determinados por el proveedor).</span><span class="sxs-lookup"><span data-stu-id="f71c5-121">DateTime at which the earliest logon by this user account occurred (provider-determined period).</span></span> <span data-ttu-id="f71c5-122">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="f71c5-122">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="f71c5-123">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="f71c5-123">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="f71c5-124">lastSeenDateTime</span><span class="sxs-lookup"><span data-stu-id="f71c5-124">lastSeenDateTime</span></span>|<span data-ttu-id="f71c5-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f71c5-125">DateTimeOffset</span></span>|<span data-ttu-id="f71c5-126">Fecha y hora en que se produjo el último inicio de sesión por esta cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f71c5-126">DateTime at which the latest logon by this user account occurred.</span></span> <span data-ttu-id="f71c5-127">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="f71c5-127">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="f71c5-128">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="f71c5-128">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="f71c5-129">ID de registro</span><span class="sxs-lookup"><span data-stu-id="f71c5-129">logonId</span></span>|<span data-ttu-id="f71c5-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="f71c5-130">String</span></span>|<span data-ttu-id="f71c5-131">Identificador de inicio de sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="f71c5-131">User logon ID.</span></span>|
|<span data-ttu-id="f71c5-132">logonTypes</span><span class="sxs-lookup"><span data-stu-id="f71c5-132">logonTypes</span></span>|<span data-ttu-id="f71c5-133">Colección String</span><span class="sxs-lookup"><span data-stu-id="f71c5-133">String collection</span></span>|<span data-ttu-id="f71c5-134">Colección de los tipos de inicio de sesión para el usuario ha iniciado la sesión de observar cuando primero a último visto.</span><span class="sxs-lookup"><span data-stu-id="f71c5-134">Collection of the logon types observed for the logged on user from when first to last seen.</span></span> <span data-ttu-id="f71c5-135">Los valores posibles son: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.</span><span class="sxs-lookup"><span data-stu-id="f71c5-135">Possible values are: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f71c5-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f71c5-136">JSON representation</span></span>

<span data-ttu-id="f71c5-137">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f71c5-137">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.logonUser"
}-->

```json
{
  "accountDomain": "String",
  "accountName": "String",
  "accountType": "String",
  "firstSeenDateTime": "String (timestamp)",
  "lastSeenDateTime": "String (timestamp)",
  "logonId": "String",
  "logonTypes": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "logonUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
