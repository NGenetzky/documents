---
document:
  date: 2017-05-22
  name: "Communication_Protocols_for_Embedded_Systems-poster.pub"
  ext: pub
---

<h3>{{ page.document.name }}</h3>

<h4>Table</h4>

<table style="width:100%" border="1px solid black">
    <tr> 
        <th>name</th>
        <th>date</th>
        <th>ext</th>
    </tr>
    <tr> 
        <td>{{ page.document.name }}</td>
        <td>{{ page.document.date }}</td>
        <td>{{ page.document.ext }}</td>
    </tr>
</table>

<h4>Ruby Object</h4>
```
{{ page.document }}
```