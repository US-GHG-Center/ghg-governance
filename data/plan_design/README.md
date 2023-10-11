**1.1 Planning and Design**
-----------------------

<table>
<thead>
<tr class="header">
<th><strong>Requirement</strong></th>
<th><strong>Procedure</strong> [Role - Data Steward (DS) or Data Engineer (DE)]</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>A1.1.1 Define a data flow diagram with the purpose of identifying data sources and touchpoints for the project and for communicating to data users how data was handled.</td>
<td><p>B1.1.1 Create a data flow diagram extending from acquisition/creation to user delivery and add diagram to DMP. [DE]</p>
<p>Example diagram: <img src="_images/image1.png" style="width:3.10417in;height:1.55556in" /></p></td>
</tr>
<tr class="even">
<td>A1.1.2 Develop touchpoint agreements identified in the data flow diagram</td>
<td>B1.1.2 Create needed touchpoint agreements such as <a href="https://docs.google.com/document/d/1hTrdT2v_D8ThWRjwsVUE_blSNmbwjF2cZrlEltX0gtU/edit"><span class="underline">Interface Control Documents, (ICDs) </span></a> / Submission Agreement (SA), <a href="https://docs.google.com/document/d/12oEjLFqsEsPElqDlEzsW_Km8v4ozuvSd3mckLScGQ7g/edit"><span class="underline">Memorandum of Understanding (MOU)</span></a> or Service Level Agreement (SLA) [DS + DE]</td>
</tr>
<tr class="odd">
<td>A1.1.3 Adhere to community accepted standard machine readable data file formats</td>
<td><p>B1.1.3 GHGC Use Case 1:</p>
<ul>
<li><blockquote>
<p>EPA Methane data delivered in NetCDF</p>
</blockquote></li>
<p>GHGC Use Case 2:</p>
<li><blockquote>
<p>Gridded CO2 data (format TBD)</p>
</blockquote></li>
<p>GHGC Use Case 3:</p>
<li><blockquote>
<p>Methane plume data from JPL delivered in COG</p>
</blockquote></li>
</ul>
<p>All data ingested into the GHGC system will be transformed into Cloud Optimized GeoTIFF (COG) format which is listed as an emerging standard.</p></td>
</tr>
<tr class="even">
<td>A1.1.4 Identify and document all data product characteristics</td>
<td>B1.1.4 <blockquote><li><p>The GHGC is collecting data product characteristic information in the following spreadsheet:<a href="https://docs.google.com/spreadsheets/d/199blJH2JBr5eyW-PaH6vCzsj1W8u5AigA4SpjSV04Rc/edit#gid=511491842"><span class="underline"> GHG Center Dataset Information </span></a></blockquote></li></p><p><blockquote><li>In addition, when working with a new data provider, we use the following form to collect dataset information from the provider: <a href="https://docs.google.com/document/d/1B892eXoiirZsw8rylgejNyw1Zh6Fhg1568EOMGUbWIA/edit"><span class="underline"> GHGC Dataset Intake Form Template </span></a></blockquote></li></p>
 [DS]</td>
</tr>
<tr class="odd">
<td>A1.1.5 Adhere to community best practice(s) on data file naming conventions</td>
<td>B1.1.5 <blockquote><li><a href="https://docs.google.com/document/d/18GcGJeJBTzY6UH4F_F6s_c3cmvLuUs2TOwpiVaHwoEs/edit"><span class="underline">GHG Center Naming Conventions</span></a></blockquote></li>[DS]</td>
</tr>
<tr class="even">
<td>A1.1.6 Adhere to community standard variable names, types, and unit(s), keywords</td>
<td>B1.1.6 Utilize standard variable(s), types, and unit(s) such as <a href="http://cfconventions.org/"><span class="underline">CF convention</span> <span class="underline"></span></a>,<blockquote><li>We are working with what the agencies have provided. We need to understand and communicate the variables and units accurately. Any changes would need approval of the providing agency. 
</li></blockquote>[DS]</td>
</tr>
<tr class="odd">
<td>A1.1.7 Adhere to community standards for coordinate systems</td>
<td><p>B1.1.7 Utilize coordinate reference systems (CRS) from this list (<a href="https://epsg.io/"><span class="underline">https://epsg.io/</span></a>) [DE]</p>
<ul>
<li><blockquote>
<p>Recommended global CRS:</p>
</blockquote>
<ul>
<li><blockquote>
<p>2-dimensional World Geodetic System 1984 (WGS 84) (Lat/Long): <a href="https://epsg.io/4326"><span class="underline">EPSG:4326</span></a></p>
</blockquote>
<ul>
<li><blockquote>
<p>WGS 84 World Mercator: <a href="https://epsg.io/3395"><span class="underline">EPSG:3395</span></a></p>
</blockquote></li>
<li><blockquote>
<p>WGS 84 Pseudo-Mercator: <a href="https://epsg.io/3857"><span class="underline">EPSG:3857</span></a></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>3-dimensional WGS 84 (Lat/Long/Elevation)<span class="underline">:</span> <a href="https://epsg.io/4979"><span class="underline">EPSG:4979</span></a></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Recommended CRS for data over polar regions:</p>
</blockquote>
<ul>
<li><blockquote>
<p>WGS 84 Arctic Polar Stereographic: <a href="https://epsg.io/3995"><span class="underline">EPSG:3995</span></a></p>
</blockquote>
<ul>
<li><blockquote>
<p>NSIDC Sea Ice Polar Stereographic North: <a href="https://epsg.io/3413"><span class="underline">EPSG:3413</span></a></p>
</blockquote></li>
<li><blockquote>
<p>NSIDC Sea Ice Polar Stereographic South: <a href="https://epsg.io/3976"><span class="underline">EPSG:3976</span></a></p>
</blockquote></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>A1.1.8 Adhere to community standards for map projections</td>
<td>B1.1.8 Utilize map projections from this list (<a href="https://epsg.io/"><span class="underline">https://epsg.io/</span></a>)<blockquote><li>In most cases, we will keep data as sent to us provided the projection is a standard projection. If we need to transform to another projection, we will use WGS84
</li></blockquote>[DE]</td>
</tr>
<tr class="odd">
<td>A1.1.9 Adhere to community standards for date and time formats</td>
<td>B1.1.9 To maximize interoperability of the data received from the various agencies all received data will be converted to a single date/time standard format. The format used will be<a href="https://www.w3.org/TR/NOTE-datetime"><span class="underline"> ISO 8601</span></a> [DE]</td>
</tr>
<tr class="even">
<td>A1.1.10 Define a data product versioning scheme</td>
<td>B1.1.10 <p><blockquote><li>The data version in use by the providing agency will be used by GHGC when presenting the data</li></blockquote></p><p><blockquote><li>However, there may be cases where no version numbering has been used. In that case we will add V1.0 to the product so that if the data is replaced in the future we have a means to indicate the new version. In our system, decimal numbers indicate minor changes to the product and whole numbers indicate significant product overhaul including algorithm improvements or new data inputs in production.</li></blockquote></p>[DE]</td>
</tr>
<tr class="odd">
<td>A1.1.11 Define a science quality evaluation plan for data products</td>
<td><p>B1.1.11 Develop the characteristics of the science quality evaluation needed for each data product [DS]</p>
<p>Suggested:</p>
<ul>
<li><blockquote>
<p>Univariate visualization of each field in the raw dataset, with summary statistics and Fill Values, Mask Values</p>
</blockquote></li>
</ul></td>
</tr>
<tr class="even">
<td>A1.1.12 Develop a data retention plan including a process for when and how data will be sunset</td>
<td>B1.1.12 Create a data retention plan that includes information about the end of project preservation plan and rolling archive plans. Use the <a href="https://docs.google.com/document/d/1nWOkkKoICDhb9VWcZF7cvp31pjtZyRP1VM3wqNj4HHo/edit"><span class="underline">CSDA data retirement policy template</span></a> as needed. [DS]</td>
</tr>
<tr class="odd">
<td><p>A.1.1.13 Define metrics to be collected along the following dimensions:</p>
<ul>
<li><blockquote>
<p>Data use (search and access)</p>
</blockquote></li>
<li><blockquote>
<p>Data quality</p>
</blockquote></li>
<li><blockquote>
<p>Data/information (quality) profile</p>
</blockquote></li>
<li><blockquote>
<p>Data Processing</p>
</blockquote></li>
<li><blockquote>
<p>Ingest</p>
</blockquote></li>
<li><blockquote>
<p>Data Access APIs/Services</p>
</blockquote></li>
</ul></td>
<td><p>B1.1.13 Develop a metrics implementation plan. [DE]</p>
<p>Recommended minimum metrics:</p>
<blockquote>
<p><strong>Data Use Metrics</strong></p>
</blockquote>
<ul>
<li><blockquote>
<p>Data Product Search frequency</p>
</blockquote></li>
<li><blockquote>
<p>S3 Bucket Access frequency</p>
</blockquote></li>
<li><blockquote>
<p>Data download counts</p>
</blockquote></li>
</ul>
<blockquote>
<p><strong>Information/Data Profile</strong>:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Data completeness</p>
</blockquote></li>
<li><blockquote>
<p>Metadata completeness</p>
</blockquote></li>
<li><blockquote>
<p>Data lineage completeness</p>
</blockquote></li>
</ul>
<blockquote>
<p><strong>Data Quality</strong></p>
</blockquote>
<ul>
<li><blockquote>
<p>Checksum validation</p>
</blockquote></li>
</ul>
<blockquote>
<p><strong>Data Processing</strong></p>
</blockquote>
<ul>
<li><blockquote>
<p>Processing time</p>
</blockquote></li>
<li><blockquote>
<p>Processing throughput</p>
</blockquote></li>
<li><blockquote>
<p>Error rate</p>
</blockquote></li>
<li><blockquote>
<p>Resource utilization</p>
</blockquote></li>
</ul>
<blockquote>
<p><strong>Ingest</strong>:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Ingest rate</p>
</blockquote></li>
<li><blockquote>
<p>Ingest completeness / volume</p>
</blockquote></li>
<li><blockquote>
<p>Ingest error rate</p>
</blockquote></li>
</ul>
<blockquote>
<p><strong>Data Access APIs/Services</strong>:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Service availability</p>
</blockquote></li>
<li><blockquote>
<p>Service usage</p>
</blockquote></li>
<li><blockquote>
<p>Service response time</p>
</blockquote></li>
<li><blockquote>
<p>Service error rate</p>
</blockquote></li>
</ul></td>
</tr>
<tr class="even">
<td>A1.1.14 Identify the most appropriate data license for the data product</td>
<td>B1.1.14 If there are no other restrictions, SMD scientific data should be released with a Creative Commons Zero license. [DS]</td>
</tr>
<tr class="odd">
<td>A1.1.15 Determine content and format for the dataset landing page</td>
<td><p>B1.1.15 Design dataset landing page format and content. Recommend using the <a href="https://docs.google.com/document/d/1qEoqYMh6K0QjY4HFqJ55yinwn4u0s22j88IAED583_U/edit?usp=sharing"><span class="underline">IMPACT data product landing page design</span></a>. [DS]</p>
<p>Note that dataset landing pages can be automatically generated using UMM metadata (published to CMR) and STAC metadata (using STAC Browser). All information needed in the dataset landing page should be included in the metadata.</p></td>
</tr>
<tr class="even">
<td>A1.1.16 Determine whether API-based data access is needed &amp; if so, identify an API standard</td>
<td><p>B1.1.16a </p><p><blockquote><li>API-based data access will be provided for the GHGC via the STAC API.</li></blockquote></p>
<p>B1.1.16</p><p><blockquote><li>The STAC API is fully aligned with <a href="http://docs.opengeospatial.org/is/17-069r3/17-069r3.html"><span class="underline">OGC API-Features</span></a> Version 1.0, and STAC is working to stay aligned as additional OGC API components mature.</li></blockquote></p></td>
</tr>
</tbody>
</table>
