## Project Setup ##
  1. Add the gwt-links archive in your application library folder (for example war/WEB-INF/lib/)
  1. Add the archive of the gwt-incubator library [gwt-incubator.jar](http://google-web-toolkit-incubator.googlecode.com/files/gwt-incubator-20101117-r1766.jar) in your application library folder (for example war/WEB-INF/lib/)
  1. Insert in your module file (ending with .gwt.xml) the lines below :

```
   <inherits name='com.orange.links.Links' />
   <inherits name='com.google.gwt.widgetideas.WidgetIdeas' />   
   <inherits name='com.google.gwt.libideas.LibIdeas' />
```

## Simple Example ##

Begin by instantiating a controller to manage the events and the links logic :
```
DiagramController controller = new DiagramController(400,400);
controller.showGrid(true); // Display a background grid
```

Add some widgets and link them together :
```
Label helloLabel = new Label("Hello");
controller.addWidget(labelHello,25,115);

Label worldLabel = new Label("World");
controller.addWidget(labelWorld,200,115);

Connection c1 = controller.drawStraightArrowConnection(labelHello, labelWorld);
```

Handle events on tie or untie :
```
controller.addTieLinkHandler(new TieLinkHandler() {
			@Override
			public void onTieLink(TieLinkEvent event) {
				// Do fun stuff
			}
		});
```

Now, we want to add a nice decoration on the link :
```
Label decorationLabel = new Label("Mickey");
controller.addDecoration(decorationLabel, c1);
```

Finally, you can use the gwt-dnd library to drag them on the canvas :
```
PickupDragController dragController = new PickupDragController(controller.getView(), true);
dragController.makeDraggable(labelHello);
dragController.makeDraggable(labelWorld);
// Register the dragController in gwt-links
controller.registerDragController(dragController);
```