A more complex 脚手架 demo。
forked from: https://gitee.com/zhutouqietuzai/simple-cli


【关于 glob 库】
`glob` 是一个 Node.js 库，用于使用模式匹配来搜索文件路径。它是基于正则表达式的匹配算法，允许你指定一个或多个模式（globs），然后它会返回匹配这些模式的文件路径列表。`glob` 库常用于构建系统、自动化脚本、文件操作任务等场景，可以极大地简化文件搜索和操作的复杂性。

### 主要特点：

1. **模式匹配**：可以使用通配符（如 `*`、`?`、`[...]` 等）来指定匹配模式。
   - `*` 匹配任意数量的字符（除了目录分隔符）。
   - `?` 匹配任意单个字符。
   - `[...]` 匹配括号内的任意一个字符。
   - `!` 表示否定模式，排除匹配的文件。

2. **递归搜索**：可以指定是否递归地搜索子目录。

3. **同步和异步操作**：`glob` 库提供了同步和异步两种方式来执行模式匹配。

4. **流式接口**：支持流式接口，可以逐步处理匹配到的文件路径。

5. **缓存机制**：`glob` 库使用缓存来提高性能，避免重复的文件系统操作。

### 使用示例：

下面是一个简单的使用 `glob` 库的示例：

```javascript
const glob = require('glob');

// 异步模式
glob('**/*.js', (err, files) => {
  if (err) {
    console.error(err);
    return;
  }
  console.log('找到的 JavaScript 文件:', files);
});

// 同步模式
const files = glob.sync('**/*.js');
console.log('找到的 JavaScript 文件（同步）:', files);
```

在这个示例中，`glob` 被用来查找当前目录及其子目录下所有的 `.js` 文件。

### 安装：

要使用 `glob` 库，你可以通过 npm 来安装它：

```sh
npm install glob
```

`glob` 是一个非常实用的工具，特别是在处理大量文件和自动化任务时，它可以让你的代码更加简洁和高效。
