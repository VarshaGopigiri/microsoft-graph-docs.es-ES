---
title: Tipo de recurso person
description: Una agregación de información sobre un contacto de correo electrónico, contactos y redes sociales. Los contactos pueden ser contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype).
ms.openlocfilehash: 098e1bd67e151b8c08607ad358935ba45065c8d2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029639"
---
# <a name="person-resource-type"></a><span data-ttu-id="9efba-104">Tipo de recurso person</span><span class="sxs-lookup"><span data-stu-id="9efba-104">person resource type</span></span>

<span data-ttu-id="9efba-p102">Una agregación de información sobre un contacto de correo electrónico, contactos y redes sociales. Los contactos pueden ser contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype).</span><span class="sxs-lookup"><span data-stu-id="9efba-p102">An aggregation of information about a person from across mail, contacts, and social networks. People can be local contacts, contacts from social networking or your organization's directory, and people from recent communications (such as email and Skype).</span></span>

## <a name="methods"></a><span data-ttu-id="9efba-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="9efba-107">Methods</span></span>

| <span data-ttu-id="9efba-108">Método</span><span class="sxs-lookup"><span data-stu-id="9efba-108">Method</span></span> | <span data-ttu-id="9efba-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9efba-109">Return Type</span></span> | <span data-ttu-id="9efba-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9efba-110">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="9efba-111">List people</span><span class="sxs-lookup"><span data-stu-id="9efba-111">List people</span></span>](../api/user-list-people.md) | <span data-ttu-id="9efba-112">**person**</span><span class="sxs-lookup"><span data-stu-id="9efba-112">**person**</span></span> |<span data-ttu-id="9efba-113">Obtenga una colección de objetos person ordenados por su relevancia para el [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="9efba-113">Get a collection of person objects ordered by their relevance to the [user](../resources/user.md).</span></span>|

## <a name="properties"></a><span data-ttu-id="9efba-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9efba-114">Properties</span></span>

| <span data-ttu-id="9efba-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9efba-115">Property</span></span> | <span data-ttu-id="9efba-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="9efba-116">Type</span></span> | <span data-ttu-id="9efba-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9efba-117">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="9efba-118">birthday</span><span class="sxs-lookup"><span data-stu-id="9efba-118">birthday</span></span>|<span data-ttu-id="9efba-119">String</span><span class="sxs-lookup"><span data-stu-id="9efba-119">String</span></span>|<span data-ttu-id="9efba-120">Cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-120">The person's birthday.</span></span>|
|<span data-ttu-id="9efba-121">companyName</span><span class="sxs-lookup"><span data-stu-id="9efba-121">companyName</span></span>|<span data-ttu-id="9efba-122">String</span><span class="sxs-lookup"><span data-stu-id="9efba-122">String</span></span>|<span data-ttu-id="9efba-123">Nombre de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-123">The name of the person's company.</span></span>|
|<span data-ttu-id="9efba-124">department</span><span class="sxs-lookup"><span data-stu-id="9efba-124">department</span></span>|<span data-ttu-id="9efba-125">String</span><span class="sxs-lookup"><span data-stu-id="9efba-125">String</span></span>|<span data-ttu-id="9efba-126">Departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-126">The person's department.</span></span>|
|<span data-ttu-id="9efba-127">displayName</span><span class="sxs-lookup"><span data-stu-id="9efba-127">displayName</span></span>|<span data-ttu-id="9efba-128">String</span><span class="sxs-lookup"><span data-stu-id="9efba-128">String</span></span>|<span data-ttu-id="9efba-129">Nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-129">The person's display name.</span></span>|
|<span data-ttu-id="9efba-130">scoredEmailAddresses</span><span class="sxs-lookup"><span data-stu-id="9efba-130">scoredEmailAddresses</span></span>|<span data-ttu-id="9efba-131">Colección [scoredEmailAddress](scoredemailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="9efba-131">[scoredEmailAddress](scoredemailaddress.md) collection</span></span>|<span data-ttu-id="9efba-132">Direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-132">The person's email addresses.</span></span>|
|<span data-ttu-id="9efba-133">givenName</span><span class="sxs-lookup"><span data-stu-id="9efba-133">givenName</span></span>|<span data-ttu-id="9efba-134">String</span><span class="sxs-lookup"><span data-stu-id="9efba-134">String</span></span>|<span data-ttu-id="9efba-135">Nombre propio del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-135">The person's given name.</span></span>|
|<span data-ttu-id="9efba-136">id</span><span class="sxs-lookup"><span data-stu-id="9efba-136">id</span></span>|<span data-ttu-id="9efba-137">String</span><span class="sxs-lookup"><span data-stu-id="9efba-137">String</span></span>|<span data-ttu-id="9efba-p103">Identificador único del contacto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9efba-p103">The person's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="9efba-140">imAddress</span><span class="sxs-lookup"><span data-stu-id="9efba-140">imAddress</span></span>|<span data-ttu-id="9efba-141">String</span><span class="sxs-lookup"><span data-stu-id="9efba-141">String</span></span>|<span data-ttu-id="9efba-p104">Dirección del protocolo de inicio de sesión (SIP) de voz sobre IP (VOIP) del servicio de mensajería instantánea correspondiente al usuario. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9efba-p104">The instant message voice over IP (VOIP) session initiation protocol (SIP) address for the user. Read-only.</span></span>|
|<span data-ttu-id="9efba-144">isFavorite</span><span class="sxs-lookup"><span data-stu-id="9efba-144">isFavorite</span></span>|<span data-ttu-id="9efba-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="9efba-145">Boolean</span></span>|<span data-ttu-id="9efba-146">`true` si el usuario ha marcado este contacto como favorito.</span><span class="sxs-lookup"><span data-stu-id="9efba-146">`true` if the user has flagged this person as a favorite.</span></span>|
|<span data-ttu-id="9efba-147">jobTitle</span><span class="sxs-lookup"><span data-stu-id="9efba-147">jobTitle</span></span>|<span data-ttu-id="9efba-148">String</span><span class="sxs-lookup"><span data-stu-id="9efba-148">String</span></span>|<span data-ttu-id="9efba-149">Puesto del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-149">The person's job title.</span></span>|
|<span data-ttu-id="9efba-150">officeLocation</span><span class="sxs-lookup"><span data-stu-id="9efba-150">officeLocation</span></span>|<span data-ttu-id="9efba-151">String</span><span class="sxs-lookup"><span data-stu-id="9efba-151">String</span></span>|<span data-ttu-id="9efba-152">Ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-152">The location of the person's office.</span></span>|
|<span data-ttu-id="9efba-153">personNotes</span><span class="sxs-lookup"><span data-stu-id="9efba-153">personNotes</span></span>|<span data-ttu-id="9efba-154">String</span><span class="sxs-lookup"><span data-stu-id="9efba-154">String</span></span>|<span data-ttu-id="9efba-155">Notas de forma libre que el usuario ha tomado sobre este contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-155">Free-form notes that the user has taken about this person.</span></span>|
|<span data-ttu-id="9efba-156">personType</span><span class="sxs-lookup"><span data-stu-id="9efba-156">personType</span></span>|[<span data-ttu-id="9efba-157">personType</span><span class="sxs-lookup"><span data-stu-id="9efba-157">personType</span></span>](persontype.md) |<span data-ttu-id="9efba-158">Tipo de contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-158">The type of person.</span></span>|
|<span data-ttu-id="9efba-159">phones</span><span class="sxs-lookup"><span data-stu-id="9efba-159">phones</span></span>|<span data-ttu-id="9efba-160">Colección [phone](phone.md)</span><span class="sxs-lookup"><span data-stu-id="9efba-160">[phone](phone.md) collection</span></span>|<span data-ttu-id="9efba-161">Número de teléfono del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-161">The person's phone numbers.</span></span>|
|<span data-ttu-id="9efba-162">postalAddresses</span><span class="sxs-lookup"><span data-stu-id="9efba-162">postalAddresses</span></span>|<span data-ttu-id="9efba-163">Colección [location](location.md)</span><span class="sxs-lookup"><span data-stu-id="9efba-163">[location](location.md) collection</span></span>|<span data-ttu-id="9efba-164">Direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-164">The person's addresses.</span></span>|
|<span data-ttu-id="9efba-165">profession</span><span class="sxs-lookup"><span data-stu-id="9efba-165">profession</span></span>|<span data-ttu-id="9efba-166">String</span><span class="sxs-lookup"><span data-stu-id="9efba-166">String</span></span>|<span data-ttu-id="9efba-167">Profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-167">The person's profession.</span></span>|
|<span data-ttu-id="9efba-168">surname</span><span class="sxs-lookup"><span data-stu-id="9efba-168">surname</span></span>|<span data-ttu-id="9efba-169">String</span><span class="sxs-lookup"><span data-stu-id="9efba-169">String</span></span>|<span data-ttu-id="9efba-170">Apellido del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-170">The person's surname.</span></span>|
|<span data-ttu-id="9efba-171">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9efba-171">userPrincipalName</span></span>|<span data-ttu-id="9efba-172">String</span><span class="sxs-lookup"><span data-stu-id="9efba-172">String</span></span>|<span data-ttu-id="9efba-p105">Nombre principal de usuario (UPN) del contacto. El UPN es un nombre de inicio de sesión de Internet del contacto basado en la norma [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). Por convención, se debe asignar al nombre de correo electrónico del contacto. El formato general es alias@domain.</span><span class="sxs-lookup"><span data-stu-id="9efba-p105">The user principal name (UPN) of the person. The UPN is an Internet-style login name for the person based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). By convention, this should map to the person's email name. The general format is alias@domain.</span></span>|
|<span data-ttu-id="9efba-177">websites</span><span class="sxs-lookup"><span data-stu-id="9efba-177">websites</span></span>|<span data-ttu-id="9efba-178">Colección [website](website.md)</span><span class="sxs-lookup"><span data-stu-id="9efba-178">[website](website.md) collection</span></span>|<span data-ttu-id="9efba-179">Sitios web del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-179">The person's websites.</span></span>|
|<span data-ttu-id="9efba-180">yomiCompany</span><span class="sxs-lookup"><span data-stu-id="9efba-180">yomiCompany</span></span>|<span data-ttu-id="9efba-181">String</span><span class="sxs-lookup"><span data-stu-id="9efba-181">String</span></span>|<span data-ttu-id="9efba-182">Nombre fonético japonés de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="9efba-182">The phonetic Japanese name of the person's company.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9efba-183">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9efba-183">Relationships</span></span>

<span data-ttu-id="9efba-184">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9efba-184">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9efba-185">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9efba-185">JSON representation</span></span>

<span data-ttu-id="9efba-186">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9efba-186">The following is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.person"
}-->

```json
{
  "birthday": "string",
  "companyName": "string",
  "department": "string",
  "displayName": "string",
  "scoredEmailAddresses": [{"@odata.type": "microsoft.graph.scoredEmailAddress"}],
  "givenName": "string",
  "id": "string (identifier)",
  "imAddress": "string",
  "isFavorite": true,
  "jobTitle": "string",
  "officeLocation": "string",
  "personNotes": "string",
  "personType": {"@odata.type": "microsoft.graph.personType"},
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "postalAddresses": [{"@odata.type": "microsoft.graph.location"}],
  "profession": "string",
  "surname": "string",
  "userPrincipalName": "string",
  "websites": [{"@odata.type": "microsoft.graph.website"}],
  "yomiCompany": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "person resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
