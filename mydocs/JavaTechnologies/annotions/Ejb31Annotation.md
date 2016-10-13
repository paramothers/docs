

EJB 3.1
=======

|                                          |                             |                           |      |       |                  |                          |               |
| ---------------------------------------- | --------------------------- | ------------------------- | ---- | ----- | ---------------- | ------------------------ | ------------- |
|                                          | @Stateless                  |                           |      | name  | mappedBy         |                          |               |
|                                          | @Stateful                   |                           |      | name  |                  |                          |               |
|                                          | @Remove                     |                           |      |       |                  |                          |               |
|                                          | @PrePassivate               |                           |      |       |                  |                          |               |
|                                          | @PostActivate               |                           |      |       |                  |                          |               |
|                                          | @Singleton                  |                           |      |       |                  |                          |               |
|                                          | @Startup                    |                           |      |       |                  |                          |               |
|                                          | @ConcurrencyManagement      |                           |      |       |                  |                          |               |
|                                          | @Lock                       |                           |      |       |                  |                          |               |
|                                          | @AccessTimeout              |                           |      | value | unit             |                          |               |
|                                          | @MessageDriven              |                           |      | name  | activationConfig | messageListenerInterface |               |
|                                          |                             | @ActivationConfigProperty |      |       | propertyName     | propertyValue            |               |
|                                          | @Asynchronous               |                           |      |       |                  |                          |               |
|                                          | @Local                      |                           |      |       |                  |                          |               |
|                                          | @Remote                     |                           |      |       |                  |                          |               |
|                                          | @WebService                 |                           |      |       |                  |                          |               |
|                                          | *@LocalBean*                |                           |      |       |                  |                          |               |
|                                          | *@LocalHome*                |                           |      |       |                  |                          |               |
|                                          | *@RemoteHome*               |                           |      |       |                  |                          |               |
| one of the usage of this annotation is, to plug Spring context in a EJB bean | @Interceptors               |                           |      |       |                  |                          |               |
|                                          | @AroundInvoke               |                           |      |       |                  |                          |               |
|                                          | @ExcludeDefaultInterceptors |                           |      |       |                  |                          |               |
|                                          | @ExcludeClassInterceptors   |                           |      |       |                  |                          |               |
|                                          | @Timeout                    |                           |      |       |                  |                          |               |
|                                          | @TransactionManagement      |                           |      |       |                  |                          |               |
|                                          | @TransactionAttribute       |                           |      |       |                  |                          |               |
|                                          | @ApplicationException       |                           |      |       | rollback         |                          |               |
|                                          | @EJB                        |                           |      | name  | beanName         | mappedName               | beanInterface |
|                                          | @Resource                   |                           |      | name  | type             | mappedName               |               |
|                                          |                             |                           |      |       |                  |                          |               |
|                                          |                             | **GENERAL ANNOTATION**    |      |       |                  |                          |               |
|                                          | @DeclareRoles               |                           |      |       |                  |                          |               |
|                                          | @RolesAllowed               |                           |      |       |                  |                          |               |
|                                          | @PermitAll                  |                           |      |       |                  |                          |               |
|                                          | @DenyAll                    |                           |      |       |                  |                          |               |
|                                          | @RunAs                      |                           |      |       |                  |                          |               |