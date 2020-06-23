<variable name="align">bottom</variable>
<variable name="arrow">→</variable>
<table>
<tr>
  <td valign="top">

{{ input | safe }}
  </td>
  <td valign="{{ align }}">&nbsp;{{ arrow }}&nbsp;<br><br></td>
  <td valign="bottom">

{{ output | safe }}
  </td>
</tr>
</table>