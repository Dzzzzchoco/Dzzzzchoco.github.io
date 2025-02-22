A First Level Header
====================

A Second Level Header
---------------------

Now is the time for all good men to come to
the aid of their country. This is just a
regular paragraph.

The quick brown fox jumped over the lazy
dog's back.

### Header 3

> This is a blockquote.
> 
> This is the second paragraph in the blockquote.
>
> ## This is an H2 in a blockquote

# 网站搜索

## 搜索框

<form id="search-form">
  <input type="text" id="search-input" placeholder="输入关键词...">
  <button type="submit">搜索</button>
</form>

## 搜索结果

<div id="search-results">
  </div>

## JavaScript 代码 (示例)

```javascript
document.getElementById('search-form').addEventListener('submit', function(event) {
  event.preventDefault(); // 阻止表单默认提交行为
  const searchTerm = document.getElementById('search-input').value;
  performSearch(searchTerm);
});

function performSearch(searchTerm) {
  // 在此处编写搜索逻辑，例如：
  // 1. 从网站内容中搜索匹配项
  // 2. 将搜索结果显示在 #search-results 元素中
  const results = searchWebsiteContent(searchTerm); // 假设有一个搜索函数
  displayResults(results);
}

function searchWebsiteContent(searchTerm) {
  // 示例搜索函数，实际中需要根据网站内容进行调整
  const websiteContent = document.body.innerText; // 获取网站所有文本内容
  const results = [];
  const regex = new RegExp(searchTerm, 'gi'); // 创建正则表达式，忽略大小写
  let match;
  while ((match = regex.exec(websiteContent)) !== null) {
    results.push({
      text: websiteContent.substring(match.index - 50, match.index + 50), // 获取匹配文本前后各 50 个字符
      index: match.index
    });
  }
  return results;
}

function displayResults(results) {
  const resultsDiv = document.getElementById('search-results');
  resultsDiv.innerHTML = ''; // 清空之前的搜索结果
  if (results.length === 0) {
    resultsDiv.innerHTML = '<p>未找到匹配结果。</p>';
    return;
  }
  const ul = document.createElement('ul');
  results.forEach(result => {
    const li = document.createElement('li');
    li.textContent = result.text;
    ul.appendChild(li);
  });
  resultsDiv.appendChild(ul);
}
