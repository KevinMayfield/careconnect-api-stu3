
### Search Parameters

<table style="min-width:100%;width:100%">
<tr id="clinical">
<th style="width:15%;">Name</th>
<th style="width:10%;">Type</th>
<th style="width:40%;">Description</th>
<th style="width:5%;">Conformance</th>
<th style="width:30%;">Path</th>
</tr>
<tr>
<td><code class="highlighter-rouge">address-postalcode</code></td>
<td><code class="highlighter-rouge">string</code></td>
<td>A postalCode specified in an address</td>
<td>MAY</td>
<td>Patient.address.postalCode </td>
</tr>
<tr>
<td><code class="highlighter-rouge">birthdate</code></td>
<td><code class="highlighter-rouge">date</code></td>
<td>The patient's date of birth</td>
<td>SHALL</td>
<td>Patient.birthDate</td>
</tr>
<tr>
<td><code class="highlighter-rouge">email</code></td>
<td><code class="highlighter-rouge">token</code></td>
<td>A value in an email contact</td>
<td>MAY</td>
<td>Patient.telecom <br>(system=email)</td>
</tr>
<tr>
<td><code class="highlighter-rouge">family</code></td>
<td><code class="highlighter-rouge">string</code></td>
<td>A portion of the family name of the patient</td>
<td>SHALL</td>
<td>Patient.name.family</td>
</tr>
<tr>
<td><code class="highlighter-rouge">gender</code></td>
<td><code class="highlighter-rouge">token </code></td>
<td>Gender of the patient</td>
<td>SHALL</td>
<td>Patient.gender</td>
</tr>
<tr>
<td><code class="highlighter-rouge">given</code></td>
<td><code class="highlighter-rouge">string</code></td>
<td>A portion of the given name of the patient</td>
<td>SHALL</td>
<td>Patient.name.given</td>
</tr>
<tr>
<td><code class="highlighter-rouge">identifier</code></td>
<td><code class="highlighter-rouge">token</code></td>
<td>A patient identifier (NHS Number, Hospital Number, etc)</td>
<td>SHALL</td>
<td>Patient.identifier</td>
</tr>
<tr>
<td><code class="highlighter-rouge">name </code></td>
<td><code class="highlighter-rouge">string </code></td>
<td>A portion of either family or given name of the patient</td>
<td>SHALL</td>
<td>Patient.name</td>
</tr>
<tr>
<td><code class="highlighter-rouge">phone </code></td>
<td><code class="highlighter-rouge">token </code></td>
<td>A value in a phone contact</td>
<td>MAY</td>
<td>Patient.telecom(system=phone)</td>
</tr>
</table>

Client systems SHALL provide at least two parameters of differing types, unless searching on identifier where one parameter is permitted. Systems SHALL support the following search combinations:

* name + gender
* name + birthdate
* family + gender
* given + gender
