---
layout: post
title:  "Metodi Computazionali"
subtitle: "Appunti universitari"
date:   2018-10-01 21:36:09 +0200
categories: jekyll update
tabella: true
---

<table id="metodi_computazionali" class="display">
    <thead>
        <tr>
            <th>Giorno</th>
            <th>Descrizione</th>
            <th>Link</th>
        </tr>
    </thead>
    <tbody>
            {% for appunto in site.data.fisicateorica %}
            <tr>
                <td><span>{{appunto.day}}</span></td> <!-- Data deve essere dentro a span sennò non funziona lo script di ordinamento -->
                <td>{{appunto.desc}}</td>
                <td><a href="{{appunto.link}}">Click qui</a></td>
            </tr>
            {% endfor %}
    </tbody>

</table>

<script type="text/javascript">
    $(document).ready( function () {
        jQuery.extend(jQuery.fn.dataTableExt.oSort, {
            "extract-date-pre": function(value) {
                var date = $(value, 'span')[0].innerHTML;
                date = date.split('/');
                return Date.parse(date[1] + '/' + date[0] + '/' + date[2])
            },
            "extract-date-asc": function(a, b) {
                return ((a < b) ? -1 : ((a > b) ? 1 : 0));
            },
            "extract-date-desc": function(a, b) {
                return ((a < b) ? 1 : ((a > b) ? -1 : 0));
            }
        });
        
        $('#metodi_computazionali').DataTable(
            {
                "language": {
                    "url": "//cdn.datatables.net/plug-ins/1.10.19/i18n/Italian.json"
                },
                columnDefs: [{
                    type: 'extract-date',
                    targets: [0]
                }]
            }
        );
    } );
</script>