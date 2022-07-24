---
# DO NOT TOUCH — Managed by doc writer
ContentId: AD26EFB1-FFC6-4284-BAB8-F3BCB8294728
DateApproved: 7/7/2022

# Summarize the whole topic in less than 300 characters for SEO purpose
MetaDescription: Visual Studio Code has a rich extension API. Learn how to create your own extensions for VS Code.
---

# Extension API

Visual Studio код создан с учетом расширяемости. От пользовательского интерфейса до опыта редактирования, почти каждая часть VS -кода может быть настроена и улучшена с помощью API расширения. На самом деле, многие основные функции кода VS созданы как [расширения](https://github.com/microsoft/vscode/tree/main/extensions) и используют то же Extension API.

Эта документация описывает:

* Как построить, запускать, отлаживать, тестировать и публиковать расширение
* Как воспользоваться API расширения VS Code
* Где найти [руководства](https://code.visualstudio.com/api/extension-guides/overview) и [примеры кода](https://github.com/microsoft/vscode-extension-samples) Чтобы помочь вам начать
* Следуйте нашему [UX гайдлайну](/api/ux-guidelines/overview) лучших практик

Образцы кода доступны на [Microsoft/vscode-extension-samples](https://github.com/microsoft/vscode-extension-samples).

Если вы ищете опубликованные расширения, отправляйтесь в [Маркетплэйс расширений VS Code](https://marketplace.visualstudio.com/vscode).

## Что могут делать расширения?

Вот несколько примеров того, чего вы можете достичь с помощью API расширения:

* Измените внешний вид VS code с темой значка цвета или файла - [Theming](/api/extension-capabilities/theming)
* Добавить пользовательские компоненты и представления в UI - [Extending the Workbench](/api/extension-capabilities/extending-workbench)
* Создайте WebView для отображения пользовательской веб-страницы, созданной с HTML/CSS/JS - [Webview Guide](/api/extension-guides/webview)
* Поддерживать новый язык программирования - [Language Extensions Overview](/api/language-extensions/overview)
* Поддержка отладки определенной среды выполнения - [Debugger Extension Guide](/api/extension-guides/debugger-extension)

If you'd like to have a more comprehensive overview of the Extension API, refer to the [Extension Capabilities Overview](/api/extension-capabilities/overview) page. [Extension Guides Overview](/api/extension-guides/overview) also includes a list of code samples and guides that illustrate various Extension API usage.

## Как создать расширения?

Создание хорошего расширения может занять много времени и усилий.

* **Get Started** преподает фундаментальные концепции для продления строительства с [Hello World](https://github.com/microsoft/vscode-extension-samples/tree/main/helloworld-sample) примера.
* **Extension Capabilities** Рассматривает обширный API code в более мелкие категории и указывает на более подробные темы.
* **Extension Guides** Включает в себя руководства и образцы кода, которые объясняют конкретные использование API расширения VS Code.
* **UX Guidelines** демонстрирует лучшие практики для обеспечения отличного пользовательского опыта в расширении.
* **Language Extensions** Иллюстрирует, как добавить поддержку языка программирования с помощью гидов и образцов кода.
* **Testing and Publishing** включает в себя подробные руководства по различным темам развития расширения, например [testing](/api/working-with-extensions/testing-extension) и [publishing](/api/working-with-extensions/publishing-extension) расширений.
* **Advanced Topics** объясняет передовые понятия, такие как [Extension Host](/api/advanced-topics/extension-host), [Supporting Remote Development and GitHub Codespaces](/api/advanced-topics/remote-extensions), и [Proposed API](/api/advanced-topics/using-proposed-api).
* **References** содержит исчерпывающие ссылки для [VS Code API](/api/references/vscode-api), [Contribution Points](/api/references/contribution-points), и многие другие темы.

## Что нового?

VS Code updates on a monthly cadence, and that applies to the Extension API as well. New features and APIs become available every month to increase the power and scope of VS Code extensions.

To stay current with the Extension API, you can review the monthly release notes, which have dedicated sections covering:

* [Extension authoring](https://code.visualstudio.com/updates#_extension-authoring) - Learn what new extension APIs are available in the latest release.
* [Proposed extension APIs](https://code.visualstudio.com/updates#_proposed-extension-apis) - Review and give feedback on upcoming proposed APIs.

## Looking for help

If you have questions for extension development, try asking on:

* [VS Code Discussions](https://github.com/microsoft/vscode-discussions): GitHub community to discuss VS Code's extension platform, ask questions, help other members of the community, and get answers.
* [Stack Overflow](https://stackoverflow.com/questions/tagged/visual-studio-code): There are [thousands of questions](https://stackoverflow.com/questions/tagged/visual-studio-code) tagged `visual-studio-code`, and over half of them already have answers. Search for your issue, ask questions, or help your fellow developers by answering VS Code extension development questions!
* [VS Code Dev Slack](https://aka.ms/vscode-dev-community): Public chatroom for extension developers. VS Code team members often join in the conversations.

To provide feedback on the documentation, create new issues at [Microsoft/vscode-docs](https://github.com/microsoft/vscode-docs/issues).
If you have extension questions that you cannot find an answer for, or issues with the VS Code Extension API, please open new issues at [Microsoft/vscode](https://github.com/microsoft/vscode/issues).
