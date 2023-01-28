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
| ID  |                                            REPO                                            |   START    |   UPDATE   | LAUGUAGE | STARS |
|-----|--------------------------------------------------------------------------------------------|------------|------------|----------|-------|
|   1 | [iouring-go](https://github.com/Iceber/iouring-go)                                         | 2020-10-10 | 2023-01-25 | Go       |   369 |
|   2 | [scheme](https://github.com/Iceber/scheme)                                                 | 2021-12-03 | 2022-11-14 | Go       |     3 |
|   3 | [iouring-net](https://github.com/Iceber/iouring-net)                                       | 2020-10-15 | 2021-02-03 | md       |     2 |
|   4 | [thanos-chart](https://github.com/Iceber/thanos-chart)                                     | 2019-12-17 | 2019-12-19 | Smarty   |     1 |
|   5 | [deploy-clusterpedia-to-karmada](https://github.com/Iceber/deploy-clusterpedia-to-karmada) | 2022-07-12 | 2022-10-14 | Shell    |     1 |
|   6 | [clusterpedia-test-storage](https://github.com/Iceber/clusterpedia-test-storage)           | 2022-12-13 | 2022-12-13 | Go       |     0 |
|   7 | [Iim](https://github.com/Iceber/Iim)                                                       | 2020-03-13 | 2020-03-15 | Go       |     0 |
|   8 | [irpc](https://github.com/Iceber/irpc)                                                     | 2019-11-21 | 2019-11-21 | md       |     0 |
|   9 | [kupid](https://github.com/Iceber/kupid)                                                   | 2022-04-26 | 2022-04-26 | md       |     0 |
|  10 | [migrate_data](https://github.com/Iceber/migrate_data)                                     | 2018-04-28 | 2018-05-26 | Python   |     0 |
|  11 | [prome-thanos-chart](https://github.com/Iceber/prome-thanos-chart)                         | 2019-12-17 | 2020-06-01 | Smarty   |     0 |
|  12 | [router-tree](https://github.com/Iceber/router-tree)                                       | 2019-11-19 | 2019-11-21 | Go       |     0 |
|  13 | [exitar](https://github.com/Iceber/exitar)                                                 | 2020-12-14 | 2020-12-14 | md       |     0 |
|  14 | [Small-Python](https://github.com/Iceber/Small-Python)                                     | 2018-08-16 | 2018-11-25 | C        |     0 |
|  15 | [sqlgen](https://github.com/Iceber/sqlgen)                                                 | 2020-03-21 | 2020-03-21 | Go       |     0 |
|  16 | [config](https://github.com/Iceber/config)                                                 | 2020-04-22 | 2020-04-23 | Shell    |     0 |
|  17 | [Web](https://github.com/Iceber/Web)                                                       | 2018-02-04 | 2018-02-04 | Python   |     0 |
| sum |                                                                                            |            |            |          |   376 |

## The repos I contributed to
| ID  |                                     REPO                                      |                                   FIRSTDATE                                    |                                   LASTEDATE                                    |                                                    PRCOUNT                                                    |
|-----|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
|   1 | [clusterpedia](https://github.com/clusterpedia-io/clusterpedia)               | [2022-01-06](https://github.com/clusterpedia-io/clusterpedia/pull/44)          | [2022-12-29](https://github.com/clusterpedia-io/clusterpedia/pull/477)         | [128](https://github.com/clusterpedia-io/clusterpedia/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)         |
|   2 | [website](https://github.com/clusterpedia-io/website)                         | [2022-01-20](https://github.com/clusterpedia-io/website/pull/2)                | [2022-12-16](https://github.com/clusterpedia-io/website/pull/70)               | [48](https://github.com/clusterpedia-io/website/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)               |
|   3 | [clusterpedia-helm](https://github.com/clusterpedia-io/clusterpedia-helm)     | [2022-10-17](https://github.com/clusterpedia-io/clusterpedia-helm/pull/11)     | [2022-12-23](https://github.com/clusterpedia-io/clusterpedia-helm/pull/32)     | [15](https://github.com/clusterpedia-io/clusterpedia-helm/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)     |
|   4 | [containerd](https://github.com/containerd/containerd)                        | [2022-05-18](https://github.com/containerd/containerd/pull/6955)               | [2022-12-30](https://github.com/containerd/containerd/pull/7881)               | [14](https://github.com/containerd/containerd/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)                 |
|   5 | [ci-bot-playground](https://github.com/DaoCloud-OpenSource/ci-bot-playground) | [2022-08-05](https://github.com/DaoCloud-OpenSource/ci-bot-playground/pull/18) | [2022-09-07](https://github.com/DaoCloud-OpenSource/ci-bot-playground/pull/57) | [12](https://github.com/DaoCloud-OpenSource/ci-bot-playground/pulls?q=created%3A2022+is%3Apr+author%3Aiceber) |
|   6 | [harbor](https://github.com/goharbor/harbor)                                  | [2022-12-05](https://github.com/goharbor/harbor/pull/17915)                    | [2022-12-06](https://github.com/goharbor/harbor/pull/17922)                    | [5](https://github.com/goharbor/harbor/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)                        |
|   7 | [kubernetes](https://github.com/kubernetes/kubernetes)                        | [2022-06-13](https://github.com/kubernetes/kubernetes/pull/110531)             | [2022-12-08](https://github.com/kubernetes/kubernetes/pull/114356)             | [5](https://github.com/kubernetes/kubernetes/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)                  |
|   8 | [docs](https://github.com/DaoCloud-OpenSource/docs)                           | [2022-12-05](https://github.com/DaoCloud-OpenSource/docs/pull/10)              | [2022-12-08](https://github.com/DaoCloud-OpenSource/docs/pull/13)              | [4](https://github.com/DaoCloud-OpenSource/docs/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)               |
|   9 | [sample-storage](https://github.com/clusterpedia-io/sample-storage)           | [2022-11-23](https://github.com/clusterpedia-io/sample-storage/pull/1)         | [2022-12-15](https://github.com/clusterpedia-io/sample-storage/pull/5)         | [4](https://github.com/clusterpedia-io/sample-storage/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)         |
|  10 | [landscape](https://github.com/cncf/landscape)                                | [2022-04-22](https://github.com/cncf/landscape/pull/2561)                      | [2022-06-20](https://github.com/cncf/landscape/pull/2635)                      | [2](https://github.com/cncf/landscape/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)                         |
|  11 | [awesome-cloud-native](https://github.com/rootsongjc/awesome-cloud-native)    | [2022-03-03](https://github.com/rootsongjc/awesome-cloud-native/pull/58)       | [2022-03-03](https://github.com/rootsongjc/awesome-cloud-native/pull/58)       | [1](https://github.com/rootsongjc/awesome-cloud-native/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)        |
|  12 | [client-go](https://github.com/clusterpedia-io/client-go)                     | [2022-10-11](https://github.com/clusterpedia-io/client-go/pull/51)             | [2022-10-11](https://github.com/clusterpedia-io/client-go/pull/51)             | [1](https://github.com/clusterpedia-io/client-go/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)              |
|  13 | [contribute](https://github.com/cncf/contribute)                              | [2022-06-20](https://github.com/cncf/contribute/pull/113)                      | [2022-06-20](https://github.com/cncf/contribute/pull/113)                      | [1](https://github.com/cncf/contribute/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)                        |
|  14 | [foundation](https://github.com/cncf/foundation)                              | [2022-06-24](https://github.com/cncf/foundation/pull/372)                      | [2022-06-24](https://github.com/cncf/foundation/pull/372)                      | [1](https://github.com/cncf/foundation/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)                        |
|  15 | [tower](https://github.com/kubesphere/tower)                                  | [2022-08-22](https://github.com/kubesphere/tower/pull/52)                      | [2022-08-22](https://github.com/kubesphere/tower/pull/52)                      | [1](https://github.com/kubesphere/tower/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)                       |
|  16 | [artwork](https://github.com/cncf/artwork)                                    | [2022-06-20](https://github.com/cncf/artwork/pull/344)                         | [2022-06-20](https://github.com/cncf/artwork/pull/344)                         | [1](https://github.com/cncf/artwork/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)                           |
|  17 | [opa](https://github.com/open-policy-agent/opa)                               | [2022-03-28](https://github.com/open-policy-agent/opa/pull/4505)               | [2022-03-28](https://github.com/open-policy-agent/opa/pull/4505)               | [1](https://github.com/open-policy-agent/opa/pulls?q=created%3A2022+is%3Apr+author%3Aiceber)                  |
| sum |                                                                               |                                                                                |                                                                                |                                                                                                           244 |

## The repos I stared (random 10)
| ID |                                 REPO                                 | STAREDDATE |  LAUGUAGE  | LATESTUPDATE |
|----|----------------------------------------------------------------------|------------|------------|--------------|
|  1 | [ferry](https://github.com/ferryproxy/ferry)                         | 2022-08-26 | Go         | 2022-12-16   |
|  2 | [kui](https://github.com/kubernetes-sigs/kui)                        | 2022-08-09 | TypeScript | 2023-01-27   |
|  3 | [kubernetes](https://github.com/kubernetes/kubernetes)               | 2022-04-27 | Go         | 2023-01-28   |
|  4 | [sample-controller](https://github.com/kubernetes/sample-controller) | 2019-12-06 | Go         | 2023-01-27   |
|  5 | [caddy](https://github.com/caddyserver/caddy)                        | 2019-07-11 | Go         | 2023-01-28   |
|  6 | [xdp-tutorial](https://github.com/xdp-project/xdp-tutorial)          | 2020-11-16 | C          | 2023-01-27   |
|  7 | [libvirt-go-module](https://github.com/libvirt/libvirt-go-module)    | 2022-07-06 | Go         | 2023-01-12   |
|  8 | [go-fuzz](https://github.com/dvyukov/go-fuzz)                        | 2022-03-07 | Go         | 2023-01-27   |
|  9 | [foniod](https://github.com/foniod/foniod)                           | 2022-02-24 | Rust       | 2023-01-23   |
| 10 | [rakelimit](https://github.com/cloudflare/rakelimit)                 | 2022-03-22 | C          | 2023-01-27   |

<!--END_SECTION:my_github-->
