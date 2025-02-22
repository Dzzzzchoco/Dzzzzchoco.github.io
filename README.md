
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
      // ... (蔬菜主题内容)
      break;
    case '水果':
      // ... (水果主题内容)
      break;
    case '其他':
      // ... (其他主题内容)
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
