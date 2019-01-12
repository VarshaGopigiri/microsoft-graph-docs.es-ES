---
title: Preguntas frecuentes de inicio rápido de Microsoft Graph
description: En este documento de preguntas frecuentes encontrará respuestas a cuestiones relacionadas con los inicios rápidos de Microsoft Graph.
author: jasonjoh
ms.author: jasonjoh
ms.date: 12/13/2018
localization_priority: Normal
ms.openlocfilehash: 457b82813420b8771a5e59e9723f11885388c7b4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834948"
---
# <a name="microsoft-graph-quick-start-faq"></a><span data-ttu-id="aab91-103">Preguntas frecuentes de inicio rápido de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="aab91-103">Microsoft Graph quick start FAQ</span></span>

<span data-ttu-id="aab91-104">En este documento de preguntas frecuentes encontrará respuestas a cuestiones relacionadas con los [inicios rápidos de Microsoft Graph](https://developer.microsoft.com/graph/quick-start).</span><span class="sxs-lookup"><span data-stu-id="aab91-104">This FAQ answers questions related to the [Microsoft Graph Quick Starts](https://developer.microsoft.com/graph/quick-start).</span></span>

## <a name="general-design"></a><span data-ttu-id="aab91-105">Diseño general</span><span class="sxs-lookup"><span data-stu-id="aab91-105">General design</span></span>

<span data-ttu-id="aab91-106">Los ejemplos de inicio rápido muestran cómo tener acceso a la potencia de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="aab91-106">The quick start samples show you how to access the power of Microsoft Graph.</span></span> <span data-ttu-id="aab91-107">Estos ejemplos acceden a dos servicios con una autenticación: cuenta de Microsoft y Outlook.</span><span class="sxs-lookup"><span data-stu-id="aab91-107">These samples access two services with one authentication: Microsoft account and Outlook.</span></span> <span data-ttu-id="aab91-108">Cada inicio rápido obtiene información de los perfiles de los usuarios de cuentas de Microsoft y muestra los eventos de su calendario.</span><span class="sxs-lookup"><span data-stu-id="aab91-108">Each quick start accesses information from Microsoft account users' profiles and displays events from their calendar.</span></span>

<span data-ttu-id="aab91-109">Los inicios rápidos incluyen cuatro pasos:</span><span class="sxs-lookup"><span data-stu-id="aab91-109">The quick starts involve four steps:</span></span>

- <span data-ttu-id="aab91-110">Seleccione la plataforma.</span><span class="sxs-lookup"><span data-stu-id="aab91-110">Select your platform</span></span>
- <span data-ttu-id="aab91-111">Obtenga el identificador de la aplicación (identificador del cliente)</span><span class="sxs-lookup"><span data-stu-id="aab91-111">Get your app ID (client ID)</span></span>
- <span data-ttu-id="aab91-112">Compile el ejemplo</span><span class="sxs-lookup"><span data-stu-id="aab91-112">Build the sample</span></span>
- <span data-ttu-id="aab91-113">Inicie sesión y vea los eventos del calendario</span><span class="sxs-lookup"><span data-stu-id="aab91-113">Sign in, and view events on your calendar</span></span>

<span data-ttu-id="aab91-114">Cuando complete el inicio rápido, tendrá una aplicación lista para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="aab91-114">When you complete the quick start, you have an app that's ready to run.</span></span>

## <a name="general-quick-start-sample-questions"></a><span data-ttu-id="aab91-115">Preguntas de ejemplo generales de inicio rápido</span><span class="sxs-lookup"><span data-stu-id="aab91-115">General quick start sample questions</span></span>

<!-- markdownlint-disable MD026 -->

<span data-ttu-id="aab91-116">En esta sección se responde a las preguntas sobre el contenido de los ejemplos de inicio rápido.</span><span class="sxs-lookup"><span data-stu-id="aab91-116">This section answers questions about the contents of the quick start samples.</span></span>

### <a name="can-i-get-the-quick-start-code-without-downloading-through-the-quick-start-page"></a><span data-ttu-id="aab91-117">¿Puedo obtener el código de inicio rápido sin descargar en la página de inicio rápido?</span><span class="sxs-lookup"><span data-stu-id="aab91-117">Can I get the quick start code without downloading through the quick start page?</span></span>

<span data-ttu-id="aab91-118">Por supuesto.</span><span class="sxs-lookup"><span data-stu-id="aab91-118">Absolutely!</span></span> <span data-ttu-id="aab91-119">Cada descarga de inicio rápido se basa en un [tutorial de Microsoft Graph](tutorials.md), por lo que tiene otras dos opciones para obtener el mismo código fuente:</span><span class="sxs-lookup"><span data-stu-id="aab91-119">Each quick start download is based on a [Microsoft Graph tutorial](tutorials.md), so you have two other options to get the same source code:</span></span>

- <span data-ttu-id="aab91-120">Crear el código siguiendo el tutorial paso a paso.</span><span class="sxs-lookup"><span data-stu-id="aab91-120">Build the code yourself by following the step-by-step tutorial.</span></span>
- <span data-ttu-id="aab91-121">Descargar el proyecto completado del repositorio de GitHub correspondiente y seguir las instrucciones en el archivo LÉAME para configurar y ejecutar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="aab91-121">Download the completed project from the corresponding GitHub repository and follow the instructions in the README to configure and run the sample.</span></span>

> <span data-ttu-id="aab91-122">**Nota:** Estamos en proceso de crear tutoriales para cada una de las plataformas que disponen de un inicio rápido.</span><span class="sxs-lookup"><span data-stu-id="aab91-122">**Note:** We are in the process of generating tutorials for each of the platforms that currently have a quick start.</span></span> <span data-ttu-id="aab91-123">Algunas de las guías de inicios rápidos no tienen todavía tutoriales correspondientes.</span><span class="sxs-lookup"><span data-stu-id="aab91-123">Some of the quick starts do not have corresponding tutorials yet.</span></span>

#### <a name="tutorials-and-github-repositories"></a><span data-ttu-id="aab91-124">Tutoriales y repositorios de GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-124">Tutorials and GitHub repositories</span></span>

<span data-ttu-id="aab91-125">La tabla siguiente incluye el tutorial correspondiente y el repositorio de GitHub de cada ejemplo de inicio rápido.</span><span class="sxs-lookup"><span data-stu-id="aab91-125">The following table lists the corresponding tutorial and GitHub repository for each quick start sample.</span></span>

| <span data-ttu-id="aab91-126">Inicio rápido</span><span class="sxs-lookup"><span data-stu-id="aab91-126">Quick start</span></span> | <span data-ttu-id="aab91-127">Tutorial</span><span class="sxs-lookup"><span data-stu-id="aab91-127">Tutorial</span></span> | <span data-ttu-id="aab91-128">Repositorio de GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-128">GitHub repository</span></span> |
|-------------|----------|-------------------|
| <span data-ttu-id="aab91-129">Android</span><span class="sxs-lookup"><span data-stu-id="aab91-129">Android</span></span> | <span data-ttu-id="aab91-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="aab91-130">None</span></span> | [<span data-ttu-id="aab91-131">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-131">GitHub</span></span>](https://github.com/microsoftgraph/android-java-connect-sample) |
| <span data-ttu-id="aab91-132">Angular</span><span class="sxs-lookup"><span data-stu-id="aab91-132">Angular</span></span> | [<span data-ttu-id="aab91-133">Tutorial</span><span class="sxs-lookup"><span data-stu-id="aab91-133">Tutorial</span></span>](/graph/tutorials/angular) | [<span data-ttu-id="aab91-134">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-134">GitHub</span></span>](https://github.com/microsoftgraph/msgraph-training-angularspa) |
| <span data-ttu-id="aab91-135">ASP.NET MVC</span><span class="sxs-lookup"><span data-stu-id="aab91-135">ASP.NET MVC</span></span> | [<span data-ttu-id="aab91-136">Tutorial</span><span class="sxs-lookup"><span data-stu-id="aab91-136">Tutorial</span></span>](/graph/tutorials/aspnet) | [<span data-ttu-id="aab91-137">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-137">GitHub</span></span>](https://github.com/microsoftgraph/msgraph-training-aspnetmvcapp) |
| <span data-ttu-id="aab91-138">iOS Swift</span><span class="sxs-lookup"><span data-stu-id="aab91-138">iOS Swift</span></span> | <span data-ttu-id="aab91-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="aab91-139">None</span></span> | [<span data-ttu-id="aab91-140">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-140">GitHub</span></span>](https://github.com/microsoftgraph/ios-swift-connect-sample) |
| <span data-ttu-id="aab91-141">iOS Objective-C</span><span class="sxs-lookup"><span data-stu-id="aab91-141">iOS Objective-C</span></span> | <span data-ttu-id="aab91-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="aab91-142">None</span></span> | [<span data-ttu-id="aab91-143">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-143">GitHub</span></span>](https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample) |
| <span data-ttu-id="aab91-144">Node.js</span><span class="sxs-lookup"><span data-stu-id="aab91-144">Node.js</span></span> | [<span data-ttu-id="aab91-145">Tutorial</span><span class="sxs-lookup"><span data-stu-id="aab91-145">Tutorial</span></span>](/graph/tutorials/node) | [<span data-ttu-id="aab91-146">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-146">GitHub</span></span>](https://github.com/microsoftgraph/msgraph-training-nodeexpressapp) |
| <span data-ttu-id="aab91-147">PHP</span><span class="sxs-lookup"><span data-stu-id="aab91-147">PHP</span></span> | [<span data-ttu-id="aab91-148">Tutorial</span><span class="sxs-lookup"><span data-stu-id="aab91-148">Tutorial</span></span>](/graph/tutorials/php) | [<span data-ttu-id="aab91-149">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-149">GitHub</span></span>](https://github.com/microsoftgraph/msgraph-training-phpapp) |
| <span data-ttu-id="aab91-150">Python</span><span class="sxs-lookup"><span data-stu-id="aab91-150">Python</span></span> | [<span data-ttu-id="aab91-151">Tutorial</span><span class="sxs-lookup"><span data-stu-id="aab91-151">Tutorial</span></span>](/graph/tutorials/python) | [<span data-ttu-id="aab91-152">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-152">GitHub</span></span>](https://github.com/microsoftgraph/msgraph-training-pythondjangoapp) |
| <span data-ttu-id="aab91-153">Ruby</span><span class="sxs-lookup"><span data-stu-id="aab91-153">Ruby</span></span> | [<span data-ttu-id="aab91-154">Tutorial</span><span class="sxs-lookup"><span data-stu-id="aab91-154">Tutorial</span></span>](/graph/tutorials/ruby) | [<span data-ttu-id="aab91-155">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-155">GitHub</span></span>](https://github.com/microsoftgraph/msgraph-training-rubyrailsapp) |
| <span data-ttu-id="aab91-156">UWP</span><span class="sxs-lookup"><span data-stu-id="aab91-156">UWP</span></span> | [<span data-ttu-id="aab91-157">Tutorial</span><span class="sxs-lookup"><span data-stu-id="aab91-157">Tutorial</span></span>](/graph/tutorials/uwp) | [<span data-ttu-id="aab91-158">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-158">GitHub</span></span>](https://github.com/microsoftgraph/msgraph-training-uwp) |
| <span data-ttu-id="aab91-159">Xamarin</span><span class="sxs-lookup"><span data-stu-id="aab91-159">Xamarin</span></span> | <span data-ttu-id="aab91-160">Ninguno</span><span class="sxs-lookup"><span data-stu-id="aab91-160">None</span></span> | [<span data-ttu-id="aab91-161">GitHub</span><span class="sxs-lookup"><span data-stu-id="aab91-161">GitHub</span></span>](https://github.com/microsoftgraph/xamarin-csharp-connect-sample) |

### <a name="why-dont-any-of-the-quick-start-samples-show-advanced-authentication-use-cases"></a><span data-ttu-id="aab91-162">¿Por qué ningún ejemplo de inicio rápido muestra casos de uso de autenticación avanzada?</span><span class="sxs-lookup"><span data-stu-id="aab91-162">Why don't any of the quick start samples show advanced authentication use cases?</span></span>

<span data-ttu-id="aab91-163">Los ejemplos de inicio rápido le ofrecen una introducción a la autenticación y a las llamadas a la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="aab91-163">The quick start samples give you an introduction to authentication and Microsoft Graph API calls.</span></span> <span data-ttu-id="aab91-164">Puede obtener más información sobre los otros flujos de autenticación en la documentación de [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/authentication-scenarios).</span><span class="sxs-lookup"><span data-stu-id="aab91-164">You can learn more about other authentication flows in the [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/authentication-scenarios) documentation.</span></span>

### <a name="what-if-i-run-into-an-unexpected-error-or-problem-with-a-quick-start"></a><span data-ttu-id="aab91-165">¿Qué ocurre si encuentro algún error inesperado o un problema con un inicio rápido?</span><span class="sxs-lookup"><span data-stu-id="aab91-165">What if I run into an unexpected error or problem with a quick start?</span></span>

<span data-ttu-id="aab91-166">Si tiene problemas para configurar el inicio rápido para que funcione correctamente, abra un problema en el repositorio de GitHub correspondiente.</span><span class="sxs-lookup"><span data-stu-id="aab91-166">If you have trouble getting the quick start to work properly, please open an issue on the corresponding GitHub repository.</span></span>

## <a name="didnt-find-what-you-need"></a><span data-ttu-id="aab91-167">¿No encuentra lo que necesita?</span><span class="sxs-lookup"><span data-stu-id="aab91-167">Didn't find what you need?</span></span>

<span data-ttu-id="aab91-168">Si estas preguntas frecuentes no resuelven su pregunta o problema relacionado con uno o varios inicios rápidos, infórmenos mediante la sección **Informes** a continuación.</span><span class="sxs-lookup"><span data-stu-id="aab91-168">If this FAQ didn't address a question or problem you encountered with one or more of the quick starts, please let us know using the **Feedback** section below.</span></span>
