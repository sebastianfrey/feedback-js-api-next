# Change log

The `next` version of 4.26 is now available.  Planned release date is February 2023.

![Current build version](https://img.shields.io/npm/v/arcgis-js-api/next?label=Current%20build)

## TBD


# Breaking Changes
- TBD

The following classes, methods, properties and events have been deprecated for at least 2 releases and have now been removed from the SDK:

| Class/Property/Method/Event | Alternate option | Version deprecated |
|----------|-------------|--------------------|
| `esri/views/layers/support/FeatureEffect` | Use [esri/layers/support/FeatureEffect](https://developers.arcgis.com/javascript/latest/api-reference/esri-layers-support-FeatureEffect.html) instead | 4.22 |
| `esri/views/layers/support/FeatureFilter` | Use [esri/layers/support/FeatureFilter](https://developers.arcgis.com/javascript/latest/api-reference/esri-layers-support-FeatureFilter.html) instead | 4.22 |
| `BasemapToggle.toggle` and `BasemapToggleViewModel.toggle` events | Watch the [activeBasemap](https://developers.arcgis.com/javascript/latest/api-reference/esri-widgets-BasemapToggle.html#activeBasemap) property instead | 4.22 |
| `CSVLayerView.effect` | Use [CSVLayerView.featureEffect](https://developers.arcgis.com/javascript/latest/api-reference/esri-views-layers-CSVLayerView.html#featureEffect) instead | 4.22 |
| `FeatureLayerView.effect` | Use [FeatureLayerView.featureEffect](https://developers.arcgis.com/javascript/latest/api-reference/esri-views-layers-FeatureLayerView.html#featureEffect) instead | 4.22 |
| `GeoJSONLayerView.effect` | Use [GeoJSONLayerView.featureEffect](https://developers.arcgis.com/javascript/latest/api-reference/esri-views-layers-GeoJSONLayerView.html#featureEffect) instead | 4.22 |
| `OGCFeatureLayerView.effect` | Use [OGCFeatureLayerView.featureEffect](https://developers.arcgis.com/javascript/latest/api-reference/esri-views-layers-OGCFeatureLayerView.html#featureEffect) instead | 4.22 |
| `PrintViewModel.scaleEnabled` | Use [TemplateOptions.scaleEnabled](https://developers.arcgis.com/javascript/latest/api-reference/esri-widgets-Print-TemplateOptions.html#scaleEnabled) or [PrintTemplate.scalePreserved](https://developers.arcgis.com/javascript/latest/api-reference/esri-rest-support-PrintTemplate.html#scalePreserved) instead | 4.22 |
| `SearchViewModel.defaultSymbol	` | Use [SearchViewModel.defaultSymbols](https://developers.arcgis.com/javascript/latest/api-reference/esri-widgets-Search-SearchViewModel.html#defaultSymbols) instead | 4.22 |
| `StreamLayerView.effect` | Use [StreamLayerView.featureEffect](https://developers.arcgis.com/javascript/latest/api-reference/esri-views-layers-StreamLayerView.html#featureEffect) instead | 4.22 |
| `WFSLayerView.effect` | Use [WFSLayerView.featureEffect](https://developers.arcgis.com/javascript/latest/api-reference/esri-views-layers-WFSLayerView.html#featureEffect) instead | 4.22 |

Please refer to the [Breaking changes](https://developers.arcgis.com/javascript/latest/breaking-changes/) guide topic for a complete list of breaking changes across all releases of the 4.x.

## Bug fixes and enhancements
- BUG-000146636: Fixed an issue where using the Zoom To action in popups would zoom passed the selected geometry's extent.
- BUG-000153564: Fixed an issue where VectorTileLayer intermittently stopped drawing some tiles at certain zoom levels.
- Esri Community - 1241411: Fixed an issue where an AbortError thrown when deleting a layer after changing its definitionExpression.
- Fixed an issue where MediaContent charts in a pop-up displaying information from a relationship were only showing one related feature.
- Fixed an issue where two queryAttachments requests were sent to the service when selecting a feature that had AttachmentsContent in it's pop-up.

## Deprecations

The following are deprecated and will be removed in a future release. For anything deprecated in 4.25 and earlier, additional information and links are in the [release notes](https://developers.arcgis.com/javascript/latest/release-notes/#deprecated-classes-properties-methods-events).

<details>
  <summary>Click to expand!</summary>  

* Compatibility with implementations that don't support async/await at runtime, within AMD modules, is deprecated since version 4.25. For example, Angular applications using esri-loader will need to migrate from AMD modules to using @arcgis/core ES modules.
* CreateWorkflow deprecated since version 4.23. Use CreateFeaturesWorkflow instead.
* CreateWorkflowData.edits deprecated since 4.23. Use CreateFeaturesWorkflow.pendingFeatures to access edits made to the workflow data.
* CreateWorkflowData deprecated since version 4.23. Use CreateFeaturesWorkflowData instead.
* Directions.routeServiceUrl deprecated since version 4.24. Use url from layer instead.
* Directions.routeSymbol deprecated since version 4.24. Use directionLines from layer instead.
* Directions.stopSymbols deprecated since version 4.24. Use RouteStopSymbols from layer instead.
* DirectionsViewModel.highlightSegment deprecated since version 4.24. Use highlight instead.
* DirectionsViewModel.routeServiceUrl deprecated since version 4.24. Use url from layer instead.
* DirectionsViewModel.routeSymbol deprecated since version 4.24. Use directionLines from layer instead.
* DirectionsViewModel.stops deprecated since version 4.24. Use stops from layer instead.
* DirectionsViewModel.stopSymbols deprecated since version 4.24. Use RouteStopSymbols from layer instead.
* Editor.startCreateWorkflowAtFeatureCreation deprecated since version 4.23. Instead use startCreateFeaturesWorkflowAtFeatureCreation
* Editor.startCreateWorkflowAtFeatureEdit deprecated since 4.23
* Editor.startCreateWorkflowAtFeatureTypeSelection deprecated since version 4.23. Instead use startCreateFeaturesWorkflowAtFeatureTypeSelection instead.
* Editor.useDeprecatedCreateWorkflow deprecated since version 4.23. Although new at 4.23, this property was introduced to help migrate from the legacy CreateWorkflow to the updated CreateFeaturesWorkflow. Once CreateWorkflow is fully removed, this property will no longer be necessary.
* EditorViewModel.startCreateWorkflowAtFeatureCreation deprecated since version 4.23. Instead use startCreateFeaturesWorkflowAtFeatureCreation.
* EditorViewModel.startCreateWorkflowAtFeatureEdit deprecated since 4.23
* EditorViewModel.startCreateWorkflowAtFeatureTypeSelection deprecated since version 4.23. Instead use startCreateFeaturesWorkflowAtFeatureTypeSelection.
* EventAttachedCallback.EventAttachedCallback deprecated since version 4.24. Use reactiveUtils.ReactiveListenerChangeCallback() instead.
* FeatureTable.clearHighlights deprecated since version 4.25. Use highlightIds.removeAll() instead.
* FeatureTable.clearSelection deprecated since version 4.25. Use highlightIds.removeAll() instead.
* FeatureTable.fieldConfigs deprecated since version 4.24. Use FieldColumnTemplate via the FeatureTable's tableTemplate.
* FeatureTable.highlightOnRowSelectEnabled deprecated since version 4.25. Use highlightEnabled instead.
* FeatureTableViewModel.clearHighlights deprecated since version 4.25. Use highlightEnabled instead.
* FeatureTableViewModel.clearSelection deprecated since version 4.25. Use highlightEnabled instead.
* FeatureTableViewModel.fieldConfigs deprecated since version 4.24. Use FieldColumnTemplate via the FeatureTable's tableTemplate.
* FeatureTableViewModel.highlightOnRowSelectEnabled deprecated since version 4.25. Use highlightEnabled instead.
* FieldColumn.config deprecated since version 4.24. Use FieldColumnTemplate via the FeatureTable's tableTemplate.
* FieldColumnConfig deprecated since version 4.24. Use FieldColumnTemplate via the FeatureTable's tableTemplate.
* FieldGroupConfig.visibilityExpression deprecated since version 4.23. Set fields via the GroupElement.visibilityExpression
* FieldGroupConfig deprecated since version 4.23. Set field groupings via the GroupElement.
* HeatmapRenderer.blurRadius is deprecated since version 4.24. Use radius instead.
* HeatmapRenderer.maxPixelIntensity is deprecated since version 4.24. Use maxDensity instead.
* HeatmapRenderer.minPixelIntensity is deprecated since version 4.24. Use minDensity instead.
* ImageParameters deprecated since version 4.24. Use ImageParameters instead.
* InputFieldGroup.visibilityExpression deprecated Since 4.23. Use groupElement.visibilityExpression
* Lighting deprecated since version 4.24. Use SunLighting instead.
* PausableWatchHandle.PausableWatchHandle deprecated since version 4.24.
* PromisedWatchHandle.PromisedWatchHandle deprecated since version 4.24. Use Promise instead.
* promiseUtils.create deprecated since version 4.24. Use Promise instead.
* SlicePlane deprecated This module was moved in 4.23. Use SlicePlane instead.
* UtilityNetwork.rulesTableId deprecated since version 4.25. Use networkSystemLayers.rulesTableId instead.
* UtilityNetwork.rulesTableUrl deprecated since version 4.25. Use networkSystemLayers.rulesTableUrl instead.
* UtilityNetwork.subnetworksTableId deprecated since version 4.25. Use networkSystemLayers.subnetworksTableId instead.
* UtilityNetwork.subnetworksTableUrl deprecated since version 4.25. Use networkSystemLayers.subnetworksTableUrl instead.
* VoxelVariable deprecated This module was moved in 4.25. Use VoxelVariable instead.
* VoxelVolumeStyle deprecated This module was moved in 4.25. Use VoxelVolumeStyle instead.
* watchUtils.init deprecated since 4.24. Use reactiveUtils.watch() instead.
* watchUtils.on deprecated since 4.24. Use reactiveUtils.on() instead.
* watchUtils.once deprecated since 4.24. Use reactiveUtils.once() instead.
* watchUtils.pausable deprecated Since 4.24.
* watchUtils.watch deprecated since 4.24. Use reactiveUtils.watch() instead.
* watchUtils.when deprecated since 4.24. Use reactiveUtils.when() instead.
* watchUtils.whenDefined deprecated since 4.24. Use reactiveUtils.when() instead.
* watchUtils.whenDefinedOnce deprecated since 4.24. Use reactiveUtils.whenOnce() instead.
* watchUtils.whenEqual deprecated since 4.24. Use reactiveUtils.when() instead
* watchUtils.whenEqualOnce deprecated since 4.24. Use reactiveUtils.whenOnce() instead.
* watchUtils.whenFalse deprecated since 4.24. Use reactiveUtils.when() instead.
* watchUtils.whenFalseOnce deprecated since 4.24. Use reactiveUtils.whenOnce() instead.
* watchUtils.whenNot deprecated since 4.24. Use reactiveUtils.when() instead.
* watchUtils.whenNotOnce deprecated since 4.24. Use reactiveUtils.whenOnce() instead.
* watchUtils.whenOnce deprecated since 4.24. Use reactiveUtils.whenOnce() instead.
* watchUtils.whenTrue deprecated since 4.24. Use reactiveUtils.when() instead.
* watchUtils.whenTrueOnce deprecated since 4.24. Use reactiveUtils.whenOnce() instead.
* watchUtils.whenUndefined deprecated since 4.24. Use reactiveUtils.when() instead.
* watchUtils.whenUndefinedOnce deprecated since 4.24. Use reactiveUtils.whenOnce() instead.
* watchUtils deprecated since version 4.24. Use reactiveUtils instead.

</details>

The following are deprecations to the SDK's TypeScript type definitions, and will be removed in a future release (expand to read more). 

<details>
<summary>Click to expand</summary>

* `IPromise` deprecated since version 4.25. Use native `Promise` instead.
* Instances of `*Constructor` deprecated since 4.25. Update usage of `__esri.ModuleConstructor` to `typeof __esri.Module`, or `import` the module from typings and change the type assignment to `typeof Module`.

</details>
