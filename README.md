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
| ID  |                             REPO                              |   START    |   UPDATE   | LAUGUAGE | STARS |
|-----|---------------------------------------------------------------|------------|------------|----------|-------|
|   1 | [mock-kubelet](https://github.com/cyclinder/mock-kubelet)     | 2022-03-03 | 2022-03-03 | Go       |     1 |
|   2 | [opa-deploy](https://github.com/cyclinder/opa-deploy)         | 2021-11-02 | 2022-03-25 | md       |     1 |
|   3 | [ferry-proxy](https://github.com/cyclinder/ferry-proxy)       | 2021-12-07 | 2021-12-08 | md       |     0 |
|   4 | [github-ci](https://github.com/cyclinder/github-ci)           | 2022-03-29 | 2022-10-24 | Go       |     0 |
|   5 | [goweb](https://github.com/cyclinder/goweb)                   | 2020-07-28 | 2020-07-28 | md       |     0 |
|   6 | [kpng-demo](https://github.com/cyclinder/kpng-demo)           | 2022-04-16 | 2022-07-25 | Shell    |     0 |
|   7 | [concurrent-pod](https://github.com/cyclinder/concurrent-pod) | 2022-03-22 | 2022-03-22 | Go       |     0 |
|   8 | [eBPF-demo](https://github.com/cyclinder/eBPF-demo)           | 2022-03-12 | 2022-03-14 | C        |     0 |
|   9 | [sync-ci-action](https://github.com/cyclinder/sync-ci-action) | 2022-03-30 | 2022-03-30 | md       |     0 |
| sum |                                                               |            |            |          |     2 |

## The repos I contributed to
| ID  |                                   REPO                                   |                                 FIRSTDATE                                  |                                 LASTEDATE                                  |                                                  PRCOUNT                                                   |
|-----|--------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
|   1 | [cni-plugins](https://github.com/spidernet-io/cni-plugins)               | [2022-08-29](https://github.com/spidernet-io/cni-plugins/pull/2)           | [2022-12-27](https://github.com/spidernet-io/cni-plugins/pull/134)         | [45](https://github.com/spidernet-io/cni-plugins/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)        |
|   2 | [dce-charts-repackage](https://github.com/DaoCloud/dce-charts-repackage) | [2022-08-23](https://github.com/DaoCloud/dce-charts-repackage/pull/65)     | [2022-12-30](https://github.com/DaoCloud/dce-charts-repackage/pull/468)    | [34](https://github.com/DaoCloud/dce-charts-repackage/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)   |
|   3 | [kubernetes](https://github.com/kubernetes/kubernetes)                   | [2022-01-19](https://github.com/kubernetes/kubernetes/pull/107634)         | [2022-11-22](https://github.com/kubernetes/kubernetes/pull/114068)         | [13](https://github.com/kubernetes/kubernetes/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)           |
|   4 | [calico](https://github.com/projectcalico/calico)                        | [2022-01-17](https://github.com/projectcalico/calico/pull/5453)            | [2022-11-02](https://github.com/projectcalico/calico/pull/6942)            | [6](https://github.com/projectcalico/calico/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)             |
|   5 | [kubespray](https://github.com/kubernetes-sigs/kubespray)                | [2022-05-12](https://github.com/kubernetes-sigs/kubespray/pull/8813)       | [2022-11-04](https://github.com/kubernetes-sigs/kubespray/pull/9465)       | [6](https://github.com/kubernetes-sigs/kubespray/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)        |
|   6 | [spiderpool](https://github.com/spidernet-io/spiderpool)                 | [2022-04-19](https://github.com/spidernet-io/spiderpool/pull/143)          | [2022-05-20](https://github.com/spidernet-io/spiderpool/pull/246)          | [6](https://github.com/spidernet-io/spiderpool/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)          |
|   7 | [metallb](https://github.com/metallb/metallb)                            | [2022-07-19](https://github.com/metallb/metallb/pull/1522)                 | [2022-10-12](https://github.com/metallb/metallb/pull/1637)                 | [5](https://github.com/metallb/metallb/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)                  |
|   8 | [DaoCloud-docs](https://github.com/DaoCloud/DaoCloud-docs)               | [2022-09-30](https://github.com/DaoCloud/DaoCloud-docs/pull/220)           | [2022-12-25](https://github.com/DaoCloud/DaoCloud-docs/pull/652)           | [5](https://github.com/DaoCloud/DaoCloud-docs/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)           |
|   9 | [public-image-mirror](https://github.com/DaoCloud/public-image-mirror)   | [2022-08-25](https://github.com/DaoCloud/public-image-mirror/pull/204)     | [2022-12-01](https://github.com/DaoCloud/public-image-mirror/pull/280)     | [5](https://github.com/DaoCloud/public-image-mirror/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)     |
|  10 | [e2eframework](https://github.com/spidernet-io/e2eframework)             | [2022-05-10](https://github.com/spidernet-io/e2eframework/pull/7)          | [2022-10-20](https://github.com/spidernet-io/e2eframework/pull/105)        | [5](https://github.com/spidernet-io/e2eframework/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)        |
|  11 | [multus-cni](https://github.com/k8snetworkplumbingwg/multus-cni)         | [2022-03-04](https://github.com/k8snetworkplumbingwg/multus-cni/pull/805)  | [2022-11-11](https://github.com/k8snetworkplumbingwg/multus-cni/pull/959)  | [4](https://github.com/k8snetworkplumbingwg/multus-cni/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)  |
|  12 | [sriov-cni](https://github.com/k8snetworkplumbingwg/sriov-cni)           | [2022-09-28](https://github.com/k8snetworkplumbingwg/sriov-cni/pull/227)   | [2022-11-27](https://github.com/k8snetworkplumbingwg/sriov-cni/pull/234)   | [3](https://github.com/k8snetworkplumbingwg/sriov-cni/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)   |
|  13 | [cilium](https://github.com/cilium/cilium)                               | [2022-06-09](https://github.com/cilium/cilium/pull/20137)                  | [2022-06-15](https://github.com/cilium/cilium/pull/20213)                  | [2](https://github.com/cilium/cilium/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)                    |
|  14 | [whereabouts](https://github.com/k8snetworkplumbingwg/whereabouts)       | [2022-05-23](https://github.com/k8snetworkplumbingwg/whereabouts/pull/227) | [2022-05-23](https://github.com/k8snetworkplumbingwg/whereabouts/pull/227) | [1](https://github.com/k8snetworkplumbingwg/whereabouts/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder) |
|  15 | [helm-charts](https://github.com/k8snetworkplumbingwg/helm-charts)       | [2022-07-11](https://github.com/k8snetworkplumbingwg/helm-charts/pull/22)  | [2022-07-11](https://github.com/k8snetworkplumbingwg/helm-charts/pull/22)  | [1](https://github.com/k8snetworkplumbingwg/helm-charts/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder) |
|  16 | [p2cli](https://github.com/wrouesnel/p2cli)                              | [2022-04-21](https://github.com/wrouesnel/p2cli/pull/31)                   | [2022-04-21](https://github.com/wrouesnel/p2cli/pull/31)                   | [1](https://github.com/wrouesnel/p2cli/pulls?q=created%3A2022+is%3Apr+author%3Acyclinder)                  |
| sum |                                                                          |                                                                            |                                                                            |                                                                                                        142 |

## The repos I stared (random 10)
| ID |                                          REPO                                          | STAREDDATE | LAUGUAGE | LATESTUPDATE |
|----|----------------------------------------------------------------------------------------|------------|----------|--------------|
|  1 | [go-cni](https://github.com/containerd/go-cni)                                         | 2022-03-21 | Go       | 2023-01-25   |
|  2 | [gateway](https://github.com/envoyproxy/gateway)                                       | 2022-05-17 | Go       | 2023-01-28   |
|  3 | [fake-kubelet](https://github.com/wzshiming/fake-kubelet)                              | 2022-05-19 | Go       | 2023-01-07   |
|  4 | [kilo](https://github.com/squat/kilo)                                                  | 2022-03-23 | Go       | 2023-01-26   |
|  5 | [delve](https://github.com/go-delve/delve)                                             | 2021-12-03 | Go       | 2023-01-27   |
|  6 | [kubernetes-kactus-cni-plugin](https://github.com/kaloom/kubernetes-kactus-cni-plugin) | 2022-06-09 | Go       | 2022-11-28   |
|  7 | [kubean](https://github.com/kubean-io/kubean)                                          | 2022-07-06 | Go       | 2023-01-25   |
|  8 | [ipify-api](https://github.com/rdegges/ipify-api)                                      | 2022-01-29 | Go       | 2023-01-26   |
|  9 | [userspace-cni-network-plugin](https://github.com/intel/userspace-cni-network-plugin)  | 2022-07-12 | Go       | 2023-01-11   |
| 10 | [xdp-tutorial](https://github.com/xdp-project/xdp-tutorial)                            | 2022-03-10 | C        | 2023-01-27   |

<!--END_SECTION:my_github-->
