---
---

# Index of /documents/

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

## documents

{% for d in site.documents %}
### {{ d.document.name }}
#### document
{% include table_from_document.html document=d %}
#### document.document
{% include table_from_dict.html dict=d.document %}
#### document.file
{% assign sf = site.static_files | where: "path", d.file.path | first %}
{% include table_from_static_file.html sf=sf %}
{% endfor %}

## files
{% assign files = site.static_files | where_exp: "file", "file.path contains '/documents/'"%}
{% for sf in files %}
{% include table_from_static_file.html sf=sf %}
{% endfor %}



