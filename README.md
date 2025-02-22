# Food Nutrition Information Website (食物营养信息网站)

## Search (搜索)

<form id="search-form">
  <input type="text" id="search-input" placeholder="Enter food name... (输入食物名称...)">
  <button type="submit">Search (搜索)</button>
</form>

<div id="search-results"></div>

## Data (1) (资料 (1))

<div id="food-data">
  <div class="food-item" data-name="Apple (苹果)">
    <h3><a href="#apple-page">Apple (苹果)</a></h3>
  </div>
    <div class="food-item" data-name="Banana (香蕉)">
    <h3><a href="#banana-page">Banana (香蕉)</a></h3>
  </div>
  <div class="food-item" data-name="Beef (牛肉)">
    <h3><a href="#beef-page">Beef (牛肉)</a></h3>
  </div>
  <div class="food-item" data-name="Egg (鸡蛋)">
    <h3><a href="#egg-page">Egg (鸡蛋)</a></h3>
  </div>
  <div class="food-item" data-name="Milk (牛奶)">
    <h3><a href="#milk-page">Milk (牛奶)</a></h3>
  </div>
  <div class="food-item" data-name="Nuts (坚果)">
    <h3><a href="#nut-page">Nuts (坚果)</a></h3>
  </div>
  <div class="food-item" data-name="Salmon (三文鱼)">
    <h3><a href="#salmon-page">Salmon (三文鱼)</a></h3>
  </div>
    <div class="food-item" data-name="Spinach (菠菜)">
    <h3><a href="#spinach-page">Spinach (菠菜)</a></h3>
  </div>

</div>

## Add Food Data (添加食物资料)

<form id="add-food-form">
  <label for="food-name">Food Name (食物名称):</label>
  <input type="text" id="food-name" required><br><br>

  <label for="food-benefits">Benefits (利):</label>
  <input type="text" id="food-benefits" required><br><br>

  <label for="food-drawbacks">Drawbacks (弊):</label>
  <input type="text" id="food-drawbacks" required><br><br>

  <button type="submit">Add (添加)</button>
</form>

## Food Details Pages (食物详情页面)

<div id="food-pages">
  <div id="apple-page" class="food-page">
    <h2>Apple (苹果)</h2>
    <p><strong>Benefits (利):</strong> Vitamin C: Boosts immunity, promotes collagen synthesis, aids skin health. (维生素C：增强免疫力，促进胶原蛋白合成，有助于皮肤健康。)</p>
    <p>Dietary fiber: Promotes bowel movements, prevents constipation, helps control blood sugar. (膳食纤维：促进肠道蠕动，预防便秘，有助于控制血糖。)</p>
    <p>Antioxidants (like flavonoids): Helps fight free radical damage, prevents cardiovascular diseases and cancer. (抗氧化剂（如类黄酮）：有助于抵抗自由基损伤，预防心血管疾病和癌症。)</p>
    <p>Potassium: Helps maintain blood pressure balance. (钾：有助于维持血压平衡。)</p>
    <p><strong>Drawbacks (弊):</strong> Fructose: Excessive consumption may lead to energy surplus, increased risk of obesity and diabetes. (果糖：过量食用可能导致能量过剩，增加肥胖和糖尿病风险。)</p>
    <p>Pesticide residues: Wash thoroughly before eating or choose organic apples. (农药残留：食用前应清洗干净或选择有机苹果。)</p>
  </div>
    <div id="banana-page" class="food-page">
    <h2>Banana (香蕉)</h2>
    <p><strong>Benefits (利):</strong> Potassium: Helps maintain blood pressure balance, prevents muscle cramps. (钾：有助于维持血压平衡，预防肌肉痉挛。)</p>
    <p>Dietary fiber: Promotes bowel movements, prevents constipation. (膳食纤维：促进肠道蠕动，预防便秘。)</p>
    <p>Vitamin B6: Helps nervous system health, promotes red blood cell production. (维生素B6：有助于神经系统健康，促进红细胞生成。)</p>
    <p>Carbohydrates: Provides quick energy. (碳水化合物：提供快速能量。)</p>
    <p><strong>Drawbacks (弊):</strong> Sugar: Ripe bananas have high sugar content, diabetics should consume in moderation. (糖分：成熟香蕉含糖量较高，糖尿病患者应适量食用。)</p>
    <p>Some people may be allergic. (部分人群可能对其过敏。)</p>
  </div>
  <div id="beef-page" class="food-page">
    <h2>Beef (牛肉)</h2>
    <p><strong>Benefits (利):</strong> High-quality protein: Provides essential amino acids for tissue repair and growth. (优质蛋白质：提供人体必需的氨基酸，有助于组织修复和生长。)</p>
    <p>Iron: Prevents iron deficiency anemia. (铁：预防缺铁性贫血。)</p>
    <p>Zinc: Helps immune system health, promotes wound healing. (锌：有助于免疫系统健康，促进伤口愈合。)</p>
    <p>Vitamin B12: Helps nervous system health, promotes red blood cell production. (维生素B12：有助于神经系统健康，促进红细胞生成。)</p>
    <p><strong>Drawbacks (弊):</strong> Saturated fat and cholesterol: Excessive consumption may increase the risk of cardiovascular disease. (饱和脂肪和胆固醇：过量食用可能增加心血管疾病风险。)</p>
    <p>Processed beef: Contains high levels of harmful substances such as nitrites, increasing the risk of cancer. (加工牛肉：含有较高的亚硝酸盐等有害物质，增加患癌风险。)</p>
  </div>
  <div id="egg-page" class="food-page">
    <h2>Egg (鸡蛋)</h2>
    <p><strong>Benefits (利):</strong> High-quality protein: Provides essential amino acids for tissue repair and growth. (优质蛋白质：提供人体必需的氨基酸，有助于组织修复和生长。)</p>
    <p>Choline: Helps brain development and memory. (胆碱：有助于大脑发育和记忆力。)</p>
    <p>Lutein and zeaxanthin: Helps protect vision, prevents macular degeneration. (叶黄素和玉米黄素：有助于保护视力，预防黄斑变性。)</p>
    <p>Various vitamins and minerals: Such as vitamin D, vitamin B12, iron, zinc, etc. (多种维生素和矿物质：如维生素D、维生素B12、铁、锌等。)</p>
    <p><strong>Drawbacks (弊):</strong> Cholesterol: Egg yolks have high cholesterol, high cholesterol patients should consume in moderation. (胆固醇：蛋黄含有较高的胆固醇，高胆固醇患者应适量食用。)</p>
    <p>Some people may be allergic. (部分人群可能对其过敏。)</p>
  </div>
  <div id="milk-page" class="food-page">
    <h2>Milk (牛奶)</h2>
    <p><strong>Benefits (利):</strong> Calcium: Is the best source of calcium, helps bone and teeth health. (钙：是钙的最佳来源，有助于骨骼和牙齿健康。)</p>
    <p>Protein: Provides high-quality protein, helps tissue repair and growth. (蛋白质：提供优质蛋白质，有助于组织修复和生长。)</p>
    <p>Vitamin D: Helps calcium absorption. (维生素D：有助于钙的吸收。)</p>
    <p><strong>Drawbacks (弊):</strong> Lactose: Some people have lactose intolerance. (乳糖：部分人群有乳糖不耐受现象。)</p>
    <p>Saturated fat: Whole milk contains high saturated fat. (饱和脂肪：全脂牛奶含有较高的饱和脂肪。)</p>
  </div>
  <div id="nut-page" class="food-page">
    <h2>Nuts (坚果)</h2>
    <p><strong>Benefits (利):</strong> Healthy fats: Contains unsaturated fats, helps lower blood lipids. (健康脂肪：含有不饱和脂肪，有助于降低血脂。)</p>
    <p>Dietary fiber: Promotes bowel movements, prevents constipation. (膳食纤维：促进肠道蠕动，预防便秘。)</p>
    <p>Vitamin E: Antioxidant, helps protect cells from damage. (维生素E：抗氧化剂，有助于保护细胞免受损伤。)</p>
    <p>Magnesium: Helps maintain nerve and muscle function. (镁：有助于维持神经和肌肉功能。)</p>
    <p><strong>
