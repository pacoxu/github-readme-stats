# Use

## You can also use the [Demo Server](https://github.com/yihong0618/github-readme-stats-server) for test

- Update your README

Add a comment to your `README.md` like this:

```md
<!--START_SECTION:your_github-->
<!--END_SECTION:your_github-->
```
To use above, change `your_github` to `my_github`.

- Write your own `yml` file

[Sample](https://github.com/yihong0618/2021)

```yml
name: GitHub README STATS

on:
  workflow_dispatch:
  schedule:
    - cron: "0 0 * * *"
  push:
    branches:
      - main

env:
  GITHUB_NAME: yihong0618
  GITHUB_EMAIL: zouzou0208@gmail.com
  STARRED_NUM: 10

jobs:
  build:
    name: Build
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: My GitHub Status
        uses: yihong0618/github-readme-stats@main
        with:
          # if you also want to send TELE
          TELEGRAM_TOKEN: ${{ secrets.TELE_TOKEN }}
          TELEGRAM_CHAT_ID: ${{ secrets.TELE_CHAT_ID }}
          STARRED_NUM: ${{ env.STARRED_NUM }}

      - name: Push README
        run: |
          git config --local user.email "${{ env.GITHUB_EMAIL }}"
          git config --local user.name "${{ env.GITHUB_EMAIL }}"
          git commit -a -m 'docs: update readme.md' || echo "nothing to commit"
          git push || echo "nothing to push"
```



# [My example](https://github.com/yihong0618/2021).

## My GitHub Status
<img align="middle" src="https://github-readme-stats-1.yihong0618.vercel.app/api?username=yihong0618&show_icons=true&&&hide_title=true" />

<!--START_SECTION:my_github-->
## The repos I created
| ID  |                              REPO                               |   START    |   UPDATE   | LAUGUAGE | STARS |
|-----|-----------------------------------------------------------------|------------|------------|----------|-------|
|   1 | [LearnCloudNative](https://github.com/carlory/LearnCloudNative) | 2022-05-16 | 2022-07-04 | md       |     1 |
|   2 | [carlory](https://github.com/carlory/carlory)                   | 2022-07-16 | 2022-07-16 | md       |     0 |
|   3 | [images](https://github.com/carlory/images)                     | 2022-09-06 | 2022-09-06 | md       |     0 |
| sum |                                                                 |            |            |          |     1 |

## The repos I contributed to
| ID  |                                REPO                                |                               FIRSTDATE                                |                               LASTEDATE                                |                                               PRCOUNT                                                |
|-----|--------------------------------------------------------------------|------------------------------------------------------------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
|   1 | [karmada](https://github.com/karmada-io/karmada)                   | [2022-01-02](https://github.com/karmada-io/karmada/pull/1206)          | [2022-12-26](https://github.com/karmada-io/karmada/pull/2990)          | [54](https://github.com/karmada-io/karmada/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)          |
|   2 | [kwok](https://github.com/kubernetes-sigs/kwok)                    | [2022-11-17](https://github.com/kubernetes-sigs/kwok/pull/71)          | [2022-11-26](https://github.com/kubernetes-sigs/kwok/pull/88)          | [11](https://github.com/kubernetes-sigs/kwok/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)        |
|   3 | [clusterpedia](https://github.com/clusterpedia-io/clusterpedia)    | [2022-11-01](https://github.com/clusterpedia-io/clusterpedia/pull/439) | [2022-11-01](https://github.com/clusterpedia-io/clusterpedia/pull/439) | [2](https://github.com/clusterpedia-io/clusterpedia/pulls?q=created%3A2022+is%3Apr+author%3Acarlory) |
|   4 | [karmada-operator1](https://github.com/DaoCloud/karmada-operator1) | [2022-08-18](https://github.com/DaoCloud/karmada-operator1/pull/49)    | [2022-08-30](https://github.com/DaoCloud/karmada-operator1/pull/57)    | [2](https://github.com/DaoCloud/karmada-operator1/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)   |
|   5 | [karmada-operator](https://github.com/karmada-io/karmada-operator) | [2022-11-29](https://github.com/karmada-io/karmada-operator/pull/5)    | [2022-12-08](https://github.com/karmada-io/karmada-operator/pull/9)    | [2](https://github.com/karmada-io/karmada-operator/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)  |
|   6 | [community](https://github.com/karmada-io/community)               | [2022-07-27](https://github.com/karmada-io/community/pull/9)           | [2022-07-27](https://github.com/karmada-io/community/pull/9)           | [1](https://github.com/karmada-io/community/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)         |
|   7 | [dashboard](https://github.com/karmada-io/dashboard)               | [2022-06-08](https://github.com/karmada-io/dashboard/pull/19)          | [2022-06-08](https://github.com/karmada-io/dashboard/pull/19)          | [1](https://github.com/karmada-io/dashboard/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)         |
|   8 | [kubernetes](https://github.com/kubernetes/kubernetes)             | [2022-02-13](https://github.com/kubernetes/kubernetes/pull/108092)     | [2022-02-13](https://github.com/kubernetes/kubernetes/pull/108092)     | [1](https://github.com/kubernetes/kubernetes/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)        |
| sum |                                                                    |                                                                        |                                                                        |                                                                                                   74 |

## The repos I stared (random 10)
| ID |                                          REPO                                          | STAREDDATE |     LAUGUAGE     | LATESTUPDATE |
|----|----------------------------------------------------------------------------------------|------------|------------------|--------------|
|  1 | [prometheus-adapter](https://github.com/kubernetes-sigs/prometheus-adapter)            | 2019-09-23 | Go               | 2023-01-25   |
|  2 | [docker_env](https://github.com/wangzheng422/docker_env)                               | 2022-09-07 | Jupyter Notebook | 2022-12-25   |
|  3 | [interview_internal_reference](https://github.com/0voice/interview_internal_reference) | 2019-07-31 | Python           | 2023-01-29   |
|  4 | [kaniko](https://github.com/GoogleContainerTools/kaniko)                               | 2019-04-18 | Go               | 2023-01-28   |
|  5 | [CKAD-exercises](https://github.com/dgkanatsios/CKAD-exercises)                        | 2019-03-11 | md               | 2023-01-29   |
|  6 | [martini](https://github.com/go-martini/martini)                                       | 2018-08-29 | Go               | 2023-01-29   |
|  7 | [book](https://github.com/KeKe-Li/book)                                                | 2019-10-30 | md               | 2022-12-07   |
|  8 | [navigator](https://github.com/jetstack/navigator)                                     | 2019-03-14 | Go               | 2022-12-10   |
|  9 | [kubespy](https://github.com/pulumi/kubespy)                                           | 2018-09-29 | Go               | 2023-01-24   |
| 10 | [mysql-operator](https://github.com/bitpoke/mysql-operator)                            | 2019-08-05 | Go               | 2023-01-17   |

<!--END_SECTION:my_github-->
