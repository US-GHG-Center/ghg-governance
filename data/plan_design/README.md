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
<td><p>B1.1.1 Data Flow Diagram from the 4 primary providers:</p>
<p><img src="_images/image1.png" style="width:3.10417in;height:1.55556in" /></p>(Draft diagram - to be updated with greater detail)</td>
</tr>
<tr class="even">
<td>A1.1.2 Develop touchpoint agreements identified in the data flow diagram</td>
<td>B1.1.2 Agreements are handled at the HQ level.</td>
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
<td>B1.1.4 <p>The GHGC is collecting data product characteristic information in the following spreadsheet:<a href="https://docs.google.com/spreadsheets/d/199blJH2JBr5eyW-PaH6vCzsj1W8u5AigA4SpjSV04Rc/edit#gid=511491842"><span class="underline"> GHG Center Dataset Information </span></a></p><p>In addition, when working with a new data provider, we use the following form to collect dataset information from the provider: <a href="https://docs.google.com/document/d/1B892eXoiirZsw8rylgejNyw1Zh6Fhg1568EOMGUbWIA/edit"><span class="underline"> GHGC Dataset Intake Form Template </span></a></p></td>
</tr>
<tr class="odd">
<td>A1.1.5 Adhere to community best practice(s) on data file naming conventions</td>
<td>B1.1.5 <p><a href="https://docs.google.com/document/d/18GcGJeJBTzY6UH4F_F6s_c3cmvLuUs2TOwpiVaHwoEs/edit"><span class="underline">GHG Center Naming Conventions</span></a></p><p>We will work with file naming conventions in use unless the file convention used is confusing and poorly communicative. Only if needed, will we change file names of received data. For data we generate (such as transformations of provided data) we will use the following convention:
</p><ul>
<p><li><blockquote><mark>Dataset Shortname = (TBD)</mark></li></p><p><li><blockquote>Long Filename = GHGC_&ltagency&gt_&ltinstr&gt_&ltdate&gt_&ltoptional&gt_&ltversion&gt.ext where:</blockquote></li></p>
<p><ul><li><blockquote>&ltinstr&gt = instrument ID of  up to 10 letters; separated by a “_” from the next field o e.g., avaps, cpl, hamsr, hirad, s-his, hiwrap, … 
<blockquote></li></ul></p>
<p><ul><ul><li><blockquote>Navigation datasets should include the aircraft abbreviation in the instr field (e.g., er2, cit, …)<blockquote></li></ul></ul></p>
<p><ul><li><blockquote>&ltdate&gt = in yyyymmdd format; separated by a “_” from the next field.  Four digit years are required 
<blockquote></li></ul></p>
<p><ul><ul><li><blockquote>If both start and stop dates are required, then separate the two dates by an underscore.<blockquote></li></ul></ul></p>
</ul>
</td>
</tr>
<tr class="even">
<td>A1.1.6 Adhere to community standard variable names, types, and unit(s), keywords</td>
<td><p>B1.1.6 We are working with what the agencies have provided. We need to understand and communicate the variables and units accurately. Any changes would need approval of the providing agency.</p></td>
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
<td>B1.1.8 Utilize map projections from this list (<a href="https://epsg.io/"><span class="underline">https://epsg.io/</span></a>)<ul><li><blockquote>In most cases, we will keep data as sent to us provided the projection is a standard projection. If we need to transform to another projection, we will use WGS84</blockquote></li></ul></td>
</tr>
<tr class="odd">
<td>A1.1.9 Adhere to community standards for date and time formats</td>
<td>B1.1.9 To maximize interoperability of the data received from the various agencies all received data will be converted to a single date/time standard format. The format used will be<a href="https://www.w3.org/TR/NOTE-datetime"><span class="underline"> ISO 8601</span></a> [DE]</td>
</tr>
<tr class="even">
<td>A1.1.10 Define a data product versioning scheme</td>
<td>B1.1.10 <p>The data version in use by the providing agency will be used by GHGC when presenting the data.</p><p>However, there may be cases where no version numbering has been used. In that case we will add V1.0 to the product so that if the data is replaced in the future we have a means to indicate the new version. In our system, decimal numbers indicate minor changes to the product and whole numbers indicate significant product overhaul including algorithm improvements or new data inputs in production.</p></td>
</tr>
<tr class="odd">
<td>A1.1.11 Define a science quality evaluation plan for data products</td>
<td><p>B1.1.11 The GHGC does the following checks to ensure the integrity of the data brought into the system: </p>
<p><blockquote><strong>Data Transfer Confirmation:</strong></blockquote></p><ul>
<p><li><blockquote>Overall checksum report (if used in data transfer
</blockquote></li></p>
<p><li><blockquote>Results from individual checksum file comparisons of pre-transfer and post-transfer</blockquote></li></p>
<p><li><blockquote>Report any individual file issues</blockquote></li></p></ul>
<p><blockquote><strong>Overall Dataset Statistics:</strong></blockquote></p>
<ul>
<p><li><blockquote>Data file reads confirmed</blockquote></li></p>
<p><li><blockquote>Mean, min, max across all files</blockquote></li></p>
<p><li><blockquote>Distribution of values across all data (by variable)</blockquote></li></p>
<p><li><blockquote>What file range (most cases will be all files)</blockquote></li></p>
<p><li><blockquote>Bounding box of all data</blockquote></li></p>
<p><li><blockquote>Link to transformation record in Jupyter Notebook</blockquote></li></p>
<p><li><blockquote>All values are in expected range (catches out of range values)</blockquote></li></p></ul>
<p><blockquote><strong>Visual Confirmation and Random Sample Checking:</strong></blockquote></p><ul>
<p><li><blockquote>Visual example and side by side comparison</blockquote></li></p>
<p><li><blockquote>More detailed statistics for specific files (randomly chose)</li></blockquote></p>
<p><li><blockquote>Data Comparison at a few specific locations</li></blockquote></p>
</blockquote></li></p>
<p>The results of these checks are documented in a Dataset Intake Processing and Verification Report that is shared with the data provider using the following template: <a href="https://docs.google.com/document/d/1Ni-aRIkNwTPTZYZDnZ3Ckg2Ew-nZLCUUN5OepDypc1c/edit"><span class = "underline">GHGC Dataset Intake Report Template</span></a>
Intake reports are also made publicly accessible in the GHGC_docs GitHub repository: <a href="https://github.com/US-GHG-Center/ghgc-docs/tree/main/processing_and_verification_reports"><span class = "underline">https://github.com/US-GHG-Center/ghgc-docs/tree/main/processing_and_verification_reports</span></a></p>
</ul>
</td>
</tr>
<tr class="even">
<td>A1.1.12 Develop a data retention plan including a process for when and how data will be sunset</td>
<td><p>B1.1.12</p>
<p><mark>Action: check with Manil</mark></p>
<p>Maintain for the lifespan of the GHGC or unless the agency requests that the data be retired.</p></td>
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
<td><p>B1.1.13 <mark>Action: Check with Abdelhak on feasibility of these metrics for GHGC. What other metrics do we need? Note: implementing Google Analytics to track website usage metrics. Lets capture what metrics are captured with Google Analytics in a separate doc and link here. Action: document baseline metrics for R1 Document ideal metrics for full release.</mark></p>
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
<p>Metadata completeness</p>
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
<td><p>B1.1.16a API-based data access will be provided for the GHGC via the STAC API.</p>
<p>B1.1.16b The STAC API is fully aligned with <a href="http://docs.opengeospatial.org/is/17-069r3/17-069r3.html"><span class="underline">OGC API-Features</span></a> Version 1.0, and STAC is working to stay aligned as additional OGC API components mature.</p></td>
</tr>
</tbody>
</table>
