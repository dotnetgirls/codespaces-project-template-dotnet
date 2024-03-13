[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=education/codespaces-project-template-dotnet) 

# .NET (Blazor) Portfolio Site with GitHub Codespaces

_Create, customize and deploy your own portfolio website in minutes._ ✨

In this template repository we have the development environment and base set and ready to go. So that you can immediately launch the Codespaces to customize with no setup.

- **Who is this for?** __Anyone__ looking to create a portfolio site, learn web development, or test out Codespaces.
- **How much experience do you need?** __Zero__. You decide how much you want to customize based on your experience, and time available.
- **Tools needed:** _None_. No need to install anything! All you need is a web browser.
- **Prerequisites:** _None_. This template includes your development environment and deployable web app for you to create your own site.

## About this portfolio template

In this "choose your own adventure" template portfolio, we have a [Blazor](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor?WT.mc_id=dotnet-82024-juyoo) based web application ready for you to easily customize and deploy using only your web browser.  

![Blazor WebAssembly profile web application](./images/blazorwasm-portfolio-site.gif "Blazor WebAssembly profile web application")

### Quick Start

1. Click the **Use this Template** button

   [![Use this Template](/images/template-button.svg)](https://github.com/education/codespaces-project-template-dotnet/generate)

1. Select the repository owner (e.g. your GitHub account)
1. Enter a unique name for your new repository
1. Click the **Code** button
1. Click **Create Codespace on main** button
1. [Customize your portfolio site](#-customize-your-site-in-4-steps)
1. [Deploy your site](#-deploy-your-web-application)

<details>
   <summary><b>🎥 To learn more about Codespaces, watch our video tutorial series</b></summary>

   [![Codespaces Tutorial](https://img.youtube.com/vi/ozuDPmcC1io/0.jpg)](https://aka.ms/CodespacesVideoTutorial "Codespaces Tutorial")
</details>

<br />

## 🗃️ .NET (Blazor) Portfolio template

This repo is a GitHub template to build a .NET personal portfolio frontend web application using the Blazor WebAssembly framework. The goal is to give you a template to you can immediately utilize to create your own website through Codespaces.

The repo contains the following:

- `/.devcontainer`
  - `.devcontainer/Dockerfile`: Configuration file used by Codespaces to determine operating system and other details.
  - `.devcontainer/devcontainer.json`: Configuration file used by Codespaces to configure Visual Studio Code settings, such as the enabling of additional extensions.
  - `.devcontainer/on-create.sh`: Configuration file used by Codespaces to install additional tools, such as PowerShell.
- `/src`: Blazor WebAssembly project to build your portfolio site.
- `.editorconfig`: Settings for [EditorConfig](https://editorconfig.org/) that helps maintain consistent coding styles in Codespaces.
- `global.json`: Settings for the Blazor WebAssembly app to avoid using pre-released .NET version.
- `swa-cli.config.json`: Settings for [Azure SWA CLI](https://azure.github.io/static-web-apps-cli/) to run the Blazor WebAssembly app on your Codespaces.
- `MyPortfolio.sln`: The solution file that contains the Blazor WebAssembly application project.

<br />

## 🚀 Getting started

This portfolio site project is filled with sample data so that you can immediately open Codespaces, see it running, and deploy at any point.

Your development environment is all set for you to start. Based on our [.NET Codespaces Template](https://github.com/education/codespaces-teaching-template-dotnet), here is what's already setup and ready for you to use:

- Simple [Blazor WebAssembly](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor?WT.mc_id=dotnet-82024-juyoo) application with components for each section of the portfolio site
- [SWA CLI](https://azure.github.io/static-web-apps-cli/) in place to build your site when deploying
- Code linting and formatting using [EditorConfig](https://editorconfig.org/) for code consistency.

### Create your portfolio

1. Create a repository from this template. Use this [create repo link](https://github.com/education/codespaces-teaching-template-dotnet/generate). Select the repository owner, provide a name, a description if you'd like and if you'd like the new repository to be public or private.
1. Navigate to the main page of the newly created repository.
1. Under the repository name, use the Code drop-down menu, and in the Codespaces tab, select "Create codespace on main".

    <img src="./images/new-codespace-button.png" alt="Create codespace" style="width:270px;"/>

1. Wait as GitHub initializes the Codespaces.

    <img src="./images/codespaces-initializing.png" alt="Codespaces initializing" style="width: 600px;"/>

1. When complete you will see your Codespaces load with a terminal section at the bottom. Here you will see `dotnet restore && dotnet build` executing. When complete you will return to the terminal prompt where you can run the web application by executing: `swa start`.

   When the web application is started you will see a prompt telling you it started successfully on port 4280, and you can open that site within your browser:

   <img src="./images/app-running-in-codespaces.png" alt="Web application started on port 4280" style="width: 340px;"/>

<br />

## ✨ Customize your site in 4 steps

This project is built to be easily customizable. Each section of the site is a separate component, and your information needs to be set in only one spot. This is not only for ease of updating, but so you can see how values are passed to Blazor components.

For each step, open the project in Codespaces, then you can make and commit your changes while within your Codespaces.

> See [Using source control in your codespaces](https://docs.github.com/codespaces/developing-in-codespaces/using-source-control-in-your-codespace) for more Codespaces source control how-tos

### 1️⃣ Add your details and social media accounts

Open `/src/BlazorApp/wwwroot/sample-data/siteproperties.json`. This is a JSON object that hold the key value pairs needed to customize your name, title, email, and social media accounts.

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

Update to the name and title you'd like displayed at the top of your site.

_Optional values_ are email address and social accounts. These are used in the `Footer` component. If any item is not included in the list or set to an empty string ("") it will not display the icon and link.

### 2️⃣ Update images

This portfolio site includes 3 images: top section background, "About me" background and portfolio section (desk). These can be any **landscape** sized images of your choosing from your own collection, or found that have a license allowing you to use without attribution.

A couple possible sites to find photos are [Pixabay](https://pixabay.com/) and [Unsplash](https://unsplash.com). Photos, illustrations, vectors, your choice! When you find your images, save each one to `/src/BlazorApp/wwwroot/images` with a short, meaningful file name.

Open `/src/BlazorApp/wwwroot/sample-data/heroimages.json` and update images with your preferred ones, as well as the alt text for each image:

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

### 3️⃣ Add your "about me"

The about section helps to give people a bit more information about your skills and passions. Open `/src/BlazorApp/wwwroot/sample-data/aboutme.json` and update those 3 properties:

* `description`: short sentence or two describing yourself, career goal, and/or passions
* `skillsList`: an [array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) of your skills to list on the site, can be as many or little as you wish
* `detailOrQuote`: longer block for you to add more detail about yourself, or even a quote you like

### 4️⃣ Add items you've worked on and detail text

This section to update is portfolio, where you highlight items you've worked on. These would be articles, videos, logo designs, GitHub projects, anything that highlights you!

Open `/src/BlazorApp/wwwroot/sample-data/projects.json` that is a JSON array. Each item you want to highlight needs: title, description, and URL.

The sample design has 4, but the number you include is up to you.

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

## 🏃 Deploy your web application

Project includes the setup needed for you to deploy **free** to both [Azure Static Web Apps](https://azure.microsoft.com/products/app-service/static/?WT.mc_id=dotnet-82024-juyoo) and [GitHub Pages](https://pages.github.com/)</a>.

### Azure Static Web Apps

[Azure Static Web Apps](https://azure.microsoft.com/products/app-service/static/?WT.mc_id=dotnet-82024-juyoo) is Microsoft's hosting solution for static sites (or sites that are rendered in the user's browser, not on a server) through Azure. This service provides additional opportunities to expand your site through Azure Functions, authentication, staging versions and more.

You'll need both Azure and GitHub accounts to deploy your web application. If you don't yet have an Azure account you can create it from within during the deploy process, or from below links:

* [Create a (no Credit Card required) Azure For Students account](https://azure.microsoft.com/free/students/?WT.mc_id=dotnet-82024-juyoo)
* [Create a new Azure account](https://azure.microsoft.com/free/?WT.mc_id=dotnet-82024-juyoo)

With your project open in Codespaces:

1. Click Azure icon in the left sidebar. Log in if you are not already, and if new to Azure, follow the prompts to create your account.
1. From Azure menu click "➕" sign and then choose "Create Static Web App".

   <img src="./images/deploy-to-azure.png" alt="Create Static Web App" style="width: 300px;" />

1. If you are not logged into GitHub you will be prompted to log in. If you have any pending file changes you will then be prompted to commit those changes.
1. Set you application information when prompted:
    1. **Name for Static Web App**: enter the name for the Static Web App. Default to your GitHub repository name.
    1. **Region**: pick the one closest to your region
    1. **Project structure**: select "Blazor"
    1. **Location of application code**: enter `/src/BlazorApp`
    1. **Output location**: enter `wwwroot`
1. When complete you will see notification at the bottom of your screen, and a new GitHub Action workflow will be added to your project. If you click "Open Action in GitHub" you will see the action that was created for you, and it is currently running.

> 🤩 **Bonus**: [Setup a custom domain for your Azure Static Web App](https://learn.microsoft.com/shows/azure-tips-and-tricks-static-web-apps/how-to-set-up-a-custom-domain-name-in-azure-static-web-apps-10-of-16--azure-tips-and-tricks-static-w/?WT.mc_id=dotnet-82024-juyoo)

### GitHub Pages

[GitHub Pages](https://pages.github.com/) allows you to host websites directly from your GitHub repository. This project is already set up for you to get your portfolio deployed to GitHub pages with minimal steps.

On your GitHub repository:

1. Go to the "Settings" tab and navigate to the "Pages" menu.
1. Under the _Build and deployment_ section, select the source to **GitHub Actions**.

    <img src="./images/deploy-to-ghpages-01.png" alt="Choose GitHub Actions for deployment to GitHub Pages" style="width: 600px;" />

1. Ensure your GitHub Pages visibility to **Public**.
1. Run a GitHub Action workflow by pushing code or manually invoke it.

    <img src="./images/deploy-to-ghpages-02.png" alt="Invoke GitHub Actions" style="width: 600px;" />

1. Visit your GitHub Pages.

    <img src="./images/deploy-to-ghpages-03.png" alt="Visit GitHub Pages" style="width: 600px;" />

> 🤩 **Bonus**: [Setup a custom domain for your GitHub pages site](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

<br />


## 🏆 도전과제

아래는 포트폴리오 사이트를 사용자 정의하고 Codespaces, CSS, HTML 및 JavaScript를 익힐 수 있는 추가적인 방법 4가지입니다.

  1. [코드스페이스 사용자 정의하기](#1-customize-your-codespaces)
  1. [부드럽게 섹션으로 이동하기](#2-update-to-smooth-scroll-to-a-section)
  1. [책상 사진에 애니메이션 추가하기](#3-animate-desk-photo)
  1. [새로운 섹션 추가하기](#4-add-a-new-section)

### 1. Codespaces 사용자 정의하기

환경에는 미리 설치된 확장 프로그램이 포함되어 있습니다. 코드스페이스 환경에서 시작할 때 어떤 확장 프로그램을 사용할지 변경할 수 있습니다. 다음과 같이 진행합니다:

1. 파일 .devcontainer/devcontainer.json 을 열고 다음 JSON 요소 extensions 을 찾습니다. **extensions**

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

1. `indent-rainbow` 확장 프로그램을 추가해 봅시다.  이를 위해 **extensions** 목록으로 이동하여 다음을 추가합니다:

    ```jsonc
    "oderwat.indent-rainbow"
    ```
  
   위에서 수행한 것은 indent-rainbow의 고유 식별자를 추가한 것입니다. 이렇게 함으로써 코드스페이스가 시작할 때 이 확장 프로그램이 사전 설치되어야 함을 알 수 있습니다.

확장 프로그램의 고유 식별자를 찾기:

* 다음과 같은 확장 프로그램의 웹 페이지로 이동합니다. [https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow&WT.mc_id=dotnet-82024-juyoo)
* 오른쪽의 **More info** 섹션 아래에서 고유 식별자 필드를 찾습니다.

> 💡 이곳에서 더 배울 수 있습니다. <https://docs.github.com/codespaces/customizing-your-codespace/personalizing-github-codespaces-for-your-account>



### 2. 부드럽게 섹션으로 이동하기

사이트 헤더에는 아래의 각 섹션에 대한 링크가 있습니다. 이 링크 중 하나를 클릭하면 페이지가 해당 섹션으로 스크롤됩니다. 스크롤이라기보다는 바로 이동되는 것처럼 보입니다.

사용자가 무슨 일이 일어나고 있는지, 페이지에서 어디로 이동하는지를 알 수 있도록 이것을 더 나은 사용자 경험으로 만들어봅시다.

1. `/src/BlazorApp/wwwroot/css/app.css`를 엽니다. 우리는 html에 대한 스타일을 추가해야 합니다. 지금 살펴보면 현재 html 및 body 스타일이 함께 설정되어 있습니다. 따라서 다음 CSS 스니펫을 추가하여 html 요소의 스크롤을 설정합시다:

    ```css
    html {
      scroll-behavior: smooth;
    }
    ```

이미 코드스페이스에서 사이트가 실행 중이며 변경 사항이 페이지에 자동으로 다시로드될 것입니다. 상단 헤더의 링크를 클릭하여 부드러운 스크롤이 작동하는 것을 확인할 수 있습니다.



### 3. 책상 사진에 애니메이션 추가

애니메이션은 페이지의 요소에 동작을 추가하여 사용자 상호작용을 증가시키고 강조하고자 하는 항목을 주목할 수 있도록 하는 방법입니다. 이번에는 포트폴리오 섹션의 책상 사진에 애니메이션을 추가해 봅시다.

1. Codespaces 내에서 사이트의 스타일시트인 `/src/BlazorApp/wwwroot/css/app.css`을 엽니다. `@keyframes` 정의를 추가하여 왼쪽에서 슬라이드하는 애니메이션 시퀀스를 추가해봅시다:

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

1. 이제 `slideInLeft` 애니메이션 시퀀스를 정의했으므로, 책상 사진에 해당 시퀀스로 자신을 애니메이트하도록 지시할 수 있습니다. `/src/BlazorApp/Components/Portfolio.razor`를 열고 `img` 태그를 찾으세요. 인라인 CSS를 사용하여 스타일을 설정합니다. 그 스타일 정의 내에 다음을 추가해봅시다:

    ```css
    animation: 1s ease-out 0s 1 slideInLeft;
    ```

    이미지 태그는 다음과 같아야 합니다:

    ```html
    <img src="@(hero.Src)" style="height: 90%; width: 100%; object-fit: cover; animation: 1s ease-out 0s 1 slideInLeft;" alt="@(hero.Alt)" />
    ```

코드스페이스에서 이미 사이트가 실행 중이며 변경 사항이 페이지에 자동으로 다시로드될 것입니다. 페이지를 위아래로 스크롤하여 책상 사진이 페이지에 슬라이드되는 것을 관찰할 수 있습니다.

> 🤩 **추가 사항**: 스크롤 다운 화살표도 애니메이션을 추가할 수 있습니다.



### 4. 새로운 섹션 추가하기

포트폴리오 사이트에 몇 가지 기본 섹션을 시작했지만, 여러분은 자신만의 창의적인 자유를 가지고 여러분의 사이트에 추가하고 싶은 새로운 섹션을 추가할 수 있습니다.

예를 들어, 포트폴리오 사이트에 교육 섹션을 추가해 보겠습니다.

1. `Components` 폴더 내에 새로운 섹션을 위한 새 컴포넌트를 만듭니다. `Education.razor`라는 새 파일을 추가합니다.

1. `Education.razor` 에 컴포넌트 기능과 포함하고자 하는 정보를 추가해봅시다:

    ```razor
    <section class="light" id="portfolio">
        <h2>Education</h2>
    </section>
    ```

1. `Index.razor`에 페이지 내에서 렌더링되길 원하는 위치에 Education 컴포넌트를 추가해봅시다:

    ```razor
    <Education />
    ```

여러분의 Codespaces에서 포트폴리오 애플리케이션이 실행 중이어야 하며 변경 사항이 사이트에 자동으로 다시로드될 것입니다.

<br />


## 📚 Resources

* [GitHub Codespaces 문서 개요](https://docs.github.com/codespaces/overview)
* [GitHub Codespaces 가이드](https://docs.github.com/codespaces/guides)
* [VS Code와 Docker를 사용하여 로컬에서 dev containers 사용하기](https://github.com/microsoft/vscode-remote-try-dotnet#vs-code-dev-containers)
* [Blazor 시작하기](https://learn.microsoft.com/training/paths/build-web-apps-with-blazor/?WT.mc_id=dotnet-82024-juyoo)
* [초보자를 위한 웹 개발](https://github.com/microsoft/Web-Dev-For-Beginners)

> #### Codespaces 브라우저 앱
>
> Edge 또는 Chrome을 사용하는 경우 Codespaces를 시작할 때 Codespaces 앱을 설치할 수 있는 옵션이 표시됩니다. Codespaces 앱을 사용하면 브라우저 외부에서 작업할 수 있도록 Codespaces를 앱 내에서 시작할 수 있습니다. 앱 아이콘과 설치 팝업을 찾아서 시도할 수 있습니다.
>
> <img src="./images/codespaces-app.png" alt="Codespaces browser app" style="width: 400px;"/>

<br />

## 🔎 문제를 발견하거나 개선 아이디어가 있나요?

[우리에게 알려주고 이슈를 오픈](/../../issues/new)해서 이 템플릿 저장소를 더 나은 방향으로 만드는 데 도와 줄 수 있습니다!
