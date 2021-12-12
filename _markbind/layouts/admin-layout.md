<head-bottom>
<link rel="stylesheet" href="{{baseUrl}}/css/main.css">
<link rel="stylesheet" href="{{baseUrl}}/css/admin.css">
</head-bottom>
{% include '_markbind/layouts/header.md' %}
{% set file =  "" if module in ['TIC2002', 'TEE3201'] else "admin" %}
{% set sitenav_title =  "Admin info" %}
{% include '_markbind/layouts/body.md' %}
{% include '_markbind/layouts/footer.md' %}
