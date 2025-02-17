**1.3 Data Sharing**
----------------

<table>
<thead>
<tr class="header">
<th><strong>Requirement</strong></th>
<th><strong>Procedure</strong> [Role - Data Steward (DS) or Data Engineer (DE)]</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
    A1.3.1 Ensure data product identifiers are resolvable
</td>
<td><p>B1.3.1a The persistent identifier should resolve to the appropriate dataset landing page (see A3.1.1)</p>
<ul><li><blockquote><p>The GHGC team will check that DOI for the source data product provided on the data product overview page works and resolves to the original dataset landing page. If there is any issue resolving the DOI, it will be reported to the data provider. 
</p></li></blockquote><li><blockquote><p>For new DOIs generated by the GHGC, the resolution of the DOI to the landing page will be confirmed quarterly.</p></blockquote></li>
</ul>
<p>B1.3.1b The landing page should use RDFa – lite semantic annotations (<a href="https://www.w3.org/TR/rdfa-lite/"><span class="underline">https://www.w3.org/TR/rdfa-lite/</span></a>) [DE]</p>
<p><mark>TBD</mark></p></td>
</tr>
<tr class="even">
<td>A1.3.2 Ensure policy-based access to data</td>
<td>B1.3.2 <p>No end user license agreement is needed for data access or use for government generated data. If the GHGC incorporates data from other sources at a future time, the need for license agreements will be addressed then.
</p><p>To meet the requirements of <a href="https://science.nasa.gov/science-red/s3fs-public/atoms/files/SMD-information-policy-SPD-41a.pdf"><span class="underline">SPD-41a</span></a>, all NASA data is openly available.</p></td>
</tr>
<tr class="odd">
<td>A1.3.3 Ensure all shared data products are self-describing with sufficient structural metadata for data use</td>
<td>B1.3.3 Use well defined conventions, such as <a href="https://urs.earthdata.nasa.gov/oauth/authorize?client_id=u1o_8zOuolqNjuLQz6wzYQ&response_type=code&redirect_uri=https%3A%2F%2Fwiki.earthdata.nasa.gov%2Fplugins%2Fservlet%2FConfluenceOAuth2&state=%2Fdisplay%2FESDSWG%2FTemplate%2Bfor%2BCF%2B%28Climate-Forecast%29%2BCompliance"><span class="underline">Climate Forecast (CF)</span></a> for netCDF and HDF files.<ul><li><blockquote><p>All data currently ingested into the GHGC data system are transformed into Cloud Optimized GeoTIFF (COG): <a href="https://www.cogeo.org/">https://www.cogeo.org/</a></p></blockquote></li><li><blockquote><p><mark>add info about COG conventions/best practices the dev team implements for COG. E.g. is the file structure tested? <a href="https://www.cogeo.org/developers-guide.html">https://www.cogeo.org/developers-guide.html</a></marl></p></blockquote></li>
</ul>
</td>
</tr>
<tr class="even">
<td>A1.3.4 Ensure all data product files are accessible (user registration may be required)</td>
<td><p>B1.3.4a Check that data access links are working [DE]</p><ul><li><blockquote><p>Team will develop code to confirm the data product access link correctly resolves to the data product files. A report will be produced by the code to identify success or failure for each check and a summary for each operation. The code will be run monthly.</p></blockquote></li></ul>
<p>B1.3.4b Check that data access APIs are working</p><ul><li><blockquote><p>The code developed for B1.3.4a can be used to also identify whether the API is working to access the data products. The summary of API checks can be placed in the same report and should be run monthly.</p></blockquote></li></ul>
<p>B1.3.4c Implement <a href="https://https.cio.gov/"><span class="underline">secure</span></a> transfer protocol access in compliance with U.S. government policy</p><ul><li><blockquote><p><mark>The GHGC will only utilize https protocol in compliance with government policy for data and information access. (s3?)</mark></p></blockquote></li></ul></td>
</tr>
<tr class="odd">
<td>A1.3.5 Ensure checksum and manifest file is available to users (for users to verify downloaded files)</td>
<td>B1.3.5<p>The GHGC will ensure there is a manifest file containing file name, checksum and total number of files placed in the same location as the data files. This will be done by the same code that performs checks for 1.3.4a and 1.3.4b and at the same cadence.<mark>Need to follow up to see if there are plans to do this</mark></p></td>
</tr>
</tbody>
</table>
