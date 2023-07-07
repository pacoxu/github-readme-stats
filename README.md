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
|   4 | [goweb](https://github.com/cyclinder/goweb)                   | 2020-07-28 | 2020-07-28 | md       |     0 |
|   5 | [ipconflict](https://github.com/cyclinder/ipconflict)         | 2023-04-20 | 2023-04-20 | Go       |     0 |
|   6 | [kpng-demo](https://github.com/cyclinder/kpng-demo)           | 2022-04-16 | 2022-07-25 | Shell    |     0 |
|   7 | [concurrent-pod](https://github.com/cyclinder/concurrent-pod) | 2022-03-22 | 2022-03-22 | Go       |     0 |
|   8 | [eBPF-demo](https://github.com/cyclinder/eBPF-demo)           | 2022-03-12 | 2022-03-14 | C        |     0 |
|   9 | [sync-ci-action](https://github.com/cyclinder/sync-ci-action) | 2022-03-30 | 2022-03-30 | md       |     0 |
|  10 | [test1](https://github.com/cyclinder/test1)                   | 2023-06-13 | 2023-06-13 | Go       |     0 |
| sum |                                                               |            |            |          |     2 |

## The repos I contributed to
| ID  |                                                REPO                                                |                                         FIRSTDATE                                          |                                         LASTEDATE                                          |                                                          PRCOUNT                                                           |
|-----|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
|   1 | [dce-charts-repackage](https://github.com/DaoCloud/dce-charts-repackage)                           | [2023-01-03](https://github.com/DaoCloud/dce-charts-repackage/pull/478)                    | [2023-06-29](https://github.com/DaoCloud/dce-charts-repackage/pull/1201)                   | [16](https://github.com/DaoCloud/dce-charts-repackage/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                   |
|   2 | [cni-plugins](https://github.com/spidernet-io/cni-plugins)                                         | [2023-01-03](https://github.com/spidernet-io/cni-plugins/pull/138)                         | [2023-06-27](https://github.com/spidernet-io/cni-plugins/pull/179)                         | [15](https://github.com/spidernet-io/cni-plugins/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                        |
|   3 | [spiderpool](https://github.com/spidernet-io/spiderpool)                                           | [2023-03-16](https://github.com/spidernet-io/spiderpool/pull/1451)                         | [2023-07-06](https://github.com/spidernet-io/spiderpool/pull/2012)                         | [12](https://github.com/spidernet-io/spiderpool/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                         |
|   4 | [calico](https://github.com/projectcalico/calico)                                                  | [2023-01-06](https://github.com/projectcalico/calico/pull/7151)                            | [2023-07-06](https://github.com/projectcalico/calico/pull/7843)                            | [9](https://github.com/projectcalico/calico/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                             |
|   5 | [kubespray](https://github.com/kubernetes-sigs/kubespray)                                          | [2023-01-03](https://github.com/kubernetes-sigs/kubespray/pull/9631)                       | [2023-06-01](https://github.com/kubernetes-sigs/kubespray/pull/10177)                      | [7](https://github.com/kubernetes-sigs/kubespray/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                        |
|   6 | [kubernetes](https://github.com/kubernetes/kubernetes)                                             | [2023-02-08](https://github.com/kubernetes/kubernetes/pull/115617)                         | [2023-06-24](https://github.com/kubernetes/kubernetes/pull/118846)                         | [6](https://github.com/kubernetes/kubernetes/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                            |
|   7 | [plugins](https://github.com/spidernet-io/plugins)                                                 | [2023-03-07](https://github.com/spidernet-io/plugins/pull/3)                               | [2023-03-13](https://github.com/spidernet-io/plugins/pull/5)                               | [5](https://github.com/spidernet-io/plugins/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                             |
|   8 | [metallb](https://github.com/metallb/metallb)                                                      | [2023-01-03](https://github.com/metallb/metallb/pull/1766)                                 | [2023-04-23](https://github.com/metallb/metallb/pull/1903)                                 | [4](https://github.com/metallb/metallb/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                                  |
|   9 | [kubean](https://github.com/kubean-io/kubean)                                                      | [2023-04-04](https://github.com/kubean-io/kubean/pull/622)                                 | [2023-04-18](https://github.com/kubean-io/kubean/pull/662)                                 | [2](https://github.com/kubean-io/kubean/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                                 |
|  10 | [multus-cni](https://github.com/k8snetworkplumbingwg/multus-cni)                                   | [2023-07-05](https://github.com/k8snetworkplumbingwg/multus-cni/pull/1119)                 | [2023-07-05](https://github.com/k8snetworkplumbingwg/multus-cni/pull/1119)                 | [2](https://github.com/k8snetworkplumbingwg/multus-cni/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                  |
|  11 | [public-image-mirror](https://github.com/DaoCloud/public-image-mirror)                             | [2023-03-20](https://github.com/DaoCloud/public-image-mirror/pull/305)                     | [2023-06-25](https://github.com/DaoCloud/public-image-mirror/pull/324)                     | [2](https://github.com/DaoCloud/public-image-mirror/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                     |
|  12 | [cilium](https://github.com/cilium/cilium)                                                         | [2023-01-10](https://github.com/cilium/cilium/pull/23019)                                  | [2023-06-02](https://github.com/cilium/cilium/pull/25851)                                  | [2](https://github.com/cilium/cilium/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                                    |
|  13 | [submariner](https://github.com/submariner-io/submariner)                                          | [2023-03-20](https://github.com/submariner-io/submariner/pull/2346)                        | [2023-06-19](https://github.com/submariner-io/submariner/pull/2552)                        | [2](https://github.com/submariner-io/submariner/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                         |
|  14 | [test](https://github.com/spidernet-io/test)                                                       | [2023-03-30](https://github.com/spidernet-io/test/pull/4)                                  | [2023-04-18](https://github.com/spidernet-io/test/pull/5)                                  | [2](https://github.com/spidernet-io/test/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                                |
|  15 | [public-helm-charts-mirror](https://github.com/DaoCloud/public-helm-charts-mirror)                 | [2023-02-22](https://github.com/DaoCloud/public-helm-charts-mirror/pull/41)                | [2023-02-22](https://github.com/DaoCloud/public-helm-charts-mirror/pull/41)                | [1](https://github.com/DaoCloud/public-helm-charts-mirror/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)               |
|  16 | [e2eframework](https://github.com/spidernet-io/e2eframework)                                       | [2023-06-30](https://github.com/spidernet-io/e2eframework/pull/164)                        | [2023-06-30](https://github.com/spidernet-io/e2eframework/pull/164)                        | [1](https://github.com/spidernet-io/e2eframework/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                        |
|  17 | [egressgateway](https://github.com/spidernet-io/egressgateway)                                     | [2023-03-29](https://github.com/spidernet-io/egressgateway/pull/257)                       | [2023-03-29](https://github.com/spidernet-io/egressgateway/pull/257)                       | [1](https://github.com/spidernet-io/egressgateway/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                       |
|  18 | [sriov-network-device-plugin](https://github.com/k8snetworkplumbingwg/sriov-network-device-plugin) | [2023-01-03](https://github.com/k8snetworkplumbingwg/sriov-network-device-plugin/pull/457) | [2023-01-03](https://github.com/k8snetworkplumbingwg/sriov-network-device-plugin/pull/457) | [1](https://github.com/k8snetworkplumbingwg/sriov-network-device-plugin/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder) |
|  19 | [DaoCloud-docs](https://github.com/DaoCloud/DaoCloud-docs)                                         | [2023-02-26](https://github.com/DaoCloud/DaoCloud-docs/pull/949)                           | [2023-02-26](https://github.com/DaoCloud/DaoCloud-docs/pull/949)                           | [1](https://github.com/DaoCloud/DaoCloud-docs/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                           |
|  20 | [subctl](https://github.com/submariner-io/subctl)                                                  | [2023-02-23](https://github.com/submariner-io/subctl/pull/570)                             | [2023-02-23](https://github.com/submariner-io/subctl/pull/570)                             | [1](https://github.com/submariner-io/subctl/pulls?q=created%3A2023+is%3Apr+author%3Acyclinder)                             |
| sum |                                                                                                    |                                                                                            |                                                                                            |                                                                                                                         92 |

## The repos I stared (random 10)
| ID |                                      REPO                                       | STAREDDATE |  LAUGUAGE  | LATESTUPDATE |
|----|---------------------------------------------------------------------------------|------------|------------|--------------|
|  1 | [ebpf-slide](https://github.com/gojue/ebpf-slide)                               | 2022-06-07 | md         | 2023-07-04   |
|  2 | [youki](https://github.com/containers/youki)                                    | 2023-06-20 | Rust       | 2023-07-07   |
|  3 | [zig](https://github.com/ziglang/zig)                                           | 2023-03-24 | Zig        | 2023-07-07   |
|  4 | [kpng](https://github.com/kubernetes-sigs/kpng)                                 | 2021-10-25 | Go         | 2023-07-01   |
|  5 | [golang-hellowolrd](https://github.com/yank1/golang-hellowolrd)                 | 2021-12-31 | TypeScript | 2022-08-06   |
|  6 | [HowToLiveLonger](https://github.com/geekan/HowToLiveLonger)                    | 2023-05-18 | md         | 2023-07-07   |
|  7 | [goxdp-template](https://github.com/takehaya/goxdp-template)                    | 2022-03-12 | Go         | 2022-12-07   |
|  8 | [bpf-developer-tutorial](https://github.com/eunomia-bpf/bpf-developer-tutorial) | 2023-06-05 | C          | 2023-07-07   |
|  9 | [nftgw](https://github.com/aojea/nftgw)                                         | 2023-02-06 | Go         | 2023-03-20   |
| 10 | [sdn-handbook](https://github.com/tonydeng/sdn-handbook)                        | 2023-03-22 | Shell      | 2023-07-05   |

<!--END_SECTION:my_github-->
