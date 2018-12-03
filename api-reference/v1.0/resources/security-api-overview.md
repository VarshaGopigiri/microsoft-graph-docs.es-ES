---
title: Usar la API de seguridad de Microsoft Graph
description: 'La API de seguridad de Microsoft Graph proporciona una interfaz unificada y el esquema que se integra con soluciones de seguridad de Microsoft y ecosistema de socios. Esto permite a los clientes a optimizar las operaciones de seguridad y defenderse mejor contra el aumento de las amenazas de Internet. La API de seguridad de Microsoft Graph puede usarse como un servicio de agregación de seguridad federada para enviar consultas a todos los proveedores de seguridad onboarded para obtener respuestas agregadas. Usar API de seguridad de Microsoft Graph para crear aplicaciones que:'
ms.openlocfilehash: 511abbc6221ee9efb58cbfb36082514d98f9b918
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032698"
---
# <a name="use-the-microsoft-graph-security-api"></a><span data-ttu-id="63be7-106">Usar la API de seguridad de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="63be7-106">Use the Microsoft Graph Security API</span></span>

<span data-ttu-id="63be7-107">La API de seguridad de Microsoft Graph proporciona una interfaz unificada y el esquema que se integra con soluciones de seguridad de Microsoft y ecosistema de socios.</span><span class="sxs-lookup"><span data-stu-id="63be7-107">The Microsoft Graph Security API provides a unified interface and schema to integrate with security solutions from Microsoft and ecosystem partners.</span></span> <span data-ttu-id="63be7-108">Esto permite a los clientes a optimizar las operaciones de seguridad y defenderse mejor contra el aumento de las amenazas de Internet.</span><span class="sxs-lookup"><span data-stu-id="63be7-108">This empowers customers to streamline security operations and better defend against increasing cyber threats.</span></span> <span data-ttu-id="63be7-109">La API de seguridad de Microsoft Graph puede usarse como un servicio de agregación de seguridad federada para enviar consultas a todos los proveedores de seguridad onboarded para obtener respuestas agregadas.</span><span class="sxs-lookup"><span data-stu-id="63be7-109">The Microsoft Graph Security API can be used as a federated security aggregation service to submit queries to all onboarded security providers to get aggregated responses.</span></span> <span data-ttu-id="63be7-110">Usar API de seguridad de Microsoft Graph para crear aplicaciones que:</span><span class="sxs-lookup"><span data-stu-id="63be7-110">Use Microsoft Graph Security API to build applications that:</span></span>

- <span data-ttu-id="63be7-111">Consolidar y correlacionar las alertas de seguridad de varios orígenes</span><span class="sxs-lookup"><span data-stu-id="63be7-111">Consolidate and correlate security alerts from multiple sources</span></span>
- <span data-ttu-id="63be7-112">Desbloquear datos contextuales para informar a las investigaciones</span><span class="sxs-lookup"><span data-stu-id="63be7-112">Unlock contextual data to inform investigations</span></span>
- <span data-ttu-id="63be7-113">Automatizar las operaciones de seguridad para aumentar la eficacia</span><span class="sxs-lookup"><span data-stu-id="63be7-113">Automate security operations for greater efficiency</span></span>
- <span data-ttu-id="63be7-114">Proporcionar visibilidad a los datos de seguridad para habilitar la administración de riesgos proactiva</span><span class="sxs-lookup"><span data-stu-id="63be7-114">Provide visibility into security data to enable proactive risk management</span></span>

<span data-ttu-id="63be7-115">La API de seguridad de Microsoft Graph incluye las siguientes entidades de clave.</span><span class="sxs-lookup"><span data-stu-id="63be7-115">The Microsoft Graph Security API includes the following key entities.</span></span>

## <a name="alerts"></a><span data-ttu-id="63be7-116">Alertas</span><span class="sxs-lookup"><span data-stu-id="63be7-116">Alerts</span></span>

<span data-ttu-id="63be7-117">Las alertas son posibles problemas de seguridad dentro de inquilino de un cliente que las soluciones de seguridad de Microsoft o socio han identificado y están marcadas para acción o notificación.</span><span class="sxs-lookup"><span data-stu-id="63be7-117">Alerts are potential security issues within a customer's tenant that Microsoft or partner security solutions have identified and are flagged for action or notification.</span></span> <span data-ttu-id="63be7-118">Con la entidad de [alertas](alert.md) de seguridad de Microsoft Graph, puede unificar y optimizar los problemas de seguridad en todas las soluciones integradas.</span><span class="sxs-lookup"><span data-stu-id="63be7-118">With the Microsoft Graph Security [alerts](alert.md) entity, you can unify and streamline security  issues across all integrated solutions.</span></span> <span data-ttu-id="63be7-119">Esto también permite aplicaciones correlacionar las alertas y contexto para mejorar la protección contra amenazas y la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63be7-119">This also enables applications to correlate alerts and context to improve threat protection and response.</span></span> <span data-ttu-id="63be7-120">Estos desbloquear la eficacia operativa de seguridad reduciendo el tiempo de investigación y tiempo de resolución de incidentes.</span><span class="sxs-lookup"><span data-stu-id="63be7-120">These unlock security operational efficiencies by reducing investigation time and time to resolution for incidents.</span></span> <span data-ttu-id="63be7-121">Con la capacidad de actualización de la alerta, puede sincronizar el estado de alertas específicas a través de productos de seguridad diferentes y servicios que se integran con la API de seguridad de Microsoft Graph mediante la actualización de la entidad de [alertas](alert.md) .</span><span class="sxs-lookup"><span data-stu-id="63be7-121">With the alert update capability, you can sync the status of specific alerts across different security products and services that are integrated with the Microsoft Graph Security API by updating your [alerts](alert.md) entity.</span></span>

<span data-ttu-id="63be7-122">Las soluciones de Microsoft Graph seguridad integrada va a recibir alertas de los siguientes proveedores de seguridad:</span><span class="sxs-lookup"><span data-stu-id="63be7-122">Microsoft Graph Security-integrated solutions will receive alerts from the following security providers:</span></span>

- <span data-ttu-id="63be7-123">Centro de seguridad de Azure</span><span class="sxs-lookup"><span data-stu-id="63be7-123">Azure Security Center</span></span>
- <span data-ttu-id="63be7-124">Protección de identidad de Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="63be7-124">Azure Active Directory Identity Protection</span></span>
- <span data-ttu-id="63be7-125">Protección de la información de Azure</span><span class="sxs-lookup"><span data-stu-id="63be7-125">Azure Information Protection</span></span>
- <span data-ttu-id="63be7-126">Seguridad de aplicaciones de nube de Microsoft</span><span class="sxs-lookup"><span data-stu-id="63be7-126">Microsoft Cloud Application Security</span></span>
- <span data-ttu-id="63be7-127">Windows Defender una protección avanzada</span><span class="sxs-lookup"><span data-stu-id="63be7-127">Windows Defender Advanced Threat Protection</span></span>
- <span data-ttu-id="63be7-128">Microsoft Intune (privada preview)</span><span class="sxs-lookup"><span data-stu-id="63be7-128">Microsoft Intune (private preview)</span></span>
- <span data-ttu-id="63be7-129">Office 365 (próximamente)</span><span class="sxs-lookup"><span data-stu-id="63be7-129">Office 365 (coming soon)</span></span>
- <span data-ttu-id="63be7-130">Azure avanzada protección contra amenazas (próximamente)</span><span class="sxs-lookup"><span data-stu-id="63be7-130">Azure Advanced Threat Protection (coming soon)</span></span>
- <span data-ttu-id="63be7-131">Soluciones de socios, como el marco de aplicaciones de redes de Palo Alto</span><span class="sxs-lookup"><span data-stu-id="63be7-131">Partner solutions, such as Palo Alto Networks App Framework</span></span>

> <span data-ttu-id="63be7-132">**Nota:** Los proveedores de nuevo continuamente son incorporación al ecosistema de seguridad de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="63be7-132">**Note:** New providers are continuously onboarding to the Microsoft Graph Security ecosystem.</span></span>

## <a name="common-use-cases"></a><span data-ttu-id="63be7-133">Casos de uso común</span><span class="sxs-lookup"><span data-stu-id="63be7-133">Common use cases</span></span>

<span data-ttu-id="63be7-134">Las siguientes son algunas de las solicitudes de los más populares para trabajar con la API de seguridad de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="63be7-134">The following are some of the most popular requests for working with the Microsoft Graph Security API:</span></span>

| <span data-ttu-id="63be7-135">**Casos de uso**</span><span class="sxs-lookup"><span data-stu-id="63be7-135">**Use cases**</span></span>   | <span data-ttu-id="63be7-136">**Recursos de REST**</span><span class="sxs-lookup"><span data-stu-id="63be7-136">**REST resources**</span></span> | <span data-ttu-id="63be7-137">**Pruébelo en el Explorador de gráfico**</span><span class="sxs-lookup"><span data-stu-id="63be7-137">**Try it in Graph Explorer**</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="63be7-138">List alerts</span><span class="sxs-lookup"><span data-stu-id="63be7-138">List alerts</span></span> | [<span data-ttu-id="63be7-139">List alerts</span><span class="sxs-lookup"><span data-stu-id="63be7-139">List alerts</span></span>](../api/alert-list.md) | [https://graph.microsoft.com/v1.0/security/alerts](https://developer.microsoft.com/graph/graph-explorer?request=security/alerts&method=GET&version=v1.0&GraphUrl=https://graph.microsoft.com) |
| <span data-ttu-id="63be7-140">Actualización de alertas</span><span class="sxs-lookup"><span data-stu-id="63be7-140">Update alerts</span></span> | [<span data-ttu-id="63be7-141">Update alert</span><span class="sxs-lookup"><span data-stu-id="63be7-141">Update alert</span></span>](../api/alert-update.md) | [https://graph.microsoft.com/v1.0/security/alerts/{alert-id}](https://developer.microsoft.com/graph/graph-explorer?request=security/alerts/{alert-id}&method=PATCH&version=v1.0&GraphUrl=https://graph.microsoft.com) |

<span data-ttu-id="63be7-142">Puede utilizar Microsoft Graph [webhooks](/graph/webhooks) para suscribirse a y recibir notificaciones sobre las actualizaciones a las entidades de seguridad de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="63be7-142">You can use Microsoft Graph [webhooks](/graph/webhooks) to subscribe to and receive notifications about updates to Microsoft Graph Security entities.</span></span>

## <a name="resources"></a><span data-ttu-id="63be7-143">Resources</span><span class="sxs-lookup"><span data-stu-id="63be7-143">Resources</span></span>

<span data-ttu-id="63be7-144">Código y contribuir a estos ejemplos de API de seguridad de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="63be7-144">Code and contribute to these Microsoft Graph Security API samples:</span></span>

- [<span data-ttu-id="63be7-145">Ejemplo de ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="63be7-145">ASP.NET (C#) sample</span></span>](https://github.com/microsoftgraph/aspnet-security-api-sample)
- [<span data-ttu-id="63be7-146">Ejemplo de Python</span><span class="sxs-lookup"><span data-stu-id="63be7-146">Python sample</span></span>](https://github.com/microsoftgraph/python-security-rest-sample)
- [<span data-ttu-id="63be7-147">Ejemplo de Node.js (JavaScript)</span><span class="sxs-lookup"><span data-stu-id="63be7-147">Node.js (JavaScript) sample</span></span>](https://github.com/microsoftgraph/nodejs-security-sample)

<span data-ttu-id="63be7-148">Integrarse con la Comunidad:</span><span class="sxs-lookup"><span data-stu-id="63be7-148">Engage with the community:</span></span>

- [<span data-ttu-id="63be7-149">Únase a la Comunidad de tech</span><span class="sxs-lookup"><span data-stu-id="63be7-149">Join the tech community</span></span>](https://aka.ms/graphsecuritycommunity)
- [<span data-ttu-id="63be7-150">Se analizan en StackOverflow</span><span class="sxs-lookup"><span data-stu-id="63be7-150">Discuss on StackOverflow</span></span>](https://stackoverflow.com/questions/tagged/microsoft-graph-security)

## <a name="next-steps"></a><span data-ttu-id="63be7-151">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="63be7-151">Next steps</span></span>

<span data-ttu-id="63be7-152">La API de seguridad de Microsoft Graph puede abrir nuevas maneras para que pueda integrarse con diferentes soluciones de seguridad de Microsoft y socios.</span><span class="sxs-lookup"><span data-stu-id="63be7-152">The Microsoft Graph Security API can open up new ways for you to engage with different security solutions from Microsoft and partners.</span></span> <span data-ttu-id="63be7-153">Siga estos pasos para empezar:</span><span class="sxs-lookup"><span data-stu-id="63be7-153">Follow these steps to get started:</span></span>

- <span data-ttu-id="63be7-154">Profundizar en [las alertas](alert.md).</span><span class="sxs-lookup"><span data-stu-id="63be7-154">Drill down into [alerts](alert.md).</span></span>
- <span data-ttu-id="63be7-155">Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="63be7-155">Try the API in the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span> <span data-ttu-id="63be7-156">En **Las consultas de ejemplo**, elija **Mostrar más muestras** y establezca la categoría de seguridad **en**.</span><span class="sxs-lookup"><span data-stu-id="63be7-156">Under **Sample Queries**, choose **show more samples** and set the Security category to **on**.</span></span>
- <span data-ttu-id="63be7-157">Intente [receptora y suscribirse a las notificaciones](/graph/webhooks) de cambios de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63be7-157">Try [subscribing to and receiving notifications](/graph/webhooks) on entity changes.</span></span>

<span data-ttu-id="63be7-p106">¿Necesita más ideas? Vea [cómo algunos de nuestros socios utilizan Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).</span><span class="sxs-lookup"><span data-stu-id="63be7-p106">Need more ideas? See [how some of our partners are using Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).</span></span>