# 项目工程化配置

## editorconfig

* [官网](http://editorconfig.org)

* vscode需要安装EditorConfig for VS Code插件; HBuilderX需要在设置中将editorConfig启用

有些规则，editorconfig 和 .prettierrc 同时可以定义。因此，我们要避免冗余、重复的定义。这些规则如下：

end_of_line

indent_style

indent_size/tab_width

max_line_length

我们将这些规则的定义，均放在 .editorconfig 中。

如果prettierrc中的options.editorconfig是true并且您的项目中有一个.editorconfig文件，Prettier 将解析它并将其属性转换为相应的 Prettier 配置。但是如果prettierrc中也进行了配置，那么prettier的优先级高。

https://prettier.io/docs/en/configuration.html

## prettier

* [官网](https://prettier.io/)

* 使用vscode插件时无需本地安装prettier
* [eslint-config-prettier](https://github.com/prettier/eslint-config-prettier) ：关闭掉可能与eslint冲突的规则,使eslint对这些规则不进行校验
* [eslint-plugin-prettier](https://github.com/prettier/eslint-plugin-prettier) ：关闭掉坑与eslint冲突的规则，使eslint用prettier的规则进行校验，使用eslint --fix时也会进行修复
* [prettier-eslint](https://github.com/prettier/prettier-eslint) ：使用prettier格式化代码并进行eslint规则校验
* 对于stylelint ，prettier也提供了如上配套的三个库 [stylelint-config-prettier](https://github.com/prettier/stylelint-config-prettier)  [stylelint-prettier](https://github.com/prettier/stylelint-prettier)  [prettier-stylelint](https://github.com/hugomrdias/prettier-stylelint) 

## eslint

* [官网](https://eslint.org/)

* [rule格式](https://eslint.org/docs/latest/user-guide/configuring/rules)

  > * plugin1 === eslint-plugin-plugin1
  > * @jquery/jquery === @jquery/eslint-plugin-jquery
  > * @foobar  === @foobar/eslint-plugin

* [extends格式](https://eslint.org/docs/latest/developer-guide/shareable-configs)

  >* eslint:recommended  === eslint的内置推荐配置
  >* eslint:all === eslint的内置全部配置 
  >* standard === eslint-config-standard
  >* plugin:react/recommended === plugin:eslint-plugin-react/recommended 
  >* plugin:prettier/recommended === plugin:eslint-plugin-prettier/recommended 
  >* prettier/prettier === eslint-config-prettier/prettier
  >* @vue/typescript/recommended === @vue/eslint-config-typescript/recommended 
  >* @vue/prettier === @vue/eslint-config-prettier

## stylelint

* [官网](https://stylelint.io/)
* 配置原理基本和eslint一致

## husky

* [官网](https://typicode.github.io/husky)

## lint-staged

* [官网](https://www.npmjs.com/package/lint-staged)
* 只对暂存区的文件进行lint

## commitlint

* [官网](https://commitlint.js.org/)
* @commitlint/cli 对提交信息进行lint
* @commitlint/config-conventional  配置了规则
* @commitlint/prompt-cli 可以进行提示