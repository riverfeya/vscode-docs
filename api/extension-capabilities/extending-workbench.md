---
# DO NOT TOUCH — Managed by doc writer
ContentId: e0d5bd37-f020-4235-ad81-c977baaeb24f
DateApproved: 7/7/2022

# Summarize the whole topic in less than 300 characters for SEO purpose
MetaDescription: Explain how to extend Visual Studio Code's workbench area with custom UI components
---

# Расширение Workbench

«Workbench» относится к общему пользовательскому интерфейсу кода Visual Studio, который охватывает следующие компоненты пользовательского интерфейса:

- Title Bar
- Activity Bar
- Side Bar
- Panel
- Editor Group
- Status Bar

VS Code предоставляет различные API, которые позволяют добавлять свои собственные компоненты в Workbench.

![workbench-contribution](images/extending-workbench/workbench-contribution.png)

- Activity Bar: The [Azure App Service extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureappservice) adds a [View Container](#views-container)
- Side Bar: The built-in [NPM extension](https://github.com/microsoft/vscode/tree/main/extensions/npm) adds a [Tree View](#tree-view) to the Explorer View
- Editor Group: The built-in [Markdown extension](https://github.com/microsoft/vscode/tree/main/extensions/markdown-language-features) adds a [Webview](#webview) next to other editors in the Editor Group
- Status Bar: The [VSCodeVim extension](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim) adds a [Status Bar Item](#status-bar-item) in the Status Bar

## Views Container

With the [`contributes.viewsContainers`](/api/references/contribution-points#contributes.viewsContainers) Contribution Point, you can add new Views Containers that display next to the five built-in Views Containers. Learn more at the [Tree View](/api/extension-guides/tree-view) topic.

## Tree View

With the [`contributes.views`](/api/references/contribution-points#contributes.views) Contribution Point, вы можете добавить новые Views которые будут отображаться в любом из View Containers. Узнайте больше в [Tree View](/api/extension-guides/tree-view).

## Webview

Webviews высоко кастомизированые views построенные на HTML/CSS/JavaScript. Они отображают рядом с редакторами текста в областях группы редакторов. Почитайте больше о Webview в [Webview guide](/api/extension-guides/webview).

## Status Bar Item

Extensions могут создавать кастомные [`StatusBarItem`](/api/references/vscode-api#StatusBarItem) который отображается в строке состояния. Элементы строки состояния могут отображать текст и значки и запускать команды на событиях клика.

- Отображать текст и иконки
- Запустить команду по клику

Вы можете узнать больше, просмотрев [примеры Status Bar](https://github.com/microsoft/vscode-extension-samples/tree/main/statusbar-sample).
