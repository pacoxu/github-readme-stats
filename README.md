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
| ID  |                                         REPO                                          |                                     FIRSTDATE                                     |                                     LASTEDATE                                     |                                             PRCOUNT                                              |
|-----|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
|   1 | [karmada](https://github.com/karmada-io/karmada)                                      | [2021-12-23](https://github.com/karmada-io/karmada/pull/1152)                     | [2022-12-26](https://github.com/karmada-io/karmada/pull/2990)                     | [59](https://github.com/karmada-io/karmada/pulls?q=is%3Apr+author%3Acarlory)                     |
|   2 | [kubernetes](https://github.com/kubernetes/kubernetes)                                | [2017-05-05](https://github.com/kubernetes/kubernetes/pull/45408)                 | [2022-02-13](https://github.com/kubernetes/kubernetes/pull/108092)                | [48](https://github.com/kubernetes/kubernetes/pulls?q=is%3Apr+author%3Acarlory)                  |
|   3 | [kwok](https://github.com/kubernetes-sigs/kwok)                                       | [2022-11-17](https://github.com/kubernetes-sigs/kwok/pull/71)                     | [2022-11-26](https://github.com/kubernetes-sigs/kwok/pull/88)                     | [11](https://github.com/kubernetes-sigs/kwok/pulls?q=is%3Apr+author%3Acarlory)                   |
|   4 | [helm](https://github.com/helm/helm)                                                  | [2017-07-25](https://github.com/helm/helm/pull/2715)                              | [2017-09-18](https://github.com/helm/helm/pull/2946)                              | [7](https://github.com/helm/helm/pulls?q=is%3Apr+author%3Acarlory)                               |
|   5 | [hwameistor](https://github.com/hwameistor/hwameistor)                                | [2023-01-13](https://github.com/hwameistor/hwameistor/pull/606)                   | [2023-01-17](https://github.com/hwameistor/hwameistor/pull/610)                   | [6](https://github.com/hwameistor/hwameistor/pulls?q=is%3Apr+author%3Acarlory)                   |
|   6 | [website](https://github.com/merbridge/website)                                       | [2017-06-20](https://github.com/kubernetes/website/pull/4143)                     | [2023-01-17](https://github.com/merbridge/website/pull/36)                        | [4](https://github.com/merbridge/website/pulls?q=is%3Apr+author%3Acarlory)                       |
|   7 | [service-catalog](https://github.com/kubernetes-retired/service-catalog)              | [2018-10-18](https://github.com/kubernetes-retired/service-catalog/pull/2423)     | [2018-10-30](https://github.com/kubernetes-retired/service-catalog/pull/2446)     | [4](https://github.com/kubernetes-retired/service-catalog/pulls?q=is%3Apr+author%3Acarlory)      |
|   8 | [karmada-operator](https://github.com/karmada-io/karmada-operator)                    | [2022-11-29](https://github.com/karmada-io/karmada-operator/pull/5)               | [2022-12-08](https://github.com/karmada-io/karmada-operator/pull/9)               | [2](https://github.com/karmada-io/karmada-operator/pulls?q=is%3Apr+author%3Acarlory)             |
|   9 | [karmada-operator1](https://github.com/DaoCloud/karmada-operator1)                    | [2022-08-18](https://github.com/DaoCloud/karmada-operator1/pull/49)               | [2022-08-30](https://github.com/DaoCloud/karmada-operator1/pull/57)               | [2](https://github.com/DaoCloud/karmada-operator1/pulls?q=is%3Apr+author%3Acarlory)              |
|  10 | [clusterpedia](https://github.com/clusterpedia-io/clusterpedia)                       | [2022-11-01](https://github.com/clusterpedia-io/clusterpedia/pull/439)            | [2022-11-01](https://github.com/clusterpedia-io/clusterpedia/pull/439)            | [2](https://github.com/clusterpedia-io/clusterpedia/pulls?q=is%3Apr+author%3Acarlory)            |
|  11 | [cri-o](https://github.com/cri-o/cri-o)                                               | [2017-10-25](https://github.com/cri-o/cri-o/pull/1070)                            | [2017-10-25](https://github.com/cri-o/cri-o/pull/1070)                            | [2](https://github.com/cri-o/cri-o/pulls?q=is%3Apr+author%3Acarlory)                             |
|  12 | [enhancements](https://github.com/kubernetes/enhancements)                            | [2020-08-25](https://github.com/kubernetes/enhancements/pull/1955)                | [2020-08-25](https://github.com/kubernetes/enhancements/pull/1955)                | [1](https://github.com/kubernetes/enhancements/pulls?q=is%3Apr+author%3Acarlory)                 |
|  13 | [dashboard](https://github.com/karmada-io/dashboard)                                  | [2022-06-08](https://github.com/karmada-io/dashboard/pull/19)                     | [2022-06-08](https://github.com/karmada-io/dashboard/pull/19)                     | [1](https://github.com/karmada-io/dashboard/pulls?q=is%3Apr+author%3Acarlory)                    |
|  14 | [community](https://github.com/karmada-io/community)                                  | [2022-07-27](https://github.com/karmada-io/community/pull/9)                      | [2022-07-27](https://github.com/karmada-io/community/pull/9)                      | [1](https://github.com/karmada-io/community/pulls?q=is%3Apr+author%3Acarlory)                    |
|  15 | [apiserver-builder-alpha](https://github.com/kubernetes-sigs/apiserver-builder-alpha) | [2019-09-08](https://github.com/kubernetes-sigs/apiserver-builder-alpha/pull/419) | [2019-09-08](https://github.com/kubernetes-sigs/apiserver-builder-alpha/pull/419) | [1](https://github.com/kubernetes-sigs/apiserver-builder-alpha/pulls?q=is%3Apr+author%3Acarlory) |
|  16 | [plugins](https://github.com/rakelkar/plugins)                                        | [2018-02-05](https://github.com/rakelkar/plugins/pull/4)                          | [2018-02-05](https://github.com/rakelkar/plugins/pull/4)                          | [1](https://github.com/rakelkar/plugins/pulls?q=is%3Apr+author%3Acarlory)                        |
|  17 | [istio](https://github.com/istio/istio)                                               | [2017-12-26](https://github.com/istio/istio/pull/2335)                            | [2017-12-26](https://github.com/istio/istio/pull/2335)                            | [1](https://github.com/istio/istio/pulls?q=is%3Apr+author%3Acarlory)                             |
| sum |                                                                                       |                                                                                   |                                                                                   |                                                                                              153 |

## The repos I stared (random 10)
| ID |                                       REPO                                       | STAREDDATE |  LAUGUAGE  | LATESTUPDATE |
|----|----------------------------------------------------------------------------------|------------|------------|--------------|
|  1 | [ebpf-beginners](https://github.com/lizrice/ebpf-beginners)                      | 2023-01-17 | Python     | 2023-01-24   |
|  2 | [IngressMonitorController](https://github.com/stakater/IngressMonitorController) | 2018-12-15 | Go         | 2023-01-26   |
|  3 | [kubernetes-app](https://github.com/grafana/kubernetes-app)                      | 2018-12-15 | TypeScript | 2023-01-28   |
|  4 | [metacontroller](https://github.com/metacontroller/metacontroller)               | 2022-05-21 | Go         | 2023-01-27   |
|  5 | [network-lab](https://github.com/vincentbernat/network-lab)                      | 2020-11-20 | Shell      | 2022-12-24   |
|  6 | [kube-prometheus](https://github.com/prometheus-operator/kube-prometheus)        | 2020-01-19 | Jsonnet    | 2023-01-29   |
|  7 | [StudyGo](https://github.com/liusuxian/StudyGo)                                  | 2021-04-28 | Go         | 2022-08-06   |
|  8 | [misc](https://github.com/rhvgoyal/misc)                                         | 2018-09-19 | C          | 2021-12-06   |
|  9 | [negroni](https://github.com/urfave/negroni)                                     | 2018-08-29 | Go         | 2023-01-28   |
| 10 | [awesome-go](https://github.com/avelino/awesome-go)                              | 2019-05-08 | Go         | 2023-01-29   |

<!--END_SECTION:my_github-->
