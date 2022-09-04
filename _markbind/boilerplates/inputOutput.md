{% set align="bottom" %}
{% set arrow="→" %}
<table>
<tbody>
<tr>
  <td valign="top">

{{ input | safe }}
  </td>
  <td valign="{{ align }}">&nbsp;{{ arrow }}&nbsp;<br><br></td>
  <td valign="bottom">

{{ output | safe }}
  </td>
</tr>
</tbody>
</table>
