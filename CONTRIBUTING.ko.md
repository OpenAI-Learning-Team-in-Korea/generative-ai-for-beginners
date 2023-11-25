# 기여하기

이 프로젝트는 기여와 제안을 환영합니다. 여러분이 하는 대부분의 기여는 
기여자 라이선스 계약(CLA, Contributor License Agreement)에 동의한 
것으로 보며 이는 여러분이 여러분의 기여를 우리가 사용할 권리를 부여할
권한을 갖고 있다는 것을 나타냅니다.
자세한 내용은 아래 사이트를 방문해주세요.
<https://cla.microsoft.com>

> 중요: 이 저장소(repository)에 있는 텍스트를 번역할 때는 기계 번역을 사용하지 마세요. 커뮤니티를 통해 번역을 검증할 예정이므로 자신이 능숙한 언어로만 번역에 자원해 주세요.

풀 리퀘스트(pull request)를 제출하실 때, CLA-봇(bot)이 자동으로 여러분이 CLA를 제공해야하는 지와 PR을 적절히 갖췄는 지(예를 들어 라벨과 코멘트 등을 갖췄는 지)를 판단합니다. 해당 봇이 제공하는 안내를 따르시기만 하면 됩니다. 우리 CLA를 사용하는 모든 저장소에서 한 번만 이를 실행하시면 됩니다.

## 실행 규칙(Code of Conduct)

이 프로젝트는 [마이크로소프트 오픈소스 실행 규칙(Microsoft Open Source Code of Conduct)](https://opensource.microsoft.com/codeofconduct/)을 채택하고 있습니다.
더 상세한 정보는 [실행규칙에 대한 자주하는 질문들(Code of Conduct FAQ)](https://opensource.microsoft.com/codeofconduct/faq/) 참조하시거나 [opencode@microsoft.com](mailto:opencode@microsoft.com)에 추가 질문이나 코멘트를 보내주시면 됩니다.

## 질문 또는 문제?

깃허브 리스트(Github list)는 기능(feature) 요구 및 버그(bug) 리포트 용도이므로 일반적인 지원관련 질문은 깃허브 이슈(Github issues)를 개시하시지 말아주세요. 이런 방식은 우리가 좀 더 손쉽게 코드에서 보이는 실제 이슈들 또는 버그를 추적하기 위한 것으로 실제 코드와 일반 토론을 분리하기 위한 것입니다.

## Typos, Issues, Bugs and contributions

Whenever you are submitting any changes to the Generative AI for Beginners repository, please follow these recommendations.

* Always fork the repository to your own account before making your modifications
* Do not combine multiple changes to one pull request. For example, submit any bug fix and documentation updates using separate PRs
* If your pull request shows merge conflicts, make sure to update your local main to be a mirror of what's in the main repository before making your modifications
* If you are submitting a translation, please create one PR for all the translated files as we don't accept partial translations for the content
* If you are submitting a typo or documentation fix, you can combine modifications to a single PR where suitable

## General Guidance for writing

- Ensure that all your URLs are wrapped in square brackets followed by a parenthesis with no extra spaces around them or inside them `[]()`.
- Ensure that any relative link (i.e. links to other files and folders in the repository) starts with a `./` referring to a file or a folder located in the current working directory or a `../` referring to a file or a folder located in a parent working directory.
- Ensure that any relative link (i.e. links to other files and folders in the repository) has a tracking ID (i.e. `?` or `&` then `wt.mc_id=` or `WT.mc_id=`) at the end of it.
- Ensure that any URL from the following domains _github.com, microsoft.com, visualstudio.com, aka.ms, and azure.com_ has a tracking ID (i.e. `?` or `&` then `wt.mc_id=` or `WT.mc_id=`) at the end of it.
- Ensure that your links don't have country specific locale in them (i.e. `/en-us/` or `/en/`).
- Ensure that all images are stored in the `./images` folder.
- Ensure that the images have descriptive names using English characters, numbers, and dashes in the name of your image.

## GitHub Workflows

When you submit a pull request, four different workflows will be triggered to validate the previous rules.
Simply follow the instructions listed here to pass the workflow checks.

- [Check Broken Relative Paths](#check-broken-relative-paths)
- [Check Paths Have Tracking](#check-paths-have-tracking)
- [Check URLs Have Tracking](#check-urls-have-tracking)
- [Check URLs Don't Have Locale](#check-urls-dont-have-locale)

### Check Broken Relative Paths

This workflow ensures that any relative path in your files is working.
This repository is deployed to GitHub pages so you need to be very careful when you type the links that glue everything together to not direct anyone to the wrong place.

To make sure that your links are working properly simply use VS code to check that.

For example, when you hover over any link in your files you will be prompted to follow the link by pressing on **ctrl + click**

![VS code follow links screenshot](./images/vscode-follow-link.png "Screenshot from vs code prompt to follow a link when you hover over a link.")

If you click on a link and it's not working locally then, surely it will trigger the workflow and won't work on GitHub.

To fix this issue, try to type the link with the help of VS code.

When you type `./` or `../` VS code will prompt you to choose from the available options according to what you typed.

![VS code select relative path screenshot](./images/vscode-select-relative-path.png "Screenshot from vs code prompt to select relative path from a pop up list.")

Follow the path by clicking on the desired file or folder and you will be sure that your path is not broken.

Once you add the correct relative path, save, and push your changes the workflow will be triggered again to verify your changes.
If you pass the check then you are good to go.

### Check Paths Have Tracking

This workflow ensures that any relative path has tracking in it.
This repository is deployed to GitHub pages so we need to track the movement between the different files and folders.

To make sure your relative paths have tracking in them simply check for the following text `?wt.mc_id=` at the end of the path.
If it's appended to your relative paths then you will pass this check.

If not, you may get the following error.

![GitHub check paths missing tracking comment screenshot](./images/github-check-paths-missing-tracking-comment.png "Screenshot from github comment that shows missing tracking from relative paths")

To fix this issue, try to open the file path that the workflow highlighted and add the tracking ID to the end of the relative paths.

Once you add the tracking ID, save, and push your changes the workflow will be triggered again to verify your changes.
If you pass the check then you are good to go.

### Check URLs Have Tracking

This workflow ensures that any web URL has tracking in it.
This repository is available to everyone so you need to make sure to track the access to know from where the traffic is coming.

To make sure your URLs have tracking in them simply check for the following text `?wt.mc_id=` at the end of the URL.
If it's appended to your URLs then you will pass this check.

If not, you may get the following error.

![GitHub check urls missing tracking comment screenshot](./images/github-check-urls-missing-tracking-comment.png "Screenshot from github comment that shows missing tracking from urls")

To fix this issue, try to open the file path that the workflow highlighted and add the tracking ID to the end of the URLs.

Once you add the tracking ID, save, and push your changes the workflow will be triggered again to verify your changes.
If you pass the check then you are good to go.

### Check URLs Don't Have Locale

This workflow ensures that any web URL doesn't have country specific locale in it.
This repository is available to everyone around the world so you need to make sure not to include your country's locale in URLs.

To make sure your URLs don't have country locale in them simply check for the following text `/en-us/` or `/en/` or any other language locale anywhere in the URL.
If it's not present in your URLs then you will pass this check.

If not, you may get the following error.

![GitHub check country locale comment screenshot](./images/github-check-country-locale-comment.png "Screenshot from github comment that shows added country locale to urls")

To fix this issue, try to open the file path that the workflow highlighted and remove the country locale from the URLs.

Once you remove the country locale, save, and push your changes the workflow will be triggered again to verify your changes.
If you pass the check then you are good to go.

Congratulations! We will get back to you as soon as possible with feedback about your contribution.
