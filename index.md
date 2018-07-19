<html>
<body>

<p>Some charts for EGI Notebooks deployment</p>

<h2>Releases</h2>
{% assign charts = site.data.index.entries.notekook-monitor | sort: 'created' | reverse %}
<table>
  <tr>
    <th>release</th>
    <th>date</th>
  </tr>
  {% for chart in charts %}
    <tr>
      <td>
      <a href="{{ chart.urls[0] }}">
          {{ chart.name }}-{{ chart.version }}
      </a>
      </td>
      <td>
      <span class='date'>{{ chart.created | date_to_rfc822 }}</span>
      </td>
    </tr>
  {% endfor %}
</table>

</body>
</html>
