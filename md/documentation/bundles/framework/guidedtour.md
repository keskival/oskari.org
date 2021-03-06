# Guided Tour

<table class="table">
  <tr>
    <td>ID</td><td>guidedtour</td>
  </tr>
  <tr>
    <td>API</td><td>[link](/api/latest/classes/Oskari.mapframework.bundle.guidedtour.GuidedTourBundleInstance.html)</td>
  </tr>
</table>

## Description

Shows a dialog on startup to instruct user on map functionalities in paikkatietoikkuna.fi

## Screenshot

![screenshot](/images/bundles/guidedtour.png)

## Bundle configuration

No configuration is required.

## Bundle state

No statehandling has been implemented.

## Requests the bundle handles

This bundle doesn't handle any requests.

## Requests the bundle sends out

<table class="table">
  <tr>
    <th>Request</th><th>Why/when</th>
  </tr>
  <tr>
    <td>userinterface.UpdateExtensionRequest</td><td>Opens and closes flyouts when demonstrating functionalities</td>
  </tr>
</table>

## Events the bundle listens to

This bundle doesn't listen to any events.

## Events the bundle sends out

This bundle doesn't send out any events.

## Dependencies

<table class="table">
  <tr>
    <th>Dependency</th><th>Linked from</th><th>Purpose</th>
  </tr>
  <tr>
    <td> [jQuery](http://api.jquery.com/) </td>
    <td> Linked in portal theme </td>
    <td> Used to create the component UI from begin to end</td>
  </tr>
  <tr>
    <td> [Oskari divmanazer](/documentation/bundles/framework/divmanazer) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for flyout/tile functionality</td>
  </tr>
  <tr>
    <td> [Oskari toolbar](/documentation/bundles/framework/toolbar) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for demonstrating functionality</td>
  </tr>
  <tr>
    <td> [Oskari search](/documentation/bundles/framework/search) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for demonstrating functionality</td>
  </tr>
  <tr>
    <td> [Oskari layerselector](/documentation/bundles/framework/layerselector) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for demonstrating functionality</td>
  </tr>
  <tr>
    <td> [Oskari layerselection](/documentation/bundles/framework/layerselection) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for demonstrating functionality</td>
  </tr>
  <tr>
    <td> [Oskari personaldata](/documentation/bundles/framework/personaldata) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for demonstrating functionality</td>
  </tr>
  <tr>
    <td> [Oskari publisher](/documentation/bundles/framework/publisher) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for demonstrating functionality</td>
  </tr>
  <tr>
    <td> [Oskari mapmodule](/documentation/bundles/framework/mapmodule) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for demonstrating functionality</td>
  </tr>
  <tr>
    <td> [Oskari mapmodule/portti2zoombar](/documentation/bundles/framework/mapmodule/portti2zoombar) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for demonstrating functionality</td>
  </tr>
  <tr>
    <td> [Oskari mapmodule/panbuttons](/documentation/bundles/framework/mapmodule/panbuttons) </td>
    <td> Expects to be present in application setup </td>
    <td> Needed for demonstrating functionality</td>
  </tr>
</table>