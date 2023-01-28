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
| ID  |                                     REPO                                     |   START    |   UPDATE   |  LAUGUAGE  | STARS |
|-----|------------------------------------------------------------------------------|------------|------------|------------|-------|
|   1 | [Blogs-CloudNative](https://github.com/kerthcet/Blogs-CloudNative)           | 2021-08-21 | 2022-11-14 | md         |    48 |
|   2 | [kubernetes-design](https://github.com/kerthcet/kubernetes-design)           | 2021-10-17 | 2022-10-08 | md         |    22 |
|   3 | [WX-App](https://github.com/kerthcet/WX-App)                                 | 2017-08-30 | 2022-08-06 | Python     |     4 |
|   4 | [EffectiveGo](https://github.com/kerthcet/EffectiveGo)                       | 2022-02-21 | 2022-08-06 | md         |     3 |
|   5 | [kerthcet.github.io](https://github.com/kerthcet/kerthcet.github.io)         | 2021-08-22 | 2022-11-05 | HTML       |     3 |
|   6 | [kerthcet](https://github.com/kerthcet/kerthcet)                             | 2021-07-01 | 2022-12-14 | md         |     3 |
|   7 | [Blogs](https://github.com/kerthcet/Blogs)                                   | 2021-09-03 | 2022-08-06 | md         |     3 |
|   8 | [ddd](https://github.com/kerthcet/ddd)                                       | 2020-02-10 | 2022-08-06 | Go         |     2 |
|   9 | [kubot](https://github.com/kerthcet/kubot)                                   | 2022-03-14 | 2022-08-06 | md         |     1 |
|  10 | [issues](https://github.com/kerthcet/issues)                                 | 2020-04-03 | 2022-08-06 | md         |     1 |
|  11 | [dot_files](https://github.com/kerthcet/dot_files)                           | 2018-05-26 | 2022-08-06 | Python     |     1 |
|  12 | [InterviewPath](https://github.com/kerthcet/InterviewPath)                   | 2022-03-29 | 2022-08-06 | md         |     1 |
|  13 | [cdc](https://github.com/kerthcet/cdc)                                       | 2020-06-09 | 2022-08-06 | Makefile   |     1 |
|  14 | [tbcd-errbot](https://github.com/kerthcet/tbcd-errbot)                       | 2020-06-07 | 2022-08-06 | Python     |     1 |
|  15 | [leetcode](https://github.com/kerthcet/leetcode)                             | 2021-06-27 | 2022-08-06 | Go         |     1 |
|  16 | [Mahjong](https://github.com/kerthcet/Mahjong)                               | 2022-02-25 | 2022-08-06 | md         |     1 |
|  17 | [personal-website](https://github.com/kerthcet/personal-website)             | 2021-07-02 | 2022-08-06 | JavaScript |     1 |
|  18 | [Python-design-patterns](https://github.com/kerthcet/Python-design-patterns) | 2018-05-26 | 2022-08-06 | Python     |     1 |
|  19 | [tbcd](https://github.com/kerthcet/tbcd)                                     | 2021-06-28 | 2022-08-06 | Mustache   |     1 |
|  20 | [hello-operator](https://github.com/kerthcet/hello-operator)                 | 2020-10-16 | 2022-08-06 | Go         |     1 |
|  21 | [ide](https://github.com/kerthcet/ide)                                       | 2021-06-30 | 2021-09-05 | md         |     0 |
| sum |                                                                              |            |            |            |   100 |

## The repos I contributed to
| ID  |                                          REPO                                           |                                     FIRSTDATE                                      |                                     LASTEDATE                                      |                                                      PRCOUNT                                                      |
|-----|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
|   1 | [kubernetes](https://github.com/kubernetes/kubernetes)                                  | [2022-01-14](https://github.com/kubernetes/kubernetes/pull/107542)                 | [2022-12-28](https://github.com/kubernetes/kubernetes/pull/114717)                 | [84](https://github.com/kubernetes/kubernetes/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                   |
|   2 | [kueue](https://github.com/kubernetes-sigs/kueue)                                       | [2022-04-07](https://github.com/kubernetes-sigs/kueue/pull/184)                    | [2022-12-22](https://github.com/kubernetes-sigs/kueue/pull/490)                    | [57](https://github.com/kubernetes-sigs/kueue/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                   |
|   3 | [volcano](https://github.com/volcano-sh/volcano)                                        | [2022-08-10](https://github.com/volcano-sh/volcano/pull/2423)                      | [2022-10-26](https://github.com/volcano-sh/volcano/pull/2548)                      | [15](https://github.com/volcano-sh/volcano/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                      |
|   4 | [karmada](https://github.com/karmada-io/karmada)                                        | [2022-01-20](https://github.com/karmada-io/karmada/pull/1289)                      | [2022-04-26](https://github.com/karmada-io/karmada/pull/1663)                      | [14](https://github.com/karmada-io/karmada/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                      |
|   5 | [enhancements](https://github.com/kubernetes/enhancements)                              | [2022-01-05](https://github.com/kubernetes/enhancements/pull/3105)                 | [2022-11-04](https://github.com/kubernetes/enhancements/pull/3645)                 | [13](https://github.com/kubernetes/enhancements/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                 |
|   6 | [website](https://github.com/kubernetes/website)                                        | [2022-03-02](https://github.com/kubernetes/website/pull/32003)                     | [2022-11-03](https://github.com/kubernetes/website/pull/37688)                     | [8](https://github.com/kubernetes/website/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                       |
|   7 | [ferry](https://github.com/ferryproxy/ferry)                                            | [2022-07-29](https://github.com/ferryproxy/ferry/pull/92)                          | [2022-09-05](https://github.com/ferryproxy/ferry/pull/122)                         | [3](https://github.com/ferryproxy/ferry/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                         |
|   8 | [cilium](https://github.com/cilium/cilium)                                              | [2022-05-30](https://github.com/cilium/cilium/pull/20001)                          | [2022-10-28](https://github.com/cilium/cilium/pull/21913)                          | [2](https://github.com/cilium/cilium/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                            |
|   9 | [public-image-mirror](https://github.com/DaoCloud/public-image-mirror)                  | [2022-02-10](https://github.com/DaoCloud/public-image-mirror/pull/72)              | [2022-04-24](https://github.com/DaoCloud/public-image-mirror/pull/118)             | [2](https://github.com/DaoCloud/public-image-mirror/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)             |
|  10 | [pipeline](https://github.com/tektoncd/pipeline)                                        | [2022-05-15](https://github.com/tektoncd/pipeline/pull/4876)                       | [2022-06-03](https://github.com/tektoncd/pipeline/pull/4936)                       | [2](https://github.com/tektoncd/pipeline/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                        |
|  11 | [istio](https://github.com/istio/istio)                                                 | [2022-01-27](https://github.com/istio/istio/pull/37047)                            | [2022-02-05](https://github.com/istio/istio/pull/37180)                            | [2](https://github.com/istio/istio/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                              |
|  12 | [kube-scheduler-simulator](https://github.com/kubernetes-sigs/kube-scheduler-simulator) | [2022-10-21](https://github.com/kubernetes-sigs/kube-scheduler-simulator/pull/244) | [2022-10-21](https://github.com/kubernetes-sigs/kube-scheduler-simulator/pull/244) | [1](https://github.com/kubernetes-sigs/kube-scheduler-simulator/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet) |
|  13 | [org](https://github.com/kubernetes/org)                                                | [2022-04-28](https://github.com/kubernetes/org/pull/3396)                          | [2022-04-28](https://github.com/kubernetes/org/pull/3396)                          | [1](https://github.com/kubernetes/org/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                           |
|  14 | [kubernetes-lts](https://github.com/klts-io/kubernetes-lts)                             | [2022-01-12](https://github.com/klts-io/kubernetes-lts/pull/115)                   | [2022-01-12](https://github.com/klts-io/kubernetes-lts/pull/115)                   | [1](https://github.com/klts-io/kubernetes-lts/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                   |
|  15 | [gitdm](https://github.com/cncf/gitdm)                                                  | [2022-01-19](https://github.com/cncf/gitdm/pull/911)                               | [2022-01-19](https://github.com/cncf/gitdm/pull/911)                               | [1](https://github.com/cncf/gitdm/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                               |
|  16 | [docs](https://github.com/DaoCloud-OpenSource/docs)                                     | [2022-04-20](https://github.com/DaoCloud-OpenSource/docs/pull/6)                   | [2022-04-20](https://github.com/DaoCloud-OpenSource/docs/pull/6)                   | [1](https://github.com/DaoCloud-OpenSource/docs/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                 |
|  17 | [elastic-gpu-scheduler](https://github.com/elastic-ai/elastic-gpu-scheduler)            | [2022-07-28](https://github.com/elastic-ai/elastic-gpu-scheduler/pull/17)          | [2022-07-28](https://github.com/elastic-ai/elastic-gpu-scheduler/pull/17)          | [1](https://github.com/elastic-ai/elastic-gpu-scheduler/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)         |
|  18 | [community](https://github.com/istio/community)                                         | [2022-02-09](https://github.com/istio/community/pull/692)                          | [2022-02-09](https://github.com/istio/community/pull/692)                          | [1](https://github.com/istio/community/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)                          |
|  19 | [clusterpedia](https://github.com/clusterpedia-io/clusterpedia)                         | [2022-01-14](https://github.com/clusterpedia-io/clusterpedia/pull/51)              | [2022-01-14](https://github.com/clusterpedia-io/clusterpedia/pull/51)              | [1](https://github.com/clusterpedia-io/clusterpedia/pulls?q=created%3A2022+is%3Apr+author%3Akerthcet)             |
| sum |                                                                                         |                                                                                    |                                                                                    |                                                                                                               210 |

## The repos I stared (random 10)
| ID | REPO | STAREDDATE | LAUGUAGE | LATESTUPDATE |
|----|------|------------|----------|--------------|

<!--END_SECTION:my_github-->
