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

[VS Code](https://code.visualstudio.com/) это легковесный редактор исходного кода и мощная среда разработки для построения и отладки современных веб, мобтльных, и облачных приложений. It is free and available on your favorite platform - Linux, macOS, and Windows.

If you landed here looking for other information about VS Code, head over to [our website](https://code.visualstudio.com) for additional information.

## Feedback

If you want to give documentation feedback, please use the feedback control located at the bottom of each documentation page.

## Documentation Issues

To enter documentation bugs, please create a [new GitHub issue](https://github.com/microsoft/vscode-docs/issues). Please check if there is an existing issue first.

If you think the issue is with the VS Code product itself, please enter issues in the VS Code product repo [here](https://github.com/microsoft/vscode/issues).

## Contributing

To contribute new topics/information or make changes to existing documentation, please read the [Contributing Guideline](./CONTRIBUTING.md#contributing).

### Workflow

The two suggested workflows are:

- For small changes, use the "Edit" button on each page to edit the Markdown file directly on GitHub.
- If you plan to make significant changes or preview the Markdown files in VS Code, [clone](#cloning) the repo to [edit and preview](https://code.visualstudio.com/docs/languages/markdown) the files directly in VS Code.

![Markdown Preview Button](images/MDPreviewButton.png)

### Cloning

1. Install [Git LFS](https://git-lfs.github.com/).
2. Run `git lfs install` to setup global git hooks. You only need to run this once per machine.
3. SSH auth: `git clone git@github.com:microsoft/vscode-docs.git`<br>HTTPS auth: `git clone https://github.com/microsoft/vscode-docs.git`
4. Now you can `git add` binary files and commit them. They'll be tracked in LFS.

#### Cloning without binary files

You might want to clone the repo without the 1.6GB images. Here are the steps:

1. Install [Git LFS](https://git-lfs.github.com/).
2. Run `git lfs install` to setup global git hooks. You only need to run this once per machine.
3. Clone the repo without binary files.
    - macOS / Linux:
      - SSH auth: `GIT_LFS_SKIP_SMUDGE=1 git clone git@github.com:microsoft/vscode-docs.git`
      - HTTPS auth: `GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/microsoft/vscode-docs.git`
    - Windows:
      - SSH auth: `$env:GIT_LFS_SKIP_SMUDGE="1"; git clone git@github.com:microsoft/vscode-docs.git`
      - HTTPS auth: `$env:GIT_LFS_SKIP_SMUDGE="1"; git clone https://github.com/microsoft/vscode-docs.git`
4. Now you can selectively checkout some binary files to work with. For example:
    - `git lfs pull -I "docs/nodejs"` to only download images in `docs/nodejs`
    - `git lfs pull -I "release-notes/images/1_4*/*"` to only download images in `release-notes/images/1_4*`
    - `git lfs pull -I "docs,api"` to download all images in `docs` and in `api`
    - `git lfs pull -I <PATTERN>`, as long as `<PATTERN>` is a valid [Git LFS Include and Exclude pattern](https://github.com/git-lfs/git-lfs/blob/main/docs/man/git-lfs-fetch.1.ronn#include-and-exclude).

The history of this repo before we adopted LFS can be found at [microsoft/vscode-docs-archive](https://github.com/microsoft/vscode-docs-archive).

## Publishing

Steps for how to publish documentation changes can be found [here](https://github.com/microsoft/vscode-website#publishing-a-documentation-change) in the (private) repository of the VS Code website.
