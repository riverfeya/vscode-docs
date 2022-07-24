<p align="center">
  <img alt="vscode logo" src="images/logo-stable.png" width="100px" />
  <h1 align="center">Документиация Visual Studio Code</h1>
</p>

Это GitHub реппозиторий Visual Studio Code, который содержит контент для [Visual Studio Code documentation](https://code.visualstudio.com/docs).

Представленные здесь темы будут опубликованы на портале [Visual Studio Code](https://code.visualstudio.com).

Если вы ищете репозиторий продукта VS-code GitHub, вы можете его найти его [здесь](https://github.com/microsoft/vscode).

>**Note**: реппозиторий vscode-docs использует [Git LFS](https://git-lfs.github.com/) (Large File Storage) для хранения бинарных файловтаких как картинки и `.gif`ки. Если вы вкладываете или обновляете изображения, пожалуйста, включите GIT LFS по инструкциям в разделе [Contributing](#cloning).

## Index

- [Index](#index)
- [Visual Studio Code](#visual-studio-code)
- [Feedback](#feedback)
- [Documentation Issues](#documentation-issues)
- [Contributing](#contributing)
  - [Workflow](#workflow)
  - [Cloning](#cloning)
    - [Cloning without binary files](#cloning-without-binary-files)
- [Publishing](#publishing)

## Visual Studio Code

[VS Code](https://code.visualstudio.com/) это легковесный редактор исходного кода и мощная среда разработки для построения и отладки современных веб, мобильных, и облачных приложений. Он свободный и доступен для вашей платформы - Linux, macOS, и Windows.

Если вы попали сюда в поиске другой информации о VS-code, пройдите на [наш сайт](https://code.visualstudio.com) за дополнительной информацией.

## Feedback

Если вы хотите дать обратную связь с документацией, используйте управление обратной связью, расположенную в нижней части каждой страницы документации.

## Documentation Issues

To enter documentation bugs, please create a [new GitHub issue](https://github.com/microsoft/vscode-docs/issues). Please check if there is an existing issue first.

If you think the issue is with the VS Code product itself, please enter issues in the VS Code product repo [here](https://github.com/microsoft/vscode/issues).

## Contributing

To contribute new topics/information or make changes to existing documentation, please read the [Contributing Guideline](./CONTRIBUTING.md#contributing).

### Workflow

Два предложенных рабочих процесса:

- For small changes, use the "Edit" button on each page to edit the Markdown file directly on GitHub.
- If you plan to make significant changes or preview the Markdown files in VS Code, [clone](#cloning) the repo to [edit and preview](https://code.visualstudio.com/docs/languages/markdown) the files directly in VS Code.

![Markdown Preview Button](images/MDPreviewButton.png)

### Cloning

1. Установка [Git LFS](https://git-lfs.github.com/).
2. Запуск `git lfs install` для настройки глобальных хуков GIT. Вам нужно запустить только один раз на машину.
3. SSH аутентификация: `git clone git@github.com:microsoft/vscode-docs.git`<br>HTTPS авторизация: `git clone https://github.com/microsoft/vscode-docs.git`
4. Теперь вы можете `git add` бинарные файлы и коммитнуть их. Тогда они будут отслеживаться LFS.

#### Клонирование без бинарных файлов

Вы можете клонировать репо без изображений 1,6 ГБ. Вот шаги:

1. Устанвите [Git LFS](https://git-lfs.github.com/).
2. Запустите `git lfs install` для настройки глобального хука git. Вам нужно запустить только один раз на машину.
3. Клонировать репо без двоичных файлов.
    - macOS / Linux:
      - SSH авторизация: `GIT_LFS_SKIP_SMUDGE=1 git clone git@github.com:microsoft/vscode-docs.git`
      - HTTPS авторизация: `GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/microsoft/vscode-docs.git`
    - Windows:
      - SSH авторизация: `$env:GIT_LFS_SKIP_SMUDGE="1"; git clone git@github.com:microsoft/vscode-docs.git`
      - HTTPS авторизация: `$env:GIT_LFS_SKIP_SMUDGE="1"; git clone https://github.com/microsoft/vscode-docs.git`
4. Теперь вы можете выборочно оформить некоторые двоичные файлы для работы с ними. Например:
    - `git lfs pull -I "docs/nodejs"` для загрузки изображений только `docs/nodejs`
    - `git lfs pull -I "release-notes/images/1_4*/*"` для загрузки изображений только из `release-notes/images/1_4*`
    - `git lfs pull -I "docs,api"` для загрузки всех изображений из `docs` и `api`
    - `git lfs pull -I <PATTERN>`, as long as `<PATTERN>` is a valid [Git LFS Include and Exclude pattern](https://github.com/git-lfs/git-lfs/blob/main/docs/man/git-lfs-fetch.1.ronn#include-and-exclude).

The history of this repo before we adopted LFS can be found at [microsoft/vscode-docs-archive](https://github.com/microsoft/vscode-docs-archive).

## Publishing

Steps for how to publish documentation changes can be found [here](https://github.com/microsoft/vscode-website#publishing-a-documentation-change) in the (private) repository of the VS Code website.
