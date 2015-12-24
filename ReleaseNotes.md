## What's new in gwt-links-1.4.jar ? ##

- 1.4.1 : option to disable user interactions

### Bug fixes ###
  * Minor bug fixes

### New in this release ###
  * Improve the refresh system performance
  * Export/Import with XML
  * Support ScrollPanel - getViewAsScrollPanel()


## What's new in gwt-links-1.3.jar ? ##

### Bug fixes ###
  * Shape stays translucide on Mouse Over
  * Left and right selectable ares doesn't appear

### New in this release ###
  * Improve the refresh system performance
  * Stop refreshing when nothing happens
  * Some refactoring

## What's new in gwt-links-1.2.jar ? ##

### Bug Fixes ###
  * [Issue 5](http://code.google.com/p/gwt-links/issues/detail?id=5) : Add a specific exception to notify the developper that the view has to be added to the RootPanel or a widget.

### New in this release ###
  * [Issue 3](http://code.google.com/p/gwt-links/issues/detail?id=3) : Add specific options in the contextual menu (on right click) with :
```
// Diagram Controller
public void addOptionInContextualMenu(String text, Command command);
public void addDeleteOptionInContextualMenu(String text);
public void addSetStraightOptionInContextualMenu(String text);
```

  * [Issue 4](http://code.google.com/p/gwt-links/issues/detail?id=4) : Manage a segment directly with the API to add line segments or straighten a segment :
```
//Diagram Controller
public void addPointOnConnection(Connection c,int left, int right);
public void straightenConnection(Connection c);
```


## What's new in gwt-links-1.1.1.jar ? ##

It's old ! get the earlier one ;)