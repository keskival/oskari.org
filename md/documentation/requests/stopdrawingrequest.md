# StopDrawingRequest

If the user is allowed to draw on the map this request can be used to complete the drawing and/or clear the drawing from the map.

## Parameters

(* means the parameter is required)

<table class="table">
<tr>
  <th> Name</th><th> Type</th><th> Description</th><th> Default value</th>
</tr>
<tr>
  <td> * id</td><td> String</td><td> Identifier for request</td><td> </td>
</tr>
<tr>
  <td> clearCurrent</td><td> Boolean</td><td> True - all selection will be removed from the map after stopping plugin, false - will keep selection on the map.</td><td> false</td>
</tr>
</table>

For example:
```javascript
 var sb = Oskari.getSandbox();
 sb.postRequestByName('DrawTools.StopDrawingRequest', ['bufferedLineSelection', true]);
```

## Examples

Complete a draw for 'measure' functionality and keep the drawing on the map:
```javascript
var sb = Oskari.getSandbox();
sb.postRequestByName('DrawTools.StopDrawingRequest', ['measure']);
```

This expects that drawing has been started for id 'measure' and will result in an 'DrawingEvent' where id is 'measure' with the measure data available in event.getData().

Complete a draw for 'myplaces' functionality and clear the drawing from the map:
```javascript
var sb = Oskari.getSandbox();
sb.postRequestByName('DrawTools.StopDrawingRequest', ['myplaces', true]);
```
Again, this expects that drawing has been started for id 'myplaces' and will result in an 'DrawingEvent' where id is 'myplaces' with the drawn shape as geojson available in event.getGeoJson().
