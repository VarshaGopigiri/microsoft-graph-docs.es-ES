---
title: Introducción a la API de registro de auditoría de Azure AD
description: Azure Active Directory (AD Azure) realiza un seguimiento de las métricas de actividad e inicio de sesión de usuario y auditoría de crea informes de registro que le ayudarán a comprender la forma en que los usuarios tener acceso y aprovechan los servicios de Azure AD. Usar la API de gráfico de Microsoft para Azure AD para analizar los datos subyacentes de estos informes y para crear soluciones personalizadas adaptadas a necesidades específicas de su organización.
ms.openlocfilehash: b25e9820d4f6df0c6a38fc9784a37ce8a82ceeb1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084594"
---
# <a name="azure-ad-audit-log-api-overview"></a><span data-ttu-id="5cefd-104">Introducción a la API de registro de auditoría de Azure AD</span><span class="sxs-lookup"><span data-stu-id="5cefd-104">Azure AD audit log API overview</span></span>

> <span data-ttu-id="5cefd-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5cefd-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5cefd-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5cefd-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5cefd-107">Azure Active Directory (AD Azure) realiza un seguimiento de las métricas de actividad e inicio de sesión de usuario y auditoría de crea informes de registro que le ayudarán a comprender la forma en que los usuarios tener acceso y aprovechan los servicios de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5cefd-107">Azure Active Directory (Azure AD) tracks user activity and sign-in metrics and creates audit log reports that help you understand how your users access and leverage Azure AD services.</span></span> <span data-ttu-id="5cefd-108">Usar la API de gráfico de Microsoft para Azure AD para analizar los datos subyacentes de estos informes y para crear soluciones personalizadas adaptadas a necesidades específicas de su organización.</span><span class="sxs-lookup"><span data-stu-id="5cefd-108">Use the Microsoft Graph API for Azure AD to analyze the data underlying these reports and to create custom solutions tailored to your organization's specific needs.</span></span>

## <a name="what-are-azure-ad-activity-logs"></a><span data-ttu-id="5cefd-109">¿Cuáles son las actividades de Azure AD registros?</span><span class="sxs-lookup"><span data-stu-id="5cefd-109">What are Azure AD activity logs?</span></span>

<span data-ttu-id="5cefd-110">Azure AD proporciona dos tipos de registros de actividad:</span><span class="sxs-lookup"><span data-stu-id="5cefd-110">Azure AD provides two types of activity logs:</span></span>

- <span data-ttu-id="5cefd-111">registros de auditoría</span><span class="sxs-lookup"><span data-stu-id="5cefd-111">audit logs</span></span> 
- <span data-ttu-id="5cefd-112">registros de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="5cefd-112">sign-in logs</span></span>

### <a name="audit-logs"></a><span data-ttu-id="5cefd-113">Registros de auditoría</span><span class="sxs-lookup"><span data-stu-id="5cefd-113">Audit logs</span></span>

<span data-ttu-id="5cefd-114">El informe de actividad de los registros de auditoría proporciona acceso al historial de cada tarea que se lleva a cabo en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="5cefd-114">The audit logs activity report provides you with access to the history of every task performed in your tenant.</span></span> <span data-ttu-id="5cefd-115">El informe de los registros de auditoría proporciona con los registros de las actividades del sistema para el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="5cefd-115">The audit logs report provides you with records of system activities for compliance.</span></span> <span data-ttu-id="5cefd-116">Entre otras cosas, los datos proporcionados permiten abordar escenarios comunes, como:</span><span class="sxs-lookup"><span data-stu-id="5cefd-116">Amongst others, the provided data enables you to address common scenarios such as:</span></span>

- <span data-ttu-id="5cefd-117">¿Quién concedido acceso al grupo de administración a un usuario de Active directory?</span><span class="sxs-lookup"><span data-stu-id="5cefd-117">Who granted admin group access to a directory user?</span></span>

- <span data-ttu-id="5cefd-118">¿Los usuarios que inicien sesión en una aplicación de adquirido recientemente?</span><span class="sxs-lookup"><span data-stu-id="5cefd-118">Which users are signing in to a recently acquired app?</span></span>

- <span data-ttu-id="5cefd-119">¿Restablece las contraseñas cuántos se han realizado en el directorio?</span><span class="sxs-lookup"><span data-stu-id="5cefd-119">How many passwords resets were made within the directory?</span></span>

### <a name="sign-in-logs"></a><span data-ttu-id="5cefd-120">Inicie sesión en los registros</span><span class="sxs-lookup"><span data-stu-id="5cefd-120">Sign in logs</span></span>

<span data-ttu-id="5cefd-121">El informe de actividad de inicios de sesión le ayuda a determinar quién realizó las tareas de los informes de registro de auditoría.</span><span class="sxs-lookup"><span data-stu-id="5cefd-121">The sign-ins activity report helps you determine who performed the tasks reported by audit log reports.</span></span> <span data-ttu-id="5cefd-122">El informe de actividad de inicios de sesión le ayudará a responder a preguntas como:</span><span class="sxs-lookup"><span data-stu-id="5cefd-122">The sign-ins activity report helps you answer questions like:</span></span>

- <span data-ttu-id="5cefd-123">¿Qué es la trama de un usuario para iniciar sesión?</span><span class="sxs-lookup"><span data-stu-id="5cefd-123">What is the sign in pattern of a user?</span></span>
- <span data-ttu-id="5cefd-124">¿Cuántos usuarios han iniciado sesión en durante la última semana?</span><span class="sxs-lookup"><span data-stu-id="5cefd-124">How many users have signed in during the last week?</span></span>
- <span data-ttu-id="5cefd-125">¿Qué es el estado de estos inicios de sesión?</span><span class="sxs-lookup"><span data-stu-id="5cefd-125">What's the status of these sign-ins?</span></span>

## <a name="what-can-i-do-with-audit-log-apis-in-microsoft-graph"></a><span data-ttu-id="5cefd-126">¿Qué puedo hacer con el registro de auditoría de las API en Microsoft Graph?</span><span class="sxs-lookup"><span data-stu-id="5cefd-126">What can I do with audit log APIs in Microsoft Graph?</span></span>

<span data-ttu-id="5cefd-127">Aquí están las solicitudes más populares para trabajar con datos de registro de auditoría:</span><span class="sxs-lookup"><span data-stu-id="5cefd-127">Here are popular requests for working with audit log data:</span></span>

<span data-ttu-id="5cefd-128">Operación</span><span class="sxs-lookup"><span data-stu-id="5cefd-128">Operation</span></span> | <span data-ttu-id="5cefd-129">URL</span><span class="sxs-lookup"><span data-stu-id="5cefd-129">URL</span></span>
:----------|:----
<span data-ttu-id="5cefd-130">OBTENER A inquilino las actividades del usuario</span><span class="sxs-lookup"><span data-stu-id="5cefd-130">GET tenant user activities</span></span> | [https://graph.microsoft.com/beta/auditLogs/directoryAudits](https://developer.microsoft.com/graph/graph-explorer?request=auditLogs/directoryAudits&version=beta)
<span data-ttu-id="5cefd-131">OBTENER A inquilino inicios de sesión de usuario</span><span class="sxs-lookup"><span data-stu-id="5cefd-131">GET tenant user sign-ins</span></span> | [https://graph.microsoft.com/beta/auditLogs/signIns](https://developer.microsoft.com/graph/graph-explorer?request=auditLogs/signIns&version=beta)

## <a name="what-licenses-do-i-need"></a><span data-ttu-id="5cefd-132">¿Qué licencias es necesario?</span><span class="sxs-lookup"><span data-stu-id="5cefd-132">What licenses do I need?</span></span>

<span data-ttu-id="5cefd-133">Informes de registro de auditoría están disponibles para las características que ha obtenido una licencia.</span><span class="sxs-lookup"><span data-stu-id="5cefd-133">Audit log reports are available for features that you've licensed.</span></span>  <span data-ttu-id="5cefd-134">Si tiene una licencia para una característica específica, también tiene acceso a sus registros de auditoría.</span><span class="sxs-lookup"><span data-stu-id="5cefd-134">If you have a license for a specific feature, you also have access to its audit logs.</span></span>

<span data-ttu-id="5cefd-135">Por ejemplo, necesita una licencia de Azure AD Premium P1 para acceder a los informes de auditoría de contraseña self-service.</span><span class="sxs-lookup"><span data-stu-id="5cefd-135">For example, you need an Azure AD Premium P1 license to access self-service password audit reports.</span></span>  <span data-ttu-id="5cefd-136">Para obtener más información, vea [licencias de Azure AD](https://azure.microsoft.com/pricing/details/active-directory/).</span><span class="sxs-lookup"><span data-stu-id="5cefd-136">To learn more, see [Azure AD licensing](https://azure.microsoft.com/pricing/details/active-directory/).</span></span>

<span data-ttu-id="5cefd-137">Inicio de sesión de los informes requieren una licencia de Azure AD Premium.</span><span class="sxs-lookup"><span data-stu-id="5cefd-137">Sign-in reports require an Azure AD Premium license.</span></span>

<span data-ttu-id="5cefd-138">Para obtener más información, vea [precios de Azure AD](https://azure.microsoft.com/pricing/details/active-directory/).</span><span class="sxs-lookup"><span data-stu-id="5cefd-138">To learn more, see [Azure AD pricing](https://azure.microsoft.com/pricing/details/active-directory/).</span></span>

## <a name="next-steps"></a><span data-ttu-id="5cefd-139">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="5cefd-139">Next Steps</span></span>

- <span data-ttu-id="5cefd-140">[Registrar la aplicación](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) para satisfacer los requisitos previos del registro de auditoría.</span><span class="sxs-lookup"><span data-stu-id="5cefd-140">[Register your app](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) to satisfy audit log prerequisites.</span></span> 
- <span data-ttu-id="5cefd-141">Obtenga información de [registro de auditoría](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-audit-samples) y [ejemplos de inicio de sesión](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-sign-in-activity-samples).</span><span class="sxs-lookup"><span data-stu-id="5cefd-141">Learn from [audit log](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-audit-samples) and [sign-in samples](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-sign-in-activity-samples).</span></span>  
- <span data-ttu-id="5cefd-142">Revisar [directoryAudit](directoryaudit.md) recurso y acciones.</span><span class="sxs-lookup"><span data-stu-id="5cefd-142">Review [directoryAudit](directoryaudit.md) resource and actions.</span></span>
- <span data-ttu-id="5cefd-143">Revise los recursos de [Inicio de sesión](signin.md) y acciones.</span><span class="sxs-lookup"><span data-stu-id="5cefd-143">Review [signIn](signin.md) resource and actions.</span></span> 