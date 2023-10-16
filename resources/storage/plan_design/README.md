**5.1 Planning and Design**
---------------------------

<table>
<thead>
<tr class="header">
<th><strong>Requirement</strong></th>
<th><strong>Procedure</strong> [Role - Data Steward (DS) or Data Engineer (DE)]</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>A5.1.1 Define storage metrics to be collected</td>
<td><p>B5.1.1 The GHGC MSFC team will collect the following storage metrics on a quarterly basis:</p><ul><li><blockquote><p>There are different types</p></blockquote></li><ul>
<li><blockquote><p>Access types:</p></blockquote></li><ul><ul>
<li><blockquote><p>Public</p></blockquote></li>
<li><blockquote><p>Protected</p></blockquote></li>
<li><blockquote><p>Private</p></blockquote></li></ul>
<li><blockquote><p>All storage would not be write access if not part of team or have distinct granule permission for writing.</p></blockquote></li><li><blockquote><p>All storage would be read access by team members and some storage is read access by the public.</p></blockquote></li></ul>
<li><blockquote><p>Storage types (set rules of automatic transition between storage types. Data moves deeper in storage depending on length of time since last access (data lifecycle policy)</p></blockquote></li><ul><ul><li><blockquote><p>Standard access (available always)</p></blockquote></li><ul>
<li><blockquote><p><a href="https://docs.google.com/document/d/1uo0GBsn11n7eHdJPP5aGpZVJoav3gS3YpFnjFa6j3Iw/edit#heading=h.vzwbu8wjjgqi">Pros and cons</a></p></blockquote></li></ul>
<li><blockquote><p>Infrequent access (might be a small latency involved in retrieving the data compared to the standard storage class)
</p></blockquote></li><ul>
<li><blockquote><p><a href="https://docs.google.com/document/d/1uo0GBsn11n7eHdJPP5aGpZVJoav3gS3YpFnjFa6j3Iw/edit#heading=h.90xvueqn2wpl">Pros and cons</a></p></blockquote></li></ul>
<li><blockquote><p>Glacier (require manual restore) - retired data</p></blockquote></li><ul>
<li><blockquote><p><a href="https://docs.google.com/document/d/1uo0GBsn11n7eHdJPP5aGpZVJoav3gS3YpFnjFa6j3Iw/edit#heading=h.oh0i94ed3jje">Pros and cons</a></p></blockquote></li></ul>
<li><blockquote><p>Deep archive</p></blockquote></li><ul>
<li><blockquote><p><a href="https://docs.google.com/document/d/1uo0GBsn11n7eHdJPP5aGpZVJoav3gS3YpFnjFa6j3Iw/edit#heading=h.o6z4fwdsiioy">Pros and cons</a></p></blockquote></li></ul></ul>
<li><blockquote><p>All public, protected and private for GHGC will be standard access</p></blockquote></li>
<li><blockquote><p>All data listed in the GHGC data catalog will remain in standard or infrequent access unless retired or removed from use at which point it is either fully removed from the system or stored in glacier for a period of time and then placed in deep archive</p></blockquote></li></ul></ul><li><blockquote><p>Metrics to be monitored include:</p></blockquote></li><ul>
<li><blockquote><p>Size of storage by storage type</p></blockquote></li>
<li><blockquote><p>Frequency of access by data products and total for project</p></blockquote></li>
<li><blockquote><p>Remaining space vs cost budget comparisons</p></blockquote></li>
<li><blockquote><p>Storage/Access(from where) vs Costs per availability zone (East/West) irrelevant if data stored only in one region</p></blockquote></li>
<li><blockquote><p>Access failure metrics (200, 300, 400, 500)</p></blockquote></li></ul></ul></td>
</tr>
<tr class="even">
<td>A5.1.2 Develop storage and egress cost estimates</td>
<td><p>B5.1.2 Use data sheet (B1.1.4) to generate storage and egress <a href="https://www.cloudysave.com/aws/cost-calculator/"><span class="underline">costs using this calculator</span></a>. Costs to consider include total product size, whether redundant storage for operations and backup/archive are require], projected growth, and estimated use[DE]</p>
<ul>
<li><blockquote>
<p><a href="https://drive.google.com/file/d/1mLtWKImjQQixeZOWl0SVx7BkA_KXxBox/view?usp=share_link"><span class="underline">ESDIS template</span></a> [ who fills this out?  Is this just for GHGC costing or IMPACT wide?]</p>
</blockquote></li>
<li><blockquote><p>What is the protocol used to access the data (affects cost projections)?</p></blockquote></li>
</ul></td>
</tr>
<tr class="odd">
<td>A5.1.3 Define the S3 Bucket structure including the naming convention, tagging, logs, etc.</td>
<td>B5.1.3 Adopt <a href="https://docs.google.com/document/d/16oStNf6eRKFUjH5D11a4Vwxsn24a4TVr8HRLIqruHTU/edit"><span class="underline">these best practices</span></a> for key aspects of cloud storage [DS + DE]<ul><li><blockquote><p>For GHGC we use S3 storage and RDS storage [need what this is]</p></blockquote></li></ul></td>
</tr>
<tr class="even">
<td>A5.1.4 Define data storage environments needed such as sandbox, development, staging, production (operational + backup copies)</td>
<td><p>B5.1.4 Recommend creating a minimum of three storage environments - sandbox, development/staging and production:</p><ul><li><blockquote><p>Development (UAH)</p></blockquote></li>
<li><blockquote><p>Staging (SMC)</p></blockquote></li>
<li><blockquote><p>Production (MCP)</p></blockquote></li></ul>
<p>All 3 are located in 3 different AWS accounts.</p></td>
</tr>
<tr class="odd">
<td>A5.1.5 Define storage policy for retention including the rules for defining which storage class to use and when the storage class should be changed</td>
<td><p>B5.1.5 For a rolling archive with capped storage capacity, use information in the <a href="https://docs.google.com/document/d/16oStNf6eRKFUjH5D11a4Vwxsn24a4TVr8HRLIqruHTU/edit"><span class="underline">best practices document</span></a>. [DE]</p>
<ul>
<li><blockquote>
<p>If selected metrics show that the usage for a dataset is below a threshold, then the dataset should be moved to cold storage or deleted</p>
</blockquote></li>
<li><blockquote>
<p>Storage class can be changed manually (s3 cli) or by setting bucket specific rules. These rules or changes should be cost based (or time based) - need to determine at what usage it becomes more costly to store and retrieve from “colder” storage class versus keeping data in “warmer class” (i.e. &lt;~40% of total dataset egress it becomes cheaper to use IA vs standard storage)</p>
</blockquote></li>
</ul></td>
</tr>
<tr class="even">
<td>A5.1.6 Define storage policy for retiring data</td>
<td>B5.1.6 The retired dataset should be moved to cold storage or deleted [<a href="https://docs.google.com/document/d/1cmqX_CMLQyCtpB3nMyEOyKear4BmYPvtK6SZfjqhM74/edit?pli=1"><span class="underline">draft CSDA retirement document</span></a> [DE]</td>
</tr>
</tbody>
</table>
