**1.2 Generation / Curation (Collection, Creation, Production, Acquisition, Curation, Ingestion, Storage)**
-------------------------------------------------------------------------------------------------------

<table>
<thead>
<tr class="header">
<th><strong>Requirement</strong></th>
<th><strong>Procedure</strong> [Role - Data Steward (DS) or Data Engineer (DE)]</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>A1.2.1 Ensure complete and accurate ingest of data</td>
<td><p>B1.2.1a Obtain a manifest file from the data provider</p><ul><li><blockquote><p>Each data provider is requested to provide GHGC with a list of files and checksum values to be obtained by GHGC</p></blockquote></li>
<li><blockquote><p>File is placed in the same directory as data to be retrieved, or is sent with files delivered</p></blockquote></li>
<li><blockquote><p>Manifest file is a text document indicating the total number of files followed by file names and checksums, one per filename and checksum value on each line.</p>
</blockquote></li></ul>
<p>B1.2.1b Confirm number of ingested files matches source [DE]</p>
<ul><li><blockquote><p>Part of the GHGC data ingest includes an automated check that the number of delivered or downloaded files match the total number indicated in the manifest file</p>
</blockquote></li>
<li><blockquote><p>Results are provided in the <a href="https://github.com/US-GHG-Center/ghgc-docs/tree/main/processing_and_verification_reports">GHGC Dataset Intake Report</a></p></blockquote></li></ul>
<p>B1.2.1c Perform checksums and confirm match to source [DE]</p>
<ul><li><blockquote><p>GHGC will derive the checksums for each file (delivered or downloaded).</p></blockquote></li>
<li><blockquote><p>Code will be used to compare calculated checksum against value in manifest file
</p></blockquote></li>
<p><li><blockquote>Any code used to move an obtained file within the GHGC system must include recalculation of the checksum and confirmation of matched values.</blockquote></li></p>
<li><blockquote><p>The results and any errors found are provided in the <a href="https://github.com/US-GHG-Center/ghgc-docs/tree/main/processing_and_verification_reports">GHGC Dataset Intake Report</a></p></blockquote></li></ul>
<p>B1.2.1d Generate an ingest report</p>
<ul>
<li><blockquote>
<p>All GHGC data providers will receive a <a href="https://github.com/US-GHG-Center/ghgc-docs/tree/main/processing_and_verification_reports">Dataset Intake Report</a> (Processing and Verification Report) once data ingest is complete</p>
</blockquote></li>
</ul>
<p>B1.2.1e Perform planned data quality checks for the ingested data before sharing (release)</p>
<ul>
<li><blockquote>
<p>All planned quality checks (see B1.1.11) will be performed and shared with the data provider prior to public release. The GHGC will work with the data provider to resolve any issue that arise during quality checking prior to release. 
</p>
</blockquote></li>
</ul>
</td>
</tr>

<tr class="even">
<td>A1.2.2 Ensure complete and accurate production of data</td>
<td><p>B1.2.2a If the GHGC transforms the data or uses the data to create a new merged product of some kind, a file manifest document will be generated and stored with the newly generated data files (contents include total number of files, filenames and checksum file - one filename and checksum per line)
</p>
<p>B1.2.2b All planned quality checks (see B1.1.11) will be performed and shared with the data provider prior to public release. The GHGC will work with the data provider to resolve any issue that arise during quality checking prior to release.</p></td>
</tr>
<tr class="odd">
<td>A1.2.3 Validate that Planning and Design requirements (from Section A1.1) are met for data ingest and / or production</td>
<td>B1.2.3 Perform review demonstrating implementation has met the defined requirements<ul><li><blockquote><p><mark>Action: develop a pre-release checklist</mark></p></blockquote></li></ul></td>
</tr>
<tr class="even">
<td>A1.2.4 Ensure data products are assigned persistent identifiers and cross-referenced if appropriate</td>
<td><p>B1.2.4a The data product overview page on the GHGC website includes a ‘Source Data Product Citation’ section that cites the authoritative data source including its DOI (if available). 
</p><p>B1.2.4b Every data product presented in the GHGC will have a DOI resolving to a data product landing page</p>
<ul>
<li><blockquote>
<p>For data with an existing DOI, the landing page is hosted by the organization providing the data. The dataset overview page in GHGC will contain the existing DOI.</p>
</blockquote></li>
<li><blockquote>
<p>No data will be incorporated into the GHGC until it has a DOI minted by the source agency.
</p>
</blockquote></li>
<li><blockquote>
<p>Transformed data in the GHGC will not be given a new DOI, but will indicate to users the source data product DOI.
</p>
</blockquote></li>

<li><blockquote>
<p>Landing pages must be publicly available at the time of data release in the GHGC.</p>
</blockquote></li>
<li><blockquote>
<p>DOI resolution to source landing page and landing page access will be confirmed once per quarter.</p>
</blockquote></li>
<li><blockquote>
<p>If a unique new dataset is created as part of the GHGC then the GHGC team will be responsible for minting a DOI and supporting a landing page for the DOI to resolve to.</p>
</blockquote></li>
<li><blockquote>
<p>Content of GHGC landing pages must meet the minimal requirements stated in section B1.1.15</p>
</blockquote></li></ul>
<p><mark>For any DOI the GHGC needs to obtain, an approved method will be used (TBD)</mark></p>
<p><mark>What process for obtaining a DOI for this multi-agency project???  Need opinions here</mark></p></td>
</tr>
</tbody>
</table>
