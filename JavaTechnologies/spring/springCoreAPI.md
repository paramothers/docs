# BeanFactory typed Containers

|                     |                            |                                |                |                        |                     |
| ------------------- | -------------------------- | ------------------------------ | -------------- | ---------------------- | ------------------- |
| BeanFactory         |                            |                                |                |                        |                     |
|                     | DefaultListableBeanFactory |                                |                |                        |                     |
|                     |                            | fgfgXMLBeanFactory             |                |                        |                     |
|                     | BeanDefinitionRegistry     |                                |                |                        |                     |
|                     |                            | XmlBeanDefinitionReader        |                |                        |                     |
|                     |                            | PropertiesBeanDefinitionReader |                |                        |                     |
|                     |                            |                                | BeanDefinition |                        |                     |
|                     |                            |                                |                | BeanDefinitionVisistor |                     |
|                     |                            |                                |                |                        | StringValueResolver |
|                     |                            |                                | Resource       |                        |                     |
|                     |                            |                                |                | FileSystemResource     |                     |
|                     |                            |                                |                | ByteArrayResource      |                     |
|                     |                            |                                |                | ClassPathResource      |                     |
|                     |                            |                                |                | DescriptiveResource    |                     |
|                     |                            |                                |                | InputStreamResource    |                     |
|                     |                            |                                |                | PortletContextResource |                     |
|                     |                            |                                |                | ServletContextResource |                     |
|                     |                            |                                |                | UrlResource            |                     |
|                     |                            |                                | ResourceLoader |                        |                     |
|                     |                            |                                |                | DefaultResourceLoader  |                     |
| MethodReplacer      |                            |                                |                |                        |                     |
| FactoryBean         |                            |                                |                |                        |                     |
|                     | JndiObjectFactoryBean      |                                |                |                        |                     |
| PropertyEditor      |                            |                                |                |                        |                     |
|                     | PropertyEditorSupport      |                                |                |                        |                     |
| ExpressionParser    |                            |                                |                |                        |                     |
|                     | Expression                 |                                |                |                        |                     |
| ParseException      |                            |                                |                |                        |                     |
| EvaluationException |                            |                                |                |                        |                     |
| FileUtil            |                            |                                |                |                        |                     |
| ExceptionUtil       |                            |                                |                |                        |                     |
| FileCopyUtil        |                            |                                |                |                        |                     |

# ApplicationContext typed Container

<table>
<colgroup>
<col width="15%" />
<col width="43%" />
<col width="15%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td>ApplicationContext</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>ConfigurableApplicationContext</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><del>ClassPathXmlApplicationContext</del></td>
<td></td>
<td>Load configuration from classpath</td>
</tr>
<tr class="even">
<td></td>
<td><del>FileSystemXmlApplicationContext</del></td>
<td></td>
<td>Load configuration from filesystem</td>
</tr>
<tr class="odd">
<td></td>
<td><del>XmlPortletApplicationContext</del></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><del>WebApplicationContext</del></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><del>XmlWebApplicationContext</del></td>
<td>Load configuration from war file</td>
</tr>
<tr class="even">
<td></td>
<td><span style="background-color: rgb(0, 255, 0);">AnnotationConfigApplicationContext</span></td>
<td></td>
<td>Load configuration from JavaConfig</td>
</tr>
<tr class="odd">
<td></td>
<td><span style="background-color: rgb(0, 255, 0);">AnnotationWebConfigApplicationContext</span></td>
<td></td>
<td>Load configuration from JavaConfig for web application</td>
</tr>
<tr class="even">
<td></td>
<td>ContextLoader</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td>ContextLoaderListener</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td>ContextLoaderServlet</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td>ApplicationContextAwareProcessor</td>
<td></td>
</tr>
<tr class="even">
<td>LoadTimeWeaverAware</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>MessageSourceAware</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>ApplicationEventPublisherAware</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>ResourceLoaderAware</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>LifeCycle</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>ApplicationEvent</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>ApplicationListener</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>ApplicationEventPublisher</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>ContextClosedEvent</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td>ContextRefreshedEvent</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>RequestHandledEvent</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>ApplicationEventMulticaster</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>BeanNameGenerator</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

# Bean life-cycle API

Bean life-cycle phases

1.  Instantiate

2.  populate properties

3.  BeanName<span style="color: rgb(255, 0, 0);">Aware</span>

4.  BeanFactory<span style="color: rgb(255, 0, 0);">Aware</span>

5.  ApplicationContext<span style="color: rgb(255, 0, 0);">Aware</span>

6.  Bean<span style="color: rgb(45, 229, 45);">PostProcessor</span>( Pre-Initialization )

7.  InitializingBean's afterPropertiesSet();

8.  call custom init-method

9.  Bean<span style="color: rgb(45, 229, 45);">PostProcessor</span>( Post

-   Initialization )

( Live Bean in Application context )

1.  DisposableBean

2.  custom-destory method

|                                   |                                          |
| --------------------------------- | ---------------------------------------- |
| InitializingBean                  | replace by @PostConstruct                |
| DisposableBean                    | replace by @PreDestory                   |
| BeanPostProcessors                |                                          |
|                                   | **CommonAnnotationBeanPostProcessor**    |
|                                   | **AutowiredAnnotationBeanPostProcessor** |
| DestructionAwareBeanPostProcessor |                                          |
|                                   | **InitDestroyAnnotationBeanPostProcessor** |
| BeanFactoryPostProcessor          |                                          |
|                                   | it has 8 BeanFactory post process comes with spring distribution |
| BeanNameAware                     |                                          |
| BeanFactoryAware                  |                                          |
| ApplicationContextAware           |                                          |
