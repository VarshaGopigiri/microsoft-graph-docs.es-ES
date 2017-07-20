<span data-ttu-id="c4420-p119">Ahora que ha visto cómo realizar llamadas a Microsoft Graph, puede usar la referencia de la API para construir cualquier otro tipo de llamada que su aplicación necesite realizar. Sin embargo, tenga en cuenta que su aplicación debe tener los permisos adecuados configurados en el registro de aplicaciones para las llamadas que realice.</span><span class="sxs-lookup"><span data-stu-id="c4420-p119">Now that you've seen how to make calls to Microsoft Graph, you can use the API reference to construct any other kinds of calls your app needs to make. However, bear in mind that your app needs to have the appropriate permissions configured on the app registration for the calls it makes.</span></span>

```
GET https://graph.microsoft.com/v1.0/me/messages?$select=subject,from,receivedDateTime&$top=25&$orderby=receivedDateTime%20DESC
Accept: application/json
Authorization: Bearer eyJ0eXAi...b66LoPVA
```

Ahora que ha visto cómo realizar llamadas a Microsoft Graph, puede usar la referencia de la API para construir cualquier otro tipo de llamada que su aplicación necesite realizar. Sin embargo, tenga en cuenta que su aplicación debe tener los permisos adecuados configurados en el registro de aplicaciones para las llamadas que realice.

## <a name="next-steps"></a><span data-ttu-id="c4420-189">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="c4420-189">Next steps</span></span>
- <span data-ttu-id="c4420-190">Pruebe más características de la API de REST mediante el [Probador de Graph](https://graph.microsoft.io/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="c4420-190">Try out more of the REST API using the [Graph explorer](https://graph.microsoft.io/graph-explorer).</span></span>

## <a name="see-also"></a><span data-ttu-id="c4420-191">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c4420-191">See also</span></span>
- [<span data-ttu-id="c4420-192">Obtener tokens de acceso para llamar a Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c4420-192">Get access tokens to call Microsoft Graph</span></span>](https://developer.microsoft.com/en-us/graph/docs/concepts/auth_overview)
- [<span data-ttu-id="c4420-193">Obtener acceso en nombre de un usuario</span><span class="sxs-lookup"><span data-stu-id="c4420-193">Get access on behalf of a user</span></span>](https://developer.microsoft.com/en-us/graph/docs/concepts/auth_v2_user)
- [<span data-ttu-id="c4420-194">Obtener acceso sin un usuario</span><span class="sxs-lookup"><span data-stu-id="c4420-194">Get access without a user</span></span>](https://developer.microsoft.com/en-us/graph/docs/concepts/auth_v2_service)
