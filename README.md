# 水果营养信息网站

## 搜索

<form id="search-form">
  <input type="text" id="search-input" placeholder="输入水果名称...">
  <button type="submit">搜索</button>
</form>

<div id="search-results"></div>

## 水果资料

<div id="fruit-data">
  <h3>苹果</h3>
  <p>富含维生素 C。</p>

  <h3>香蕉</h3>
  <p>富含维生素 B6。</p>
</div>

## 添加水果资料

<form id="add-fruit-form">
  <label for="fruit-name">水果名称：</label>
  <input type="text" id="fruit-name" required><br><br>

  <label for="fruit-vitamins">维生素含量：</label>
  <input type="text" id="fruit-vitamins" required><br><br>

  <button type="submit">添加</button>
</form>

## JavaScript 代码

```javascript
// 搜索功能
document.getElementById('search-form').addEventListener('submit', function(event) {
  event.preventDefault();
  const searchTerm = document.getElementById('search-input').value.toLowerCase();
  const fruitData = document.getElementById('fruit-data').children;
  const resultsDiv = document.getElementById('search-results');
  resultsDiv.innerHTML = '';

  let found = false;
  for (let i = 0; i < fruitData.length; i++) {
    const fruitName = fruitData[i].querySelector('h3').textContent.toLowerCase();
    if (fruitName.includes(searchTerm)) {
      resultsDiv.appendChild(fruitData[i].cloneNode(true));
      found = true;
    }
  }

  if (!found && searchTerm.trim() !== '') {
    resultsDiv.innerHTML = '<p>未找到匹配结果。</p>';
  }
});

// 添加水果资料功能
document.getElementById('add-fruit-form').addEventListener('submit', function(event) {
  event.preventDefault();
  const fruitName = document.getElementById('fruit-name').value;
  const fruitVitamins = document.getElementById('fruit-vitamins').value;
  const fruitDataDiv = document.getElementById('fruit-data');

  const newFruitDiv = document.createElement('div');
  newFruitDiv.innerHTML = `<h3>${fruitName}</h3><p>${fruitVitamins}</p>`;
  fruitDataDiv.appendChild(newFruitDiv);

  // 清空表单
  document.getElementById('fruit-name').value = '';
  document.getElementById('fruit-vitamins').value = '';
});
