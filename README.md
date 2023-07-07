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
|   5 | [wilsonwu](https://github.com/wilsonwu/wilsonwu)                         | 2020-03-14 | 2023-07-07 | Vue        |     1 |
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
| ID  |                                                      REPO                                                       |                                          FIRSTDATE                                          |                                          LASTEDATE                                           |                                                                    PRCOUNT                                                                     |
|-----|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
|   1 | [istio.io](https://github.com/istio/istio.io)                                                                   | [2023-04-21](https://github.com/istio/istio.io/pull/13089)                                  | [2023-06-20](https://github.com/istio/istio.io/pull/13417)                                   | [34](https://github.com/istio/istio.io/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                                     |
|   2 | [public-image-mirror](https://github.com/DaoCloud/public-image-mirror)                                          | [2022-08-09](https://github.com/DaoCloud/public-image-mirror/pull/173)                      | [2022-12-08](https://github.com/DaoCloud/public-image-mirror/pull/282)                       | [8](https://github.com/DaoCloud/public-image-mirror/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                        |
|   3 | [nacos-docker](https://github.com/nacos-group/nacos-docker)                                                     | [2022-12-01](https://github.com/nacos-group/nacos-docker/pull/297)                          | [2023-05-25](https://github.com/nacos-group/nacos-docker/pull/340)                           | [6](https://github.com/nacos-group/nacos-docker/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                            |
|   4 | [rollouts-plugin-trafficrouter-contour](https://github.com/argoproj-labs/rollouts-plugin-trafficrouter-contour) | [2023-03-15](https://github.com/argoproj-labs/rollouts-plugin-trafficrouter-contour/pull/1) | [2023-04-15](https://github.com/argoproj-labs/rollouts-plugin-trafficrouter-contour/pull/13) | [6](https://github.com/argoproj-labs/rollouts-plugin-trafficrouter-contour/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu) |
|   5 | [letscrum](https://github.com/letscrum/letscrum)                                                                | [2022-08-27](https://github.com/letscrum/letscrum/pull/1)                                   | [2023-03-08](https://github.com/letscrum/letscrum/pull/8)                                    | [6](https://github.com/letscrum/letscrum/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                                   |
|   6 | [openinsight-helm-charts](https://github.com/openinsight-proj/openinsight-helm-charts)                          | [2022-10-21](https://github.com/openinsight-proj/openinsight-helm-charts/pull/33)           | [2023-02-27](https://github.com/openinsight-proj/openinsight-helm-charts/pull/79)            | [6](https://github.com/openinsight-proj/openinsight-helm-charts/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)            |
|   7 | [nacos](https://github.com/alibaba/nacos)                                                                       | [2023-01-05](https://github.com/alibaba/nacos/pull/9803)                                    | [2023-05-11](https://github.com/alibaba/nacos/pull/10473)                                    | [5](https://github.com/alibaba/nacos/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                                       |
|   8 | [gateway-api](https://github.com/kubernetes-sigs/gateway-api)                                                   | [2022-10-18](https://github.com/kubernetes-sigs/gateway-api/pull/1462)                      | [2022-11-21](https://github.com/kubernetes-sigs/gateway-api/pull/1554)                       | [4](https://github.com/kubernetes-sigs/gateway-api/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                         |
|   9 | [charts](https://github.com/bitnami/charts)                                                                     | [2022-08-09](https://github.com/bitnami/charts/pull/11675)                                  | [2022-08-09](https://github.com/bitnami/charts/pull/11675)                                   | [4](https://github.com/bitnami/charts/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                                      |
|  10 | [sentinel-dashboard-k8s-operator](https://github.com/sentinel-group/sentinel-dashboard-k8s-operator)            | [2022-11-22](https://github.com/sentinel-group/sentinel-dashboard-k8s-operator/pull/9)      | [2022-12-07](https://github.com/sentinel-group/sentinel-dashboard-k8s-operator/pull/17)      | [4](https://github.com/sentinel-group/sentinel-dashboard-k8s-operator/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)      |
|  11 | [sentinel-cluster-flow-control-java](https://github.com/projectsesame/sentinel-cluster-flow-control-java)       | [2023-03-28](https://github.com/projectsesame/sentinel-cluster-flow-control-java/pull/2)    | [2023-04-14](https://github.com/projectsesame/sentinel-cluster-flow-control-java/pull/7)     | [4](https://github.com/projectsesame/sentinel-cluster-flow-control-java/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)    |
|  12 | [Sentinel](https://github.com/alibaba/Sentinel)                                                                 | [2022-11-23](https://github.com/alibaba/Sentinel/pull/2970)                                 | [2022-12-01](https://github.com/alibaba/Sentinel/pull/2983)                                  | [2](https://github.com/alibaba/Sentinel/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                                    |
|  13 | [argo-rollouts](https://github.com/argoproj/argo-rollouts)                                                      | [2023-04-17](https://github.com/argoproj/argo-rollouts/pull/2729)                           | [2023-04-17](https://github.com/argoproj/argo-rollouts/pull/2729)                            | [2](https://github.com/argoproj/argo-rollouts/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                              |
|  14 | [nacos-k8s](https://github.com/nacos-group/nacos-k8s)                                                           | [2022-12-25](https://github.com/nacos-group/nacos-k8s/pull/373)                             | [2023-05-29](https://github.com/nacos-group/nacos-k8s/pull/417)                              | [2](https://github.com/nacos-group/nacos-k8s/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                               |
|  15 | [contour](https://github.com/projectcontour/contour)                                                            | [2023-04-20](https://github.com/projectcontour/contour/pull/5299)                           | [2023-04-20](https://github.com/projectcontour/contour/pull/5299)                            | [2](https://github.com/projectcontour/contour/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                              |
|  16 | [opencost](https://github.com/opencost/opencost)                                                                | [2023-03-16](https://github.com/opencost/opencost/pull/1773)                                | [2023-03-23](https://github.com/opencost/opencost/pull/1799)                                 | [2](https://github.com/opencost/opencost/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                                   |
|  17 | [community](https://github.com/istio/community)                                                                 | [2023-04-22](https://github.com/istio/community/pull/1035)                                  | [2023-04-22](https://github.com/istio/community/pull/1035)                                   | [1](https://github.com/istio/community/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                                     |
|  18 | [jwks-generator](https://github.com/projectsesame/jwks-generator)                                               | [2023-06-16](https://github.com/projectsesame/jwks-generator/pull/1)                        | [2023-06-16](https://github.com/projectsesame/jwks-generator/pull/1)                         | [1](https://github.com/projectsesame/jwks-generator/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                        |
|  19 | [letscrum-ui](https://github.com/letscrum/letscrum-ui)                                                          | [2022-08-06](https://github.com/letscrum/letscrum-ui/pull/1)                                | [2022-08-06](https://github.com/letscrum/letscrum-ui/pull/1)                                 | [1](https://github.com/letscrum/letscrum-ui/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                                |
|  20 | [enovy-remote-jwks-go](https://github.com/projectsesame/enovy-remote-jwks-go)                                   | [2023-06-16](https://github.com/projectsesame/enovy-remote-jwks-go/pull/1)                  | [2023-06-16](https://github.com/projectsesame/enovy-remote-jwks-go/pull/1)                   | [1](https://github.com/projectsesame/enovy-remote-jwks-go/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                  |
|  21 | [opentelemetry-demo](https://github.com/openinsight-proj/opentelemetry-demo)                                    | [2023-01-08](https://github.com/openinsight-proj/opentelemetry-demo/pull/1)                 | [2023-01-08](https://github.com/openinsight-proj/opentelemetry-demo/pull/1)                  | [1](https://github.com/openinsight-proj/opentelemetry-demo/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                 |
|  22 | [envoy-authz-java](https://github.com/projectsesame/envoy-authz-java)                                           | [2023-05-16](https://github.com/projectsesame/envoy-authz-java/pull/7)                      | [2023-05-16](https://github.com/projectsesame/envoy-authz-java/pull/7)                       | [1](https://github.com/projectsesame/envoy-authz-java/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                      |
|  23 | [argo-cd](https://github.com/argoproj/argo-cd)                                                                  | [2023-04-20](https://github.com/argoproj/argo-cd/pull/13300)                                | [2023-04-20](https://github.com/argoproj/argo-cd/pull/13300)                                 | [1](https://github.com/argoproj/argo-cd/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                                    |
|  24 | [public-helm-charts-mirror](https://github.com/DaoCloud/public-helm-charts-mirror)                              | [2022-11-09](https://github.com/DaoCloud/public-helm-charts-mirror/pull/29)                 | [2022-11-09](https://github.com/DaoCloud/public-helm-charts-mirror/pull/29)                  | [1](https://github.com/DaoCloud/public-helm-charts-mirror/pulls?q=created%3A2022-07-01..2023-07-01+is%3Apr+author%3Awilsonwu)                  |
| sum |                                                                                                                 |                                                                                             |                                                                                              |                                                                                                                                            105 |

## The repos I stared (random 10)
| ID |                                 REPO                                 | STAREDDATE |  LAUGUAGE  | LATESTUPDATE |
|----|----------------------------------------------------------------------|------------|------------|--------------|
|  1 | [KeymouseGo](https://github.com/taojy123/KeymouseGo)                 | 2023-04-02 | Python     | 2023-07-07   |
|  2 | [kdoctor](https://github.com/kdoctor-io/kdoctor)                     | 2023-06-29 | Go         | 2023-07-06   |
|  3 | [kubean](https://github.com/kubean-io/kubean)                        | 2023-06-29 | Go         | 2023-07-06   |
|  4 | [go-msgraph](https://github.com/open-networks/go-msgraph)            | 2022-10-08 | Go         | 2023-04-25   |
|  5 | [DS4Windows](https://github.com/Ryochan7/DS4Windows)                 | 2021-06-26 | C#         | 2023-07-07   |
|  6 | [shipit](https://github.com/18chetanpatel/shipit)                    | 2021-09-30 | Vue        | 2023-06-27   |
|  7 | [project-layout](https://github.com/golang-standards/project-layout) | 2022-07-11 | Makefile   | 2023-07-07   |
|  8 | [graphql-yoga](https://github.com/dotansimha/graphql-yoga)           | 2020-07-25 | TypeScript | 2023-07-05   |
|  9 | [multi-v2ray](https://github.com/Jrohy/multi-v2ray)                  | 2020-02-04 | Python     | 2023-07-06   |
| 10 | [cloudtty](https://github.com/cloudtty/cloudtty)                     | 2022-05-20 | Go         | 2023-07-05   |

<!--END_SECTION:my_github-->
