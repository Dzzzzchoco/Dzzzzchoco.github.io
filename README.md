
# 网页主题切换示例

## 主题列表

- [蔬菜](#蔬菜)
- [水果](#水果)
- [其他](#其他)

<div id="content">
  </div>

## 食物资料

<div id="food-data">
  <div class="food-item" data-name="苹果">
    <h3><a href="#apple-page">苹果</a></h3>
    <p><strong>利：</strong>维生素C、膳食纤维、抗氧化剂、钾。</p>
    <p><strong>弊：</strong>果糖、农药残留。</p>
  </div>
  <div class="food-item" data-name="香蕉">
    <h3><a href="#banana-page">香蕉</a></h3>
    <p><strong>利：</strong>钾、膳食纤维、维生素B6、碳水化合物。</p>
    <p><strong>弊：</strong>糖分、过敏。</p>
  </div>
  <div class="food-item" data-name="菠菜">
    <h3><a href="#spinach-page">菠菜</a></h3>
    <p><strong>利：</strong>维生素K、维生素A、铁、叶酸。</p>
    <p><strong>弊：</strong>草酸、硝酸盐。</p>
  </div>
  <div class="food-item" data-name="鸡蛋">
    <h3><a href="#egg-page">鸡蛋</a></h3>
    <p><strong>利：</strong>优质蛋白质、胆碱、叶黄素和玉米黄素、多种维生素和矿物质。</p>
    <p><strong>弊：</strong>胆固醇、过敏。</p>
  </div>
    <div class="food-item" data-name="牛肉">
    <h3><a href="#beef-page">牛肉</a></h3>
    <p><strong>利：</strong>优质蛋白质、铁、锌、维生素B12。</p>
    <p><strong>弊：</strong>饱和脂肪和胆固醇、加工牛肉的有害物质。</p>
  </div>
    <div class="food-item" data-name="三文鱼">
    <h3><a href="#salmon-page">三文鱼</a></h3>
    <p><strong>利：</strong>Omega-3脂肪酸、优质蛋白质、维生素D。</p>
    <p><strong>弊：</strong>重金属、过敏。</p>
  </div>
    <div class="food-item" data-name="坚果">
    <h3><a href="#nut-page">坚果（如杏仁）</a></h3>
    <p><strong>利：</strong>健康脂肪、膳食纤维、维生素E、镁。</p>
    <p><strong>弊：</strong>能量、过敏。</p>
  </div>
    <div class="food-item" data-name="牛奶">
    <h3><a href="#milk-page">牛奶</a></h3>
    <p><strong>利：</strong>钙、蛋白质、维生素D。</p>
    <p><strong>弊：</strong>乳糖、饱和脂肪。</p>
  </div>
</div>  

<script> 
 function loadTheme(themeId, targetDivId) {
  let contentDiv = document.getElementById(targetDivId);
  let themeContent = '';

  switch (themeId) {
    case '蔬菜':
       themeContent = `
         <h2>蔬菜</h2>
         <ul>
          <li><a href="#蔬菜-Asparagus (芦笋)" onclick="loadSubTheme('蔬菜-Asparagus (芦笋)'); return right;">Asparagus (芦笋)</a></li>
          <li><a href="#蔬菜-子主题二" onclick="loadSubTheme('蔬菜-子主题二'); return false;">根茎类</a></li>
         </ul>
        <div id="subContent">
          </div>
      `;
      break;
    case '水果':
      themeContent = `
          <h2>水果</h2>
          <ul>
            <li><a href="#水果-苹果" onclick="loadSubTheme('水果-苹果'); return false;">苹果</a></li>
             <li><a href="#水果-子主题二" onclick="loadSubTheme('水果-子主题二'); return false;">浆果类</a></li>
          </ul>
            <div id="subContent">
            </div>
        `;
      break;
    case '其他':
      themeContent = `
          <h2>其他</h2>
          <ul>
            <li><a href="#其他-子主题一" onclick="loadSubTheme('其他-子主题一'); return false;">坚果类</a></li>
            <li><a href="#其他-子主题二" onclick="loadSubTheme('其他-子主题二'); return false;">菌菇类</a></li>
          </ul>
            <div id="subContent">
            </div>
        `;
      break;
    default:
      themeContent = '<p>请选择一个主题。</p>';
  }

  contentDiv.innerHTML = themeContent;
}

    contentDiv.innerHTML = themeContent;
  }

  function loadSubTheme(subThemeId) {
    let subContentDiv = document.getElementById('subContent');
    let subThemeContent = '';

    switch (subThemeId) {
      case '蔬菜-子主题一':
        subThemeContent = '<p>蔬菜的叶菜类内容。</p>';
        break;
      case '蔬菜-子主题二':
        subThemeContent = '<p>蔬菜的根茎类内容。</p>';
        break;
      case '水果-子主题一':
        subThemeContent = '<p>水果的柑橘类内容。</p>';
        break;
      case '水果-子主题二':
        subThemeContent = '<p>水果的浆果类内容。</p>';
        break;
      case '其他-子主题一':
        subThemeContent = '<p>其他的坚果类内容。</p>';
        break;
      case '其他-子主题二':
        subThemeContent = '<p>其他的菌菇类内容。</p>';
        break;
      default:
        subThemeContent = '<p>请选择一个子主题。</p>';
    }

    subContentDiv.innerHTML = subThemeContent;
  }



  // 初始加载第一个主题
  loadTheme('水果');
  loadTheme('蔬菜');
  loadTheme('其他');
</script>
