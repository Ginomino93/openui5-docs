<!-- loio7b826642c45d4b8d97c5013cdc240ad6 -->

| loio |
| -----|
| 7b826642c45d4b8d97c5013cdc240ad6 |

<div id="loio">

view on: [demo kit nightly build](https://openui5nightly.hana.ondemand.com/#/topic/7b826642c45d4b8d97c5013cdc240ad6) | [demo kit latest release](https://openui5.hana.ondemand.com/#/topic/7b826642c45d4b8d97c5013cdc240ad6)</div>

## What's New in OpenUI5 1.73

With this release OpenUI5 is upgraded from version 1.72 to 1.73.

***

<a name="loio7b826642c45d4b8d97c5013cdc240ad6__section_bkm_s15_zcb"/>

### New Controls

| **`sap.f.AvatarGroup` \(Experimental\)** `AvatarGroup` is used to display a group of related avatars, arranged horizontally. The control allows you to display the avatars in different sizes, depending on your use case. Two group types are available: `Group` and `Individual`.  ![](loiod2ac28d2859f484fb9228049eefe0372_HiRes.gif) 

 For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.f.AvatarGroup) and the [Samples](https://openui5.hana.ondemand.com/#/entity/sap.f.AvatarGroup).|

***

<a name="loio7b826642c45d4b8d97c5013cdc240ad6__section_qwl_pb5_zcb"/>

### Improved Features

 > **Warning:** The below table contains complex elements that cannot not be displayed within a simple markdown table. It has been automatically converted to an HTML table. It's design may vary from the source page!

<table>
	<thead>
		<tr>
			<th>**Export Functions**The `sap.ui.core.util.Export` class has been deprecated.</th>

 -   Methods for finding bindings that have become public:

     -   `sap.ui.model.odata.v4.ODataModel#getAllBindings`
     -   `sap.ui.model.Binding#getPath` 
     -   `sap.ui.model.Binding#getContext`
     -   `sap.ui.model.Binding#getModel`

 > Restriction:  
 > Due to the limited feature scope of this version of the OpenUI5 OData V4 model, check that all required features are in place before developing applications. Double-check the detailed documentation of the features, as certain parts of a feature may be missing. While we aim to be compatible with existing controls, some controls might not work due to small incompatibilities compared to `sap.ui.model.odata.(v2.)ODataModel`, or due to missing features in the model \(such as tree binding\). This also applies to controls such as `TreeTable` and `AnalyticalTable`, which are not supported in combination with the OpenUI5 OData V4 model. The interface for applications has been changed for easier and more efficient use of the model. For a summary of these changes, see [Changes Compared to OData V2 Model](Changes_Compared_to_OData_V2_Model_abd4d7c.md).

 For more information, see [OData V4 Model](OData_V4_Model_5de13cf.md), the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.ui.model.odata.v4), and the [Samples](https://openui5.hana.ondemand.com/#/entity/sap.ui.model.odata.v4.ODataModel).</td>
		</tr>

***

<a name="loio7b826642c45d4b8d97c5013cdc240ad6__section_rqn_wd5_zcb"/>

### Improved Controls

		<tr>
			<td> **`sap.f.semantic.SemanticPage`** The `fitContent` property of the `sap.f.DynamicPage` control is now also exposed in `sap.f.semantic.SemanticPage`. It's used to optimize the responsiveness and behavior of the control and we recommend using this property when displaying content of adaptive controls that stretch to fill the available space.For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.f.semantic.SemanticPage). </td>
			<td>**`sap.m.Button`**Four new button types were introduced in the `sap.m.ButtonType` enum. Designed as message triggering buttons, use them to open `sap.m.MessagePopover`. Each button type has a dedicated meaning.
 -   Critical
 -   Negative
 -   Success
 -   Neutral

 ![](loiodbf0df86dd374616b631e278ab40f5de_LowRes.png) 

For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.ButtonType).</td>
		</tr>
		<tr>
			<td>**`sap.m.ComboBox`, `sap.m.MultiComboBox`**We have updated the behavior of the `showItems` method. When the control's picker is opened, the dropdown arrow is not in pressed state, as it was previously. Now, pressing the dropdown arrow for the first time opens the control's picker with all items, and with the second press the picker is closed. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.ComboBoxBase).</td>
			<td>**`sap.m.Dialog`**We have enabled responsive padding support. Application developers can now configure `sap.m.Dialog` and enable its responsive padding in the SAP Fiori 3 themes. For more information, see [Enabling Responsive Paddings According to the Control Width](Enabling_Responsive_Paddings_According_to_the_Control_Width_3b718b5.md).</td>
			<td>**`sap.m.Input`**A `change` event is now fired when the browser autofill fills an input.
 > Note:  
 > If `showValueHelp` or `showSuggestion` are set to `true`, the native browser autofill will not fire a `change` event.

 For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.Input).
			</td>
		</tr>
		<tr>
			<td>**`sap.m.Label`**A visual change was introduced for the `sap.m.Label` control to align it with SAP Fiori Design Guidelines. The asterisk is now positioned on the right side of the text. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.Label) and the [Sample](https://openui5.hana.ondemand.com/#/entity/sap.m.Label/sample/sap.m.sample.Label).</td>
			<td> **`sap.m.list`**, **`sap.m.StandardListItem`** The usability of the additional information text and its combination with title and description has been improved for these controls. The information text is no longer truncated if it is shorter than or equal to the character limit predefined by the control. For more information, see the [Card Explorer](https://openui5.hana.ondemand.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/list/numeric). </td>
			<td>**`sap.m.MessagePopover`**We have exposed the `groupItems` property and `navigateBack` function as APIs in the control. Using the `navigateBack` function you can navigate back to the list page, and with the `groupItems` property you can configure whether or not items should be grouped. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.MessagePopover). </td>
			<td>**`sap.m.NotificationListItem`**, **`sap.m.NotificationListGroup`**We have redesigned the notifications, and now they are lighter, easy to use, and aligned with the SAP Fiori 3 user experience. The changes include:
 -   The priority of the notifications is now visualized with a status icon.
 -   Action buttons in the `sap.m.OverflowToolbar` could now be hidden.
 -   Collapse/expand functionality of the `sap.m.NotificationListGroup` is implemented with an arrow button instead of text.
 -   For the `sap.m.NotificationListGroup`, we have enabled an item counter, which represents the count of currently loaded items inside this group. It can be visible or hidden using the new `showItemsCounter` property.
 -   The new `authorInitials` property is now introduced for `sap.m.NotificationListItem`. It is visualized as an avatar, and used as a fallback when the `authorPicture` is not provided. The background color of the avatar is chosen randomly.

For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.NotificationListGroup) and the [Samples](https://openui5.hana.ondemand.com/#/entity/sap.m.NotificationListGroup).
			</td>
		</tr>
		<tr>
			<td>**`sap.m.NumericContent`**A new `adaptiveFontSize` property is now introduced to meet different country/locale requirements according to the Unicode Common Locale Data Repository \(CLDR\). For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.NumericContent) and [CLDR](http://cldr.unicode.org/).</td>
			<td>**`sap.m.PlanningCalendar`**We have added a new `headerId` parameter to the `rowHeaderClick` event, which enables developers to directly access row header by ID.
 > Note:  
 > Do not use this feature for `PlanningCalendar`’s `rowHeader` modification.

For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.PlanningCalendar).</td>
		</tr>
		<tr>
			<td> **`sap.m.ProgressIndicator`** With the new `displayAnimation` property, you can now determine whether a percentage change is displayed with or without animation.For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.ProgressIndicator) and the [Sample](https://openui5.hana.ondemand.com/#/entity/sap.m.ProgressIndicator/sample/sap.m.sample.ProgressIndicator). </td>
			<td>**`sap.ui.integration.widgets.Card`**-   We have improved the support for the relative date ranges. This allows the card developers to use date ranges, such as `lastYear` or `nextQuarter` inside the card's manifest. Such automatically calculated date ranges can be used in data requests or other card attributes. For more information, see [Integration Card Date Range Handling](https://openui5.hana.ondemand.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/featureDateRangeHandling) in the Card Explorer. -   We have added a new `format` namespace to hold formatters used in expression bindings, and added a predefined `date` formatter method to it. For more information, see the [Sample](https://openui5.hana.ondemand.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/dateAndTime) in the Card Explorer.
 -   The custom HTML element to consume cards on any web page is refactored. Now, height and width are specified in the standard CSS syntax and no longer as separate tag attributes. For more information, see the [Sample](https://openui5.hana.ondemand.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/htmlConsumption) in the Card Explorer.
			</td>
		</tr>
		<tr>
			<td>**`sap.ui.layout.cssgrid.ResponsiveColumnLayout`**This control now also supports Microsoft Internet Explorer 11, due to the implemented polyfill. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.ui.layout.cssgrid.CSSGrid) and the [Sample](https://openui5.hana.ondemand.com/#/entity/sap.ui.layout.cssgrid.CSSGrid/sample/sap.ui.layout.sample.GridResponsiveColumnLayout).</td>
			<td> **`sap.ui.table.AnalyticalTable, sap.ui.table.Table, sap.ui.table.TreeTable`** The `navigated` property that was introduced in version 1.72 is now also available for these controls \(if no row actions are available\). The property shows a navigation indicator at the end of a row to indicate that the user has either already navigated to further details or can navigate to further details from the item, depending on the application use case. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.ui.table.RowSettings) and the [Sample](https://openui5.hana.ondemand.com/#/entity/sap.ui.table.Table/sample/sap.ui.table.sample.RowAction). </td>
			<td> **`sap.uxap.ObjectPageHeader`** With the new `objectImageBackgroundColor` property, you can now determine the background color of the icon or the image placeholder used in the `sap.uxap.ObjectPageHeader`.For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.uxap.ObjectPageHeader) and the [Sample](https://openui5.hana.ondemand.com/#/entity/sap.uxap.ObjectPageLayout/sample/sap.uxap.sample.ObjectPageHeaderContentPriorities). </td>
			<td> **`sap.uxap.ObjectPageLayout`** With the new `sectionChange` event, you can identify when the page is scrolled to a specific section. The `section` and `subSection` event parameters are provided when the event is fired.For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.uxap.ObjectPageLayout). </td>
	</tbody>
</table>

***

<a name="loio7b826642c45d4b8d97c5013cdc240ad6__section_r5v_3h5_zcb"/>

### Demo Kit Improvements

| **Search Highlighting in *Search Results* and *API Reference* Tree** You can now easily find the results you're interested in with the new search highlighting functionality that we implemented for the *Search Results* page and the *API Reference* tree filter.  ![](loio040558940043445a9299e24b37aef5c5_HiRes.gif) 

 |

