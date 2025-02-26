---
title: Flutter SDK archive
title: Flutter SDK 归档列表
short-title: Releases
short-title: 版本列表
description: "All current Flutter SDK releases: stable, beta, and master."
description: 所有 Flutter SDK 的版本列表，包括稳定版和主分支。
tags: 下载,SDK下载,Flutter版本
keywords: 构建渠道,Flutter SDK,SDK,中国镜像
toc: false
---

<style>
.scrollable-table {
  overflow-y: scroll;
  max-height: 20rem;
}
</style>

The {{site.sdk.channel | capitalize }} channel contains the
most stable Flutter builds. 
Check out [Flutter’s channels][] for details.

For details about what's new in the major Flutter releases,
check out the [release notes][] page.


{{site.alert.secondary}}
  **A note on provenance**: [provenance](https://slsa.dev/provenance)
  describes how software artifacts are built, including
  what the download contains and who created it.
  To view provenance in a more readable format
  and where nothing is downloaded, run the following
  command using the provenance file URL from a release (you might need to 
  download [jq](https://stedolan.github.io/jq/) to easily parse the JSON).

  ```terminal
  curl [provenance URL] | jq -r .payload | base64 -d | jq
  ```
{{site.alert.end}}

Flutter 的 {{site.sdk.channel | capitalize }} channel 是相对稳定的发布版本，
查阅这个文档了解更多：[Flutter 的构建（发布）渠道 channels][Flutter’s channels]。

{% comment %} Nav tabs {% endcomment -%}
<ul class="nav nav-tabs" id="editor-setup" role="tablist">
  <li class="nav-item">
    <a class="nav-link active" id="windows-tab" href="#windows" role="tab" aria-controls="windows" aria-selected="true">Windows</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="macos-tab" href="#macos" role="tab" aria-controls="macos" aria-selected="false">macOS</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="linux-tab" href="#linux" role="tab" aria-controls="linux" aria-selected="false">Linux</a>
  </li>
</ul>

{% comment %} Tab panes {% endcomment -%}
<div id="sdk-archives" class="tab-content">
{% include_relative _release_os.md os="Windows" %}
{% include_relative _release_os.md os="macOS" %}
{% include_relative _release_os.md os="Linux" %}
</div>

## Master channel

Installation bundles are not available for master.
However, you can get the SDK directly from
[GitHub repo][] by cloning the master channel,
and then triggering a download of the SDK dependencies:

我们并没有对 master channel 的提供打包下载，
不过，你可以通过 `git clone` 我们在 
[Github 上 repo]({{site.repo.flutter}}) 的 master 分支来使用。

```terminal
$ git clone -b master https://github.com/flutter/flutter.git
$ ./flutter/bin/flutter --version
```

For additional details on how our installation bundles are structured,
see [Installation bundles][].

关于安装包结构的更多信息，请查看这个页面：
[Flutter 安装包结构][Installation bundles]。

We will post a Weibo message with each Flutter releases and the merged PR,
please follow us on Weibo: [Flutter Community](https://weibo.com/u/6723427904)!

每次新版本发布以及 Flutter 主 repo 有新 PR 合并的时候，我们会在社区微博上发布一条信息，欢迎关注
[Flutter社区](https://weibo.com/u/6723427904) 微博账号！

[Flutter’s channels]: {{site.repo.flutter}}/wiki/Flutter-build-release-channels
[release notes]: {{site.url}}/release/release-notes
[Installation bundles]: {{site.repo.flutter}}/wiki/Flutter-Installation-Bundles
