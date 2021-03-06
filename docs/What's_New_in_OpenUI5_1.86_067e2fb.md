<!-- loio067e2fb0165145a5ac9b128b5853f7c9 -->

| loio |
| -----|
| 067e2fb0165145a5ac9b128b5853f7c9 |

<div id="loio">

view on: [demo kit nightly build](https://openui5nightly.hana.ondemand.com/#/topic/067e2fb0165145a5ac9b128b5853f7c9) | [demo kit latest release](https://openui5.hana.ondemand.com/#/topic/067e2fb0165145a5ac9b128b5853f7c9)</div>

## What's New in OpenUI5 1.86

With this release OpenUI5 is upgraded from version 1.85 to 1.86.

***

<a name="loio067e2fb0165145a5ac9b128b5853f7c9__section_yxw_pxt_zcb"/>

### New Features

|**Preannouncement: End of Support for Microsoft Internet Explorer 11 after OpenUI5 1.87**OpenUI5 1.87 will be the last version to support Microsoft Internet Explorer 11. For more information, see [End of Support for Microsoft Internet Explorer 11 in Future OpenUI5 Versions](Browser_and_Platform_Support_74b59ef.md#loio74b59efa0eef48988d3b716bd0ecc933__MS_IE).|

***

<a name="loio067e2fb0165145a5ac9b128b5853f7c9__section_qwl_pb5_zcb"/>

### Improved Features

| **OpenUI5 OData V4 Model** The new version of the OpenUI5 OData V4 model introduces the following features: -   A new `unit` property within the `aggregate` map of the `$$aggregation` list binding parameter.

You can use it to determine the correct currency or unit value for the grand total, as well as subtotals. Note that the name provided for `unit` has to refer to a structural property as well as to a custom aggregate. The custom aggregate has to provide the single value of that unit if there is only one, or `null` if there is more than one distinct value.

-   New `grandTotalAtBottomOnly` and `subtotalsAtBottomOnly` properties in the `$$aggregation` list binding parameter. For more information, see [`sap.ui.model.odata.v4.ODataListBinding#setAggregation`](https://openui5.hana.ondemand.com/#/api/sap.ui.model.odata.v4.ODataListBinding/methods/setAggregation).
-   You can now filter by properties that are not aggregated when using visual grouping, that is when having `groupLevels` defined in the `$$aggregation` list binding parameter.
-   If the `$$patchWithoutSideEffects` binding parameter is set, `PATCH` requests are now sent out with the `return=minimal` preference in the [`Prefer` header](http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part1-protocol/odata-v4.0-errata03-os-part1-protocol-complete.html#_Toc453752234). This allows the server to skip the determination of the response.
-   The `sap.ui.model.odata.v4.ODataListBinding#refresh` method can now handle several kept-alive contexts, and also a kept-alive context that has been deleted in the back end, for example due to a side effect. Note that refreshing dependent bindings relative to the context of a deleted entity will fail as that entity no longer exists.

A list binding context can be kept alive with the `sap.ui.model.odata.v4.Context#setKeepAlive` method introduced with OpenUI5 1.81.


 For more information, see [OData V4 Model](OData_V4_Model_5de13cf.md), the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.ui.model.odata.v4), and the [Samples](https://openui5.hana.ondemand.com/#/entity/sap.ui.model.odata.v4.ODataModel) in the Demo Kit.|

***

<a name="loio067e2fb0165145a5ac9b128b5853f7c9__section_rqn_wd5_zcb"/>

### Improved Controls

| **`sap.m.FormattedText`** We have introduced two ways to set the text direction in the control:

-   The HTML `bdi` tag and the HTML `dir` attribute can now be used in the control.
-   The new `textDirection` property sets the text direction for the root DOM element.

 To set the text alignment for the DOM element of the control, you can now use the `textAlign` property. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.FormattedText) and the [Samples](https://openui5.hana.ondemand.com/#/entity/sap.m.FormattedText). |
 > **Warning:** The below table contains complex elements that cannot not be displayed within a simple markdown table. It has been automatically converted to an HTML table. It's design may vary from the source page!

<table>
	<thead>
		<tr>
			<th> **`sap.m.IconTabBar`, `sap.m.RadioButton`** Value states are not shown when the controls are in read-only or disabled mode. If the controls are set as enabled and editable later, then value states are shown.</th>
		<tr>
			<td> **`sap.m.Select`** With the new experimental `columnRatio` property, you can now set a custom ratio of the columns when you're using a two-column layout for `sap.m.Select`.For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.Select) and the [Sample](https://openui5.hana.ondemand.com/#/entity/sap.m.Select/sample/sap.m.sample.Select2Columns). </td>
			<td>**`sap.m.Table`**In version 1.85.1 we have added the `Strict` value to the `fixedLayout` property. If this value is set, and the `width` property of `sap.m.Column` is not set to `auto` for any of the columns, the table renders a placeholder column that occupies the remaining width of the control to ensure the column width is strictly applied.For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.Table/methods/getFixedLayout) and the [Sample](https://openui5.hana.ondemand.com/#/entity/sap.m.Table/sample/sap.m.sample.TableColumnWidth).</td>
			<td> **`sap.m.Title`** We have introduced the `textDirection` property, which is also available in the `sap.m.FormattedText`, `sap.m.Label`, and `sap.m.Text` controls. It allows you to set the text direction to right-to-left \(RTL\) or left-to-right \(LTR\) on a page with mixed-language content. This is important in cases where content from different-direction languages must be shown on the same page. Do not use the `textDirection` property on single-language pages where the direction is centrally determined depending on the language. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.m.Title) and the [Samples](https://openui5.hana.ondemand.com/#/entity/sap.m.Title). </td>
			<td> **`sap.ui.integration.widgets.Card`**

 -   We have introduced a text formatter for texts with placeholders. The text formatter takes a string that contains placeholders and puts values inside these placeholders. Typically the values are translation texts coming from an `i18n` resource bundle. The text formatter allows this replacement to be performed properly for different languages \(each with its own word order\). For more information, see the [Text Formatter](https://openui5.hana.ondemand.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/learn/formatters/text) section in the Card Explorer. -   Using the new `showLoadingPlaceholders` and `hideLoadingPlaceholders` methods you can now precisely control the loading-animation placeholders when using Component card or Extension. For example, as a card developer, you can show the loading-animation placeholder when requesting data and hide it when the data is available. These placeholders can be loaded on a section \(for example, `Header`, `Content`, or `Filters`\) or on the whole card. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.ui.integration.widgets.Card) and the [Explore Extension](https://openui5.hana.ondemand.com/test-resources/sap/ui/integration/demokit/cardExplorer/webapp/index.html#/explore/extension/namedDataSection) section in the Card Explorer.
			</td>
		</tr>
		<tr>
			<td> **`sap.ui.layout.form.SemanticFormElement`** The `SemanticFormElement` element \(experimental\) now allows you to render semantically connected fields separately in edit mode. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.ui.layout.form.SemanticFormElement). </td>
			<td> **`sap.ui.table.AnalyticalTable, sap.ui.table.Table, sap.ui.table.TreeTable`** The `rowsUpdated` event is now available so applications can find out about any updates in the tables they are using, for example, if there has been a model update or a user interaction that modified the rows. For more information, see the [API Reference](https://openui5.hana.ondemand.com/#/api/sap.ui.table.Table/events/rowsUpdated). </td>
	</tbody>
</table>

***

<a name="loio067e2fb0165145a5ac9b128b5853f7c9__section_r5v_3h5_zcb"/>

### Demo Kit Improvements

|**Search Suggestions in Global Search**We’ve improved the global search functionality in the Demo Kit. Now, when you start typing in the search field, you immediately get a popover with the top ten suggestions that match your keyword. From there, you can pick one suggestion and proceed to the specific page.If you’re typing in the search field while the page you're currently on is in one of the main categories \(*API Reference*, *Documentation*, or *Samples*\), the top ten search results only display matches that belong to the same category.To proceed to the page that lists all search results, you can either finish your search by pressing *Enter*, or you can select the *All* button below the top ten search results.At the bottom of the popover, you have the *Results by Category* section from where you can proceed directly to the chosen search results page \(*API Reference*, *Documentation*, or *Samples*\).![](loiob35225c0a6b54b4e98852363ed08a0e8_HiRes.gif)|

