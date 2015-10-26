# KaPa REST Interface Specification

Documentation for the KaPa REST interface for the Oskari map.

The KaPa interface consists of two REST endpoints:
  * Indicator list (HTTP GET):
    * URL: [KaPa API URL]/1.0/indicators
    * Example response: KapaIndicators.json
  * Indicator data (HTTP GET):
    * URL: [KaPa API URL]/1.0/indicators/[indicator_id]
    * Example response: KapaIndicatorData.json

KaPa API URL is configured to Oskari as the property "kapa.baseurl". It is recommended that this ends with "/rest".

## Indicator List

The data model consists of a set of indicators defined for a set of selectors.

Each indicator has:
  * id: The identifier of the indicator in question
  * title: A localized name for the indicator for showing to the user
  * description: A localized description for the indicator for showing to the user
  * organization: An object describing the source of the information in this indicator
    * id: An identifier for this organization, uniquely identifying the data source within this API
    * title: A localized name for the source organization for showing to the user.
  * selectors: Sets of lists of allowed values keyed by the name of the selector.
    * "layer" key is mandatory, specifying the layers into which the indicator data can be projected.
    * One optional selector could be for example: "year": ["2012", "2013", "2014"]
    * The selector allowed values will be shown to the users, potentially localized by Oskari.

Localized items follow the SotkaNET schema, that is, each localized message is a JSON object containing strings keyed by the locale identifiers.

Each indicator has one mandatory selector, that is "layer", which refers to the Oskari map layers for which this indicator is defined. A typical selector for "layer" would be for example "Kunta".

The values in the layer allowed values must be a subset of layers recognized by Oskari. The allowed values for "layer" selector reflect the SotkaNET layers:
  * "Kunta"
  * "Maakunta"
  * "Erva"
  * "Aluehallintovirasto"
  * "Sairaanhoitopiiri"
  * "Maa"
  * "Suuralue"
  * "Seutukunta"
  * "Nuts1"

## Indicator Data
 
The data returned by this API is a list of objects with region ids and respective values for this indicator:
  * region: A code for the region in question. These _MUST_ follow SotkaNET region "code" values.
    * See: https://opensource.thl.fi/wiki05/pages/viewpage.action?pageId=8947502#SOTKAnetRESTAPI%28avoimendatanrajapinta%29-Aluelistaus
  * value: An integer or a floating point value, i.e. a JSON number.
