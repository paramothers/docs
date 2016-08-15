# API - Web

# Servlet Container Initializer

-   **javax.servlet.ServletContainerInitializer**, this type given by Servlet 3.0, to initialize container
    -   **SpringServletContainerInitializer**, spring provide default implementation of `ServletContainerInitializer`
        -   **WebApplicationInitializer**, we can implements when we need to configure more application serverlts, filters, Listeners
            -   AbstractDispatcherServletInitializer
            -   **AbstractAnnotationConfigDispatcherServletInitializer**, one of the implementation of `WebApplicationInitializer` dispatch servlet config automatically by Javaconfig
                -   (App specific servlet container initialzier)
-   WebApplicationContext
    -   **AnnotationConfigWebApplicationContext**, load javaconfig for Spring MVC by web.xml
-   **MultipartResolver**, used to parse multipart request
    -   **CommonsMultipartResolver**, use Common File upload library
    -   **StandardServletMultipartResolver**, use container support of Servlet 3.0
-   MultipartFile
-   HandlerMapping
    -   SimpleUrlHandlerMapping

# Spring MVC tool-bean configure (Web initializer is first step . Web MVC configurer is second step )

-   WebMvcConfigurer
    -   **WebMvcConfigurerAdapter**, configure Spring MVC tools. it is used by WebApplicationInitializer
        -   (app MVC config class), annotated with **@EnableSpringMvc**

# Spring View implementation

-   View
    -   AbstractExcelView
    -   AbstractPdfView
    -   AbstractView
    -   JstlView
-   ViewResolver
    -   **InternalResourceViewResolver**, to resolve JSP files as view
    -   ContentNegotiatingViewResolver
    -   UrlBasedViewResolver
    -   **BeanNameViewResolver**, to resolve Bean ID
    -   XmlViewResolver
    -   XsltViewResolver
    -   ResourceBundleViewResolver
        -   FreeMarkerViewResolver
        -   JasperReportsViewResolver
        -   TilesViewResolver
        -   VelocityLayoutViewResolver
        -   VelocityViewResolver
-   Model , it is just like a map and to add attribute by controller method
-   **Errors**, any POJO validation error
-   ResourceBundleMessageSource
-   ReloadableResourceBundleMessageSource

# API - web flow

-   **FlowHandlerMapping**, it forward request from DispatcherServlet to Spring Web flow based on url
-   **FlowHandlerAdapter**, it is like mvc controller

# API - Rest

|                                       |      |                           |      |      |
| ------------------------------------- | ---- | ------------------------- | ---- | ---- |
|                                       |      | HttpMethodConverter       |      |      |
|                                       |      | RestTemplate              |      |      |
|                                       |      | ContentNegotiationManager |      |      |
| it carry metadata about http response |      | ResponseEntity            |      |      |
|                                       |      | HttpStatus                |      |      |
|                                       |      | HttpHeaders               |      |      |

# Spring Porlet MVC API

1. DispatchPortlet

2. ResouceServingPortlet

3. Controller

   1. PortletModeNameViewController
   2. ParameterizabeViewController
   3. PortletWrappingController
   4. ResourceAwareController
   5. EventAwareController

4. HandlerMapping
   1. AbstractHandlerMapping
      1. PortletModeHandlerMapping
      2. ParameterHandlerMapping
      3. PortletModeParameterHandlerMapping
      4. DefaultAnnotationHandelerMapping

5. DispatcherPortlet

6. ViewRenderServlet

7. HandlerInterceptor
   1. HandlerInterceptorAdaptor
      1. ParameterMappingInterceptor

8. HandlerExceptionResolver
   1. AbstracctHandlerExceptionResolver
      1. SimpleMappingExceptionResolver
   2. AnnotationMethodHandlerExceptionResolver

9. PortletMultipartResolver

   1. CommonPortletMultipartResolverS

10. WebDataBinder

   1. ConfigurableWebBindingInitializer

11. BindingResult

12. AnnotationMethodHandlerAdapter

13. ​

   ​