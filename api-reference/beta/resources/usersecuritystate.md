---
title: tipo de recurso userSecurityState
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: f530ac1a657b4049c17bdcdd40f1dd5ea734f278
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086833"
---
# <a name="usersecuritystate-resource-type"></a><span data-ttu-id="bb9fb-104">tipo de recurso userSecurityState</span><span class="sxs-lookup"><span data-stu-id="bb9fb-104">userSecurityState resource type</span></span>

 > <span data-ttu-id="bb9fb-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bb9fb-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bb9fb-107">Contiene información de estado acerca de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-107">Contains stateful information about the user account.</span></span>

## <a name="properties"></a><span data-ttu-id="bb9fb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb9fb-108">Properties</span></span>

| <span data-ttu-id="bb9fb-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb9fb-109">Property</span></span>   | <span data-ttu-id="bb9fb-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb9fb-110">Type</span></span> |<span data-ttu-id="bb9fb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb9fb-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb9fb-112">aadUserId</span><span class="sxs-lookup"><span data-stu-id="bb9fb-112">aadUserId</span></span>|<span data-ttu-id="bb9fb-113">String</span><span class="sxs-lookup"><span data-stu-id="bb9fb-113">String</span></span>|<span data-ttu-id="bb9fb-114">AAD usuario identificador (GUID) - objeto representa la entidad de usuario físicos/multi-account.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-114">AAD User object identifier (GUID) - represents the physical/multi-account user entity.</span></span>|
|<span data-ttu-id="bb9fb-115">accountName</span><span class="sxs-lookup"><span data-stu-id="bb9fb-115">accountName</span></span>|<span data-ttu-id="bb9fb-116">String</span><span class="sxs-lookup"><span data-stu-id="bb9fb-116">String</span></span>|<span data-ttu-id="bb9fb-117">Nombre de cuenta de la cuenta de usuario (sin dominio de Active Directory o dominio DNS) - (también denominada `mailNickName`).</span><span class="sxs-lookup"><span data-stu-id="bb9fb-117">Account name of user account (without Active Directory domain or DNS domain) - (also called `mailNickName`).</span></span>|
|<span data-ttu-id="bb9fb-118">domainName</span><span class="sxs-lookup"><span data-stu-id="bb9fb-118">domainName</span></span>|<span data-ttu-id="bb9fb-119">String</span><span class="sxs-lookup"><span data-stu-id="bb9fb-119">String</span></span>|<span data-ttu-id="bb9fb-120">Dominio de NetBIOS o Active Directory de la cuenta de usuario (es decir, el formato dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="bb9fb-120">NetBIOS/Active Directory domain of user account (that is, domain\account format).</span></span>|
|<span data-ttu-id="bb9fb-121">emailRole</span><span class="sxs-lookup"><span data-stu-id="bb9fb-121">emailRole</span></span>|<span data-ttu-id="bb9fb-122">emailRole</span><span class="sxs-lookup"><span data-stu-id="bb9fb-122">emailRole</span></span>|<span data-ttu-id="bb9fb-123">Para las alertas relacionadas con el correo electrónico - correo electrónico de una cuenta de usuario 'rol'.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-123">For email-related alerts - user account's email 'role'.</span></span> <span data-ttu-id="bb9fb-124">Los valores posibles son: `unknown`, `sender` y `recipient`.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-124">Possible values are: `unknown`, `sender`, `recipient`.</span></span>|
|<span data-ttu-id="bb9fb-125">isVpn</span><span class="sxs-lookup"><span data-stu-id="bb9fb-125">isVpn</span></span>|<span data-ttu-id="bb9fb-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="bb9fb-126">Boolean</span></span>|<span data-ttu-id="bb9fb-127">Indica si el usuario se conectó a través de una red privada virtual.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-127">Indicates whether the user logged on through a VPN.</span></span>|
|<span data-ttu-id="bb9fb-128">logonDateTime</span><span class="sxs-lookup"><span data-stu-id="bb9fb-128">logonDateTime</span></span>|<span data-ttu-id="bb9fb-129">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb9fb-129">DateTimeOffset</span></span>|<span data-ttu-id="bb9fb-130">Hora a la que el inicio de sesión se produjo.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-130">Time at which the sign-in occurred.</span></span> <span data-ttu-id="bb9fb-131">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-131">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="bb9fb-132">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-132">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="bb9fb-133">ID de registro</span><span class="sxs-lookup"><span data-stu-id="bb9fb-133">logonId</span></span>|<span data-ttu-id="bb9fb-134">String</span><span class="sxs-lookup"><span data-stu-id="bb9fb-134">String</span></span>|<span data-ttu-id="bb9fb-135">Identificador de usuario de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-135">User sign-in ID.</span></span>|
|<span data-ttu-id="bb9fb-136">logonIp</span><span class="sxs-lookup"><span data-stu-id="bb9fb-136">logonIp</span></span>|<span data-ttu-id="bb9fb-137">String</span><span class="sxs-lookup"><span data-stu-id="bb9fb-137">String</span></span>|<span data-ttu-id="bb9fb-138">Dirección IP de. que la solicitud de inicio de sesión se originó.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-138">IP Address the sign-in request originated from.</span></span>|
|<span data-ttu-id="bb9fb-139">logonLocation</span><span class="sxs-lookup"><span data-stu-id="bb9fb-139">logonLocation</span></span>|<span data-ttu-id="bb9fb-140">String</span><span class="sxs-lookup"><span data-stu-id="bb9fb-140">String</span></span>|<span data-ttu-id="bb9fb-141">Ubicación (mediante la asignación de direcciones IP) asociado a un evento de inicio de sesión de usuario por este usuario.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-141">Location (by IP address mapping) associated with a user sign-in event by this user.</span></span>|
|<span data-ttu-id="bb9fb-142">logonType</span><span class="sxs-lookup"><span data-stu-id="bb9fb-142">logonType</span></span>|<span data-ttu-id="bb9fb-143">logonType</span><span class="sxs-lookup"><span data-stu-id="bb9fb-143">logonType</span></span>|<span data-ttu-id="bb9fb-144">Método de inicio de sesión de usuario en.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-144">Method of user sign in.</span></span> <span data-ttu-id="bb9fb-145">Los valores posibles son: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-145">Possible values are: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.</span></span>|
|<span data-ttu-id="bb9fb-146">onPremisesSecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="bb9fb-146">onPremisesSecurityIdentifier</span></span>|<span data-ttu-id="bb9fb-147">String</span><span class="sxs-lookup"><span data-stu-id="bb9fb-147">String</span></span>|<span data-ttu-id="bb9fb-148">Active Directory (local) identificador de seguridad (SID) del usuario.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-148">Active Directory (on-premises) Security Identifier (SID) of the user.</span></span>|
|<span data-ttu-id="bb9fb-149">riskScore</span><span class="sxs-lookup"><span data-stu-id="bb9fb-149">riskScore</span></span>|<span data-ttu-id="bb9fb-150">String</span><span class="sxs-lookup"><span data-stu-id="bb9fb-150">String</span></span>|<span data-ttu-id="bb9fb-151">Puntuación de proveedor generado/calculada en el riesgo de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-151">Provider-generated/calculated risk score of the user account.</span></span> <span data-ttu-id="bb9fb-152">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-152">Recommended value range of 0-1, which equates to a percentage.</span></span>|
|<span data-ttu-id="bb9fb-153">userAccountType</span><span class="sxs-lookup"><span data-stu-id="bb9fb-153">userAccountType</span></span>|<span data-ttu-id="bb9fb-154">userAccountSecurityType</span><span class="sxs-lookup"><span data-stu-id="bb9fb-154">userAccountSecurityType</span></span>|<span data-ttu-id="bb9fb-155">Tipo de cuenta de usuario (pertenencia a grupos), por definición de Windows.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-155">User account type (group membership), per Windows definition.</span></span> <span data-ttu-id="bb9fb-156">Los valores posibles son: `unknown`, `standard`, `power` y `administrator`.</span><span class="sxs-lookup"><span data-stu-id="bb9fb-156">Possible values are: `unknown`, `standard`, `power`, `administrator`.</span></span>|
|<span data-ttu-id="bb9fb-157">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bb9fb-157">userPrincipalName</span></span>|<span data-ttu-id="bb9fb-158">String</span><span class="sxs-lookup"><span data-stu-id="bb9fb-158">String</span></span>|<span data-ttu-id="bb9fb-159">Inicio de sesión de nombre de usuario - formato de internet: (nombre de cuenta de usuario) @(nombre de dominio DNS de cuenta de usuario).</span><span class="sxs-lookup"><span data-stu-id="bb9fb-159">User sign-in name - internet format: (user account name)@(user account DNS domain name).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="bb9fb-160">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bb9fb-160">JSON representation</span></span>

<span data-ttu-id="bb9fb-161">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="bb9fb-161">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.userSecurityState"
}-->

```json
{
  "aadUserId": "String",
  "accountName": "String",
  "domainName": "String",
  "emailRole": "@odata.type: microsoft.graph.emailRole",
  "isVpn": true,
  "logonDateTime": "String (timestamp)",
  "logonId": "String",
  "logonIp": "String",
  "logonLocation": "String",
  "logonType": "@odata.type: microsoft.graph.logonType",
  "onPremisesSecurityIdentifier": "String",
  "riskScore": "String",
  "userAccountType": "@odata.type: microsoft.graph.userAccountSecurityType",
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "userSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
