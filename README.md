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
| ID  |                                REPO                                |   START    |   UPDATE   |        LAUGUAGE         | STARS |
|-----|--------------------------------------------------------------------|------------|------------|-------------------------|-------|
|   1 | [github-repos-stats](https://github.com/pacoxu/github-repos-stats) | 2022-02-22 | 2023-04-10 | Go                      |    11 |
|   2 | [kubeadm-operator](https://github.com/pacoxu/kubeadm-operator)     | 2022-03-10 | 2022-09-26 | Go                      |    10 |
|   3 | [kubelet-reloader](https://github.com/pacoxu/kubelet-reloader)     | 2022-06-10 | 2022-08-08 | Go                      |     2 |
|   4 | [cncf-learning-path](https://github.com/pacoxu/cncf-learning-path) | 2022-02-21 | 2023-04-10 | md                      |     2 |
|   5 | [UIMessage](https://github.com/pacoxu/UIMessage)                   | 2012-08-02 | 2021-04-07 | Java                    |     1 |
|   6 | [stackoverflow](https://github.com/pacoxu/stackoverflow)           | 2014-10-09 | 2021-04-07 | md                      |     1 |
|   7 | [youth-soccer](https://github.com/pacoxu/youth-soccer)             | 2016-12-21 | 2021-04-07 | GCC Machine Description |     1 |
|   8 | [xupaco](https://github.com/pacoxu/xupaco)                         | 2012-07-24 | 2023-04-25 | md                      |     1 |
|   9 | [calculators](https://github.com/pacoxu/calculators)               | 2014-01-05 | 2021-04-07 | Java                    |     1 |
|  10 | [learning-knative](https://github.com/pacoxu/learning-knative)     | 2019-11-27 | 2021-04-07 | md                      |     0 |
|  11 | [imagesearch](https://github.com/pacoxu/imagesearch)               | 2013-01-16 | 2021-04-07 | md                      |     0 |
|  12 | [hello-prism](https://github.com/pacoxu/hello-prism)               | 2016-12-13 | 2021-08-10 | JavaScript              |     0 |
|  13 | [dubbo-example](https://github.com/pacoxu/dubbo-example)           | 2016-12-09 | 2021-04-07 | Java                    |     0 |
|  14 | [my-github-status-1](https://github.com/pacoxu/my-github-status-1) | 2022-11-07 | 2023-01-27 | md                      |     0 |
|  15 | [pacorepo](https://github.com/pacoxu/pacorepo)                     | 2013-09-20 | 2021-04-07 | Java                    |     0 |
|  16 | [pdfmanager](https://github.com/pacoxu/pdfmanager)                 | 2012-09-14 | 2021-04-07 | Java                    |     0 |
|  17 | [sample-wars](https://github.com/pacoxu/sample-wars)               | 2017-04-05 | 2021-04-07 | Dockerfile              |     0 |
|  18 | [splunk](https://github.com/pacoxu/splunk)                         | 2017-07-21 | 2021-04-07 | Shell                   |     0 |
|  19 | [docfoo](https://github.com/pacoxu/docfoo)                         | 2017-11-30 | 2021-04-07 | md                      |     0 |
|  20 | [test-codespace](https://github.com/pacoxu/test-codespace)         | 2022-05-25 | 2022-05-25 | EJS                     |     0 |
|  21 | [centos-maven](https://github.com/pacoxu/centos-maven)             | 2017-03-21 | 2021-04-07 | md                      |     0 |
|  22 | [WebSphere](https://github.com/pacoxu/WebSphere)                   | 2017-06-14 | 2022-08-20 | CSS                     |     0 |
|  23 | [caddyfile-parser](https://github.com/pacoxu/caddyfile-parser)     | 2019-06-04 | 2021-04-07 | md                      |     0 |
|  24 | [auto_test_dfc](https://github.com/pacoxu/auto_test_dfc)           | 2013-09-22 | 2021-04-07 | md                      |     0 |
| sum |                                                                    |            |            |                         |    30 |

## The repos I contributed to
| ID  |                                           REPO                                           |                                       FIRSTDATE                                       |                                       LASTEDATE                                       |                                                      PRCOUNT                                                       |
|-----|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
|   1 | [kubernetes](https://github.com/kubernetes/kubernetes)                                   | [2023-01-05](https://github.com/kubernetes/kubernetes/pull/114847)                    | [2023-07-06](https://github.com/kubernetes/kubernetes/pull/119123)                    | [78](https://github.com/kubernetes/kubernetes/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                      |
|   2 | [website](https://github.com/kubernetes/website)                                         | [2023-01-12](https://github.com/kubernetes/website/pull/38900)                        | [2023-06-25](https://github.com/kubernetes/website/pull/41754)                        | [13](https://github.com/kubernetes/website/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                         |
|   3 | [test-infra](https://github.com/kubernetes/test-infra)                                   | [2023-01-28](https://github.com/kubernetes/test-infra/pull/28574)                     | [2023-06-30](https://github.com/kubernetes/test-infra/pull/29981)                     | [10](https://github.com/kubernetes/test-infra/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                      |
|   4 | [k8s.io](https://github.com/kubernetes/k8s.io)                                           | [2023-02-08](https://github.com/kubernetes/k8s.io/pull/4736)                          | [2023-06-21](https://github.com/kubernetes/k8s.io/pull/5455)                          | [7](https://github.com/kubernetes/k8s.io/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                           |
|   5 | [kubeadm](https://github.com/kubernetes/kubeadm)                                         | [2023-01-28](https://github.com/kubernetes/kubeadm/pull/2807)                         | [2023-06-13](https://github.com/kubernetes/kubeadm/pull/2893)                         | [6](https://github.com/kubernetes/kubeadm/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                          |
|   6 | [enhancements](https://github.com/kubernetes/enhancements)                               | [2023-01-31](https://github.com/kubernetes/enhancements/pull/3801)                    | [2023-06-08](https://github.com/kubernetes/enhancements/pull/4068)                    | [5](https://github.com/kubernetes/enhancements/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                     |
|   7 | [etcd](https://github.com/etcd-io/etcd)                                                  | [2023-01-31](https://github.com/etcd-io/etcd/pull/15226)                              | [2023-01-31](https://github.com/etcd-io/etcd/pull/15226)                              | [2](https://github.com/etcd-io/etcd/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                                |
|   8 | [system-validators](https://github.com/kubernetes/system-validators)                     | [2023-01-10](https://github.com/kubernetes/system-validators/pull/34)                 | [2023-03-21](https://github.com/kubernetes/system-validators/pull/35)                 | [2](https://github.com/kubernetes/system-validators/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                |
|   9 | [landscape](https://github.com/cncf/landscape)                                           | [2023-06-01](https://github.com/cncf/landscape/pull/3227)                             | [2023-06-25](https://github.com/cncf/landscape/pull/3282)                             | [2](https://github.com/cncf/landscape/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                              |
|  10 | [gitdm.archive](https://github.com/cncf/gitdm.archive)                                   | [2023-02-14](https://github.com/cncf/gitdm.archive/pull/1361)                         | [2023-02-27](https://github.com/cncf/gitdm.archive/pull/1369)                         | [2](https://github.com/cncf/gitdm.archive/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                          |
|  11 | [kwok](https://github.com/kubernetes-sigs/kwok)                                          | [2023-01-12](https://github.com/kubernetes-sigs/kwok/pull/206)                        | [2023-01-12](https://github.com/kubernetes-sigs/kwok/pull/206)                        | [1](https://github.com/kubernetes-sigs/kwok/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                        |
|  12 | [release](https://github.com/kubernetes/release)                                         | [2023-01-11](https://github.com/kubernetes/release/pull/2852)                         | [2023-01-11](https://github.com/kubernetes/release/pull/2852)                         | [1](https://github.com/kubernetes/release/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                          |
|  13 | [public-image-mirror](https://github.com/DaoCloud/public-image-mirror)                   | [2023-02-20](https://github.com/DaoCloud/public-image-mirror/pull/296)                | [2023-02-20](https://github.com/DaoCloud/public-image-mirror/pull/296)                | [1](https://github.com/DaoCloud/public-image-mirror/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                |
|  14 | [actions-comment-on-issue](https://github.com/ben-z/actions-comment-on-issue)            | [2023-06-13](https://github.com/ben-z/actions-comment-on-issue/pull/3)                | [2023-06-13](https://github.com/ben-z/actions-comment-on-issue/pull/3)                | [1](https://github.com/ben-z/actions-comment-on-issue/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)              |
|  15 | [community](https://github.com/kubernetes/community)                                     | [2023-05-29](https://github.com/kubernetes/community/pull/7324)                       | [2023-05-29](https://github.com/kubernetes/community/pull/7324)                       | [1](https://github.com/kubernetes/community/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                        |
|  16 | [sriov-network-operator](https://github.com/k8snetworkplumbingwg/sriov-network-operator) | [2023-02-24](https://github.com/k8snetworkplumbingwg/sriov-network-operator/pull/411) | [2023-02-24](https://github.com/k8snetworkplumbingwg/sriov-network-operator/pull/411) | [1](https://github.com/k8snetworkplumbingwg/sriov-network-operator/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu) |
|  17 | [raft](https://github.com/etcd-io/raft)                                                  | [2023-01-09](https://github.com/etcd-io/raft/pull/20)                                 | [2023-01-09](https://github.com/etcd-io/raft/pull/20)                                 | [1](https://github.com/etcd-io/raft/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                                |
|  18 | [tag-contributor-strategy](https://github.com/cncf/tag-contributor-strategy)             | [2023-06-01](https://github.com/cncf/tag-contributor-strategy/pull/429)               | [2023-06-01](https://github.com/cncf/tag-contributor-strategy/pull/429)               | [1](https://github.com/cncf/tag-contributor-strategy/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)               |
|  19 | [kubectl-ai](https://github.com/sozercan/kubectl-ai)                                     | [2023-03-22](https://github.com/sozercan/kubectl-ai/pull/14)                          | [2023-03-22](https://github.com/sozercan/kubectl-ai/pull/14)                          | [1](https://github.com/sozercan/kubectl-ai/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                         |
|  20 | [kustomize](https://github.com/kubernetes-sigs/kustomize)                                | [2023-01-29](https://github.com/kubernetes-sigs/kustomize/pull/5006)                  | [2023-01-29](https://github.com/kubernetes-sigs/kustomize/pull/5006)                  | [1](https://github.com/kubernetes-sigs/kustomize/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                   |
|  21 | [oauth2](https://github.com/golang/oauth2)                                               | [2023-01-10](https://github.com/golang/oauth2/pull/620)                               | [2023-01-10](https://github.com/golang/oauth2/pull/620)                               | [1](https://github.com/golang/oauth2/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                               |
|  22 | [cadvisor](https://github.com/google/cadvisor)                                           | [2023-01-10](https://github.com/google/cadvisor/pull/3228)                            | [2023-01-10](https://github.com/google/cadvisor/pull/3228)                            | [1](https://github.com/google/cadvisor/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                             |
|  23 | [ipvs](https://github.com/moby/ipvs)                                                     | [2023-01-12](https://github.com/moby/ipvs/pull/28)                                    | [2023-01-12](https://github.com/moby/ipvs/pull/28)                                    | [1](https://github.com/moby/ipvs/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                                   |
|  24 | [corefile-migration](https://github.com/coredns/corefile-migration)                      | [2023-02-07](https://github.com/coredns/corefile-migration/pull/74)                   | [2023-02-07](https://github.com/coredns/corefile-migration/pull/74)                   | [1](https://github.com/coredns/corefile-migration/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                  |
|  25 | [org](https://github.com/kubernetes/org)                                                 | [2023-05-31](https://github.com/kubernetes/org/pull/4255)                             | [2023-05-31](https://github.com/kubernetes/org/pull/4255)                             | [1](https://github.com/kubernetes/org/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                              |
|  26 | [Python-Webscraping-Program](https://github.com/nicholls-git/Python-Webscraping-Program) | [2023-05-04](https://github.com/nicholls-git/Python-Webscraping-Program/pull/1)       | [2023-05-04](https://github.com/nicholls-git/Python-Webscraping-Program/pull/1)       | [1](https://github.com/nicholls-git/Python-Webscraping-Program/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)     |
|  27 | [docs](https://github.com/DaoCloud-OpenSource/docs)                                      | [2023-03-22](https://github.com/DaoCloud-OpenSource/docs/pull/14)                     | [2023-03-22](https://github.com/DaoCloud-OpenSource/docs/pull/14)                     | [1](https://github.com/DaoCloud-OpenSource/docs/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                    |
|  28 | [common](https://github.com/prometheus/common)                                           | [2023-01-10](https://github.com/prometheus/common/pull/432)                           | [2023-01-10](https://github.com/prometheus/common/pull/432)                           | [1](https://github.com/prometheus/common/pulls?q=created%3A2023+is%3Apr+author%3Apacoxu)                           |
| sum |                                                                                          |                                                                                       |                                                                                       |                                                                                                                145 |

## The repos I stared (random 10)
| ID |                                REPO                                 | STAREDDATE | LAUGUAGE | LATESTUPDATE |
|----|---------------------------------------------------------------------|------------|----------|--------------|
|  1 | [kubelet-reloader](https://github.com/pacoxu/kubelet-reloader)      | 2022-06-10 | Go       | 2022-08-08   |
|  2 | [SoccerAnalysis](https://github.com/joshuamataaraya/SoccerAnalysis) | 2016-09-23 | HTML     | 2017-11-06   |
|  3 | [k3s](https://github.com/k3s-io/k3s)                                | 2020-10-26 | Go       | 2023-07-07   |
|  4 | [rio](https://github.com/rancher/rio)                               | 2019-07-02 | Go       | 2023-06-29   |
|  5 | [kivy](https://github.com/kivy/kivy)                                | 2019-04-18 | Python   | 2023-07-06   |
|  6 | [ismyk8ssecure](https://github.com/ismyk8ssecure/ismyk8ssecure)     | 2022-01-14 | Python   | 2022-11-08   |
|  7 | [DaoCloud-docs](https://github.com/DaoCloud/DaoCloud-docs)          | 2016-04-02 | Python   | 2023-07-06   |
|  8 | [todos](https://github.com/izqui/todos)                             | 2020-12-13 | Go       | 2023-01-03   |
|  9 | [hwameistor](https://github.com/hwameistor/hwameistor)              | 2022-08-22 | Go       | 2023-07-07   |
| 10 | [network](https://github.com/DaoCloud-OpenSource/network)           | 2021-09-06 | md       | 2023-06-03   |

<!--END_SECTION:my_github-->
