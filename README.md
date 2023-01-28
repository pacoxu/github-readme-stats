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
| ID  |                                       REPO                                       |   START    |   UPDATE   | LAUGUAGE | STARS |
|-----|----------------------------------------------------------------------------------|------------|------------|----------|-------|
|   1 | [mengjiao-liu.github.io](https://github.com/mengjiao-liu/mengjiao-liu.github.io) | 2021-09-03 | 2022-11-11 | CSS      |     1 |
|   2 | [dev](https://github.com/mengjiao-liu/dev)                                       | 2018-12-13 | 2020-12-04 | md       |     0 |
|   3 | [mengjiao-liu](https://github.com/mengjiao-liu/mengjiao-liu)                     | 2021-10-27 | 2021-10-27 | md       |     0 |
| sum |                                                                                  |            |            |          |     1 |

## The repos I contributed to
| ID  |                          REPO                          |                             FIRSTDATE                              |                             LASTEDATE                              |                                               PRCOUNT                                               |
|-----|--------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
|   1 | [website](https://github.com/kubernetes/website)       | [2022-01-10](https://github.com/kubernetes/website/pull/31268)     | [2022-12-20](https://github.com/kubernetes/website/pull/38567)     | [76](https://github.com/kubernetes/website/pulls?q=created%3A2022+is%3Apr+author%3Amengjiao-liu)    |
|   2 | [kubernetes](https://github.com/kubernetes/kubernetes) | [2022-01-10](https://github.com/kubernetes/kubernetes/pull/107445) | [2022-12-14](https://github.com/kubernetes/kubernetes/pull/114485) | [24](https://github.com/kubernetes/kubernetes/pulls?q=created%3A2022+is%3Apr+author%3Amengjiao-liu) |
|   3 | [org](https://github.com/kubernetes/org)               | [2022-03-31](https://github.com/kubernetes/org/pull/3347)          | [2022-03-31](https://github.com/kubernetes/org/pull/3347)          | [1](https://github.com/kubernetes/org/pulls?q=created%3A2022+is%3Apr+author%3Amengjiao-liu)         |
| sum |                                                        |                                                                    |                                                                    |                                                                                                 101 |

## The repos I stared (random 10)
| ID |                                  REPO                                  | STAREDDATE | LAUGUAGE | LATESTUPDATE |
|----|------------------------------------------------------------------------|------------|----------|--------------|
|  1 | [clusterpedia](https://github.com/clusterpedia-io/clusterpedia)        | 2022-04-19 | Go       | 2023-01-20   |
|  2 | [kubernetes-lts](https://github.com/klts-io/kubernetes-lts)            | 2021-08-30 | Shell    | 2023-01-16   |
|  3 | [merbridge](https://github.com/merbridge/merbridge)                    | 2022-01-19 | Go       | 2023-01-27   |
|  4 | [effective-go-zh-en](https://github.com/bingohuang/effective-go-zh-en) | 2019-06-10 | md       | 2023-01-27   |
|  5 | [algo](https://github.com/wangzheng0822/algo)                          | 2020-06-02 | Python   | 2023-01-27   |
|  6 | [kubernetes](https://github.com/kubernetes/kubernetes)                 | 2021-12-30 | Go       | 2023-01-28   |
|  7 | [HelloGitHub](https://github.com/521xueweihan/HelloGitHub)             | 2020-05-29 | Python   | 2023-01-28   |
|  8 | [spiderpool](https://github.com/spidernet-io/spiderpool)               | 2022-07-21 | Go       | 2023-01-03   |
|  9 | [ferry](https://github.com/ferryproxy/ferry)                           | 2022-07-21 | Go       | 2022-12-16   |
| 10 | [hwameistor](https://github.com/hwameistor/hwameistor)                 | 2022-05-26 | Go       | 2023-01-26   |

<!--END_SECTION:my_github-->
