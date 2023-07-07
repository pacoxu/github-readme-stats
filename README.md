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
| ID  |                                   REPO                                   |   START    |   UPDATE   |  LAUGUAGE  | STARS |
|-----|--------------------------------------------------------------------------|------------|------------|------------|-------|
|   1 | [vuetify-audio](https://github.com/wilsonwu/vuetify-audio)               | 2017-06-12 | 2023-06-16 | Vue        |   136 |
|   2 | [translation-google](https://github.com/wilsonwu/translation-google)     | 2020-03-13 | 2023-03-01 | JavaScript |    42 |
|   3 | [netcoreauth](https://github.com/wilsonwu/netcoreauth)                   | 2017-05-31 | 2021-11-18 | C#         |    23 |
|   4 | [express-oauth2-demo](https://github.com/wilsonwu/express-oauth2-demo)   | 2018-01-23 | 2023-06-14 | JavaScript |     6 |
|   5 | [wilsonwu](https://github.com/wilsonwu/wilsonwu)                         | 2020-03-14 | 2021-11-15 | Vue        |     1 |
|   6 | [apollo-todo-gapi](https://github.com/wilsonwu/apollo-todo-gapi)         | 2020-07-01 | 2023-07-01 | JavaScript |     1 |
|   7 | [minecraft-mod-demo](https://github.com/wilsonwu/minecraft-mod-demo)     | 2020-01-31 | 2021-07-02 | Java       |     1 |
|   8 | [adservice](https://github.com/wilsonwu/adservice)                       | 2022-10-20 | 2023-04-20 | Java       |     0 |
|   9 | [kubernetes-101](https://github.com/wilsonwu/kubernetes-101)             | 2019-01-30 | 2019-01-30 | md         |     0 |
|  10 | [learnmark](https://github.com/wilsonwu/learnmark)                       | 2020-01-01 | 2020-01-01 | ASP        |     0 |
|  11 | [jsonnet](https://github.com/wilsonwu/jsonnet)                           | 2017-11-02 | 2017-11-02 | md         |     0 |
|  12 | [ImageBatchProcessor](https://github.com/wilsonwu/ImageBatchProcessor)   | 2013-07-30 | 2013-07-30 | C#         |     0 |
|  13 | [react-todo](https://github.com/wilsonwu/react-todo)                     | 2020-07-01 | 2021-10-08 | JavaScript |     0 |
|  14 | [graphql-template](https://github.com/wilsonwu/graphql-template)         | 2020-09-29 | 2020-09-29 | JavaScript |     0 |
|  15 | [VisualMongo](https://github.com/wilsonwu/VisualMongo)                   | 2013-06-22 | 2023-03-28 | C#         |     0 |
|  16 | [vue-funretro](https://github.com/wilsonwu/vue-funretro)                 | 2017-09-12 | 2017-09-12 | JavaScript |     0 |
|  17 | [express-graphql-demo](https://github.com/wilsonwu/express-graphql-demo) | 2019-02-13 | 2019-02-15 | JavaScript |     0 |
|  18 | [APILiteNET](https://github.com/wilsonwu/APILiteNET)                     | 2013-01-19 | 2023-03-21 | C#         |     0 |
|  19 | [wilsonwu.github.io](https://github.com/wilsonwu/wilsonwu.github.io)     | 2017-06-13 | 2023-03-08 | Vue        |     0 |
| sum |                                                                          |            |            |            |   210 |

## The repos I contributed to
| ID  |                                                      REPO                                                       |                                          FIRSTDATE                                          |                                          LASTEDATE                                           |                                                           PRCOUNT                                                            |
|-----|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
|   1 | [istio.io](https://github.com/istio/istio.io)                                                                   | [2023-04-21](https://github.com/istio/istio.io/pull/13089)                                  | [2023-07-03](https://github.com/istio/istio.io/pull/13500)                                   | [35](https://github.com/istio/istio.io/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                                     |
|   2 | [rollouts-plugin-trafficrouter-contour](https://github.com/argoproj-labs/rollouts-plugin-trafficrouter-contour) | [2023-03-15](https://github.com/argoproj-labs/rollouts-plugin-trafficrouter-contour/pull/1) | [2023-04-15](https://github.com/argoproj-labs/rollouts-plugin-trafficrouter-contour/pull/13) | [6](https://github.com/argoproj-labs/rollouts-plugin-trafficrouter-contour/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu) |
|   3 | [nacos](https://github.com/alibaba/nacos)                                                                       | [2023-01-05](https://github.com/alibaba/nacos/pull/9803)                                    | [2023-05-11](https://github.com/alibaba/nacos/pull/10473)                                    | [5](https://github.com/alibaba/nacos/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                                       |
|   4 | [nacos-docker](https://github.com/nacos-group/nacos-docker)                                                     | [2023-04-11](https://github.com/nacos-group/nacos-docker/pull/331)                          | [2023-05-25](https://github.com/nacos-group/nacos-docker/pull/340)                           | [4](https://github.com/nacos-group/nacos-docker/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                            |
|   5 | [sentinel-cluster-flow-control-java](https://github.com/projectsesame/sentinel-cluster-flow-control-java)       | [2023-03-28](https://github.com/projectsesame/sentinel-cluster-flow-control-java/pull/2)    | [2023-04-14](https://github.com/projectsesame/sentinel-cluster-flow-control-java/pull/7)     | [4](https://github.com/projectsesame/sentinel-cluster-flow-control-java/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)    |
|   6 | [openinsight-helm-charts](https://github.com/openinsight-proj/openinsight-helm-charts)                          | [2023-02-23](https://github.com/openinsight-proj/openinsight-helm-charts/pull/77)           | [2023-02-27](https://github.com/openinsight-proj/openinsight-helm-charts/pull/79)            | [2](https://github.com/openinsight-proj/openinsight-helm-charts/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)            |
|   7 | [contour](https://github.com/projectcontour/contour)                                                            | [2023-04-20](https://github.com/projectcontour/contour/pull/5299)                           | [2023-04-20](https://github.com/projectcontour/contour/pull/5299)                            | [2](https://github.com/projectcontour/contour/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                              |
|   8 | [community](https://github.com/istio/community)                                                                 | [2023-04-22](https://github.com/istio/community/pull/1035)                                  | [2023-07-05](https://github.com/istio/community/pull/1115)                                   | [2](https://github.com/istio/community/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                                     |
|   9 | [argo-rollouts](https://github.com/argoproj/argo-rollouts)                                                      | [2023-04-17](https://github.com/argoproj/argo-rollouts/pull/2729)                           | [2023-04-17](https://github.com/argoproj/argo-rollouts/pull/2729)                            | [2](https://github.com/argoproj/argo-rollouts/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                              |
|  10 | [letscrum](https://github.com/letscrum/letscrum)                                                                | [2023-01-10](https://github.com/letscrum/letscrum/pull/5)                                   | [2023-03-08](https://github.com/letscrum/letscrum/pull/8)                                    | [2](https://github.com/letscrum/letscrum/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                                   |
|  11 | [opencost](https://github.com/opencost/opencost)                                                                | [2023-03-16](https://github.com/opencost/opencost/pull/1773)                                | [2023-03-23](https://github.com/opencost/opencost/pull/1799)                                 | [2](https://github.com/opencost/opencost/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                                   |
|  12 | [opentelemetry-demo](https://github.com/openinsight-proj/opentelemetry-demo)                                    | [2023-01-08](https://github.com/openinsight-proj/opentelemetry-demo/pull/1)                 | [2023-01-08](https://github.com/openinsight-proj/opentelemetry-demo/pull/1)                  | [1](https://github.com/openinsight-proj/opentelemetry-demo/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                 |
|  13 | [envoy-authz-java](https://github.com/projectsesame/envoy-authz-java)                                           | [2023-05-16](https://github.com/projectsesame/envoy-authz-java/pull/7)                      | [2023-05-16](https://github.com/projectsesame/envoy-authz-java/pull/7)                       | [1](https://github.com/projectsesame/envoy-authz-java/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                      |
|  14 | [nacos-k8s](https://github.com/nacos-group/nacos-k8s)                                                           | [2023-05-29](https://github.com/nacos-group/nacos-k8s/pull/417)                             | [2023-05-29](https://github.com/nacos-group/nacos-k8s/pull/417)                              | [1](https://github.com/nacos-group/nacos-k8s/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                               |
|  15 | [argo-cd](https://github.com/argoproj/argo-cd)                                                                  | [2023-04-20](https://github.com/argoproj/argo-cd/pull/13300)                                | [2023-04-20](https://github.com/argoproj/argo-cd/pull/13300)                                 | [1](https://github.com/argoproj/argo-cd/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                                    |
|  16 | [enovy-remote-jwks-go](https://github.com/projectsesame/enovy-remote-jwks-go)                                   | [2023-06-16](https://github.com/projectsesame/enovy-remote-jwks-go/pull/1)                  | [2023-06-16](https://github.com/projectsesame/enovy-remote-jwks-go/pull/1)                   | [1](https://github.com/projectsesame/enovy-remote-jwks-go/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                  |
|  17 | [jwks-generator](https://github.com/projectsesame/jwks-generator)                                               | [2023-06-16](https://github.com/projectsesame/jwks-generator/pull/1)                        | [2023-06-16](https://github.com/projectsesame/jwks-generator/pull/1)                         | [1](https://github.com/projectsesame/jwks-generator/pulls?q=created%3A2023+is%3Apr+author%3Awilsonwu)                        |
| sum |                                                                                                                 |                                                                                             |                                                                                              |                                                                                                                           72 |

## The repos I stared (random 10)
| ID |                                      REPO                                       | STAREDDATE |  LAUGUAGE  | LATESTUPDATE |
|----|---------------------------------------------------------------------------------|------------|------------|--------------|
|  1 | [aria2](https://github.com/aria2/aria2)                                         | 2017-08-28 | C++        | 2023-07-07   |
|  2 | [faceswap](https://github.com/deepfakes/faceswap)                               | 2021-03-01 | Python     | 2023-07-07   |
|  3 | [kdoctor](https://github.com/kdoctor-io/kdoctor)                                | 2023-06-29 | Go         | 2023-07-06   |
|  4 | [project-layout](https://github.com/golang-standards/project-layout)            | 2022-07-11 | Makefile   | 2023-07-07   |
|  5 | [N_m3u8DL-CLI](https://github.com/nilaoda/N_m3u8DL-CLI)                         | 2021-03-20 | C#         | 2023-07-06   |
|  6 | [vuetify](https://github.com/vuetifyjs/vuetify)                                 | 2017-06-01 | TypeScript | 2023-07-07   |
|  7 | [KeymouseGo](https://github.com/taojy123/KeymouseGo)                            | 2023-04-02 | Python     | 2023-07-07   |
|  8 | [dark-flat-iterm-colors](https://github.com/QuentinWatt/dark-flat-iterm-colors) | 2021-02-01 | md         | 2023-06-24   |
|  9 | [vdm](https://github.com/ingbyr/vdm)                                            | 2019-02-02 | Kotlin     | 2023-06-29   |
| 10 | [multi-v2ray](https://github.com/Jrohy/multi-v2ray)                             | 2020-02-04 | Python     | 2023-07-06   |

<!--END_SECTION:my_github-->
