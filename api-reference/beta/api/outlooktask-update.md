---
title: Actualizar outlooktask
description: Cambiar las propiedades modificables de una tarea de Outlook.
ms.openlocfilehash: 1e2afb7fb69b4f305ffc69d0f40960edf9b6ca2c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083461"
---
# <a name="update-outlooktask"></a><span data-ttu-id="b6922-103">Actualizar outlooktask</span><span class="sxs-lookup"><span data-stu-id="b6922-103">Update outlooktask</span></span>

> <span data-ttu-id="b6922-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6922-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6922-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6922-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b6922-106">Cambiar las propiedades modificables de una tarea de Outlook.</span><span class="sxs-lookup"><span data-stu-id="b6922-106">Change writable properties of an Outlook task.</span></span>

<span data-ttu-id="b6922-107">La propiedad **completedDateTime** se puede establecer mediante la acción **completa** , o explícitamente mediante una operación de revisión.</span><span class="sxs-lookup"><span data-stu-id="b6922-107">The **completedDateTime** property can be set by the **complete** action, or explicitly by a PATCH operation.</span></span> <span data-ttu-id="b6922-108">Si usa revisión para establecer **completedDateTime**, asegúrese de establecer el **estado** en `completed` así como.</span><span class="sxs-lookup"><span data-stu-id="b6922-108">If you use PATCH to set **completedDateTime**, make sure you set **status** to `completed` as well.</span></span>

<span data-ttu-id="b6922-109">De forma predeterminada, esta operación (y las operaciones de tarea POST, GET y [completar](../api/outlooktask-complete.md) ) devuelve propiedades relacionadas con la fecha en UTC.</span><span class="sxs-lookup"><span data-stu-id="b6922-109">By default, this operation (and the POST, GET, and [complete](../api/outlooktask-complete.md) task operations) returns date-related properties in UTC.</span></span> <span data-ttu-id="b6922-110">Puede usar el `Prefer: outlook.timezone` encabezado para que todas las propiedades relacionadas con la fecha en la respuesta representada en una zona horaria diferente a la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="b6922-110">You can use the `Prefer: outlook.timezone` header to have all the date-related properties in the response represented in a time zone different than UTC.</span></span>

## <a name="permissions"></a><span data-ttu-id="b6922-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="b6922-111">Permissions</span></span>
<span data-ttu-id="b6922-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6922-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6922-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6922-114">Permission type</span></span>      | <span data-ttu-id="b6922-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6922-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b6922-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6922-116">Delegated (work or school account)</span></span> | <span data-ttu-id="b6922-117">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b6922-117">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="b6922-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6922-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b6922-119">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b6922-119">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="b6922-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6922-120">Application</span></span> | <span data-ttu-id="b6922-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6922-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b6922-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6922-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id|userPrincipalName}/outlook/tasks/{id}
PATCH /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks/{id}
PATCH /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="b6922-123">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="b6922-123">Optional request headers</span></span>
| <span data-ttu-id="b6922-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="b6922-124">Name</span></span>       | <span data-ttu-id="b6922-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6922-125">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="b6922-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6922-126">Authorization</span></span>  | <span data-ttu-id="b6922-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6922-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b6922-129">Prefer: outlook.timezone</span><span class="sxs-lookup"><span data-stu-id="b6922-129">Prefer: outlook.timezone</span></span> | <span data-ttu-id="b6922-130">Especifica la zona horaria de propiedades de tiempo en la respuesta, que sería en UTC si no se especifica este encabezado.</span><span class="sxs-lookup"><span data-stu-id="b6922-130">Specifies the time zone for time properties in the response, which would be in UTC if this header is not specified.</span></span> <span data-ttu-id="b6922-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b6922-131">Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b6922-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6922-132">Request body</span></span>
<span data-ttu-id="b6922-p107">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b6922-p107">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b6922-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6922-136">Property</span></span>     | <span data-ttu-id="b6922-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6922-137">Type</span></span>   |<span data-ttu-id="b6922-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6922-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b6922-139">assignedTo</span><span class="sxs-lookup"><span data-stu-id="b6922-139">assignedTo</span></span>|<span data-ttu-id="b6922-140">String</span><span class="sxs-lookup"><span data-stu-id="b6922-140">String</span></span>|<span data-ttu-id="b6922-141">El nombre de la persona que se le ha asignado la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-141">The name of the person who has been assigned the task.</span></span>|
|<span data-ttu-id="b6922-142">body</span><span class="sxs-lookup"><span data-stu-id="b6922-142">body</span></span>|[<span data-ttu-id="b6922-143">itemBody</span><span class="sxs-lookup"><span data-stu-id="b6922-143">itemBody</span></span>](../resources/itembody.md)|<span data-ttu-id="b6922-144">El cuerpo de la tarea que normalmente contiene información acerca de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-144">The task body that typically contains information about the task.</span></span> <span data-ttu-id="b6922-145">Tenga en cuenta que sólo el tipo HTML es compatible.</span><span class="sxs-lookup"><span data-stu-id="b6922-145">Note that only HTML type is supported.</span></span>|
|<span data-ttu-id="b6922-146">categories</span><span class="sxs-lookup"><span data-stu-id="b6922-146">categories</span></span>|<span data-ttu-id="b6922-147">Colección String</span><span class="sxs-lookup"><span data-stu-id="b6922-147">String collection</span></span>|<span data-ttu-id="b6922-148">Las categorías asociadas con la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-148">The categories associated with the task.</span></span>|
|<span data-ttu-id="b6922-149">changeKey</span><span class="sxs-lookup"><span data-stu-id="b6922-149">changeKey</span></span>|<span data-ttu-id="b6922-150">String</span><span class="sxs-lookup"><span data-stu-id="b6922-150">String</span></span>|<span data-ttu-id="b6922-151">La versión de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-151">The version of the task.</span></span>|
|<span data-ttu-id="b6922-152">completedDateTime</span><span class="sxs-lookup"><span data-stu-id="b6922-152">completedDateTime</span></span>|[<span data-ttu-id="b6922-153">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="b6922-153">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="b6922-154">La fecha en la zona horaria especificada que se ha finalizado la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-154">The date in the specified time zone that the task was finished.</span></span>|
|<span data-ttu-id="b6922-155">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b6922-155">createdDateTime</span></span>|<span data-ttu-id="b6922-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b6922-156">DateTimeOffset</span></span>|<span data-ttu-id="b6922-157">La fecha y la hora cuando se creó la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-157">The date and time when the task was created.</span></span> <span data-ttu-id="b6922-158">De forma predeterminada, está en UTC.</span><span class="sxs-lookup"><span data-stu-id="b6922-158">By default, it is in UTC.</span></span> <span data-ttu-id="b6922-159">Puede proporcionar una zona horaria personalizada en el encabezado de solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6922-159">You can provide a custom time zone in the request header.</span></span> <span data-ttu-id="b6922-160">El valor de la propiedad usa formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="b6922-160">The property value uses ISO 8601 format.</span></span> <span data-ttu-id="b6922-161">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="b6922-161">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="b6922-162">dueDateTime</span><span class="sxs-lookup"><span data-stu-id="b6922-162">dueDateTime</span></span>|[<span data-ttu-id="b6922-163">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="b6922-163">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="b6922-164">La fecha en la zona horaria especificada que se va finalizado la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-164">The date in the specified time zone that the task is to be finished.</span></span>|
|<span data-ttu-id="b6922-165">hasAttachments</span><span class="sxs-lookup"><span data-stu-id="b6922-165">hasAttachments</span></span>|<span data-ttu-id="b6922-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="b6922-166">Boolean</span></span>|<span data-ttu-id="b6922-167">Se establece en true si la tarea tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b6922-167">Set to true if the task has attachments.</span></span>|
|<span data-ttu-id="b6922-168">importance</span><span class="sxs-lookup"><span data-stu-id="b6922-168">importance</span></span>|<span data-ttu-id="b6922-169">string</span><span class="sxs-lookup"><span data-stu-id="b6922-169">string</span></span>|<span data-ttu-id="b6922-170">Importancia del evento.</span><span class="sxs-lookup"><span data-stu-id="b6922-170">The importance of the event.</span></span> <span data-ttu-id="b6922-171">Los valores posibles son: `low`, `normal` y `high`.</span><span class="sxs-lookup"><span data-stu-id="b6922-171">Possible values are: `low`, `normal`, `high`.</span></span>|
|<span data-ttu-id="b6922-172">isReminderOn</span><span class="sxs-lookup"><span data-stu-id="b6922-172">isReminderOn</span></span>|<span data-ttu-id="b6922-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="b6922-173">Boolean</span></span>|<span data-ttu-id="b6922-174">Se establece en true si se establece una alerta para recordarle al usuario de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-174">Set to true if an alert is set to remind the user of the task.</span></span>|
|<span data-ttu-id="b6922-175">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b6922-175">lastModifiedDateTime</span></span>|<span data-ttu-id="b6922-176">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b6922-176">DateTimeOffset</span></span>|<span data-ttu-id="b6922-177">La fecha y hora de última modificación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-177">The date and time when the task was last modified.</span></span> <span data-ttu-id="b6922-178">De forma predeterminada, está en UTC.</span><span class="sxs-lookup"><span data-stu-id="b6922-178">By default, it is in UTC.</span></span> <span data-ttu-id="b6922-179">Puede proporcionar una zona horaria personalizada en el encabezado de solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6922-179">You can provide a custom time zone in the request header.</span></span> <span data-ttu-id="b6922-180">El valor de la propiedad utiliza el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="b6922-180">The property value uses ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="b6922-181">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="b6922-181">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="b6922-182">owner</span><span class="sxs-lookup"><span data-stu-id="b6922-182">owner</span></span>|<span data-ttu-id="b6922-183">String</span><span class="sxs-lookup"><span data-stu-id="b6922-183">String</span></span>|<span data-ttu-id="b6922-184">El nombre de la persona que creó la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-184">The name of the person who created the task.</span></span>|
|<span data-ttu-id="b6922-185">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="b6922-185">parentFolderId</span></span>|<span data-ttu-id="b6922-186">String</span><span class="sxs-lookup"><span data-stu-id="b6922-186">String</span></span>|<span data-ttu-id="b6922-187">El identificador único para la carpeta principal de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-187">The unique identifier for the task's parent folder.</span></span>|
|<span data-ttu-id="b6922-188">periodicidad</span><span class="sxs-lookup"><span data-stu-id="b6922-188">recurrence</span></span>|[<span data-ttu-id="b6922-189">patternedRecurrence</span><span class="sxs-lookup"><span data-stu-id="b6922-189">patternedRecurrence</span></span>](../resources/patternedrecurrence.md)|<span data-ttu-id="b6922-190">El patrón de periodicidad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-190">The recurrence pattern for the task.</span></span>|
|<span data-ttu-id="b6922-191">reminderDateTime</span><span class="sxs-lookup"><span data-stu-id="b6922-191">reminderDateTime</span></span>|[<span data-ttu-id="b6922-192">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="b6922-192">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="b6922-193">La fecha y hora para un aviso de la tarea que se produzca.</span><span class="sxs-lookup"><span data-stu-id="b6922-193">The date and time for a reminder alert of the task to occur.</span></span>|
|<span data-ttu-id="b6922-194">sensitivity</span><span class="sxs-lookup"><span data-stu-id="b6922-194">sensitivity</span></span>|<span data-ttu-id="b6922-195">string</span><span class="sxs-lookup"><span data-stu-id="b6922-195">string</span></span>|<span data-ttu-id="b6922-196">Indica el nivel de privacidad para la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-196">Indicates the level of privacy for the task.</span></span> <span data-ttu-id="b6922-197">Los valores posibles son: `normal`, `personal`, `private` y `confidential`.</span><span class="sxs-lookup"><span data-stu-id="b6922-197">Possible values are: `normal`, `personal`, `private`, `confidential`.</span></span>|
|<span data-ttu-id="b6922-198">startDateTime</span><span class="sxs-lookup"><span data-stu-id="b6922-198">startDateTime</span></span>|[<span data-ttu-id="b6922-199">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="b6922-199">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="b6922-200">La fecha en la zona horaria especificada cuando la tarea que se va a comenzar.</span><span class="sxs-lookup"><span data-stu-id="b6922-200">The date in the specified time zone when the task is to begin.</span></span>|
|<span data-ttu-id="b6922-201">status</span><span class="sxs-lookup"><span data-stu-id="b6922-201">status</span></span>|<span data-ttu-id="b6922-202">string</span><span class="sxs-lookup"><span data-stu-id="b6922-202">string</span></span>|<span data-ttu-id="b6922-203">Indica el estado o el progreso de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-203">Indicates the state or progress of the task.</span></span> <span data-ttu-id="b6922-204">Los valores posibles son: `notStarted`, `inProgress`, `completed`, `waitingOnOthers` y `deferred`.</span><span class="sxs-lookup"><span data-stu-id="b6922-204">Possible values are: `notStarted`, `inProgress`, `completed`, `waitingOnOthers`, `deferred`.</span></span>|
|<span data-ttu-id="b6922-205">subject</span><span class="sxs-lookup"><span data-stu-id="b6922-205">subject</span></span>|<span data-ttu-id="b6922-206">String</span><span class="sxs-lookup"><span data-stu-id="b6922-206">String</span></span>|<span data-ttu-id="b6922-207">Una breve descripción o el título de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b6922-207">A brief description or title of the task.</span></span>|

## <a name="response"></a><span data-ttu-id="b6922-208">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6922-208">Response</span></span>

<span data-ttu-id="b6922-209">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [outlookTask](../resources/outlooktask.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6922-209">If successful, this method returns a `200 OK` response code and updated [outlookTask](../resources/outlooktask.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b6922-210">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6922-210">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b6922-211">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6922-211">Request</span></span>
<span data-ttu-id="b6922-212">El siguiente ejemplo se modifica la propiedad **dueDateTime** y usa el `Prefer: outlook.timezone` encabezado para especificar expresar las propiedades relacionadas con la fecha en la respuesta en la hora estándar (EST).</span><span class="sxs-lookup"><span data-stu-id="b6922-212">The following example modifies the **dueDateTime** property and uses the `Prefer: outlook.timezone` header to specify expressing the date-related properties in the response in Eastern Standard Time (EST).</span></span>
<!-- {
  "blockType": "request",
  "name": "update_outlooktask"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/outlook/tasks('AAMkADA1MTHgwAAA=')

Prefer: outlook.timezone="Eastern Standard Time"
Content-type: application/json
Content-length: 76

{
  "dueDateTime":  {
      "dateTime": "2016-05-06T16:00:00",
      "timeZone": "Eastern Standard Time"
  }
}
```
##### <a name="response"></a><span data-ttu-id="b6922-213">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6922-213">Response</span></span>
<span data-ttu-id="b6922-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6922-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 376

{
    "id": "AAMkADA1MTHgwAAA=",
    "createdDateTime": "2016-04-22T18:19:18.9526004-04:00",
    "lastModifiedDateTime": "2016-04-22T18:38:20.5541528-04:00",
    "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIW9XXg==",
    "categories": [
    ],
    "assignedTo": null,
    "body": {
        "contentType": "text",
        "content": ""
    },
    "completedDateTime": null,
    "dueDateTime": {
        "dateTime": "2016-05-06T00:00:00.0000000",
        "timeZone": "Eastern Standard Time"
    },
    "hasAttachments":false,
    "importance": "normal",
    "isReminderOn": false,
    "owner": "Administrator",
    "parentFolderId": "AQMkADA1MTIBEgAAAA==",
    "recurrence": null,
    "reminderDateTime": null,
    "sensitivity": "normal",
    "startDateTime": {
        "dateTime": "2016-05-03T00:00:00.0000000",
        "timeZone": "Eastern Standard Time"
    },
    "status": "notStarted",
    "subject": "Shop for children's weekend"

}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update outlooktask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->