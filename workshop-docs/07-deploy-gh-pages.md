# Deploy your Blazor application to GitHub Pages

In this step, you will deploy your portfolio application to GitHub Pages. GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files directly from a repository on GitHub. You can use GitHub Pages to host a website about yourself, your organization, or your project directly from a GitHub repository.

In order to publish your portfolio application to GitHub Pages, you need to create GitHub Actions workflow. GitHub Actions is a powerful tool that allows you to automate, customize, and execute your software development workflows right in your repository. You can use GitHub Actions to build and test your code, deploy your application, and more.

OK. Let's get started!

## Step 0: Restore the Blazor WebAssembly project

If you haven't completed the previous step or want to start from the save point, run the following commands to restore the Blazor WebAssembly project.

```bash
cd $CODESPACE_VSCODE_FOLDER
mkdir -p workshop && cp -a workshop-docs/save-points/step-06/. workshop/
cd workshop
```

## Step 1: Create GitHub Actions workflow

There is already a GitHub Actions workflow file in the `.github/workflows` directory, `publish-gh-pages.yml`. We'll slightly modify it so that our portfolio app is published to GitHub Pages.

1. Open the `publish-gh-pages.yml` file in the `.github/workflows` directory.
1. Update the `on` section to trigger the workflow to only pick up changes from our workshop directory.

    ```yaml
    # Remove this line
    on: [ push, workflow_dispatch ]
    
    # Add the following lines
    on:
      workflow_dispatch:
      push:
        paths:
          - 'workshop/MyPortfolio/**'
    ```

1. Update the following steps to build and publish the application to GitHub Pages.

    ```yaml
    - name: Restore NuGet packages
        shell: bash
        run: |
        dotnet restore ./workshop
    
    - name: Build solution
        shell: bash
        run: |
        dotnet build ./workshop -c Release
    
    - name: Test solution
        shell: bash
        run: |
        dotnet test ./workshop -c Release
    
    - name: Publish artifact
        shell: bash
        run: |
        dotnet publish ./workshop/MyPortfolio -c Release -o published
    ```

1. 