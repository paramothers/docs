#JAX-WS 2.1

| Description                              | Annotation          | Attributes | Attributes      | Attributes              |
| ---------------------------------------- | ------------------- | ---------- | --------------- | ----------------------- |
| declared in Service endpoint interface   | @WebService         | name       |                 |                         |
| declare handler of SOAP message          | @HandlerChain       | file       |                 |                         |
| specify either rpc or document           | @SOAPBinding        | style      | use             | parameterStyle          |
| to use SOAP 1.2 version                  | @BindingType        | value      |                 |                         |
|                                          | @RespectBinding     | enabled    |                 |                         |
|                                          | @Addressing         | enabled    | required        |                         |
|                                          | @MTOM               | enabled    | threshold       |                         |
| declared in Service endpoint interface's method | @WebMethod          | action     | operationName   |                         |
| customize response message part          | @WebResult          | name       | targetNamespace | partName, header        |
| it give custom name for parameter istead 'arg0' | @WebParam           | name       | targetNamespace | partName, header,  mode |
| soap fault exception class               | @WebFault           |            |                 |                         |
| when a method return type is VOID        | @OneWay             |            |                 |                         |
| used for JAXB                            | @RequestWrapper     | localName  | targetNamespace | className               |
|                                          | @ResponseWrapper    | localName  | targetNamespace | className               |
|                                          | @XMLSeeAlso         |            |                 |                         |
|                                          | @WebServiceClient   | name       | targetNamespace | wsdlLocation            |
|                                          | @WebEndpoint        | name       |                 |                         |
| it is annotation used for JEE web service client | @WebServiceRef      |            |                 |                         |
| RESTFul web service                      | @WebServiceProvider |            |                 |                         |
| RESTFul web service                      | @ServiceMode        |            |                 |                         |
| RESTFul web service                      | @Path               |            |                 |                         |
| RESTFul web service                      | @GET                |            |                 |                         |
| RESTFul web service                      | @Produces           |            |                 |                         |
| RESTFul web service                      | @POST               |            |                 |                         |
| RESTFul web service                      | @FormParam          |            |                 |                         |
| RESTFul web service                      | @DELETE             |            |                 |                         |

 #jaxb

|                                          |                          |      |      |           |           |
| ---------------------------------------- | ------------------------ | ---- | ---- | --------- | --------- |
| this will give package path for all of our domain class, by having create method for each DTO | @XmlRegistry             |      |      |           |           |
|                                          | @XmlAccessorOrder        |      |      |           |           |
|                                          | @XmlAccessType           |      |      |           |           |
|                                          | @XmlTransient            |      |      |           |           |
|                                          |                          |      |      |           |           |
| among many DTO, this added dto will be root element | @XmlRootElement          |      | name | namespace |           |
| java field as xml attribute              | @XmlAttribute            |      |      |           |           |
| used to specify interface type member, when only one implementation u have | @XmlElement              |      | name | namespace |           |
| used to specify interface type member    | @XmlAnyElement           |      |      |           |           |
| it add a element as a wrapper for its member, usually it is a collection | @XmlElementWrapper       |      |      |           |           |
|                                          | @XmlElementRef           |      |      |           |           |
|                                          |                          |      |      |           |           |
|                                          | @XmlType                 |      | name | namespace | propOrder |
|                                          | @XmlMimeType             |      |      |           |           |
| define custom data type between java & xml | @XmlSchemaType           |      |      |           |           |
| for custom data type adaptor, used when interface has only one impl. | @XmlJavaTypeAdapter      |      |      |           |           |
|                                          | @NormalizedStringAdapter |      |      |           |           |
|                                          |                          |      |      |           |           |
|                                          | @XmlValue                |      |      |           |           |
|                                          |                          |      |      |           |           |
|                                          | @XmlInlineBinaryData     |      |      |           |           |
|                                          | @Generated               |      |      |           |           |
|                                          |                          |      |      |           |           |
