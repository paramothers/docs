|                                  |                                          |                         |                   |
| -------------------------------- | ---------------------------------------- | ----------------------- | ----------------- |
|                                  | if u exported a filled report into XML then again load that into JasperPring | JRPrintXmlLoader        |                   |
|                                  | it is load JsperPrint file from file system to memory as JasperPrint object | JRLoader                |                   |
| 1 st step ..Load xml file        | it is used to load JRXML file into memory | JRXmlLoader             |                   |
| 3rd step .. Compiling xml file   | to compile JRXML file into Jasper Native template | JasperCompileManager    |                   |
| 4th step.. Fill data dynamically | fill data in report                      | JasperFillManager       |                   |
|                                  | it export Jasper Filled report to many format of file | JasperExportManager     |                   |
|                                  | "it is used to send report to Brwoser. It fill the report and stream to browser. | JasperRunManager        |                   |
| 2nd step ..Obtaining this object | in memory representation of JRXML file   | JasperDesign            |                   |
|                                  | in memory representation of COMPILED version of  JRXML file. That is Native format | JasperReport            |                   |
|                                  | it is memory rep. of a FILLED jasper report in native format | JasperPrint             |                   |
|                                  | it is java utillity programe to view the filled report | JasperViewer            |                   |
| testing or debuging              | It is java utillity programe to preview the report without compile & fill. It also can be used to preview compiled report also | JasperDesignViewer      |                   |
|                                  | if u want to customised facility of JFreeChart | JRChartCustomizer       |                   |
|                                  |                                          | JRParameter             |                   |
|                                  | defined some constant used by exporting classes | JRExportParameter.      |                   |
|                                  | used  constant from this when to expoert a report as plain text | JRTextExporterParameter |                   |
|                                  |                                          | JRHtmlExporterParameter |                   |
|                                  | used when a report is very big and need to store some page in virtual memory | JRVirtulaizer           |                   |
|                                  |                                          |                         | JRFileVirtualizer |

|                                          |                                          |                     |                    |
| ---------------------------------------- | ---------------------------------------- | ------------------- | ------------------ |
|                                          |                                          | JRExporter          |                    |
|                                          |                                          |                     | JRPdfExporter      |
|                                          |                                          |                     | JRRtfExporter      |
|                                          |                                          |                     | JROdtExporter      |
|                                          |                                          |                     | JExcelApiExporter  |
|                                          |                                          |                     | JRHtmlExporter     |
|                                          |                                          |                     | JRXmlExporter      |
|                                          |                                          |                     | JRCsvExporter      |
|                                          |                                          |                     | JRTextExporter     |
|                                          | it is just repesentation of Style based template. We may not use | JRTemplate          |                    |
| this is for good to know the execution time of any part of report or access field, variables, parameters values | to call Java code at the time of filling report if need. | JRAbstractScriptlet |                    |
|                                          |                                          |                     | JRDefaultScriptlet |



|                                          |              |                            |
| ---------------------------------------- | ------------ | -------------------------- |
|                                          | JRDataSource |                            |
| use this when no need any dynamic data   |              | JREmptyDataSource          |
| always use this.                         |              | JRResultSetDataSource      |
|                                          |              | JRMapArrayDatasource       |
|                                          |              | JRMapCollectionDataSource  |
| it is useful when we use JPA or Hibernate to retrive object list from DB |              | JRBeanArrayDataSource      |
| it is useful when we use JPA or Hibernate to retrive object list from DB |              | JRBeanCollectionDataSource |
| it is used by Swing Application          |              | JRTableModelDataSource     |
| plain xml going be use as data soruce, at least we can use this to demo or testing |              | JRXmlDataSource            |
| CSV file going to be use as data soruce, at least we can use this to demo or testing |              | JRCsvDataSource            |
| it is interface to create custom Data Soruce |              | JRRewindableDataSource     |
|                                          |              |                            |