**2.2 Generation / Curation**
-----------------------------

<table>
<thead>
<tr class="header">
<th><strong>Requirement</strong></th>
<th><strong>Procedure</strong> [Role - Data Steward (DS) or Data Engineer (DE)]</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>A2.2.1 Provide the metadata specification information in the collection level metadata</td>
<td><p>B2.2.1 The STAC 'type' element is required and is included in all GHGC STAC Collection records.</p></td>
</tr>
<tr class="even">
<td>A2.2.2 Provide the data product title in the collection level metadata</td>
<td><p>B2.2.2 The dataset title provided by the agency or approved by the agency is provided in the STAC 'title' element.</p></td>
</tr>
<tr class="odd">
<td>A2.2.3 Provide the DOI information in the collection level metadata</td>
<td><p>B2.2.3 STAC: Leverage the <a href="https://github.com/stac-extensions/scientific"><span class="underline">Scientific Citation Extension Specification</span></a> and the ‘sci:doi’ element within that specification. This element is meant to contain the DOI value of the data, e.g. 10.1000/xyz123. This MUST NOT be a DOI link.</p>
<ul><li><blockquote><p><mark>TBD: ‘sci:doi’ is not yet implemented in the GHGC STAC metadata</mark></p></blcokquote></li></ul></td>
</tr>
<tr class="even">
<td>A2.2.4 Provide the abstract information in the collection level metadata</td>
<td><p>B2.2.4 STAC: Include the abstract, or dataset description, in the ‘description’ element for the collection specification.</p><ul><li><blockquote><p></p></blcokquote></li></ul></td>
</tr>
<tr class="odd">
<td>A2.2.5 Provide information on the organization responsible for originating, processing, archiving, and/or distributing the dataset in the collection level metadata</td>
<td><p>B2.2.5 The GHGC is currently maintaining an internal customized list of data providers to be populated in the STAC ‘name’ and ‘role’ field. Longer term, the plan is to transition to using GCMD provider keywords in the ‘name’ element.</p>
</td>
</tr>
<tr class="even">
<td>A2.2.6 Provide the data processing level in the collection level metadata</td>
<td><p>B2.2.6 STAC: Provide the processing level using the ‘processing:level’ element using the processing extension (<a href="https://github.com/stac-extensions/processing"><span class="underline">https://github.com/stac-extensions/processing</span></a>) for Collections.</p><ul><li><blockquote><p><mark>TBD - ‘processing:level’ is not yet implemented in the GHGC STAC metadata</mark></p></blockquote></li></ul></td>
</tr>
<tr class="odd">
<td>A2.2.7 Provide the data product production status in the collection level metadata</td>
<td><p>B2.2.7 TBD: STAC: The best practice for providing the collection progress using the STAC Collection spec is still TBD. <mark>TBD.</mark></p></td>
</tr>
<tr class="even">
<td>A2.2.8 Provide science keywords applicable to the data product in the collection level metadata</td>
<td><p>B2.2.8 STAC: The ‘keywords’ element in the Collection specification should be used to provide science keywords. Science keywords should be selected from the <a href="https://www.earthdata.nasa.gov/learn/find-data/idn/gcmd-keywords"><span class="underline">GCMD science keywords list.</span></a></p>
<p><mark>TBD: 'keywords’ is not currently being implemented in the GHGC STAC. Long term the plan is to start populating GCMD science keywords in the ’keywords’ element.</mark></p></td>
</tr>
<tr class="odd">
<td>A2.2.9 Provide the temporal extent of the data in the collection level metadata</td>
<td><p>B2.2.9 STAC: The temporal information should be provided in the Extent Object -&gt; <a href="https://github.com/radiantearth/stac-api-spec/blob/main/stac-spec/collection-spec/collection-spec.md#temporal-extent-object"><span class="underline">Temporal Extent Object</span></a>. If the data has an open range (e.g. active/ongoing collection), this can be specified by setting the start and/or end time to “null”. For example, [[&quot;2019-01-01T00:00:00Z&quot;, null]]. Timestamps should consist of a date and time in UTC and MUST be formatted according to <a href="https://datatracker.ietf.org/doc/html/rfc3339#section-5.6"><span class="underline">RFC 3339, section 5.6</span></a>. The temporal reference system is the Gregorian calendar. [DS + DE]</p><ul><li><blockquote><p>The Extent Object is provided as described above in all GHGC STAC Collection records. The temporal extent is unique to each data product and is validated against the data files.  
</p></blockquote></li></ul></td>
</tr>
<tr class="even">
<td>A2.2.10 Provide the spatial extent of the data in the collection level metadata</td>
<td><p>B2.2.10 STAC: The spatial information should be provided in the Extent Object -&gt; <a href="https://github.com/radiantearth/stac-api-spec/blob/main/stac-spec/collection-spec/collection-spec.md#spatial-extent-object"><span class="underline">Spatial Extent Object</span></a>. The first bounding box always describes the overall spatial extent of the data. All subsequent bounding boxes can be used to provide a more precise description of the extent and identify clusters of data. The coordinate reference system of the values is WGS 84 longitude/latitude.</p><ul><li><blockquote><p>The Extent Object is provided as described above in all GHGC STAC Collection records. The spatial extent is unique to each data product and is validated against the data files</p></blockquote></li></ul></td>
</tr>
<tr class="odd">
<td>A2.2.11 Provide the platform information (and optionally, instrument information) in the collection level metadata</td>
<td><p>B2.2.11 TBD: STAC: Provide platform and optionally instrument information using the ‘summaries’ element in the Collection spec. Instructions on how to appropriately do this is TBD (example: <a href="https://github.com/radiantearth/stac-spec/blob/master/examples/collection.json#L45"><span class="underline">https://github.com/radiantearth/stac-spec/blob/master/examples/collection.json#L45</span></a>)</p><p><mark>TBD.</mark></p></td>
</tr>
<tr class="even">
<td>A2.2.12 Provide resource related URLs in the collection level metadata</td>
<td><p>B2.2.12 STAC: Provide links to all relevant information in the <a href="https://github.com/radiantearth/stac-api-spec/blob/main/stac-spec/collection-spec/collection-spec.md#link-object"><span class="underline">Link Object</span></a> -&gt; ‘href’ and ‘rel’ elements. Provide the actual link in the ‘href’ element. The ‘ref’ element describes the relationship between the collection and the URL. More information on relationships can be <a href="https://github.com/radiantearth/stac-spec/blob/master/collection-spec/collection-spec.md#relation-types"><span class="underline">found here.</span></a></p>
<ul><li><blockquote><p>Links to associated STAC records (specifically the related ‘items’, ‘parent’, ‘root’, and a link to ‘self’) are provided in all GHGC STAC Collection records. <mark>Providing links to any additional resources (beyond related STAC records) is still TBD.</mark></p></blockquote></li></ul></td>
</tr>
<tr class="odd">
<td>A2.2.13 Provide a unique identifier for the data product in the collection level metadata</td>
<td><p>B2.2.13 A unique identifier is provided in the ‘id’ field for each GHGC STAC Collection. The id follows the naming convention specified in B1.1.5.</p></td>
</tr>
<tr class="even">
<td>A2.2.14 Provide the data product version in the collection level metadata</td>
<td>
<p>B2.2.14 TBD: STAC: The best practice for providing the data product version using the STAC Collection spec.</p><p><mark>TBD</mark></p></td>
</tr>
<tr class="odd">
<td>A2.2.15 Provide the data product license information in the collection level metadata</td>
<td>
<p>B2.2.15 STAC: Provide the license using the ‘license’ element. The license should be selected from the SPDX License identifier list: <a href="https://spdx.org/licenses/"><span class="underline">https://spdx.org/licenses/</span></a>. Provide “varies” if multiple licenses apply and “proprietary” for all other cases. The default value for an open license should be “CC0-1.0” unless otherwise specified. [DS + DE]</p><ul><li><blockquote><p>As part of the data intake process, the data provider is asked to specify the license applied to the dataset. The corresponding license identifier is provided in the ‘license’ field. 
</p></blockquote></li></ul></td>
</tr>
<tr class="even">
<td>A2.2.16 Provide a unique identifier in the granule level metadata</td>
<td><p>B2.2.16 A unique identifier is provided in the ‘id’ field for each GHGC STAC Item. The id follows the naming convention specified in B1.1.5.</p></blockquote></li></ul></td>
</tr>
<tr class="odd">
<td>A2.2.17 Provide a date indicating when the granule metadata was created in the granule level metadata</td>
<td><p>B2.2.17 STAC: Provide the date the Item record was created using ‘properties &gt; created’ <a href="https://github.com/radiantearth/stac-api-spec/blob/main/stac-spec/item-spec/common-metadata.md#date-and-time"><span class="underline">https://github.com/radiantearth/stac-api-spec/blob/main/stac-spec/item-spec/common-metadata.md#date-and-time</span></a></p><ul><li><blockquote><p><mark>TBD: ‘properties > created’ is not currently being implemented in the GHGC STAC.</mark></p></blockquote></li></ul></td>
</tr>
<tr class="even">
<td>A2.2.18 Provide a reference to the associated collection in the granule level metadata</td>
<td>
<p>B2.2.18 The ‘collection’ element is provided in all GHGC STAC Item records.</p></td>
</tr>
<tr class="odd">
<td>A2.2.19 Provide the metadata specification information in the granule level metadata</td>
<td>
<p>B2.2.19 Provide a value of “Feature” in the STAC ‘type’ element and the version of STAC the Item implements in the ‘stac_version’ element.</p><ul><li><blockquote><p>The ‘type’ and ‘stac_version’ elements are provided in all GHGC STAC Item records.</p></blockquote></li></ul></td>
</tr>
<tr class="even">
<td>A2.2.20 Provide the temporal extent information in the granule level metadata</td>
<td><p>B2.2.20 STAC: The temporal information should be provided in the <a href="https://github.com/radiantearth/stac-spec/blob/master/item-spec/item-spec.md#properties-object"><span class="underline">Properties Object</span></a> -&gt; ‘datetime’ element. If the file can be represented as a single datetime, the time stamp can be provided directly in the ‘datetime’ element. If the temporal extent is a temporal range, then a value of “null” should be provided in ‘datetime’ followed by the ‘start_datetime’ and ‘end_datetime’ elements. Timestamps should consist of a date and time in UTC and MUST be formatted according to <a href="https://datatracker.ietf.org/doc/html/rfc3339#section-5.6"><span class="underline">RFC 3339, section 5.6</span></a>.</p></p><ul><li><blockquote><p>Start and stop datetimes representing the temporal extent of each data file is provided in each GHGC STAC Item record.</p></blockquote></li></ul></td>
</tr>
<tr class="odd">
<td>A2.2.21 Provide the spatial extent information in the granule level metadata</td>
<td><p>B2.2.21 STAC: The spatial information should be provided using either the ‘geometry’ element or the ‘bbox’ element. Use ‘geometry’ to provide a GeoJSON footprint, formatted according to <a href="https://tools.ietf.org/html/rfc7946#section-3.1">RFC 7946, section 3.1</a>. The footprint should be the default GeoJSON geometry, though additional geometries can be included. Coordinates are specified in Longitude/Latitude or Longitude/Latitude/Elevation based on <a href="http://www.opengis.net/def/crs/OGC/1.3/CRS84">WGS 84</a>. If ‘geometry’ is set to “null”, then providing a ‘bbox’ is required. The bbox should be formatted according to <a href="https://tools.ietf.org/html/rfc7946#section-5">RFC 7946, section 5</a>. <ul><li><blockquote><p>The ‘geometry’ element is used to represent the spatial extent of each data file in each GHGC STAC Item record.</p></blockquote></li></ul></p></td>
</tr>
<tr class="even">
<td>A2.2.22 Provide a link to access the data in the granule level metadata</td>
<td><p>B2.2.22 STAC: There are two required STAC elements to consider here. First is the ‘links’ element which is a list of <a href="https://github.com/radiantearth/stac-spec/blob/master/item-spec/item-spec.md#link-object"><span class="underline">Link Objects</span></a> to resources and related URLs. At minimum, a link with the ‘rel’ set to “self” is strongly recommended. It is encouraged that links pointing to other related STAC resources are also provided, such as a link to the associated collection and root or parent entity. Additional information can be found here: <a href="https://github.com/radiantearth/stac-spec/blob/master/item-spec/item-spec.md#link-object"><span class="underline">Link Object</span></a>. The second is the ‘assets’ element which is a dictionary of <a href="https://github.com/radiantearth/stac-spec/blob/master/item-spec/item-spec.md#asset-object"><span class="underline">Asset Objects</span></a> that can be downloaded, each with a unique key. This element is key to facilitating data access, as it contains a URI to data associated with the Item that can be downloaded or streamed. Details can be found here: <a href="https://github.com/radiantearth/stac-spec/blob/master/item-spec/item-spec.md#asset-object"><span class="underline">Asset Object</span></a></p><ul><li><blockquote><p>GHGC makes use of the 'assets' object to provide the S3 location link for each data file.</p></blockquote></li></ul></td>
</tr>
<tr class="odd">
<td>A2.2.23 Preserve data provenance (preserve metadata from original source, and data editing history)</td>
<td>
<p>B2.2.23 <mark>TBD</mark>: STAC Implementation procedure for data provenance</p></td>
</tr>
</tbody>
</table>
