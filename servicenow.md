## ServiceNow Dump
GIT Markdown help found here: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

### ServiceNow Style Guide

http://styleguide.servicenow.com/#/resources/platform-ui-assets

### Glide Queries

Glide Query Examples

https://docs.servicenow.com/bundle/istanbul-servicenow-platform/page/script/server-scripting/concept/c_GlideRecordQueryExamples.html

Glide Query Cheat Sheet

https://www.servicenowguru.com/scripting/gliderecord-query-cheat-sheet/

### ServiceNow CookBook

http://servicenowcookbook.com/w/index.php/Main_Page

### Scoped Applications

Scoped Applications and Client Scripts: A Primer

https://community.servicenow.com/community/develop/blog/2015/10/01/scoped-applications-and-client-scripts-a-primer

### GIT

Benefits of integrating ServiceNow with GIT

https://community.servicenow.com/thread/224468

### ServiceNow Scripting

http://wiki.servicenow.com/index.php?title=Script_in_ServiceNow#gsc.tab=0

### Others

Hiding insert and insert and stay buttons on approvals

https://community.servicenow.com/thread/204727

Adding Dependent Reference Variables

http://wiki.servicenow.com/index.php?title=Adding_Dependent_Reference_Variables#gsc.tab=0

isMemberOf function

https://community.servicenow.com/thread/155710

CMS Menu Item : can we have it Conditional?

https://community.servicenow.com/thread/195308

### Widgets

Creating an interactive United States Map

https://community.servicenow.com/community/develop/blog/2016/09/27/creating-an-interactive-united-states-map

Widget options schema

https://docs.servicenow.com/bundle/istanbul-servicenow-platform/page/build/service-portal/concept/c_WidgetInstanceOptions.html

Writing an AngularJS custom filter for Service Portal

https://community.servicenow.com/community/develop/blog/2016/06/22/writing-a-angularjs-custom-filter-for-service-portal

### Code Snippets

# Test for group membership
Client Script
```javascript
<j:if test="${gs.getUser().isMemberOf('<sysid of group>')}">  
    <div>Show me!</div>
</j:if>  
```

# Test for role
Client Script
```javascript
<j:if test="${gs.hasRole('itil','admin')}">        
  <li><a href="navpage.do" target="_blank"> Process User</a></li>
</j:if>
```
