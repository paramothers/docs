
1. one property file load using @PropertySource and access Environment object
2. use @Profile bounded bean for different deployment environment.
3. Entire SpringContext/WebContext should configure using JavaConfig.
4. Have separate marker interface in each layer and use that for scanning path specification
5. Have as many as configuration files in separate config package
6. use of AOP, for at least logger entry-exit statements using AspectJ annotations.
7. Test cases for each controller or each service bean.