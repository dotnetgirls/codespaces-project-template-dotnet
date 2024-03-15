[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=education/codespaces-project-template-dotnet) 

# GitHub Codespaces로 닷넷 (Blazor) 포트폴리오 사이트 만들기 

_빠르게 개인 포트폴리오 사이트를 생성하는 것부터 커스텀과 배포까지 모두 가능합니다._ ✨

이 리포지토리에는 개발할 수 있는 환경과 기본 포트폴리오 양식이 있어, 바로 포트폴리오 사이트를 제작 가능합니다. Codespaces를 바로 실행해서 개발 환경 셋팅 과정없이 포트폴리오 사이트 양식을 커스텀해 보겠습니다.


- **누구를 대상으로 하나요?** __모두__ 포트폴리오 사이트를 만들고 싶거나, 웹 개발을 배우고 싶거나, Codespaces를 사용해보고 싶은 모든 사람들이 대상입니다.
- **관련 경험이 있어야 하나요?** __필요 없음__. 관련 경험 유무와 얼마나 여유 시간이 있는지에 따라, 기본 포트폴리오 양식을 어느 정도 커스텀할지 결정 가능합니다.
- **필요한 준비물 :** _없음_. 별도로 설치할 것이 없습니다! 웹 브라우저(Edge, Chrome 등)만 있으면 됩니다.
- **전제 조건:** _없음_. 이 양식은 개인 포트폴리오 사이트를 만들 수 있는 개발 환경과 배포할 수 있는 웹 앱으로 이루어져 있습니다.
## 포트폴리오 사이트 양식에 대해서

    
이 "choose your own adventure" 포트폴리오 양식에는 웹 브라우저만 있으면 쉽게 사용자를 지정하고 배포할 수 있는, [Blazor](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor?WT.mc_id=dotnet-82024-juyoo) 웹 어플리케이션이 있습니다.

![Blazor WebAssembly profile web application](./images/blazorwasm-portfolio-site.gif "Blazor WebAssembly profile web application")

### 빠르게 시작하기

1.  **Use this Template** 버튼을 클릭합니다.  <br> [![Use this Template](/images/template-button.svg)](https://github.com/education/codespaces-project-template-dotnet/generate)
1. 리포지토리 소유자를 선택합니다. (예시: 자신의 GitHub 계정)
1. 새 리포지토리의 이름을 입력합니다.
1. **Code** 버튼을 클릭합니다.
1. **Create Codespace on main** 버튼을 클릭합니다.
1. [포트폴리오 사이트 커스텀하기](#-customize-your-site-in-4-steps)
1. [사이트 배포하기](#-deploy-your-web-application)

<details>
   <summary><b>🎥 Codespaces에 대해 자세히 알아보기 위해 튜토리얼 영상 시리즈를 시청 가능합니다.</b></summary>

   [![Codespaces Tutorial](https://img.youtube.com/vi/ozuDPmcC1io/0.jpg)](https://aka.ms/CodespacesVideoTutorial "Codespaces Tutorial")
</details>

<br />

## 🗃️ 닷넷 (**Blazor**) 포트폴리오 양식


이 리포지토리는 Blazor WebAssembly 프레임워크를 사용하여 닷넷 개인 포트폴리오 프론트엔드 웹 애플리케이션을 만들기 위한 GitHub 양식입니다. Codespaces를 통해 개인 웹사이트를 만드는 데 바로 활용할 수 있는 양식을 제공합니다.

이 리포지토리는 다음 내용을 담고 있습니다:

- `/.devcontainer`
  - `.devcontainer/Dockerfile`: 운영 체제 및 기타 세부 정보를 결정하기 위해 Codespaces에서 사용하는 구성 파일
  - `.devcontainer/devcontainer.json` :추가 확장 활성화와 같은 Visual Studio Code 설정을 구성하기 위해 Codespaces에서 사용하는 구성 파일
  - `.devcontainer/on-create.sh`: 추가 확장 활성화와 같은 Visual Studio Code 설정을 구성하기 위해 Codespaces에서 사용하는 구성 파일
- `/src`: 포트폴리오 사이트를 구축하기 위한 Blazor WebAssembly 프로젝트
- `.editorconfig`: Codespaces에서 일관된 코딩 스타일을 유지하는 데 도움이 되는 [EditorConfig](https://editorconfig.org/)에 대한 설정
- `global.json`: 사전 출시된 닷넷넷 버전을 사용하지 않도록 Blazor WebAssembly 앱 설정을 위한 json 파일
- `swa-cli.config.json`: Codespaces에서 Blazor WebAssembly 앱을 실행하기 위한 [Azure SWA CLI](https://azure.github.io/static-web-apps-cli/)에 대한 설정
- `MyPortfolio.sln`: Blazor WebAssembly 애플리케이션 프로젝트가 포함된 솔루션 파일

<br />

## 🚀 시작하기

이 포트폴리오 사이트 프로젝트는 샘플 데이터가 이미 있어, 바로 Codespaces를 열어 웹 앱이 실행이 되는지 확인 가능하고, 언제든지 배포 가능합니다.

시작할 때 필요한 개발 환경이 모두 마련되어 있습니다. [닷넷 Codespaces 양식](https://github.com/education/codespaces-teaching-template-dotnet)을 기반으로 이미 설정된 사용할 수 있는 항목:

- 포트폴리오 사이트의 각 섹션에 대한 구성 요소가 포함된 간단한 [블레이저 WebAssembly](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor?WT.mc_id=dotnet-82024-juyoo) 애플리케이션
- 배포 시 사이트를 구축하기 위한 [SWA CLI](https://azure.github.io/static-web-apps-cli/)
- 코드 일관성을 위해 [EditorConfig](https://editorconfig.org/)를 사용한 코드 린팅 및 형식 지정.

### 개인 포트폴리오 생성하기


1. 이 양식에서 리포지토리를 만듭니다. 이 [리포지토리 링크 생성](https://github.com/education/codespaces-teaching-template-dotnet/generate)을 사용합니다. 리포지토리 소유자를 선택하고, 원하는 경우 이름과 설명을 작성하고, 새 리포지토리를 공개 또는 비공개 중 무엇으로 지정할 것인지 선택합니다.
1. 새로 생성된 리포지토리의 메인 페이지로 이동합니다.
1. 리포지토리 이름 아래에서 코드 드롭다운 메뉴를 사용하고 Codespaces 탭에서 "Create codespace on main"을 선택합니다.

    <img src="./images/new-codespace-button.png" alt="Create codespace" style="width:270px;"/>

1. GitHub에서 Codespaces의 초기화 과정을 기다립니다.

    <img src="./images/codespaces-initializing.png" alt="Codespaces initializing" style="width: 600px;"/>

1. 완료되면 하단에 터미널 섹션과 함께 Codespaces 로드가 표시됩니다. 여기서 `dotnet Restore && dotnet build`가 실행되는 것을 볼 수 있습니다. 완료되면 `swa start`를 실행하여 웹 애플리케이션을 실행할 수 있는 터미널 프롬프트로 돌아갑니다.

   웹 애플리케이션이 시작되면 **포트 4280에서 성공적으로 앱이 시작됐다**는 메시지가 나타나고 브라우저 내에서 해당 사이트를 열 수 있습니다. 

   <img src="./images/app-running-in-codespaces.png" alt="Web application started on port 4280" style="width: 340px;"/>

<br />

## ✨ 사이트를 4단계에 걸쳐 커스텀하기

이 프로젝트는 쉽게 커스텀할 수 있도록 제작되었습니다. 사이트의 각 섹션은 별도의 컴포넌트이며, 여러분의 정보는 한 곳에만 저장해야 합니다. 이렇게 함으로써, 업데이트를 쉽게 할 수 있을 뿐더러 어떤 식으로 Blazor 컴포넌트에 값을 전달하는지 보입니다.
  
각 단계별로 Codespaces에서 프로젝트를 연 다음 Codespaces 내에서 변경하고, 변경 사항을 커밋할 수 있습니다.

> 자세한 Codespaces 원본 제어 방법은 [Codespaces에서 원본 제어 사용](https://docs.github.com/codespaces/developing-in-codespaces/using-source-control-in-your-codespace)을 참조하세요.

### 1️⃣ 세부 정보 및 소셜 미디어 계정 추가하기

`/src/BlazorApp/wwwroot/sample-data/siteproperties.json` 을 엽니다. 이 파일은 이름, 제목, 이메일 및 소셜 미디어 계정을 커스텀하는 데 필요한 키와 키에 해당하는 값을 담고 있는 JSON 객체입니다.

```jsonc
{
  "name": "Alexandrie Grenier",
  "title": "Web Designer & Content Creator",
  "email": "alex@example.com",
  "gitHub": "microsoft",
  "devDotTo": null,
  "instagram": "microsoft",
  "linkedIn": "satyanadella",
  "medium": "",
  "twitter": "microsoft",
  "youTube": "microsoft",
};
```

사이트 맨 위에 표시하고 싶은 이름과 제목으로 내용을 업데이트합니다.

이메일 주소와 소셜 계정 입력은 _선택 사항_ 입니다. `Footer` 컴포넌트에 이것들을 사용합니다. 리스트에 어떤 항목도 포함하지 않거나 빈 문자열 ("")로 설정하면 아이콘과 링크가 나타나지 않습니다.

### 2️⃣ 이미지 업데이트하기

이 포트폴리오 사이트에는 세 가지 이미지가 포함되어 있습니다 : 상단 배경, "About me" 배경, 포트폴리오 섹션(책상 그림). 기본 세가지 이미지들 대신 사용 허락이 없어도 자유롭게 사용할 수 있는 이미지나, 자신이 소유하고 있는 이미지 중 **가로 형태**의 이미지를 사용 가능합니다.

[Pixabay](https://pixabay.com/) 또는 [Unsplash](https://unsplash.com) 같은 사이트에서 사진을 찾을 수 있습니다. 사진, 일러스트, 벡터 이미지 등 원하는 것을 선택합니다. 이미지를 찾으면 각각을 `/src/BlazorApp/wwwroot/images` 에 간결하고 의미있는 파일명으로 저장합니다.

`/src/BlazorApp/wwwroot/sample-data/heroimages.json` 을 열고 여러분이 선호하는 이미지와 각 이미지에 대한 alt 텍스트를 업데이트하세요 :

```jsonc
[
  {
    // Home component
    // section at top of the page, main image you will see when site loads (woman standing by server wall in sample)
    "name": "home",
    "src": "images/server-wall.jpg",
    "alt": "woman holding laptop standing by server room with glass wall"
  },
  {
    // About me component
    // background behind the detailed "about me" section (abstract mosaic in sample)
    "name": "about",
    "src": "images/mosaic.svg",
    "alt": "purple and blue abstract background"
  },
  {
    // Portfolio component
    // image highted in left hand side of section (design desk photo in sample)
    "name": "portfolio",
    "src": "images/design-desk.jpeg",
    "alt": "desktop with books and laptop"
  }
]
```

### 3️⃣ "내 소개" 추가하기

소개 섹션은 사람들에게 여러분의 기술과 관심사에 대해 자세히 알려주는 데 도움이 됩니다. `/src/BlazorApp/wwwroot/sample-data/aboutme.json` 을 열고 다음 세 가지 속성을 업데이트하세요 : 

* `description`: 나 자신, 직업 목표 및 관심사에 대한 짧은 문장 또는 두 문장.
* `skillsList`: 사이트에 나열할 기술의 [배열](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)은 원하는 만큼 작성.
* `detailOrQuote`: 나 자신에 대해 더 많은 세부 정보를 추가하거나 좋아하는 명언을 넣을 수 있는 긴 블록.

### 4️⃣ 작업한 프로젝트를 추가하고 세부 텍스트 입력하기

이 섹션은 포트폴리오를 업데이트하는 곳이며, 여러분이 작업한 프로젝트를 강조합니다. 기사, 비디오, 로고 디자인, 깃허브 프로젝트 등 여러분을 부각하는 내용으로 구성 가능합니다.

JSON 배열인 `/src/BlazorApp/wwwroot/sample-data/projects.json` 을 엽니다. 강조하고 싶은 항목에 다음 내용을 포함하세요 : 제목, 설명 및 URL

샘플 디자인은 4개가 있지만, 여러분이 넣고 싶은 만큼 샘플 디자인 개수를 선택 가능합니다.

```jsonc
[
  {
    "title": "10 Things To Know About Azure Static Web Apps 🎉",
    "description": "Collaboration to create a beginner friendly article to help explain Azure Static Web Apps and tooling to get started.",
    "url": "https://dev.to/azure/10-things-to-know-about-azure-static-web-apps-3n4i"
  },
  {
    "title": "Web Development for Beginners",
    "description": "Contributed sketch note imagery to accompany each lesson. These help provide visual representation of what is being taught.",
    "url": "https://github.com/microsoft/web-dev-for-beginners"
  },
  {
    "title": "My Resume Site",
    "description": "Created from Microsoft's resume workshop and deployed to GitHub pages. Includes my experience and design abilities.",
    "url": "https://github.com/microsoft/workshop-library/tree/main/full/build-resume-website"
  },
  {
    "title": "GitHub Codespaces and github.dev",
    "description": "Video interview to explain when to use GitHub.dev versus GitHub Codespaces, and how best to use each tool.",
    "url": "https://www.youtube.com/watch?v=c3hHhRME_XI"
  }
]
```

<br/>

## 🏃 웹 애플리케이션 배포하기

이 프로젝트는 **무료**로 [Azure 정적 웹앱](https://azure.microsoft.com/products/app-service/static/?WT.mc_id=dotnet-82024-juyoo) 및 [GitHub 페이지](https://pages.github.com/)</a>에 배포할 수 있는 설정이 모두 포함합니다.

### Azure 정적 웹앱

[Azure 정적 웹앱](https://azure.microsoft.com/products/app-service/static/?WT.mc_id=dotnet-82024-juyoo)은 Azure를 통해 정적 사이트(또는 서버가 아닌, 사용자의 브라우저에서 렌더링되는 사이트)를 위한 마이크로소프트의 호스팅 솔루션입니다. 이 서비스의 Azure Functions, 인증, 스테이징 버전 등을 통해 사이트를 확장할 수 있습니다.

웹 애플리케이션을 배포하려면 Azure 계정과 GitHub 계정이 모두 필요합니다. Azure 계정이 아직 없다면, 배포 과정 중에 생성하거나 아래 링크에서 생성하세요 :

* [학생용 Azure 계정을 만들기(신용 카드가 필요 없습니다)](https://azure.microsoft.com/free/students/?WT.mc_id=dotnet-82024-juyoo)
* [새로운 Azure 계정을 만들기](https://azure.microsoft.com/free/?WT.mc_id=dotnet-82024-juyoo)

Codespaces에서 프로젝트가 열린 상태에서:

1. 왼쪽 사이드바의 Azure 아이콘을 클릭합니다. 아직 로그인하지 않았다면 로그인하고, Azure를 처음 사용하는 경우 안내에 따라 계정을 만듭니다.
1. Azure 메뉴에서 "➕" 기호를 누른 다음 "Create Static Web App"을 선택합니다.

   <img src="./images/deploy-to-azure.png" alt="Create Static Web App" style="width: 300px;" />

1. GitHub에 로그인하지 않은 경우 로그인하라는 메시지가 나타납니다. 보류 중인 파일 변경 사항이 있으면 해당 변경 사항을 커밋하라는 메시지가 나타납니다.
1. 메세지가 표시되면 애플리케이션 정보를 설정하세요 :
    1. **Name for Static Web App**: 정적 웹앱의 이름을 입력합니다. 기본값은 GitHub 리포지토리 이름입니다.
    1. **Region**: 여러분의 지역에서 가장 가까운 곳을 고릅니다.
    1. **Project structure**: "Blazor"를 선택합니다.
    1. **Location of application code**: `/src/BlazorApp` 을 입력합니다.
    1. **Output location**: `wwwroot` 를 입력합니다.
1. 완료되면 화면 하단에 알림이 나타나고, 새로운 GitHub Action 워크플로가 프로젝트에 추가됩니다. "Open Action in GitHub"을 클릭하면 생성된 작업을 볼 수 있고, 해당 작업은 현재 실행 중입니다.

> 🤩 **보너스**: [Azure 정적 웹앱에 대한 사용자 정의 도메인 설정하기](https://learn.microsoft.com/shows/azure-tips-and-tricks-static-web-apps/how-to-set-up-a-custom-domain-name-in-azure-static-web-apps-10-of-16--azure-tips-and-tricks-static-w/?WT.mc_id=dotnet-82024-juyoo)

### GitHub 페이지

[GitHub 페이지](https://pages.github.com/)를 사용하면 GitHub 리포지토리에서 직접 웹사이트를 호스팅할 수 있습니다. 이 프로젝트는 간단하게 포트폴리오 사이를 GitHub 페이지에 배포할 수 있습니다.
여러분의 GitHub 리포지토리에서 :

1. "Settings" 탭으로 이동하고 "Pages" 메뉴로 이동합니다.
1. _Build and deployment_ 부분에서, source를 **GitHub Actions**으로 선택합니다.

    <img src="./images/deploy-to-ghpages-01.png" alt="Choose GitHub Actions for deployment to GitHub Pages" style="width: 600px;" />

1. GitHub Pages visibility를 **Public**으로 설정합니다.
1. 코드를 푸시하거나 수동으로 호출하여 GitHub Action 워크플로를 실행합니다.

    <img src="./images/deploy-to-ghpages-02.png" alt="Invoke GitHub Actions" style="width: 600px;" />

1. 여러분의 GitHub 페이지에 접속합니다.

    <img src="./images/deploy-to-ghpages-03.png" alt="Visit GitHub Pages" style="width: 600px;" />

> 🤩 **보너스**: [GitHub 페이지 사이트에 대한 사용자 정의 도메인 설정하기](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

<br />


## 🏆 도전과제

아래는 포트폴리오 사이트를 커스텀하고 Codespaces, CSS, HTML 및 JavaScript를 익힐 수 있는 추가적인 방법 네 가지입니다.

  1. [Codespaces 커스텀하기](#1-customize-your-codespaces)
  1. [부드럽게 섹션으로 이동하기](#2-update-to-smooth-scroll-to-a-section)
  1. [책상 사진에 애니메이션 추가하기](#3-animate-desk-photo)
  1. [새로운 섹션 추가하기](#4-add-a-new-section)

### 1. Codespaces 커스텀하기

환경 파일은 미리 설치된 확장 프로그램을 포함하고 있습니다. Codespaces 환경에서 시작할 때 어떤 확장 프로그램을 사용할지 변경 가능합니다. 다음과 같이 진행하세요:

1. 파일 .devcontainer/devcontainer.json 을 열고 다음 JSON 요소 **extensions**을 찾습니다.

    ```jsonc
    "extensions": [
      "GitHub.copilot",
      "GitHub.copilot-chat",
      "ms-dotnettools.csdevkit",
      "ms-vscode.PowerShell",
      "ms-vscode.vscode-node-azure-pack",
      "VisualStudioExptTeam.vscodeintellicode"
    ]
    ```

1. `indent-rainbow` 확장 프로그램을 추가합니다. 이를 위해 **extensions** 목록으로 이동하여 다음을 추가하세요:

    ```jsonc
    "oderwat.indent-rainbow"
    ```
  
   위 내용은 indent-rainbow의 고유 식별자를 추가한 것입니다. Codespaces를 시작할 때 이 확장 프로그램을 사전 설치해야 합니다.

확장 프로그램의 고유 식별자를 찾으세요:

* 다음 확장 프로그램의 웹 페이지로 이동합니다. [https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow&WT.mc_id=dotnet-82024-juyoo)
* 오른쪽의 **More info** 섹션 아래에서 고유 식별자 필드를 찾습니다.

> 💡 이곳에서 더 배워 보세요 <https://docs.github.com/codespaces/customizing-your-codespace/personalizing-github-codespaces-for-your-account>



### 2. 부드럽게 섹션으로 이동하기

사이트 헤더에는 아래의 각 섹션에 대한 링크가 있습니다. 이 링크 중 하나를 클릭하면 페이지가 해당 섹션으로 스크롤됩니다. 하지만, 스크롤되는 것처럼 보이지 않죠?

사용자가 더 편리하게 사이트를 이용할 수 있도록, 이동 중인 페이지와 무엇이 일어나고 있는지를 느낄 수 있도록 속도를 줄여 봅시다.

1. `/src/BlazorApp/wwwroot/css/app.css`를 엽니다. html에 대한 스타일을 추가해야 합니다. 지금 살펴보면 현재 html 및 body 스타일이 함께 설정되어 있습니다. 따라서 다음 CSS 스니펫을 추가하여 html 요소의 스크롤을 설정하세요:

    ```css
    html {
      scroll-behavior: smooth;
    }
    ```

이미 Codespaces에서 사이트가 실행 중이며 변경 사항이 페이지에 자동으로 다시 로드됩니다. 상단 헤더의 링크를 클릭하여 부드러운 스크롤이 작동하는 것을 확인 가능합니다.



### 3. 책상 사진에 애니메이션 추가

애니메이션은 페이지 요소에 동작을 추가합니다. 이렇게 함으로써, 사용자의 상호작용이 증가하고 특정 항목을 강조할 수 있습니다. 이번에는 포트폴리오 섹션의 책상 사진에 애니메이션을 추가해 보겠습니다.

1. Codespaces 내에서 사이트의 스타일시트인 `/src/BlazorApp/wwwroot/css/app.css`을 엽니다. `@keyframes` 정의를 추가하여 왼쪽에서 슬라이드하는 애니메이션 시퀀스를 추가하세요 :

    ```css
    @keyframes slideInLeft {
      0% {
        transform: translateX(-100%);
      }
      100% {
        transform: translateX(0);
      }
    }
    ```

1. 이제 `slideInLeft` 애니메이션 시퀀스를 정의했으므로, 책상 사진이 해당 에니메이션 시퀀스로 동작합니다. `/src/BlazorApp/Components/Portfolio.razor`를 열고 `img` 태그를 찾습니다. 인라인 CSS를 사용하여 스타일을 설정합니다. 그 스타일 정의 내에 다음을 추가하세요:

    ```css
    animation: 1s ease-out 0s 1 slideInLeft;
    ```

    이미지 태그는 다음과 같아야 합니다:

    ```html
    <img src="@(hero.Src)" style="height: 90%; width: 100%; object-fit: cover; animation: 1s ease-out 0s 1 slideInLeft;" alt="@(hero.Alt)" />
    ```

Codespaces에서 이미 사이트가 실행 중이며 변경 사항이 페이지에 자동으로 다시 로드됩니다. 페이지를 위아래로 스크롤하여 책상 사진이 자연스럽게 나타나는 것을 확인하세요.

> 🤩 **추가 사항**: 스크롤 다운 화살표에 동작을 추가하세요.



### 4. 새로운 섹션 추가하기

기본 섹션으로 포트폴리오 사이트를 이미 만들었지만, 섹션을 추가해 원하는 대로 커스텀 가능합니다.

예를 들어, 포트폴리오 사이트에 교육 섹션을 추가하겠습니다.

1. `Components` 폴더 내에 새로운 섹션을 위한 새 컴포넌트를 만듭니다. `Education.razor`라는 새 파일을 추가합니다.

1. `Education.razor` 에 컴포넌트 기능과 포함하고 싶은 정보를 추가하세요:

    ```razor
    <section class="light" id="portfolio">
        <h2>Education</h2>
    </section>
    ```

1. `Index.razor`에 페이지 내에서 렌더링되길 원하는 위치에 Education 컴포넌트를 추가하세요:

    ```razor
    <Education />
    ```

여러분의 Codespaces에서 포트폴리오 애플리케이션이 실행 중이어야 하며 변경 사항이 사이트에 자동으로 다시 로드될 것입니다.

<br />


## 📚 Resources

* [GitHub Codespaces 문서 개요](https://docs.github.com/codespaces/overview)
* [GitHub Codespaces 가이드](https://docs.github.com/codespaces/guides)
* [VS Code와 Docker를 사용하여 로컬에서 dev containers 사용하기](https://github.com/microsoft/vscode-remote-try-dotnet#vs-code-dev-containers)
* [Blazor 시작하기](https://learn.microsoft.com/training/paths/build-web-apps-with-blazor/?WT.mc_id=dotnet-82024-juyoo)
* [초보자를 위한 웹 개발](https://github.com/microsoft/Web-Dev-For-Beginners)

> #### Codespaces 브라우저 앱
>
> Edge 또는 Chrome을 사용하는 경우, Codespaces를 시작할 때 Codespaces 앱을 설치할 수 있는 옵션이 표시됩니다. Codespaces 앱을 사용하면, 브라우저 외부에서 작업할 수 있습니다.
>
> <img src="./images/codespaces-app.png" alt="Codespaces browser app" style="width: 400px;"/>

<br />

## 🔎 문제 사항을 발견하셨거나 개선 희망 사항이 있나요?

[GitHub Issue 열기](/../../issues/new)를 통해 이 양식 리포지토리가 더 나아지도록 도와주세요!
