
# UI Widget Classes

| Class Name | className | class Name |  |Description|
|------------|-----------|------------|--|-----------|
|   **Ext.ComponentManager**     		  |        | |                                                       | every component instance are registered with its id |
|   Ext.Component-> Ext.AbstractComponent |        | |                                                       | as base class for all the ExtJS widget |
|     									  |  Ext.component.Container | 	   |        | responsible for managing children and  arrange layout. it introduce 'items' property |
|      									  |                          | Ext.tab.Panel |                       | this panel act as container for tabs|
|      									  |                          | Ext.panel.Panel |                     |one of the container, can contain panel and other ui widgets|
|      									  |                          | Ext.grid.Panel |                      |it is just grid container.|
|       								  |                          |                 | Ext.form.Panel		 | this can have any of form field to get user input |
|       								  |                          |                 | Ext.form.Basic		 | responsible for form data population, validation |

|       								  |                          | Ext.panel.Tool          | 					 | have 25 predefined icon |
|       								  |        					 |                 		   |  Ext.window.Window, | it subclass to Panel, it is floating panel |
|       								  |        					 | Ext.container.ViewPort  |     | it occupy entier brower window and listen for resize events |
|       								  |        					 | Ext.container.Container |     | it used as container |
|       								  |        					 | Ext.form.field.Field    |     					| act as super class for base class |
|       								  |        					 | Ext.form.Lable          |     					| act as super class for  base class |
|       								  |        					 | Ext.form.field.Base     |     					| it is base class for all UI widgets|
|       								  |        					 |                         | Ext.form.field.Text  	| responsible for manage text value |
|       								  |        					 |                         | Ext.form.field.Number   | responsible for manage number value |

1. The panel is a workhorse of Ext JS
2. Ext JS uses HTML and CSS to build UI controls and widgets.





# UI Widget Events

*  Events are fired by either by user or lifecyle of a UI widget
*  UI components has set of *lifecycle* events
*  UI component cross 3-phases(creation, render, destrection). each phase has several steps.
