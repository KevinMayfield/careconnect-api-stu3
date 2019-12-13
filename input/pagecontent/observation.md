
### Search Parameters

<table style="min-width:100%;width:100%">
<tr id="clinical">
    <th style="width:15%;">Name</th>
    <th style="width:15%;">Type</th>
    <th style="width:40%;">Description</th>
    <th style="width:5%;">Conformance</th>
    <th style="width:25%;">Path</th>
</tr>
<tr>
    <td><code class="highlighter-rouge">category</code></td>
    <td><code class="highlighter-rouge">token</code></td>
    <td>The classification of the type of observation</td>
    <td>SHOULD</td>
    <td>Observation.category</td>
</tr>
<tr>
    <td><code class="highlighter-rouge">code</code></td>
    <td><code class="highlighter-rouge">token</code></td>
    <td>The code of the observation type</td>
    <td>SHOULD</td>
    <td>Observation.code</td>
</tr>
<tr>
    <td><code class="highlighter-rouge">date</code></td>
    <td><code class="highlighter-rouge">date</code></td>
    <td>Obtained date/time.<br>If the obtained element is a period, a date that falls in the period</td>
    <td>SHALL</td>
    <td>Observation.effective[x]</td>
</tr>
<tr>
    <td><code class="highlighter-rouge">patient</code></td>
    <td><code class="highlighter-rouge">reference</code></td>
    <td>The subject that the observation is about (if patient) </td>
    <td>SHALL</td>
    <td>Observation.subject (Patient)</td>
</tr>
</table>

Systems SHOULD support the following search combinations:

 * patient + category
 * patient + category + date
 * patient + category + code
 * patient + category + code + date
