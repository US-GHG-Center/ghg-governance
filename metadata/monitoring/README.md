**2.6 Monitoring**
------------------

<table>
<thead>
<tr class="header">
<th><strong>Requirement</strong></th>
<th><strong>Procedure</strong> [Role - Data Steward (DS) or Data Engineer (DE)]</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>A2.6.1 Monitor and report metadata quality metrics</td>
<td>B2.6.1 Use <a href="https://github.com/NASA-IMPACT/pyQuARC"><span class="underline">pyQuARC</span></a> to generate metadata quality metrics. <a href="https://quarc.nasa-impact.net/docs/#/default/post_validate"><span class="underline">QuARC is also available via an API.</span></a>
<ul><li><blockquote><p>pyQuARC doesn’t work on STAC, but can be modified to support it. Currently for GHGC, a manual process is followed where the information provided by the data provider will be verified against the data and the information provided on the website. <mark>Action: see if there are any out of the box STAC quality checkers we can implement. </mark></blockquote></li><li><blockquote>
</p><p>The GHGC team will utilize the <a href = "https://github.com/radiantearth/stac-spec/blob/master/best-practices.md">STAC best practices</a> document in STAC development </p></blockquote></li></ul></td>
</tr>
<tr class="even">
<td>A2.6.2 Monitor changes to the metadata schema used</td>
<td><p>B2.6.2a The STAC schema Version 1.0.0 is currently used. This is the latest version.</p><ul><Li><blockquote><p>Checks for new STAC schema updates will be made on a semi-annual basis.</p></blockquote></li><li><blockquote><p>STAC release updates can be tracked here:<a href="https://github.com/radiantearth/stac-spec/releases">https://github.com/radiantearth/stac-spec/releases</a></blockquote></li></p></ul>
<p>B2.6.2b</p><p> The work needed to update all existing STAC records will be assessed and balanced against the STAC schema changes. Highly relevant changes will be implemented.</p><p>Existing STAC collections will be updated per a reasonable update plan (timeframe TBD based on needed changes).</p></td>
</tr>
<tr class="odd">
<td>A2.6.3 Monitor changes to controlled vocabularies</td>
<td><p>B2.6.3a Update controlled vocabulary keywords in metadata (e.g., GCMD; CF);</p><ul><li><blockquote><p>Partner names and ‘thematics’ (sector) are controlled vocabulary lists that the GHGC maintains internally at this time for the purposes of display and sorting on the website.</p></blockquote></li><li><blockquote><p>No external controlled vocabulary services are in use at the time of this document creation.
</p></blockquote></li><li><blockquote><p>The GCMD provider and science keywords controlled vocabulary may be implemented later in the project (after initial delivery).
</p></blockquote></li>
<li><blockquote><p>Monitoring of GCMD notifications will identify changes relevant to these two controlled lists.</p></blockquote></li>
<li><blockquote><p>New providers or science keywords that need to be added to GCMD will result in requests to the <a href = "https://forum.earthdata.nasa.gov/viewforum.php?f=7&&ServicesUsage=101&sid=66de578517225efc4ff40567515b3621">keyword community forum.</a></p></blockquote></li></ul>
<p>B2.6.3b Remove deprecated keywords, as needed</p>
<ul><li><blockquote><p>Monitoring of GCMD notifications will identify deprecated keywords relevant to provider and science keyword controlled lists, once implemented.</p></blockquote></li>
<li><blockquote><p>Any deprecated keywords will be removed and replaced as needed from the STAC record or from use in the interface.</p></blockquote></li>
</ul></td>
</tr>
</tbody>
</table>
