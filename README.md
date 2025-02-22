# 食物营养信息网站

## 搜索

<form id="search-form">
  <input type="text" id="search-input" placeholder="输入食物名称...">
  <button type="submit">搜索</button>
</form>

<div id="search-results"></div>

## 食物资料列表

<ul id="food-list">
  <li><a href="apple.html">苹果</a></li>
  <li><a href="banana.html">香蕉</a></li>
  <li><a href="spinach.html">菠菜</a></li>
  <li><a href="egg.html">鸡蛋</a></li>
  <li><a href="beef.html">牛肉</a></li>
  <li><a href="salmon.html">三文鱼</a></li>
  <li><a href="nut.html">坚果（如杏仁）</a></li>
  <li><a href="milk.html">牛奶</a></li>
</ul>

## 添加食物资料

<form id="add-food-form">
  <label for="food-name">食物名称：</label>
  <input type="text" id="food-name" required><br><br>

  <label for="food-benefits">利：</label>
  <input type="text" id="food-benefits" required><br><br>

    <label for="food-drawbacks">弊：</label>
  <input type="text" id="food-drawbacks" required><br><br>

  <button type="submit">添加</button>
</form>

// 搜索功能
document.getElementById('search-form').addEventListener('submit', function(event) {
  event.preventDefault();
  const searchTerm = document.getElementById('search-input').value.toLowerCase();
  const foodList = document.getElementById('food-list').getElementsByTagName('li');
  const resultsDiv = document.getElementById('search-results');
  resultsDiv.innerHTML = '';

  let found = false;
  for (let i = 0; i < foodList.length; i++) {
    const foodName = foodList[i].textContent.toLowerCase();
    if (foodName.includes(searchTerm)) {
      resultsDiv.appendChild(foodList[i].cloneNode(true));
      found = true;
    }
  }

  if (!found && searchTerm.trim() !== '') {
    resultsDiv.innerHTML = '<p>未找到匹配结果。</p>';
  }
});

// 添加食物资料功能
document.getElementById('add-food-form').addEventListener('submit', function(event) {
  event.preventDefault();
  const foodName = document.getElementById('food-name').value;
  const foodBenefits = document.getElementById('food-benefits').value;
    const foodDrawbacks = document.getElementById('food-drawbacks').value;
  const foodList = document.getElementById('food-list');

  const newFoodItem = document.createElement('li');
    // 创建一个动态的html文件名，例如： "newfood.html"
    const fileName = foodName.toLowerCase().replace(/ /g, '-') + ".html"
  newFoodItem.innerHTML = `<a href="${fileName}">${foodName}</a>`;
  foodList.appendChild(newFoodItem);

  // 创建新的HTML文件（模拟）
    createNewPage(fileName, foodName, foodBenefits, foodDrawbacks);

  // 清空表单
  document.getElementById('food-name').value = '';
  document.getElementById('food-benefits').value = '';
    document.getElementById('food-drawbacks').value = '';
});

// 创建新的HTML文件 (模拟，实际应用中需要后端支持)
function createNewPage(fileName, foodName, foodBenefits, foodDrawbacks){
    // 这里只是一个模拟，实际应用中，你需要使用后端语言（如Node.js, Python等）
    // 将HTML内容写入到文件中。
    const pageContent = `
    <!DOCTYPE html>
    <html>
    <head>
        <title>${foodName} 营养信息</title>
    </head>
    <body>
        <h1>${foodName}</h1>
        <p><strong>利：</strong>${foodBenefits}。</p>
        <p><strong>弊：</strong>${foodDrawbacks}。</p>
    </body>
    </html>
    `;
    console.log(`模拟创建文件：${fileName}，内容：\n${pageContent}`);
    // 在实际应用中，你需要将pageContent写入到fileName文件中。
}

<!DOCTYPE html>
<html>
<head>
    <title>苹果 营养信息</title>
</head>
<body>
    <h1>苹果</h1>
    <p><strong>利：</strong>维生素C、膳食纤维、抗氧化剂、钾。</p>
    <p><strong>弊：</strong>果糖、农药残留。</p>
</body>
</html>
