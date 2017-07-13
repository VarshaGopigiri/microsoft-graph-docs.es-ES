<span data-ttu-id="70be1-p119">Enviar un código de estado `202 - Accepted` en la respuesta a Microsoft Graph. Si Microsoft Graph no recibe un código de clase 2xx, intentará volver a enviar la notificación varias veces.</span><span class="sxs-lookup"><span data-stu-id="70be1-p119">Send a `202 - Accepted` status code in your response to Microsoft Graph. If Microsoft Graph doesn't receive a 2xx class code, it will retry resending the notification a number of times.</span></span>
3. Enviar un código de estado `202 - Accepted` en la respuesta a Microsoft Graph. Si Microsoft Graph no recibe un código de clase 2xx, intentará volver a enviar la notificación varias veces.
  > <span data-ttu-id="70be1-198">Debe enviar un código de estado `202 - Accepted`, incluso si la propiedad clientState no coincide con la enviada con la solicitud de suscripción.</span><span class="sxs-lookup"><span data-stu-id="70be1-198">You should send a `202 - Accepted` status code even if the clientState property doesn't match the one submitted with the subscription request.</span></span>

<span data-ttu-id="70be1-199">Repetir en otras notificaciones de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70be1-199">Repeat for other notifications in the request.</span></span>

# <span data-ttu-id="70be1-200">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="70be1-200">Additional resources</span></span>
<a id="additional-resources" class="xliff"></a>

* [<span data-ttu-id="70be1-201">Tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="70be1-201">Subscription resource type</span></span>](subscription.md)
* [<span data-ttu-id="70be1-202">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="70be1-202">Get subscription</span></span>](../api/subscription_get.md)
* [<span data-ttu-id="70be1-203">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="70be1-203">Create subscription</span></span>](../api/subscription_post_subscriptions.md)
* [<span data-ttu-id="70be1-204">Ejemplo de webhooks de Microsoft Graph para Node.js</span><span class="sxs-lookup"><span data-stu-id="70be1-204">Microsoft Graph Webhooks Sample for Node.js</span></span>](https://github.com/OfficeDev/Microsoft-Graph-Nodejs-Webhooks)
* [<span data-ttu-id="70be1-205">Ejemplo de webhooks de Microsoft Graph para ASP.NET</span><span class="sxs-lookup"><span data-stu-id="70be1-205">Microsoft Graph Webhooks Sample for ASP.NET</span></span>](https://github.com/OfficeDev/Microsoft-Graph-ASPNET-Webhooks)
