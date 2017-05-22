## ServiceNow Dump
GIT Markdown help found here: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

### ServiceNow On Demand Library

https://community.servicenow.com/community/on-demand-library

### KnowledgeBase

Custom knowledge base

http://www.goranlundqvist.com/2016/02/having-knowledge-public-with-version-3.html

Creating a Knowledge Search Homepage Widget

https://www.servicenowguru.com/system-ui/creating-knowledge-search-homepage-widget/

Link to Knowledge Category

https://express.servicenow.com/support/forums/topic/link-to-knowledge-category/



### ServiceNow Style Guide

http://styleguide.servicenow.com/#/resources/platform-ui-assets

### Service Portal

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
### Custom Content Blocks!!!

https://serviceportal.io/custom-content-block-types/

### Glide Queries

Glide Query Examples

https://docs.servicenow.com/bundle/istanbul-servicenow-platform/page/script/server-scripting/concept/c_GlideRecordQueryExamples.html

Glide Query Cheat Sheet

https://www.servicenowguru.com/scripting/gliderecord-query-cheat-sheet/

### Glide Ajax

Glide Ajax

http://wiki.servicenow.com/index.php?title=GlideAjax#gsc.tab=0

### ServiceNow CookBook

http://servicenowcookbook.com/w/index.php/Main_Page

### Scoped Applications

Scoped Applications and Client Scripts: A Primer

https://community.servicenow.com/community/develop/blog/2015/10/01/scoped-applications-and-client-scripts-a-primer

### JELLY

Jelly Cheat Sheet ***

http://snaug.com/?page_id=39

### GIT

Benefits of integrating ServiceNow with GIT

https://community.servicenow.com/thread/224468

### ServiceNow Scripting

http://wiki.servicenow.com/index.php?title=Script_in_ServiceNow#gsc.tab=0

## Scoped Scripting

http://wiki.servicenow.com/index.php?title=Scoped_Script_Logging#gsc.tab=0

### Others

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

### Widgets

Creating an interactive United States Map

https://community.servicenow.com/community/develop/blog/2016/09/27/creating-an-interactive-united-states-map

Widget options schema

https://docs.servicenow.com/bundle/istanbul-servicenow-platform/page/build/service-portal/concept/c_WidgetInstanceOptions.html

Writing an AngularJS custom filter for Service Portal

https://community.servicenow.com/community/develop/blog/2016/06/22/writing-a-angularjs-custom-filter-for-service-portal

### Best Practices

Client Script Best Practices

http://wiki.servicenow.com/index.php?title=Client_Script_Best_Practices#gsc.tab=0

### Popups/Alerts with UI pages

https://community.servicenow.com/thread/216806

Scripting Alert, Info, and Error Messages

http://wiki.servicenow.com/index.php?title=Scripting_Alert,_Info,_and_Error_Messages#gsc.tab=0

All users notification popup message (<<Used this)

https://community.servicenow.com/thread/157592

### Debugging

Where is gs.debug()?

https://community.servicenow.com/thread/241075

How to properly debug.

https://community.servicenow.com/message/957110?_ga=1.120582408.1658960535.1474482648#957110

### Service Portal

Unsupported features in Service Portal

https://docs.servicenow.com/bundle/istanbul-servicenow-platform/page/build/service-portal/reference/unsupported-features-sp.html

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

# iFrame Sizing
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
| --------------- |:-------------:|
| Cmd + H         | Help |
| Ctrl+M          | Toggle Full Screen |
| Cmd+F           | Start Searching |
| Cmd+G           | Find Next |
| Cmd+Shift+G     | Find Previous |
| Cmd+E           | Replace  |
| Cmd+;             | Replace All |
| Cmd+/             | Toggle Comment |
| Ctrl+Space        | Scripting Assistance |
| Show Description  | Cmd+J |
