---
title: Tipo de recurso person
description: Una agregación de información acerca de una persona de a través de correo, contactos y las redes sociales. Personas pueden ser contactos locales, los contactos de redes sociales, active directory de su organización y personas desde las comunicaciones de recientes (por ejemplo, correo electrónico y Skype).
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: 7f0f3c71769d2ad8927f634b065253cf118316b4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929385"
---
# <a name="person-resource-type"></a><span data-ttu-id="77b86-104">Tipo de recurso person</span><span class="sxs-lookup"><span data-stu-id="77b86-104">person resource type</span></span>

> <span data-ttu-id="77b86-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77b86-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77b86-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77b86-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="77b86-107">Una agregación de información acerca de una persona de a través de correo, contactos y las redes sociales.</span><span class="sxs-lookup"><span data-stu-id="77b86-107">An aggregation of information about a person from across mail, contacts and social networks.</span></span> <span data-ttu-id="77b86-108">Personas pueden ser contactos locales, los contactos de redes sociales, active directory de su organización y personas desde las comunicaciones de recientes (por ejemplo, correo electrónico y Skype).</span><span class="sxs-lookup"><span data-stu-id="77b86-108">People can be local contacts, contacts from social networking, your organization's directory, and people from recent communications (such as email and Skype).</span></span>

## <a name="methods"></a><span data-ttu-id="77b86-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="77b86-109">Methods</span></span>

| <span data-ttu-id="77b86-110">Método</span><span class="sxs-lookup"><span data-stu-id="77b86-110">Method</span></span> | <span data-ttu-id="77b86-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77b86-111">Return Type</span></span> | <span data-ttu-id="77b86-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="77b86-112">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="77b86-113">List people</span><span class="sxs-lookup"><span data-stu-id="77b86-113">List people</span></span>](../api/user-list-people.md) | <span data-ttu-id="77b86-114">**person**</span><span class="sxs-lookup"><span data-stu-id="77b86-114">**person**</span></span> |<span data-ttu-id="77b86-115">Obtenga una colección de objetos person ordenados por su relevancia para el [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="77b86-115">Get a collection of person objects ordered by their relevance to the [user](../resources/user.md).</span></span>|

## <a name="properties"></a><span data-ttu-id="77b86-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="77b86-116">Properties</span></span>

| <span data-ttu-id="77b86-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="77b86-117">Property</span></span> | <span data-ttu-id="77b86-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="77b86-118">Type</span></span> | <span data-ttu-id="77b86-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="77b86-119">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="77b86-120">birthday</span><span class="sxs-lookup"><span data-stu-id="77b86-120">birthday</span></span>|<span data-ttu-id="77b86-121">string</span><span class="sxs-lookup"><span data-stu-id="77b86-121">string</span></span>|<span data-ttu-id="77b86-122">Cumpleaños del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-122">The person's birthday.</span></span>|
|<span data-ttu-id="77b86-123">companyName</span><span class="sxs-lookup"><span data-stu-id="77b86-123">companyName</span></span>|<span data-ttu-id="77b86-124">string</span><span class="sxs-lookup"><span data-stu-id="77b86-124">string</span></span>|<span data-ttu-id="77b86-125">Nombre de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-125">The name of the person's company.</span></span>|
|<span data-ttu-id="77b86-126">department</span><span class="sxs-lookup"><span data-stu-id="77b86-126">department</span></span>|<span data-ttu-id="77b86-127">string</span><span class="sxs-lookup"><span data-stu-id="77b86-127">string</span></span>|<span data-ttu-id="77b86-128">Departamento del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-128">The person's department.</span></span>|
|<span data-ttu-id="77b86-129">displayName</span><span class="sxs-lookup"><span data-stu-id="77b86-129">displayName</span></span>|<span data-ttu-id="77b86-130">string</span><span class="sxs-lookup"><span data-stu-id="77b86-130">string</span></span>|<span data-ttu-id="77b86-131">Nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-131">The person's display name.</span></span>|
|<span data-ttu-id="77b86-132">emailAddresses</span><span class="sxs-lookup"><span data-stu-id="77b86-132">emailAddresses</span></span>|<span data-ttu-id="77b86-133">colección de [rankedEmailAddress](rankedemailaddress.md)</span><span class="sxs-lookup"><span data-stu-id="77b86-133">[rankedEmailAddress](rankedemailaddress.md) collection</span></span>|<span data-ttu-id="77b86-134">Direcciones de correo electrónico del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-134">The person's email addresses.</span></span>|
|<span data-ttu-id="77b86-135">givenName</span><span class="sxs-lookup"><span data-stu-id="77b86-135">givenName</span></span>|<span data-ttu-id="77b86-136">string</span><span class="sxs-lookup"><span data-stu-id="77b86-136">string</span></span>|<span data-ttu-id="77b86-137">Nombre propio del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-137">The person's given name.</span></span>|
|<span data-ttu-id="77b86-138">id</span><span class="sxs-lookup"><span data-stu-id="77b86-138">id</span></span>|<span data-ttu-id="77b86-139">string</span><span class="sxs-lookup"><span data-stu-id="77b86-139">string</span></span>|<span data-ttu-id="77b86-p104">Identificador único del contacto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="77b86-p104">The person's unique identifier. Read-only.</span></span>|
|<span data-ttu-id="77b86-142">isFavorite</span><span class="sxs-lookup"><span data-stu-id="77b86-142">isFavorite</span></span>|<span data-ttu-id="77b86-143">boolean</span><span class="sxs-lookup"><span data-stu-id="77b86-143">boolean</span></span>|<span data-ttu-id="77b86-144">`true` si el usuario ha marcado este contacto como favorito.</span><span class="sxs-lookup"><span data-stu-id="77b86-144">`true` if the user has flagged this person as a favorite.</span></span>|
|<span data-ttu-id="77b86-145">mailboxType</span><span class="sxs-lookup"><span data-stu-id="77b86-145">mailboxType</span></span>|<span data-ttu-id="77b86-146">string</span><span class="sxs-lookup"><span data-stu-id="77b86-146">string</span></span>|<span data-ttu-id="77b86-147">El tipo de buzón de correo que está representada por la dirección de correo electrónico de la persona.</span><span class="sxs-lookup"><span data-stu-id="77b86-147">The type of mailbox that is represented by the person's email address.</span></span>|
|<span data-ttu-id="77b86-148">officeLocation</span><span class="sxs-lookup"><span data-stu-id="77b86-148">officeLocation</span></span>|<span data-ttu-id="77b86-149">string</span><span class="sxs-lookup"><span data-stu-id="77b86-149">string</span></span>|<span data-ttu-id="77b86-150">Ubicación de la oficina del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-150">The location of the person's office.</span></span>|
|<span data-ttu-id="77b86-151">personNotes</span><span class="sxs-lookup"><span data-stu-id="77b86-151">personNotes</span></span>|<span data-ttu-id="77b86-152">string</span><span class="sxs-lookup"><span data-stu-id="77b86-152">string</span></span>|<span data-ttu-id="77b86-153">Notas de forma libre que el usuario ha tomado sobre este contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-153">Free-form notes that the user has taken about this person.</span></span>|
|<span data-ttu-id="77b86-154">personType</span><span class="sxs-lookup"><span data-stu-id="77b86-154">personType</span></span>|<span data-ttu-id="77b86-155">string</span><span class="sxs-lookup"><span data-stu-id="77b86-155">string</span></span>|<span data-ttu-id="77b86-156">El tipo de persona, por ejemplo la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="77b86-156">The type of person, for example distribution list.</span></span>|
|<span data-ttu-id="77b86-157">phones</span><span class="sxs-lookup"><span data-stu-id="77b86-157">phones</span></span>|<span data-ttu-id="77b86-158">Colección [phone](phone.md)</span><span class="sxs-lookup"><span data-stu-id="77b86-158">[phone](phone.md) collection</span></span>|<span data-ttu-id="77b86-159">Número de teléfono del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-159">The person's phone numbers.</span></span>|
|<span data-ttu-id="77b86-160">postalAddresses</span><span class="sxs-lookup"><span data-stu-id="77b86-160">postalAddresses</span></span>|<span data-ttu-id="77b86-161">Colección [location](location.md)</span><span class="sxs-lookup"><span data-stu-id="77b86-161">[location](location.md) collection</span></span>|<span data-ttu-id="77b86-162">Direcciones del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-162">The person's addresses.</span></span>|
|<span data-ttu-id="77b86-163">profession</span><span class="sxs-lookup"><span data-stu-id="77b86-163">profession</span></span>|<span data-ttu-id="77b86-164">string</span><span class="sxs-lookup"><span data-stu-id="77b86-164">string</span></span>|<span data-ttu-id="77b86-165">Profesión del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-165">The person's profession.</span></span>|
|<span data-ttu-id="77b86-166">orígenes</span><span class="sxs-lookup"><span data-stu-id="77b86-166">sources</span></span>|<span data-ttu-id="77b86-167">colección de [personDataSource](persondatasource.md)</span><span class="sxs-lookup"><span data-stu-id="77b86-167">[personDataSource](persondatasource.md) collection</span></span>|<span data-ttu-id="77b86-168">Los orígenes de los datos de usuario proceden de, por ejemplo, Active Directory o los contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="77b86-168">The sources the user data comes from, for example Directory or Outlook Contacts.</span></span>|
|<span data-ttu-id="77b86-169">surname</span><span class="sxs-lookup"><span data-stu-id="77b86-169">surname</span></span>|<span data-ttu-id="77b86-170">string</span><span class="sxs-lookup"><span data-stu-id="77b86-170">string</span></span>|<span data-ttu-id="77b86-171">Apellido del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-171">The person's surname.</span></span>|
|<span data-ttu-id="77b86-172">title</span><span class="sxs-lookup"><span data-stu-id="77b86-172">title</span></span>|<span data-ttu-id="77b86-173">string</span><span class="sxs-lookup"><span data-stu-id="77b86-173">string</span></span>|<span data-ttu-id="77b86-174">Título de la persona.</span><span class="sxs-lookup"><span data-stu-id="77b86-174">The person's title.</span></span>|
|<span data-ttu-id="77b86-175">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="77b86-175">userPrincipalName</span></span>|<span data-ttu-id="77b86-176">string</span><span class="sxs-lookup"><span data-stu-id="77b86-176">string</span></span>|<span data-ttu-id="77b86-p105">Nombre principal de usuario (UPN) del contacto. El UPN es un nombre de inicio de sesión de Internet del contacto basado en la norma [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). Por convención, se debe asignar al nombre de correo electrónico del contacto. El formato general es alias@domain.</span><span class="sxs-lookup"><span data-stu-id="77b86-p105">The user principal name (UPN) of the person. The UPN is an Internet-style login name for the person based on the Internet standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). By convention, this should map to the person's email name. The general format is alias@domain.</span></span>|
|<span data-ttu-id="77b86-181">websites</span><span class="sxs-lookup"><span data-stu-id="77b86-181">websites</span></span>|<span data-ttu-id="77b86-182">Colección [website](website.md)</span><span class="sxs-lookup"><span data-stu-id="77b86-182">[website](website.md) collection</span></span>|<span data-ttu-id="77b86-183">Sitios web del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-183">The person's websites.</span></span>|
|<span data-ttu-id="77b86-184">yomiCompany</span><span class="sxs-lookup"><span data-stu-id="77b86-184">yomiCompany</span></span>|<span data-ttu-id="77b86-185">string</span><span class="sxs-lookup"><span data-stu-id="77b86-185">string</span></span>|<span data-ttu-id="77b86-186">Nombre fonético japonés de la compañía del contacto.</span><span class="sxs-lookup"><span data-stu-id="77b86-186">The phonetic Japanese name of the person's company.</span></span>|

## <a name="relationships"></a><span data-ttu-id="77b86-187">Relaciones</span><span class="sxs-lookup"><span data-stu-id="77b86-187">Relationships</span></span>

<span data-ttu-id="77b86-188">Ninguno</span><span class="sxs-lookup"><span data-stu-id="77b86-188">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="77b86-189">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="77b86-189">JSON representation</span></span>

<span data-ttu-id="77b86-190">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="77b86-190">Here is a JSON representation of the resource.</span></span>

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
