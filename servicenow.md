# ServiceNow Dump
GIT Markdown help found here: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

## ServiceNow On Demand Library

https://community.servicenow.com/community/on-demand-library

## KnowledgeBase

Custom knowledge base

http://www.goranlundqvist.com/2016/02/having-knowledge-public-with-version-3.html

Creating a Knowledge Search Homepage Widget

https://www.servicenowguru.com/system-ui/creating-knowledge-search-homepage-widget/

Link to Knowledge Category

https://express.servicenow.com/support/forums/topic/link-to-knowledge-category/

## ServiceNow Style Guide

http://styleguide.servicenow.com/#/resources/platform-ui-assets

## Service Portal

Setting up service portal redirection

https://community.servicenow.com/community/service-automation-platform/blog/2017/04/05/setting-up-your-service-portal-redirection

Search in Service Portal

https://github.com/service-portal/search

Configure Search in Service Portal

https://docs.servicenow.com/bundle/istanbul-servicenow-platform/page/build/service-portal/concept/search-service-portal.html

Service Portal Global Search (KBs, etc...)

https://community.servicenow.com/thread/238768

Login page on Service Portal

https://community.servicenow.com/thread/243982

## Custom Content Blocks!!!

https://serviceportal.io/custom-content-block-types/

## Glide Queries

Glide Query Examples

https://docs.servicenow.com/bundle/istanbul-servicenow-platform/page/script/server-scripting/concept/c_GlideRecordQueryExamples.html

Glide Query Cheat Sheet

https://www.servicenowguru.com/scripting/gliderecord-query-cheat-sheet/

## Glide Ajax

Glide Ajax

http://wiki.servicenow.com/index.php?title=GlideAjax#gsc.tab=0

## ServiceNow CookBook

http://servicenowcookbook.com/w/index.php/Main_Page

## Scoped Applications

Scoped Applications and Client Scripts: A Primer

https://community.servicenow.com/community/develop/blog/2015/10/01/scoped-applications-and-client-scripts-a-primer

## JELLY

Jelly Cheat Sheet ***

http://snaug.com/?page_id=39

## GIT

Benefits of integrating ServiceNow with GIT

https://community.servicenow.com/thread/224468

## ServiceNow Scripting

http://wiki.servicenow.com/index.php?title=Script_in_ServiceNow#gsc.tab=0

## Scoped Scripting

http://wiki.servicenow.com/index.php?title=Scoped_Script_Logging#gsc.tab=0

## Others

Helsinki - 'more information' changed to 'preview'

https://community.servicenow.com/thread/231170

Hiding insert and insert and stay buttons on approvals

https://community.servicenow.com/thread/204727

Adding Dependent Reference Variables

http://wiki.servicenow.com/index.php?title=Adding_Dependent_Reference_Variables#gsc.tab=0

isMemberOf function

https://community.servicenow.com/thread/155710

CMS Menu Item : can we have it Conditional?

https://community.servicenow.com/thread/195308

## Widgets

Creating an interactive United States Map

https://community.servicenow.com/community/develop/blog/2016/09/27/creating-an-interactive-united-states-map

Widget options schema

https://docs.servicenow.com/bundle/istanbul-servicenow-platform/page/build/service-portal/concept/c_WidgetInstanceOptions.html

Writing an AngularJS custom filter for Service Portal

https://community.servicenow.com/community/develop/blog/2016/06/22/writing-a-angularjs-custom-filter-for-service-portal

## Common AngularJS Directives for usage in HTML Templates

| DIRECTIVE   | PURPOSE              |
| ----------- | -------------------- |
| ng-model  | This directive binds an input, Select, text area (or custom form control) to the angular scope |
| ng-repeat | Iterate through a data array for example to build a list of records or a table |
| ng-show/ng-hide |  Evaluate an expression to determine if an element is shown |
| ng-if | Evaluate an expression to determine if an element is shown it removes the element from the Dom, therefore more costly-but it will trigger a reevaluation of the widget code, which can come in handy |
| ng-class  | Equivalent of the CSS element class for example be used to assign a CSS class conditionally |
| ng-change | Triggered when the according element changes (e.g. ng-change="c.myChangeFunction()") |
| ng-include | Fetches, compiles and includes an external HTML fragment, for example an angular template |
| watch |  Angular JS record watcher-example used to do something on the client when the value changes on the server |

## Service portal client-side utilities
| API       | PURPOSE |
| ----------- | -------------------- |
| spUtil    | Client side only utility. Can be used for example to add info messages to the page-also required for record watch functionality. See documentation for more functions available |
| addErrorMessage/addInfoMessage | Displays a notification message of different types (requires  spUtil to work - for example spUtil.addInfoMessage("Your order has been placed")) |
| recordwatch |  Requires spUtil.  Well watch specific query on a defined table for updates, if an update happens you can respond to it in real time. Usage: spUtil.recordWatch($scope, "incident", "active=true"); |
| rootScope | The root scope element will for example let you broadcast an event to the root scope of the page (allows communication between widgets). Usage: $rootScope.broadcastEvent("myEvent.name",parm1); |
| console (Browser) | Powerful utility available in both client and server. Can we use to log debug messages of for example the data object.  |

## Portal server side utilities
| API | PURPOSE |
| ----------- | -------------------- |
| $SP | Server-side only utility. Can be used for example to get parameters from the URL, get the glide record for the current portal. See documentation for a list of available functions. |
| console (Browser) | Powerful utility available in both client and server. Can we use to log debug messages.  |

# Best Practices

Client Script Best Practices

http://wiki.servicenow.com/index.php?title=Client_Script_Best_Practices#gsc.tab=0

## Popups/Alerts with UI pages

https://community.servicenow.com/thread/216806

Scripting Alert, Info, and Error Messages

http://wiki.servicenow.com/index.php?title=Scripting_Alert,_Info,_and_Error_Messages#gsc.tab=0

All users notification popup message (<<Used this)

https://community.servicenow.com/thread/157592

## Debugging

Where is gs.debug()?

https://community.servicenow.com/thread/241075

How to properly debug.

https://community.servicenow.com/message/957110?_ga=1.120582408.1658960535.1474482648#957110

## Service Portal

Unsupported features in Service Portal

https://docs.servicenow.com/bundle/istanbul-servicenow-platform/page/build/service-portal/reference/unsupported-features-sp.html

# APIs/Code Snippets

## Create a new record in a table
```
var grIncident = new GlideRecord('incident');
grIncident.newRecord();
grIncident.short_description = 'Hello from the ThirstyMan';
grIncident.insert();
```

## Get a record by ID
```
var gr = new GlideRecord('incident');
if(gr.get('sys_id number goes here')){
    //Do something!
    gs.log(gr.number + ': ' = gr.short_description);
}
```

## Look up task records in new state
```
var gr = new GlideRecord('task');
gr.addQuery('state', '1');
gr.query();
 while (gr.next()) {
   //do something with each incident
 }
```

## Count active records using GlideAggregate
```
var ga = new GlideAggregate('incident');
ga.addQuery('active', 'true');
ga.addAggregate('COUNT');
gr.query();

//This will hold the final count
var count = 0;
if (count.next()) {
    count = ga.getAggregate('COUNT');
}
```

## Convert a JS Oject to JSON
```
var jsonString = JSON.stringify(obj);
```

## Convert a JSON string to JS Object
```
var obj = JSON.parse(jsonString);
```

## Add OR conditions to a GlideRecord query
```
var gr = new GlideRecord('incident');
var qc = gr.addQuery('state', '1');
qc.addOrCondition('state', '2');
qc.addOrCondition('state', '3');
gr.query();

while (gr.next()) {
    //Do Somethnig
}
```

## Test for group membership
Client Script
```javascript
<j:if test="${gs.getUser().isMemberOf('<sysid of group>')}">  
    <div>Show me!</div>
</j:if>  
```

## Test for role
Client Script
```javascript
<j:if test="${gs.hasRole('itil','admin')}">        
  <li><a href="navpage.do" target="_blank"> Process User</a></li>
</j:if>
```

## iFrame Sizing
```javascript
<script>
  function resizeme(ifm) {
  ifm.style.height = ifm.contentWindow.document.body.scrollHeight + 'px';
  }
</script>
```

```html
<iframe src="..." frameborder="0" scrolling="no" onload="resizeme(this)" /> //scrolling=0 if you don't want a slider in the iframe
```

# Studio : Keyboard Shortcuts

(Windows: Use Ctrl key instead of Cmd)

| ShortCut        | Command       |
| --------------- | ------------- |
| Cmd+H           | Help |
| Ctrl+M          | Toggle Full Screen |
| Cmd+F           | Start Searching |
| Cmd+G           | Find Next |
| Cmd+Shift+G     | Find Previous |
| Cmd+E           | Replace  |
| Cmd+;           | Replace All |
| Cmd+/           | Toggle Comment |
| Ctrl+Space      | Scripting Assistance |
| Show Description| Cmd+J |
