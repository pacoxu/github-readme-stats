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
|   6 | [kubernetes](https://github.com/kubernetes/kubernetes)             | [2022-02-13](https://github.com/kubernetes/kubernetes/pull/108092)     | [2022-02-13](https://github.com/kubernetes/kubernetes/pull/108092)     | [1](https://github.com/kubernetes/kubernetes/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)        |
|   7 | [community](https://github.com/karmada-io/community)               | [2022-07-27](https://github.com/karmada-io/community/pull/9)           | [2022-07-27](https://github.com/karmada-io/community/pull/9)           | [1](https://github.com/karmada-io/community/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)         |
|   8 | [dashboard](https://github.com/karmada-io/dashboard)               | [2022-06-08](https://github.com/karmada-io/dashboard/pull/19)          | [2022-06-08](https://github.com/karmada-io/dashboard/pull/19)          | [1](https://github.com/karmada-io/dashboard/pulls?q=created%3A2022+is%3Apr+author%3Acarlory)         |
| sum |                                                                    |                                                                        |                                                                        |                                                                                                   74 |

## The repos I stared (random 10)
| ID |                                          REPO                                          | STAREDDATE |  LAUGUAGE  | LATESTUPDATE |
|----|----------------------------------------------------------------------------------------|------------|------------|--------------|
|  1 | [use_vim_as_ide](https://github.com/yangyangwithgnu/use_vim_as_ide)                    | 2018-12-09 | VimL       | 2023-01-28   |
|  2 | [kubespy](https://github.com/pulumi/kubespy)                                           | 2018-09-29 | Go         | 2023-01-24   |
|  3 | [goreplay](https://github.com/buger/goreplay)                                          | 2019-01-11 | Go         | 2023-01-29   |
|  4 | [oauth2_proxy](https://github.com/bitly/oauth2_proxy)                                  | 2019-03-23 | Go         | 2023-01-28   |
|  5 | [etcd-cloud-operator](https://github.com/Quentin-M/etcd-cloud-operator)                | 2018-05-08 | Go         | 2023-01-02   |
|  6 | [react-router-breadcrumbs-hoc](https://github.com/icd2k3/react-router-breadcrumbs-hoc) | 2019-02-09 | JavaScript | 2023-01-24   |
|  7 | [kubernetes-app](https://github.com/grafana/kubernetes-app)                            | 2018-12-15 | TypeScript | 2023-01-28   |
|  8 | [misc](https://github.com/rhvgoyal/misc)                                               | 2018-09-19 | C          | 2021-12-06   |
|  9 | [spec](https://github.com/cloudevents/spec)                                            | 2018-05-10 | Python     | 2023-01-29   |
| 10 | [rbac-lookup](https://github.com/FairwindsOps/rbac-lookup)                             | 2019-03-11 | Go         | 2023-01-29   |

<!--END_SECTION:my_github-->
