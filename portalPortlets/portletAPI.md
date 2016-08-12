## Portlet API

+ javax.portlet.Portlet
  + javax.portlet.GenericPortlet
    + PortletResponse
      + ActionResponse
      + EventResponse
      + **MimeResponse**, has caching configuration for portlet content
        + ResourceResponse
        + RenderResponse
    + PortletRequest
      + ClientDataRequest
        + ActionRequest
        + ResourceRequest

      + RenderRequest
      + EventRequest
+ EventPortlet
+ ResourceServingPortlet
+ PortletConfig
  + PortletContext
  + PortletSession, PortletSessionUtil
  + PortletRequestDispatcher
+ PortletMode
+ PortletURL and ResourceURL
+ PortletPreference
+ WindowState
+ CacheControl
+ ClientDataRequest
+ PortletURLGenerationListener



## Portlet - Java Annotation

@RenderMode, to annotate any method name,  any one of render mode.

@ProcessAction

## Portlet Spring MVC  annotation

1. @Controller

2. @RequestMapping

3. @ActionMapping

4. @RenderMapping

5. @ResourceMapping

6. @EventMapping

   ​

