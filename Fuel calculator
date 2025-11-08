<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>جدول المحطات</title>
<style>
body {
  font-family: Arial, sans-serif;
  background: #f5f5f5;
  display: flex;
  justify-content: center;
  padding: 20px;
}
table {
  border-collapse: collapse;
  width: 100%;
  max-width: 900px;
  text-align: center;
}
th, td {
  border: 1px solid #999;
  padding: 10px;
}
th {
  background-color: #ddd;
}
.col1 { background-color: #fdf5e6; } /* أبيض/بيج */
.col2 { background-color: #8bc34a; color: #fff; } /* أخضر */
.col3 { background-color: #f44336; color: #fff; } /* أحمر */
.col4 { background-color: #ffeb3b; } /* أصفر */
input[type=number] {
  width: 80px;
  text-align: center;
}
.result {
  font-weight: bold;
}
</style>
</head>
<body>

<table>
  <tr>
    <th class="col1">الوصف</th>
    <th class="col2">91</th>
    <th class="col3">95</th>
    <th class="col4">D</th>
  </tr>

  <tr>
    <td class="col1">كمية الاستهلاك</td>
    <td><input type="number" id="c91" oninput="calcConsumption('c91')"><span class="result" id="r_c91"></span></td>
    <td><input type="number" id="c95" oninput="calcConsumption('c95')"><span class="result" id="r_c95"></span></td>
    <td><input type="number" id="cD" oninput="calcConsumption('cD')"><span class="result" id="r_cD"></span></td>
  </tr>

  <tr>
    <td class="col1">الكمية المتوفرة</td>
    <td><input type="number" id="available91" oninput="calcPercentage()"></td>
    <td><input type="number" id="available95" oninput="calcPercentage()"></td>
    <td><input type="number" id="availableD" oninput="calcPercentage()"></td>
  </tr>

  <tr>
    <td class="col1">سعة الخزانات</td>
    <td><input type="number" id="capacity91" oninput="calcPercentage()"></td>
    <td><input type="number" id="capacity95" oninput="calcPercentage()"></td>
    <td><input type="number" id="capacityD" oninput="calcPercentage()"></td>
  </tr>

  <tr>
    <td class="col1">النسبة</td>
    <td><span class="result" id="percent91">0</span></td>
    <td><span class="result" id="percent95">0</span></td>
    <td><span class="result" id="percentD">0</span></td>
  </tr>

  <tr>
    <td class="col1">عدد الخزانات</td>
    <td><input type="number" id="tanks91"></td>
    <td><input type="number" id="tanks95"></td>
    <td><input type="number" id="tanksD"></td>
  </tr>

  <tr>
    <td class="col1">خزانات لا تعمل</td>
    <td><input type="number" id="ntanks91"></td>
    <td><input type="number" id="ntanks95"></td>
    <td><input type="number" id="ntanksD"></td>
  </tr>

  <tr>
    <td class="col1">عدد المضخات</td>
    <td><input type="number" id="pumps91"></td>
    <td><input type="number" id="pumps95"></td>
    <td><input type="number" id="pumpsD"></td>
  </tr>

  <tr>
    <td class="col1">مضخات لا تعمل</td>
    <td><input type="number" id="npumps91"></td>
    <td><input type="number" id="npumps95"></td>
    <td><input type="number" id="npumpsD"></td>
  </tr>

  <tr>
    <td class="col1">عدد الاهواز</td>
    <td><input type="number" id="valves91"></td>
    <td><input type="number" id="valves95"></td>
    <td><input type="number" id="valvesD"></td>
  </tr>

  <tr>
    <td class="col1">اهواز لا تعمل</td>
    <td><input type="number" id="nvalves91"></td>
    <td><input type="number" id="nvalves95"></td>
    <td><input type="number" id="nvalvesD"></td>
  </tr>

</table>

<script>
function calcConsumption(id) {
  const input = document.getElementById(id);
  const result = document.getElementById('r_' + id);
  const value = parseFloat(input.value);
  if(!isNaN(value)) {
    result.innerText = ' → ' + (value * 7);
  } else {
    result.innerText = '';
  }
}

function calcPercentage() {
  const types = ['91', '95', 'D'];
  types.forEach(type => {
    const available = parseFloat(document.getElementById('available'+type).value);
    const capacity = parseFloat(document.getElementById('capacity'+type).value);
    const percent = document.getElementById('percent'+type);
    if(!isNaN(available) && !isNaN(capacity) && capacity !== 0){
      percent.innerText = (available / capacity).toFixed(2);
    } else {
      percent.innerText = '0';
    }
  });
}
</script>

</body>
</html>
