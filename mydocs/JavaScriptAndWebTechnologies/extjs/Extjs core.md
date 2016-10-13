
## Ext JS core methods

1. Ext.define() -  to define a class
2. Ext.create() - to create object to a class
3. Ext.apply().
4. Ext.require() - specify the required class
5. Ext.onReady() alias to Ext.EventManager.onDocumentReady();
6. Ext.get() - to get a element reference by id.

# Ext Core classess

 Ext-JS class system has set **pre-processor** and set of **post-processors**

| CLASS               | desc                                                       | Study EXT JS Doc |
|--------             |--------                                                    |--|
|Ext.Element          |    this class responsible for dealing with DOM             | Yes, it is must |
|Ext.ClassManager     |   which is responsible for creatting class and associte it with a name     |
|Ext.Base             |   which is the base class, like in java java.lang.Object     |
|Ext.Class            |   every classes of EXTJS represent by Ext.Class type. Simplarly in java java.lang.Class. (When we use the Ext.define method to define a class we are in fact creating an instance of the Ext.Class class.) |
|Ext.DomQuery         |   this class responsible for query dom element     |
|Ext.DomHelper        |   used to create dom element and html fragment    |
|Ext.ComponentQuery   |   use to query DOM tree using selector    |
|Ext.MessageBox       |   it class name and its alias is **Ext.Msg**    |
|LocalStorageProxy    | it store data in HTML 5 local storage, rather than ext js's store|



# Ext Application specific class

| Class Name | desc |
|--------|--------|
|     **Ext.app.Application**    |  introduced in ExtJS 4, as application entry poiont, give application name space      |
|     **Ext.app.Controller**    |  it is base controller    |
|     **Ext.data.Model**    |  it is base model    |
|     **Ext.app.Store**    |  it is base store    |
|  
