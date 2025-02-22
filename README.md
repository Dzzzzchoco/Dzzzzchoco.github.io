# 食物营养信息网站

## 搜索

<form id="search-form">
  <input type="text" id="search-input" placeholder="text...">
  <button type="submit">submit</button>
</form>

<div id="search-results"></div>

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

## 食物资料

<div id="food-data">
  <div class="food-item" data-name="apple">
    <h3><a href="#apple-page">apple</a></h3>
  </div>
  <div class="food-item" data-name="banana">
    <h3><a href="#banana-page">banana</a></h3>
  </div>
  <div class="food-item" data-name="spinach">
    <h3><a href="#spinach-page">spinach</a></h3>
  </div>
  <div class="food-item" data-name="egg">
    <h3><a href="#egg-page">egg</a></h3>
  </div>
    <div class="food-item" data-name="beef">
    <h3><a href="#beef-page">beef</a></h3>
  </div>
    <div class="food-item" data-name="salmon">
    <h3><a href="#salmon-page">salmon</a></h3>
  </div>
    <div class="food-item" data-name="nut">
    <h3><a href="#nut-page">nut</a></h3>
  </div>
    <div class="food-item" data-name="milk">
    <h3><a href="#milk-page">milk</a></h3>
  </div>
</div>

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

## 食物详情页面

<div id="food-pages">
  <div id="apple-page" class="food-page">
    <h2>apple</h2>
    <p><strong>利：</strong>维生素C：增强免疫力，促进胶原蛋白合成，有助于皮肤健康。</p>
    <p>膳食纤维：促进肠道蠕动，预防便秘，有助于控制血糖。</p>
    <p>抗氧化剂（如类黄酮）：有助于抵抗自由基损伤，预防心血管疾病和癌症。</p>
    <p>钾：有助于维持血压平衡。</p>
    <p><strong>弊：</strong>果糖：过量食用可能导致能量过剩，增加肥胖和糖尿病风险。</p>
    <p>农药残留：食用前应清洗干净或选择有机苹果。</p>
  </div>
  <div id="banana-page" class="food-page">
    <h2>banana</h2>
    <p><strong>利：</strong>钾：有助于维持血压平衡，预防肌肉痉挛。</p>
    <p>膳食纤维：促进肠道蠕动，预防便秘。</p>
    <p>维生素B6：有助于神经系统健康，促进红细胞生成。</p>
    <p>碳水化合物：提供快速能量。</p>
    <p><strong>弊：</strong>糖分：成熟香蕉含糖量较高，糖尿病患者应适量食用。</p>
    <p>部分人群可能对其过敏。</p>
  </div>
  <div id="spinach-page" class="food-page">
    <h2>spinach</h2>
    <p><strong>利：</strong>维生素K：有助于血液凝固和骨骼健康。</p>
    <p>维生素A：有助于视力健康，维持皮肤和黏膜健康。</p>
    <p>铁：预防缺铁性贫血。</p>
    <p>叶酸：有助于细胞生长和分裂，对孕妇尤其重要。</p>
    <p><strong>弊：</strong>草酸：过量食用可能影响钙的吸收，肾结石患者应少食。</p>
    <p>硝酸盐：过量食用可能对健康不利。</p>
  </div>
    <div id="egg-page" class="food-page">
    <h2>egg</h2>
    <p><strong>利：</strong>优质蛋白质：提供人体必需的氨基酸，有助于组织修复和生长。</p>
    <p>胆碱：有助于大脑发育和记忆力。</p>
    <p>叶黄素和玉米黄素：有助于保护视力，预防黄斑变性。</p>
    <p>多种维生素和矿物质：如维生素D、维生素B12、铁、锌等。</p>
    <p><strong>弊：</strong>胆固醇：蛋黄含有较高的胆固醇，高胆固醇患者应适量食用。</p>
    <p>部分人群可能对其过敏。</p>
  </div>
    <div id="beef-page" class="food-page">
    <h2>beef</h2>
    <p><strong>利：</strong>优质蛋白质：提供人体必需的氨基酸，有助于组织修复和生长。</p>
    <p>铁：预防缺铁性贫血。</p>
    <p>锌：有助于免疫系统健康，促进伤口愈合。</p>
    <p>维生素B12：有助于神经系统健康，促进红细胞生成。</p>
    <p><strong>弊：</strong>饱和脂肪和胆固醇：过量食用可能增加心血管疾病风险。</p>
    <p>加工牛肉：含有较高的亚硝酸盐等有害物质，增加患癌风险。</p>
  </div>
    <div id="salmon-page" class="food-page">
    <h2>salmon</h2>
    <p><strong>利：</strong>Omega-3脂肪酸：有助于降低血脂，预防心血管疾病，促进大脑发育。</p>
    <p>优质蛋白质：提供人体必需的氨基酸，有助于组织修复和生长。</p>
    <p>维生素D：有助于钙吸收，促进骨骼健康。</p>
    <p><strong>弊：</strong>重金属：部分三文鱼可能含有重金属（如汞）残留，应选择来源可靠的产品。</p>
    <p>部分人群可能对其过敏。</p>
  </div>
    <div id="nut-page" class="food-page">
    <h2>nut</h2>
    <p><strong>利：</strong>健康脂肪：含有不饱和脂肪，有助于降低血脂。</p>
    <p>膳食纤维：促进肠道蠕动，预防便秘。</p>
    <p>维生素E：抗氧化剂，有助于保护细胞免受损伤。</p>
    <p>镁：有助于维持神经和肌肉功能。</p>
    <p><strong>弊：</strong>能量：坚果能量较高，过量食用可能导致能量过剩。</p>
    <p>部分人群可能对其过敏。</p>
  </div>
    <div id="milk-page" class="food-page">
    <h2>milk</h2>
    <p><strong>利：</strong>钙：是钙的最佳来源，有助于骨骼和牙齿健康。</p>
