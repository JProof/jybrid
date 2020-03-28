Mirror-Repository for jybrid-library 

jybrid examples under https://github.com/JProof/jybrid-examples

https://jybrid.com 

current Version 0.7.9.3.1 released (fixing)
0.7.9.3 Unobtrusive Ajax (released)

javascript testings:

acceptance-test
* html-append
* html-assign
* html-attributes
* html-class-names
* html-prepend
* js-defer
* js-min-full-switch



### Ajax Response Html Commands 

[Documentation Page](https://jybrid.com/docs/ajax-response/ajax-html?target=_blank)

|command| short description | reference pages |
|---|---|---|---|---|---|
|`$objResponse->html($element,'Text or Html-Tags');`|Inserts Text/Html into the given html element|[Ajax insert Html](/https://demo.jybrid.com/ajax-html.php?target_blank)|
|`$objResponse->html($element);`|Clear/Empty with Ajax Html Element|[Ajax clear/empty Html](/https://demo.jybrid.com/ajax-html.php?target_blank)|
|`$objResponse->remove($element);`|Removes the Element if it exists |[Ajax remove Element](/https://demo.jybrid.com/ajax-html.php?target_blank)|
|`$objResponse->removeAll($elements);`|Remove all Elements with given querySelector |[Ajax remove all Elements](/https://demo.jybrid.com/ajax-html.php?target_blank)|
|`$objResponse->prependHtml($parentElement, 'Text or Html-Tag');`|Inserts Text/Html at first position in parentElement||
|`$objResponse->appendHtml($parentElement, 'Text or Html-Tag');`|Inserts Text/Html at last position in parentElement||



### Ajax html css classname handling

|type|command| initial page load | ajax request| ajax response | short description | reference pages |
|---|---|---|---|---|---|---|
| ajax response |`$objResponse->classSet($element, $classNameString);`|-| - | x |set an classname to html-attribute class="" if exists|<https://demo.jybrid.com/ajax-classNames.php>|
| ajax response |`$objResponse->classClear($element);`|-| - | x |clear all classes from the html-attribute class=""|<https://demo.jybrid.com/ajax-classNames.php>|
| ajax response |`$objResponse->classAdd($element, $classNameString);`|-| - | x |add classname to html-attribute class=""|<https://demo.jybrid.com/ajax-classNames.php>|
| ajax response |`$objResponse->classRemove($element, $classNameString);`|-| - | x |remove the classname from html-attribute class="" if exists|<https://demo.jybrid.com/ajax-classNames.php>|


### Ajax html attributes

|type|command| initial page load | ajax request| ajax response | short description | reference pages |
|---|---|---|---|---|---|---|
| ajax response |`$objResponse->attribSet($element, 'disabled', 'disabled');`|-| - | x |set attribute value |<https://demo.jybrid.com/schematic-ajax-attributes>|
| ajax response |`$objResponse->attribPrepend($element, 'value', ' +Value');`|-| - | x |prepends attribute value |<https://demo.jybrid.com/schematic-ajax-attributes>|
| ajax response |`$objResponse->attribAppend($element, 'value', ' +Value');`|-| - | x |appends attribute value |<https://demo.jybrid.com/schematic-ajax-attributes>|
| ajax response |`$objResponse->attribRemove($element, 'disabled');`|-| - | x |remove attribute if exists|<https://demo.jybrid.com/schematic-ajax-attributes>|
| ajax response |`$objResponse->attribClear($element, 'disabled');`|-| - | x |empties attribute value if exists|<https://demo.jybrid.com/schematic-ajax-attributes>|

### Ajax javascript events during response

|type|command| initial page load | ajax request| ajax response | short description | reference pages |
|---|---|---|---|---|---|---|
| ajax response |`$objResponse->setEvent($element, 'click', 'myJsMethodToCall');`|-| - | x |set event to element which executes 'myJsMethodToCall' (removes other 'click' events)|<https://demo.jybrid.com/schematic-ajax-events-dom.php>|
| ajax response |`$objResponse->addEvent($element, 'click', 'myJsMethodToCall');`|-| - | x |append/add event to element which executes 'myJsMethodToCall'|<https://demo.jybrid.com/schematic-ajax-events-dom.php>|
| ajax response |`$objResponse->fireEvent($element, 'click');`|-| - | x |fire event (exists)|<https://demo.jybrid.com/schematic-ajax-events-dom.php>|
| ajax response |`$objResponse->removeEvent($element, 'click', 'myJsMethodToCall');`|-| - | x |remove single click event 'myJsMethodToCall' from element|<https://demo.jybrid.com/schematic-ajax-events-dom.php>|
| ajax response |`$objResponse->removeEvents($element, 'click');`|-| - | x |remove all click events from element|<https://demo.jybrid.com/schematic-ajax-events-dom.php>|
| ajax response |`$objResponse->removeEvents($element, 'click');`|-| - | x |remove all click events from element|<https://demo.jybrid.com/schematic-ajax-events-dom.php>|


|type|command| initial page load | ajax request| ajax response | short description | reference pages |
|---|---|---|---|---|---|---|
| ajax response |`$objResponse->safeExecuteFunction('myJsMethodToCall');`|js method must be load in browser| - | x |calls an javascript method without eval |<https://demo.jybrid.com/schematic-ajax-events-dom.php>|


### Ajax functional helper

|type|command| initial page load | ajax request| ajax response | short description | reference pages |
|---|---|---|---|---|---|---|
|optional|`Jybrid::getConfig()->setCleanBuffer(true);`|-| x | x |tries to catch echo'd content|<https://demo.jybrid.com/schematic-ajax-response-cleanbuffer.php>|
|required|`Factory::responseRequest(true);`|-| x | x |sends the ajax response back to the client-browser| |

### Ajax http-request header 

all Request / single request

|type|command| initial page load | ajax request| ajax response | short description | reference pages |
|---|---|---|---|---|---|---|
| ajax request all/global |`Jybrid::getHeaders()->addHeaderCommon('jybrid-Ajax-Request-Common-Header', 'Post/GetHeaderValue');`|x| - | - |request GET or POST header(based upon the request-method)|<https://demo.jybrid.com/schematic-ajax-http-request-response-header.php>|
| ajax request all/global |`Jybrid::getHeaders()->addHeaderPost('jybrid-Ajax-Request-Post-Header', 'Request-POST-Header');`|x| - | - |request POST header|<https://demo.jybrid.com/schematic-ajax-http-request-response-header.php>|
| ajax request all/global |`Jybrid::getHeaders()->addHeaderGet('jybrid-Ajax-Request-Get-Header', 'Post/GetHeaderValue');`|x| - | - |request GET header|<https://demo.jybrid.com/schematic-ajax-http-request-response-header.php>|
| ajax request single/individual|`Jybrid::prepareRequest()->addHeaderCommon('jybrid-Ajax-Request-Common-Header', 'Post/GetHeaderValue');`|x| - | - |request GET or POST header(based upon the request-method) particular request|<https://demo.jybrid.com/schematic-ajax-http-request-response-header.php>|
| ajax request single/individual|`Jybrid::prepareRequest()->addHeaderPost('jybrid-Ajax-Request-Post-Header', 'Request-POST-Header');`|x| - | - |request POST header particular request|<https://demo.jybrid.com/schematic-ajax-http-request-response-header.php>|
| ajax request single/individual|`Jybrid::prepareRequest()->addHeaderGet('jybrid-Ajax-Request-Get-Header', 'Post/GetHeaderValue');`|x| - | - |request GET header particular request|<https://demo.jybrid.com/schematic-ajax-http-request-response-header.php>|

### Ajax http-response header 

all Responses / single response 

|type|command| initial page load | ajax request| ajax response | short description | reference pages |
|---|---|---|---|---|---|---|
| ajax response |`Jybrid\Response\Manager::getInstance()->getHeader()->addResponseHeader('response-header-GET-and-POST', 'Post/GetHeaderValue');`|-| - | x |response GET or POST header(based upon the request-method)|<https://demo.jybrid.com/schematic-ajax-http-request-response-header.php>|
| ajax response |`Jybrid\Response\Manager::getInstance()->getHeader()->addHeaderPost('during-POST-Request-Response-Header', 'PostHeaderValue');`|-| - | x |response POST header|<https://demo.jybrid.com/schematic-ajax-http-request-response-header.php>|
| ajax response |`Jybrid\Response\Manager::getInstance()->getHeader()->addHeaderGet('during-GET-Request-Response-Header', 'GetHeaderValue');`|-| - | x |Response GET header|<https://demo.jybrid.com/schematic-ajax-http-request-response-header.php>|


### Ajax Css-Files

add / remove css resource in/from browser.

|type|command| initial page load | ajax request| ajax response | short description | reference pages |
|---|---|---|---|---|---|---|
| ajax response |`$objResponse->includeCSS('assets/test-css/test1.css')`|-| - | x |adding an css-file into the browser head ||
| ajax response |`$objResponse->removeCSS('assets/test-css/test1.css');`|-| - | x |remove an css-file from browser||

### Ajax Javascript 

|type|command| initial page load | ajax request| ajax response | short description | reference pages |
|---|---|---|---|---|---|---|
| ajax response |`$objResponse->confirmCommands($cntNextCommands,'Do you want to apply next $cntNextCommands?');`|-| - | x |Javascript confirm command that asks the user apply(or not) the next followed response-commands in ajax-response|<https://jybrid.com/ajax-response/simple-js-commands#ajax-response-confirm-commands>|
| ajax response |`$objResponse->redirect($url,$waitSecondsBeforeRedirect);`|-| - | x |Ajax redirect the Page to an other Url |<https://jybrid.com/ajax-response/simple-js-commands#ajax-redirect>|
| ajax response |`$objResponse->openNewWindow($url,$target,$focus);`|-| - | x | Opens an new Window or Tab|<https://jybrid.com/ajax-response/simple-js-commands#ajax-open-new-window-or-tab>|
