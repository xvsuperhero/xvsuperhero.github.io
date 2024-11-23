<div style="
    background-color: #f9f9f9;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 20px;
">
<h1 style="color: #4A90E2;">Leaderboard</h>
<p style="color: #4A90E2;font-size:20px">Wem.<br></p>

<ul style="color: #4A90E2;font-size:20px"> <b>Here are some explanations about the columns in the leaderboard section:</b>
	<ul style="color: #4A90E2;font-size:20px">

<p style="color: #4A90E2;font-size:20px">ge.</p>

<table id="sortableTable">
<thead>
  <tr>
    <th >Agent name</th>
    <th onclick="sortTable(1)">AA &#x21C5;</th>
    <th onclick="sortTable(2)">A1 &#x21C5;</th>
    <th onclick="sortTable(3)">A2 &#x21C5;</th>
    <th onclick="sortTable(4)">A3 &#x21C5;</th>
    <th onclick="sortTable(5)">A4 &#x21C5;</th>
    <th onclick="sortTable(6)">AT &#x21C5;</th>
    <th onclick="sortTable(7)">T1 &#x21C5;</th>
    <th onclick="sortTable(8)">T2 &#x21C5;</th>
    <th onclick="sortTable(9)">T3 &#x21C5;</th>
    <th onclick="sortTable(10)">T4 &#x21C5;</th>
    <th>Organization</th>
    <th>Model family</th>
    <th>site</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>🥇😄FLASH</td>
    <td>619</td>
    <td>10</td>
    <td>585</td>
    <td>336</td>
    <td>555</td>
    <td>157</td>
    <td>77</td>
    <td>56</td>
    <td>59</td>
    <td>211</td>
    <td>AIOPSLAB authors</td>
    <td></td>
    <td><a href="https://www.bilibili.com">🔗</a></td>
  </tr>
  <tr>
    <td>🥈😄REACT</td>
    <td>5</td>
    <td>7</td>
    <td>64</td>
    <td>445</td>
    <td>36</td>
    <td>25</td>
    <td>39</td>
    <td>365</td>
    <td>32</td>
    <td>68</td>
    <td>AIOPSLAB authors</td>
    <td></td>
    <td><a href="https://www.baidu.com">🔗</a></td>
  </tr>
  <tr>
    <td>🥉😄GPT-4-W-SHELL</td>
    <td>44</td>
    <td>63</td>
    <td>61.54</td>
    <td>40</td>
    <td>27.27</td>
    <td>30.57</td>
    <td>8</td>
    <td>4</td>
    <td>68</td>
    <td>97</td>
    <td>AIOPSLAB authors</td>
    <td>GPT4</td>
    <td><a href="https://www.bilibili.com">🔗</a></td>
  </tr>
  <tr>
    <td>😄GPT-3.5-W-SHELL</td>
    <td>173</td>
    <td>207</td>
    <td>377</td>
    <td>09</td>
    <td>0</td>
    <td>179</td>
    <td>105</td>
    <td>6</td>
    <td>1</td>
    <td>23</td>
    <td>AIOPSLAB authors</td>
    <td>GPT3.5</td>
    <td><a href="https://www.baidu.com">🔗</a></td>
  </tr>
</tbody>
</table>
<style>
  table {
    height: 300px;
    width: 100%;
    border-collapse: collapse;
    overflow-x: auto;
    overflow-y: auto;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    text-align: center;
  }
  th {
    cursor: pointer;
    padding: 15px 20px;
    background-color: #1976D2;
    color: white;
    text-transform: uppercase;
    letter-spacing: 1px;
    position: sticky;
    top: 0;
    z-index: 2;
    border: none;
  }
  th:hover {
    background-color: #1565C0;
  }
  tr:nth-child(even) {
    background-color: #BBDEFB;
  }
  tr:nth-child(odd) {
    background-color: #E3F2FD;
  }
  td {
    padding: 15px 20px;
    border-bottom: 1px solid #81D4FA;
  }
  a {
    color: #0277BD;
    text-decoration: none;
    font-weight: bold;
  }
  a:hover {
    text-decoration: underline;
  }
</style>
<script>
  function sortTable(columnIndex) {
    var table = document.getElementById("sortableTable");
    var rows = Array.from(table.getElementsByTagName("tr")).slice(1);  // Skip header row
    var isAscending = table.rows[0].cells[columnIndex].getAttribute("data-sort-order") === "asc";
    rows.sort(function(rowA, rowB) {
      var cellA = rowA.cells[columnIndex].textContent.trim();
      var cellB = rowB.cells[columnIndex].textContent.trim();
      if (!isNaN(cellA) && !isNaN(cellB)) {
        return isAscending ? cellA - cellB : cellB - cellA;
      } else {
        return isAscending ? cellA.localeCompare(cellB) : cellB.localeCompare(cellA);
      }
    });
    rows.forEach(function(row) {
      table.appendChild(row);
    });
    table.rows[0].cells[columnIndex].setAttribute("data-sort-order", isAscending ? "desc" : "asc");
  }
</script>









