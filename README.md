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
| ID |                              REPO                              |   START    |   UPDATE   | LAUGUAGE | STARS |
|----|----------------------------------------------------------------|------------|------------|----------|-------|
|  1 | [kubeadm-operator](https://github.com/pacoxu/kubeadm-operator) | 2022-03-10 | 2022-09-26 | Go       |    10 |

## The repos I contributed to
| ID |                          REPO                          |                             FIRSTDATE                             |                             LASTEDATE                              |                                     PRCOUNT                                     |
|----|--------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------|---------------------------------------------------------------------------------|
|  1 | [kubernetes](https://github.com/kubernetes/kubernetes) | [2018-03-12](https://github.com/kubernetes/kubernetes/pull/61040) | [2022-11-10](https://github.com/kubernetes/kubernetes/pull/113800) | [302](https://github.com/kubernetes/kubernetes/pulls?q=is%3Apr+author%3Apacoxu) |

## The repos I stared (random 10)
| ID |                                                REPO                                                | STAREDDATE |  LAUGUAGE  | LATESTUPDATE |
|----|----------------------------------------------------------------------------------------------------|------------|------------|--------------|
|  1 | [hubble-otel](https://github.com/cilium/hubble-otel)                                               | 2022-02-15 | Go         | 2022-11-07   |
|  2 | [FIFA-Ultimate-Team-Toolkit](https://github.com/trydis/FIFA-Ultimate-Team-Toolkit)                 | 2016-09-23 | C#         | 2022-11-04   |
|  3 | [test-infra](https://github.com/kubernetes/test-infra)                                             | 2020-11-27 | Go         | 2022-11-16   |
|  4 | [cobra](https://github.com/spf13/cobra)                                                            | 2020-06-04 | Go         | 2022-11-16   |
|  5 | [kubernetes-issues-solution](https://github.com/AliyunContainerService/kubernetes-issues-solution) | 2019-04-25 | Shell      | 2020-07-24   |
|  6 | [distroless](https://github.com/GoogleContainerTools/distroless)                                   | 2022-05-07 | Starlark   | 2022-11-16   |
|  7 | [knative-tutorial](https://github.com/meteatamel/knative-tutorial)                                 | 2019-10-07 | C#         | 2022-10-15   |
|  8 | [dnscache](https://github.com/yahoo/dnscache)                                                      | 2019-04-28 | JavaScript | 2022-11-08   |
|  9 | [node-feature-discovery](https://github.com/kubernetes-sigs/node-feature-discovery)                | 2021-11-23 | Go         | 2022-11-14   |
| 10 | [kompose](https://github.com/kubernetes/kompose)                                                   | 2017-06-02 | Go         | 2022-11-15   |

<!--END_SECTION:my_github-->
