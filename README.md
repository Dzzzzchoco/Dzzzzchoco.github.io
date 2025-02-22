
# 网页主题切换示例

## 主题列表

- [蔬菜](#蔬菜)
- [水果](#水果)
- [其他](#其他)

<div id="content">
  </div>

<script>
  function loadTheme(themeId) {
    let contentDiv = document.getElementById('content');
    let themeContent = '';

    switch (themeId) {
      case '蔬菜':
        themeContent = `
          <h2>蔬菜</h2>
          <ul>
            <li><a href="#蔬菜-子主题一" onclick="loadSubTheme('蔬菜-子主题一'); return false;">叶菜类</a></li>
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
  loadTheme('蔬菜');
</script>
