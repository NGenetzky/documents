---
---

# Index of /documents/

## documents

<table style="width:100%" border="1px solid black">
    <tr> 
        <th>path</th>
        <th>date</th>
    </tr>
{% for d in site.documents %}
    <tr> 
        <td><a href="{{ d.url }}">{{ d.url }}</a></td>
        <td>{{ d.date }}</td>
    </tr>
{% endfor %}
</table>

## files

{% assign files = site.static_files | where_exp: "file", "file.path contains '/documents/'"%}

<table style="width:100%" border="1px solid black">
    <tr> 
        <th>path</th>
        <th>last_modified</th>
    </tr>
{% for sf in files %}
    <tr> 
        <td><a href="{{ sf.path }}">{{ sf.path }}</a></td>
        <td>{{ sf.modified_time }}</td>
    </tr>
{% endfor %}
</table>



