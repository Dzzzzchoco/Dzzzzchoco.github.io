
# 网页主题切换示例

## 主题列表

- [蔬菜](#蔬菜)
- [水果](#水果)
- [其他](#其他)

<div id="content">
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
            <li><a href="#水果-子主题一" onclick="loadSubTheme('水果-子主题一'); return false;">柑橘类</a></li>
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

  <div id="food-data">
  <div class="food-item" data-name="Asparagus (芦笋)">
    <h3><a href="#asparagus-page">Asparagus (芦笋)</a></h3>
  </div>
  <div class="food-item" data-name="Cabbage (白菜)">
    <h3><a href="#cabbage-page">Cabbage (白菜)</a></h3>
  </div>
  <div class="food-item" data-name="Spinach (菠菜)">
    <h3><a href="#spinach-page">Spinach (菠菜)</a></h3>
  </div>
  <div class="food-item" data-name="Cauliflower (菜花)">
    <h3><a href="#cauliflower-page">Cauliflower (菜花)</a></h3>
  </div>
  <div class="food-item" data-name="Onion (葱)">
    <h3><a href="#onion-page">Onion (葱)</a></h3>
  </div>
  <div class="food-item" data-name="Garlic (大蒜)">
    <h3><a href="#garlic-page">Garlic (大蒜)</a></h3>
  </div>
  <div class="food-item" data-name="Beans (豆角)">
    <h3><a href="#beans-page">Beans (豆角)</a></h3>
  </div>
  <div class="food-item" data-name="Winter melon (冬瓜)">
    <h3><a href="#winter-melon-page">Winter melon (冬瓜)</a></h3>
  </div>
  <div class="food-item" data-name="Carrots (胡萝卜)">
    <h3><a href="#carrots-page">Carrots (胡萝卜)</a></h3>
  </div>
  <div class="food-item" data-name="Cucumbers (黄瓜)">
    <h3><a href="#cucumbers-page">Cucumbers (黄瓜)</a></h3>
  </div>
  <div class="food-item" data-name="Ginger (姜)">
    <h3><a href="#ginger-page">Ginger (姜)</a></h3>
  </div>
  <div class="food-item" data-name="Leek (韭菜)">
    <h3><a href="#leek-page">Leek (韭菜)</a></h3>
  </div>
  <div class="food-item" data-name="Pepper (辣椒)">
    <h3><a href="#pepper-page">Pepper (辣椒)</a></h3>
  </div>
  <div class="food-item" data-name="Radish (萝卜)">
    <h3><a href="#radish-page">Radish (萝卜)</a></h3>
  </div>
  <div class="food-item" data-name="Eggplant (茄子)">
    <h3><a href="#eggplant-page">Eggplant (茄子)</a></h3>
  </div>
  <div class="food-item" data-name="Bell peppers (青椒)">
    <h3><a href="#bell-peppers-page">Bell peppers (青椒)</a></h3>
  </div>
  <div class="food-item" data-name="Luffa (丝瓜)">
    <h3><a href="#luffa-page">Luffa (丝瓜)</a></h3>
  </div>
  <div class="food-item" data-name="Garland chrysanthemum (茼蒿)">
    <h3><a href="#garland-chrysanthemum-page">Garland chrysanthemum (茼蒿)</a></h3>
  </div>
  <div class="food-item" data-name="Tomatoes (西红柿)">
    <h3><a href="#tomatoes-page">Tomatoes (西红柿)</a></h3>
  </div>
  <div class="food-item" data-name="Broccoli (西兰花)">
    <h3><a href="#broccoli-page">Broccoli (西兰花)</a></h3>
  </div>
  <div class="food-item" data-name="Onion (洋葱)">
    <h3><a href="#onion-page">Onion (洋葱)</a></h3>
  </div>
  <div class="food-item" data-name="Rapeseed (油菜)">
    <h3><a href="#rapeseed-page">Rapeseed (油菜)</a></h3>
  </div>
  <div class="food-item" data-name="Taro (芋头)">
    <h3><a href="#taro-page">Taro (芋头)</a></h3>
  </div>
    <div class="food-item" data-name="Sichuan vegetable (榨菜)">
    <h3><a href="#sichuan-vegetable-page">Sichuan vegetable (榨菜)</a></h3>
  </div>
  <div class="food-item" data-name="Apple (苹果)">
    <h3><a href="#apple-page">Apple (苹果)</a></h3>
  </div>
  <div class="food-item" data-name="Banana (香蕉)">
    <h3><a href="#banana-page">Banana (香蕉)</a></h3>
  </div>
  <div class="food-item" data-name="Strawberry (草莓)">
    <h3><a href="#strawberry-page">Strawberry (草莓)</a></h3>
  </div>
  <div class="food-item" data-name="Orange (橙子)">
    <h3><a href="#orange-page">Orange (橙子)</a></h3>
  </div>
  <div class="food-item" data-name="Olive (橄榄)">
    <h3><a href="#olive-page">Olive (橄榄)</a></h3>
  </div>
  <div class="food-item" data-name="Mandarin (柑橘)">
    <h3><a href="#mandarin-page">Mandarin (柑橘)</a></h3>
  </div>
  <div class="food-item" data-name="Grapes (葡萄)">
    <h3><a href="#grapes-page">Grapes (葡萄)</a></h3>
  </div>
  <div class="food-item" data-name="Cantaloupe (哈密瓜)">
    <h3><a href="#cantaloupe-page">Cantaloupe (哈密瓜)</a></h3>
  </div>
  <div class="food-item" data-name="Pitaya (火龙果)">
    <h3><a href="#pitaya-page">Pitaya (火龙果)</a></h3>
  </div>
  <div class="food-item" data-name="Tangerine (橘子)">
    <h3><a href="#tangerine-page">Tangerine (橘子)</a></h3>
  </div>
  <div class="food-item" data-name="Pear (梨)">
    <h3><a href="#pear-page">Pear (梨)</a></h3>
  </div>
  <div class="food-item" data-name="Durian (榴莲)">
    <h3><a href="#durian-page">Durian (榴莲)</a></h3>
  </div>
  <div class="food-item" data-name="Blueberry (蓝莓)">
    <h3><a href="#blueberry-page">Blueberry (蓝莓)</a></h3>
  </div>
  <div class="food-item" data-name="Mango (芒果)">
    <h3><a href="#mango-page">Mango (芒果)</a></h3>
  </div>
  <div class="food-item" data-name="Kiwi (猕猴桃)">
    <h3><a href="#kiwi-page">Kiwi (猕猴桃)</a></h3>
  </div>
  <div class="food-item" data-name="Lemon (柠檬)">
    <h3><a href="#lemon-page">Lemon (柠檬)</a></h3>
  </div>
  <div class="food-item" data-name="Grapefruit (葡萄柚)">
    <h3><a href="#grapefruit-page">Grapefruit (葡萄柚)</a></h3>
  </div>
  <div class="food-item" data-name="Kiwifruit (奇异果)">
    <h3><a href="#kiwifruit-page">Kiwifruit (奇异果)</a></h3>
  </div>
  <div class="food-item" data-name="Persimmon (柿子)">
    <h3><a href="#persimmon-page">Persimmon (柿子)</a></h3>
  </div>
  <div class="food-item" data-name="Mulberry (桑葚)">
    <h3><a href="#mulberry-page">Mulberry (桑葚)</a></h3>
  </div>
  <div class="food-item" data-name="Peach (桃子)">
    <h3><a href="#peach-page">Peach (桃子)</a></h3>
  </div>
  <div class="food-item" data-name="Watermelon (西瓜)">
    <h3><a href="#watermelon-page">Watermelon (西瓜)</a></h3>
  </div>
  <div class="food-item" data-name="Cherry (樱桃)">
    <h3><a href="#cherry-page">Cherry (樱桃)</a></h3>
  </div>
  <div class="food-item" data-name="

  // 初始加载第一个主题
  loadTheme('水果');
  loadTheme('蔬菜');
  loadTheme('其他');
</script>
