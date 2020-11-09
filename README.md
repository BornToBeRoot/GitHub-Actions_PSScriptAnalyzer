# PSScriptAnalyzer integration for GitHub Actions

[PSScriptAnalyzer](https://github.com/PowerShell/PSScriptAnalyzer) is a static code checker for PowerShell modules and scripts. Combined with GitHub Actions you can automatically check your PowerShell code everytime it is pushed to the repository or someone creates a pull request. This helps you to maintain a minimum code quality standard and find common issues.

![CI](https://github.com/BornToBeRoot/GitHub-Actions_PSScriptAnalyzer/workflows/CI/badge.svg?branch=main)

## How does it work?
Everytime you push to your main branch or a pull request agains your main branch is created, github action triggers the PowerShell script [PSScriptAnalyzer-Integration.ps1](PSScriptAnalyzer-Integration.ps1) which checks all `.ps1` and `.psm1` files in your repository.

The worklow can be modified to run on all branches and on all pull requests by editing the [psscriptanalyzer.yml](.github/workflows/psscriptanalyzer.yml).

## Install & Use

Fork this repository via GitHub or clone via commandline:

```
git clone https://github.com/BornToBeRoot/GitHub-Actions_PSScriptAnalyzer PROJEKTNAME
cd PROJEKTNAME
git remote set-url origin https://github.com/USERNAME/PROJEKTNAME
git remote -v
git push
```

Now you can push some PowerShell code to the repository or create a pull reuqest to test the workflow.

Note: _You can rename the repository in the settings after you have fork it via GitHub_

**Optional**

- Adjust the workflow file ([psscriptanalyzer.yml](.github/workflows/psscriptanalyzer.yml)) if necessary
- Adjust the [README.md](README.md), e.g. modify the URL of the badge