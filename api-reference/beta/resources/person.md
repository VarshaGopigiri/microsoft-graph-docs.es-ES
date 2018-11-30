---
title: Tipo de recurso person
description: Una agregación de información acerca de una persona de a través de correo, contactos y las redes sociales. Personas pueden ser contactos locales, los contactos de redes sociales, active directory de su organización y personas desde las comunicaciones de recientes (por ejemplo, correo electrónico y Skype).
ms.openlocfilehash: d9533c3550ec870c887b1e447fd0daf114bcfc83
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083260"
---
# <a name="person-resource-type"></a><span data-ttu-id="5f12e-104">Tipo de recurso person</span><span class="sxs-lookup"><span data-stu-id="5f12e-104">person resource type</span></span>

> <span data-ttu-id="5f12e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f12e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5f12e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f12e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5f12e-107">Una agregación de información acerca de una persona de a través de correo, contactos y las redes sociales.</span><span class="sxs-lookup"><span data-stu-id="5f12e-107">An aggregation of information about a person from across mail, contacts and social networks.</span></span> <span data-ttu-id="5f12e-108">Personas pueden ser contactos locales, los contactos de redes sociales, active directory de su organización y personas desde las comunicaciones de recientes (por ejemplo, correo electrónico y Skype).</span><span class="sxs-lookup"><span data-stu-id="5f12e-108">People can be local contacts, contacts from social networking, your organization's directory, and people from recent communications (such as email and Skype).</span></span>

## <a name="methods"></a><span data-ttu-id="5f12e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f12e-109">Methods</span></span>

| <span data-ttu-id="5f12e-110">Método</span><span class="sxs-lookup"><span data-stu-id="5f12e-110">Method</span></span> | <span data-ttu-id="5f12e-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f12e-111">Return Type</span></span> | <span data-ttu-id="5f12e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f12e-112">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="5f12e-113">List people</span><span class="sxs-lookup"><span data-stu-id="5f12e-113">List people</span></span>](../api/user-list-people.md) | <span data-ttu-id="5f12e-114">**person**</span><span class="sxs-lookup"><span data-stu-id="5f12e-114">**person**</span></span> |<span data-ttu-id="5f12e-115">Obtenga una colección de objetos person ordenados por su relevancia para el [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="5f12e-115">Get a collection of person objects ordered by their relevance to the [user](../resources/user.md).</span></span>|

## <a name="properties"></a><span data-ttu-id="5f12e-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f12e-116">Properties</span></span>

| <span data-ttu-id="5f12e-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f12e-117">Property</span></span> | <span data-ttu-id="5f12e-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f12e-118">Type</span></span> | <span data-ttu-id="5f12e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f12e-119">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="5f12e-120">birthday</span><span class="sxs-lookup"><span data-stu-id="5f12e-120">birthday</span></span>|<span data-ttu-id="5f12e-121">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-121">string</span></span>|<span data-ttu-id="5f12e-122">Cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-122">The person's birthday.</span></span>|
|<span data-ttu-id="5f12e-123">companyName</span><span class="sxs-lookup"><span data-stu-id="5f12e-123">companyName</span></span>|<span data-ttu-id="5f12e-124">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-124">string</span></span>|<span data-ttu-id="5f12e-125">Nombre de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-125">The name of the person's company.</span></span>|
|<span data-ttu-id="5f12e-126">department</span><span class="sxs-lookup"><span data-stu-id="5f12e-126">department</span></span>|<span data-ttu-id="5f12e-127">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-127">string</span></span>|<span data-ttu-id="5f12e-128">Departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-128">The person's department.</span></span>|
|<span data-ttu-id="5f12e-129">displayName</span><span class="sxs-lookup"><span data-stu-id="5f12e-129">displayName</span></span>|<span data-ttu-id="5f12e-130">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-130">string</span></span>|<span data-ttu-id="5f12e-131">Nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-131">The person's display name.</span></span>|
|<span data-ttu-id="5f12e-132">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="5f12e-132">emailAddresses</span></span>|<span data-ttu-id="5f12e-133">colección de [rankedEmailAddress](rankedemailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="5f12e-133">[rankedEmailAddress](rankedemailaddress.md) collection</span></span>|<span data-ttu-id="5f12e-134">Direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-134">The person's email addresses.</span></span>|
|<span data-ttu-id="5f12e-135">givenName</span><span class="sxs-lookup"><span data-stu-id="5f12e-135">givenName</span></span>|<span data-ttu-id="5f12e-136">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-136">string</span></span>|<span data-ttu-id="5f12e-137">Nombre propio del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-137">The person's given name.</span></span>|
|<span data-ttu-id="5f12e-138">id</span><span class="sxs-lookup"><span data-stu-id="5f12e-138">id</span></span>|<span data-ttu-id="5f12e-139">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-139">string</span></span>|<span data-ttu-id="5f12e-p104">Identificador único del contacto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f12e-p104">The person's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="5f12e-142">isFavorite</span><span class="sxs-lookup"><span data-stu-id="5f12e-142">isFavorite</span></span>|<span data-ttu-id="5f12e-143">boolean</span><span class="sxs-lookup"><span data-stu-id="5f12e-143">boolean</span></span>|<span data-ttu-id="5f12e-144">`true` si el usuario ha marcado este contacto como favorito.</span><span class="sxs-lookup"><span data-stu-id="5f12e-144">`true` if the user has flagged this person as a favorite.</span></span>|
|<span data-ttu-id="5f12e-145">mailboxType</span><span class="sxs-lookup"><span data-stu-id="5f12e-145">mailboxType</span></span>|<span data-ttu-id="5f12e-146">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-146">string</span></span>|<span data-ttu-id="5f12e-147">El tipo de buzón de correo que está representada por la dirección de correo electrónico de la persona.</span><span class="sxs-lookup"><span data-stu-id="5f12e-147">The type of mailbox that is represented by the person's email address.</span></span>|
|<span data-ttu-id="5f12e-148">officeLocation</span><span class="sxs-lookup"><span data-stu-id="5f12e-148">officeLocation</span></span>|<span data-ttu-id="5f12e-149">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-149">string</span></span>|<span data-ttu-id="5f12e-150">Ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-150">The location of the person's office.</span></span>|
|<span data-ttu-id="5f12e-151">personNotes</span><span class="sxs-lookup"><span data-stu-id="5f12e-151">personNotes</span></span>|<span data-ttu-id="5f12e-152">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-152">string</span></span>|<span data-ttu-id="5f12e-153">Notas de forma libre que el usuario ha tomado sobre este contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-153">Free-form notes that the user has taken about this person.</span></span>|
|<span data-ttu-id="5f12e-154">personType</span><span class="sxs-lookup"><span data-stu-id="5f12e-154">personType</span></span>|<span data-ttu-id="5f12e-155">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-155">string</span></span>|<span data-ttu-id="5f12e-156">El tipo de persona, por ejemplo la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="5f12e-156">The type of person, for example distribution list.</span></span>|
|<span data-ttu-id="5f12e-157">phones</span><span class="sxs-lookup"><span data-stu-id="5f12e-157">phones</span></span>|<span data-ttu-id="5f12e-158">Colección [phone](phone.md)</span><span class="sxs-lookup"><span data-stu-id="5f12e-158">[phone](phone.md) collection</span></span>|<span data-ttu-id="5f12e-159">Número de teléfono del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-159">The person's phone numbers.</span></span>|
|<span data-ttu-id="5f12e-160">postalAddresses</span><span class="sxs-lookup"><span data-stu-id="5f12e-160">postalAddresses</span></span>|<span data-ttu-id="5f12e-161">Colección [location](location.md)</span><span class="sxs-lookup"><span data-stu-id="5f12e-161">[location](location.md) collection</span></span>|<span data-ttu-id="5f12e-162">Direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-162">The person's addresses.</span></span>|
|<span data-ttu-id="5f12e-163">profession</span><span class="sxs-lookup"><span data-stu-id="5f12e-163">profession</span></span>|<span data-ttu-id="5f12e-164">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-164">string</span></span>|<span data-ttu-id="5f12e-165">Profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-165">The person's profession.</span></span>|
|<span data-ttu-id="5f12e-166">orígenes</span><span class="sxs-lookup"><span data-stu-id="5f12e-166">sources</span></span>|<span data-ttu-id="5f12e-167">colección de [personDataSource](persondatasource.md)</span><span class="sxs-lookup"><span data-stu-id="5f12e-167">[personDataSource](persondatasource.md) collection</span></span>|<span data-ttu-id="5f12e-168">Los orígenes de los datos de usuario proceden de, por ejemplo, Active Directory o los contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="5f12e-168">The sources the user data comes from, for example Directory or Outlook Contacts.</span></span>|
|<span data-ttu-id="5f12e-169">surname</span><span class="sxs-lookup"><span data-stu-id="5f12e-169">surname</span></span>|<span data-ttu-id="5f12e-170">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-170">string</span></span>|<span data-ttu-id="5f12e-171">Apellido del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-171">The person's surname.</span></span>|
|<span data-ttu-id="5f12e-172">title</span><span class="sxs-lookup"><span data-stu-id="5f12e-172">title</span></span>|<span data-ttu-id="5f12e-173">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-173">string</span></span>|<span data-ttu-id="5f12e-174">Título de la persona.</span><span class="sxs-lookup"><span data-stu-id="5f12e-174">The person's title.</span></span>|
|<span data-ttu-id="5f12e-175">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5f12e-175">userPrincipalName</span></span>|<span data-ttu-id="5f12e-176">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-176">string</span></span>|<span data-ttu-id="5f12e-p105">Nombre principal de usuario (UPN) del contacto. El UPN es un nombre de inicio de sesión de Internet del contacto basado en la norma [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). Por convención, se debe asignar al nombre de correo electrónico del contacto. El formato general es alias@domain.</span><span class="sxs-lookup"><span data-stu-id="5f12e-p105">The user principal name (UPN) of the person. The UPN is an Internet-style login name for the person based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). By convention, this should map to the person's email name. The general format is alias@domain.</span></span>|
|<span data-ttu-id="5f12e-181">websites</span><span class="sxs-lookup"><span data-stu-id="5f12e-181">websites</span></span>|<span data-ttu-id="5f12e-182">Colección [website](website.md)</span><span class="sxs-lookup"><span data-stu-id="5f12e-182">[website](website.md) collection</span></span>|<span data-ttu-id="5f12e-183">Sitios web del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-183">The person's websites.</span></span>|
|<span data-ttu-id="5f12e-184">yomiCompany</span><span class="sxs-lookup"><span data-stu-id="5f12e-184">yomiCompany</span></span>|<span data-ttu-id="5f12e-185">string</span><span class="sxs-lookup"><span data-stu-id="5f12e-185">string</span></span>|<span data-ttu-id="5f12e-186">Nombre fonético japonés de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="5f12e-186">The phonetic Japanese name of the person's company.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5f12e-187">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5f12e-187">Relationships</span></span>

<span data-ttu-id="5f12e-188">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5f12e-188">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="5f12e-189">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5f12e-189">JSON representation</span></span>

<span data-ttu-id="5f12e-190">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5f12e-190">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.person"
}-->

```json
{
  "birthday": "string",
  "companyName": "string",
  "department": "string",
  "displayName": "string",
  "emailAddresses": [{"@odata.type": "microsoft.graph.rankedEmailAddress"}],
  "givenName": "string",
  "id": "string (identifier)",
  "isFavorite": true,
  "mailboxType": "string",
  "officeLocation": "string",
  "personNotes": "string",
  "personType": "string",
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "postalAddresses": [{"@odata.type": "microsoft.graph.location"}],
  "profession": "string",
  "sources": [{"@odata.type": "microsoft.graph.personDataSource"}],
  "surname": "string",
  "title": "string",
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