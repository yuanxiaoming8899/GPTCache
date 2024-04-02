<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPTCache：用于为 LLM 查询创建语义缓存的库</font></font></h1><a id="user-content-gptcache--a-library-for-creating-semantic-cache-for-llm-queries" class="anchor" aria-label="永久链接：GPTCache：用于为 LLM 查询创建语义缓存的库" href="#gptcache--a-library-for-creating-semantic-cache-for-llm-queries"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">将您的 LLM API 成本削减 10 倍 💰，将速度提高 100 倍 ⚡</font></font></p>
<p dir="auto"><a href="https://pypi.org/project/gptcache/" rel="nofollow"><img src="https://camo.githubusercontent.com/685c462f07e223d6232b5d48dccb3487c34d9e78348cf3cefb929932f76dc4c9/68747470733a2f2f696d672e736869656c64732e696f2f707970692f762f67707463616368653f6c6162656c3d52656c6561736526636f6c6f72266c6f676f3d507974686f6e" alt="发布" data-canonical-src="https://img.shields.io/pypi/v/gptcache?label=Release&amp;color&amp;logo=Python" style="max-width: 100%;"></a>
<a href="https://pypi.org/project/gptcache/" rel="nofollow"><img src="https://camo.githubusercontent.com/3cda0e6e21db13768eae032bda768e968de01c896fe14468d1df0884e1c9598a/68747470733a2f2f696d672e736869656c64732e696f2f707970692f646d2f67707463616368652e7376673f636f6c6f723d6272696768742d677265656e266c6f676f3d50797069" alt="点下载" data-canonical-src="https://img.shields.io/pypi/dm/gptcache.svg?color=bright-green&amp;logo=Pypi" style="max-width: 100%;"></a>
<a href="https://codecov.io/gh/zilliztech/GPTCache" rel="nofollow"><img src="https://camo.githubusercontent.com/9be3c247c5ef0ed9ebf28a7ab6c6120f33f80d0e1f81b98c10bbd566278adbce/68747470733a2f2f696d672e736869656c64732e696f2f636f6465636f762f632f6769746875622f7a696c6c697a746563682f47505443616368652f6465763f6c6162656c3d436f6465636f76266c6f676f3d636f6465636f7626746f6b656e3d45333057787142654a4a" alt="代码科夫" data-canonical-src="https://img.shields.io/codecov/c/github/zilliztech/GPTCache/dev?label=Codecov&amp;logo=codecov&amp;token=E30WxqBeJJ" style="max-width: 100%;"></a>
<a href="https://opensource.org/license/mit/" rel="nofollow"><img src="https://camo.githubusercontent.com/6552afb9038154d801c50b6e55a76db78a6787a8d6e2b5252a44864503c52887/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c6963656e73652d4d49542d626c75652e737667" alt="执照" data-canonical-src="https://img.shields.io/badge/License-MIT-blue.svg" style="max-width: 100%;"></a>
<a href="https://twitter.com/zilliz_universe" rel="nofollow"><img src="https://camo.githubusercontent.com/33ccc368b657a439ac974bce50aadabf3a2beac6ac1efa9631b6aa7a4cf7319c/68747470733a2f2f696d672e736869656c64732e696f2f747769747465722f75726c2f68747470732f747769747465722e636f6d2f7a696c6c697a5f756e6976657273652e7376673f7374796c653d736f6369616c266c6162656c3d466f6c6c6f772532302534305a696c6c697a" alt="推特" data-canonical-src="https://img.shields.io/twitter/url/https/twitter.com/zilliz_universe.svg?style=social&amp;label=Follow%20%40Zilliz" style="max-width: 100%;"></a>
<a href="https://discord.gg/Q8C6WEjSWV" rel="nofollow"><img src="https://camo.githubusercontent.com/c91de9d739e38892d250bf9d2e76c46bcd23cfb6fbd3b19dd125b09216b9ed17/68747470733a2f2f696d672e736869656c64732e696f2f646973636f72642f313039323634383433323439353235313530373f6c6162656c3d446973636f7264266c6f676f3d646973636f7264" alt="不和谐" data-canonical-src="https://img.shields.io/discord/1092648432495251507?label=Discord&amp;logo=discord" style="max-width: 100%;"></a></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">🎉 GPTCache 已与🦜️🔗 </font></font><a href="https://github.com/hwchase17/langchain"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LangChain</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">全面集成！这里有详细的</font></font><a href="https://python.langchain.com/docs/modules/model_io/models/llms/integrations/llm_caching#gptcache" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用说明</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">🐳 </font></font><a href="https://github.com/zilliztech/GPTCache/blob/main/docs/usage.md#Use-GPTCache-server"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPTCache 服务器 docker 镜像</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">已经发布，这意味着</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">任何语言都</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">可以使用 GPTCache！</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">📔 该项目正在快速开发，因此 API 可能随时更改。有关最新信息，请参阅最新</font></font><a href="https://gptcache.readthedocs.io/en/latest/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文档</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><a href="https://github.com/zilliztech/GPTCache/blob/main/docs/release_note.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">发行说明</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">快速安装</font></font></h2><a id="user-content-quick-install" class="anchor" aria-label="永久链接：快速安装" href="#quick-install"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><code>pip install gptcache</code></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">🚀 什么是 GPTCache？</font></font></h2><a id="user-content--what-is-gptcache" class="anchor" aria-label="永久链接：🚀 什么是 GPTCache？" href="#-what-is-gptcache"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ChatGPT 和各种大型语言模型 (LLM) 拥有令人难以置信的多功能性，支持开发各种应用程序。然而，随着您的应用程序越来越受欢迎并遇到更高的流量水平，与 LLM API 调用相关的费用可能会变得相当可观。此外，LLM 服务可能会表现出响应时间缓慢，尤其是在处理大量请求时。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为了应对这一挑战，我们创建了 GPTCache，这是一个致力于构建用于存储 LLM 响应的语义缓存的项目。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">😊 快速开始</font></font></h2><a id="user-content--quick-start" class="anchor" aria-label="永久链接：😊 快速入门" href="#-quick-start"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">笔记</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可以快速尝试 GPTCache 并将其投入生产环境，无需进行大量开发。但是，请注意，该存储库仍在大力开发中。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">默认情况下，仅安装有限数量的库来支持基本缓存功能。当您需要使用附加功能时，会</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">自动安装</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">相关库。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">确保Python版本为</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3.8.1或更高</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">版本，检查：</font></font><code>python --version</code></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果由于 pip 版本较低而安装库时遇到问题，请运行：</font></font><code>python -m pip install --upgrade pip</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">开发安装</font></font></h3><a id="user-content-dev-install" class="anchor" aria-label="永久链接：开发安装" href="#dev-install"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c"><span class="pl-c">#</span> clone GPTCache repo</span>
git clone -b dev https://github.com/zilliztech/GPTCache.git
<span class="pl-c1">cd</span> GPTCache

<span class="pl-c"><span class="pl-c">#</span> install the repo</span>
pip install -r requirements.txt
python setup.py install</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="# clone GPTCache repo
git clone -b dev https://github.com/zilliztech/GPTCache.git
cd GPTCache

# install the repo
pip install -r requirements.txt
python setup.py install" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">用法示例</font></font></h3><a id="user-content-example-usage" class="anchor" aria-label="永久链接：示例用法" href="#example-usage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">这些示例将帮助您了解如何使用缓存的精确匹配和相似匹配。您还可以在</font></font><a href="https://colab.research.google.com/drive/1m1s-iTDfLDk-UwUAQ_L8j1C-gzkcr2Sk?usp=share_link" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Colab</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">上运行该示例。更多示例可以参考</font></font><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/openai/chat.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Bootcamp</font></font></a></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在运行示例之前，</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请确保</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">通过执行设置 OPENAI_API_KEY 环境变量</font></font><code>echo $OPENAI_API_KEY</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果尚未设置，可以</font></font><code>export OPENAI_API_KEY=YOUR_API_KEY</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在 Unix/Linux/MacOS 系统或</font></font><code>set OPENAI_API_KEY=YOUR_API_KEY</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Windows 系统上使用进行设置。</font></font></p>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">需要注意的是，这种方法只是暂时有效，所以如果想要永久生效，就需要修改环境变量配置文件。例如，在 Mac 上，您可以修改位于 的文件</font></font><code>/etc/profile</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
</blockquote>
<details>
<summary><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">单击</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">显示</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">示例代码</font></font></summary>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAI API原始用法</font></font></h4><a id="user-content-openai-api-original-usage" class="anchor" aria-label="永久链接：OpenAI API 原始用法" href="#openai-api-original-usage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-s1">os</span>
<span class="pl-k">import</span> <span class="pl-s1">time</span>

<span class="pl-k">import</span> <span class="pl-s1">openai</span>


<span class="pl-k">def</span> <span class="pl-en">response_text</span>(<span class="pl-s1">openai_resp</span>):
    <span class="pl-k">return</span> <span class="pl-s1">openai_resp</span>[<span class="pl-s">'choices'</span>][<span class="pl-c1">0</span>][<span class="pl-s">'message'</span>][<span class="pl-s">'content'</span>]


<span class="pl-s1">question</span> <span class="pl-c1">=</span> <span class="pl-s">'what‘s chatgpt'</span>

<span class="pl-c"># OpenAI API original usage</span>
<span class="pl-s1">openai</span>.<span class="pl-s1">api_key</span> <span class="pl-c1">=</span> <span class="pl-s1">os</span>.<span class="pl-en">getenv</span>(<span class="pl-s">"OPENAI_API_KEY"</span>)
<span class="pl-s1">start_time</span> <span class="pl-c1">=</span> <span class="pl-s1">time</span>.<span class="pl-en">time</span>()
<span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">openai</span>.<span class="pl-v">ChatCompletion</span>.<span class="pl-en">create</span>(
  <span class="pl-s1">model</span><span class="pl-c1">=</span><span class="pl-s">'gpt-3.5-turbo'</span>,
  <span class="pl-s1">messages</span><span class="pl-c1">=</span>[
    {
        <span class="pl-s">'role'</span>: <span class="pl-s">'user'</span>,
        <span class="pl-s">'content'</span>: <span class="pl-s1">question</span>
    }
  ],
)
<span class="pl-en">print</span>(<span class="pl-s">f'Question: <span class="pl-s1"><span class="pl-kos">{</span><span class="pl-s1">question</span><span class="pl-kos">}</span></span>'</span>)
<span class="pl-en">print</span>(<span class="pl-s">"Time consuming: {:.2f}s"</span>.<span class="pl-en">format</span>(<span class="pl-s1">time</span>.<span class="pl-en">time</span>() <span class="pl-c1">-</span> <span class="pl-s1">start_time</span>))
<span class="pl-en">print</span>(<span class="pl-s">f'Answer: <span class="pl-s1"><span class="pl-kos">{</span><span class="pl-en">response_text</span>(<span class="pl-s1">response</span>)<span class="pl-kos">}</span></span><span class="pl-cce">\n</span>'</span>)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import os
import time

import openai


def response_text(openai_resp):
    return openai_resp['choices'][0]['message']['content']


question = 'what‘s chatgpt'

# OpenAI API original usage
openai.api_key = os.getenv(&quot;OPENAI_API_KEY&quot;)
start_time = time.time()
response = openai.ChatCompletion.create(
  model='gpt-3.5-turbo',
  messages=[
    {
        'role': 'user',
        'content': question
    }
  ],
)
print(f'Question: {question}')
print(&quot;Time consuming: {:.2f}s&quot;.format(time.time() - start_time))
print(f'Answer: {response_text(response)}\n')
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAI API + GPTCache，精确匹配缓存</font></font></h4><a id="user-content-openai-api--gptcache-exact-match-cache" class="anchor" aria-label="永久链接：OpenAI API + GPTCache，精确匹配缓存" href="#openai-api--gptcache-exact-match-cache"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您向 ChatGPT 询问完全相同的两个问题，则将从缓存中获取第二个问题的答案，而无需再次请求 ChatGPT。</font></font></p>
</blockquote>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-s1">time</span>


<span class="pl-k">def</span> <span class="pl-en">response_text</span>(<span class="pl-s1">openai_resp</span>):
    <span class="pl-k">return</span> <span class="pl-s1">openai_resp</span>[<span class="pl-s">'choices'</span>][<span class="pl-c1">0</span>][<span class="pl-s">'message'</span>][<span class="pl-s">'content'</span>]

<span class="pl-en">print</span>(<span class="pl-s">"Cache loading....."</span>)

<span class="pl-c"># To use GPTCache, that's all you need</span>
<span class="pl-c"># -------------------------------------------------</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span> <span class="pl-k">import</span> <span class="pl-s1">cache</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">adapter</span> <span class="pl-k">import</span> <span class="pl-s1">openai</span>

<span class="pl-s1">cache</span>.<span class="pl-en">init</span>()
<span class="pl-s1">cache</span>.<span class="pl-en">set_openai_key</span>()
<span class="pl-c"># -------------------------------------------------</span>

<span class="pl-s1">question</span> <span class="pl-c1">=</span> <span class="pl-s">"what's github"</span>
<span class="pl-k">for</span> <span class="pl-s1">_</span> <span class="pl-c1">in</span> <span class="pl-en">range</span>(<span class="pl-c1">2</span>):
    <span class="pl-s1">start_time</span> <span class="pl-c1">=</span> <span class="pl-s1">time</span>.<span class="pl-en">time</span>()
    <span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">openai</span>.<span class="pl-v">ChatCompletion</span>.<span class="pl-en">create</span>(
      <span class="pl-s1">model</span><span class="pl-c1">=</span><span class="pl-s">'gpt-3.5-turbo'</span>,
      <span class="pl-s1">messages</span><span class="pl-c1">=</span>[
        {
            <span class="pl-s">'role'</span>: <span class="pl-s">'user'</span>,
            <span class="pl-s">'content'</span>: <span class="pl-s1">question</span>
        }
      ],
    )
    <span class="pl-en">print</span>(<span class="pl-s">f'Question: <span class="pl-s1"><span class="pl-kos">{</span><span class="pl-s1">question</span><span class="pl-kos">}</span></span>'</span>)
    <span class="pl-en">print</span>(<span class="pl-s">"Time consuming: {:.2f}s"</span>.<span class="pl-en">format</span>(<span class="pl-s1">time</span>.<span class="pl-en">time</span>() <span class="pl-c1">-</span> <span class="pl-s1">start_time</span>))
    <span class="pl-en">print</span>(<span class="pl-s">f'Answer: <span class="pl-s1"><span class="pl-kos">{</span><span class="pl-en">response_text</span>(<span class="pl-s1">response</span>)<span class="pl-kos">}</span></span><span class="pl-cce">\n</span>'</span>)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import time


def response_text(openai_resp):
    return openai_resp['choices'][0]['message']['content']

print(&quot;Cache loading.....&quot;)

# To use GPTCache, that's all you need
# -------------------------------------------------
from gptcache import cache
from gptcache.adapter import openai

cache.init()
cache.set_openai_key()
# -------------------------------------------------

question = &quot;what's github&quot;
for _ in range(2):
    start_time = time.time()
    response = openai.ChatCompletion.create(
      model='gpt-3.5-turbo',
      messages=[
        {
            'role': 'user',
            'content': question
        }
      ],
    )
    print(f'Question: {question}')
    print(&quot;Time consuming: {:.2f}s&quot;.format(time.time() - start_time))
    print(f'Answer: {response_text(response)}\n')" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAI API + GPTCache，类似搜索缓存</font></font></h4><a id="user-content-openai-api--gptcache-similar-search-cache" class="anchor" aria-label="永久链接：OpenAI API + GPTCache，类似搜索缓存" href="#openai-api--gptcache-similar-search-cache"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">从ChatGPT获得针对几个类似问题的答案后，可以从缓存中检索后续问题的答案，而无需再次请求ChatGPT。</font></font></p>
</blockquote>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-s1">time</span>


<span class="pl-k">def</span> <span class="pl-en">response_text</span>(<span class="pl-s1">openai_resp</span>):
    <span class="pl-k">return</span> <span class="pl-s1">openai_resp</span>[<span class="pl-s">'choices'</span>][<span class="pl-c1">0</span>][<span class="pl-s">'message'</span>][<span class="pl-s">'content'</span>]

<span class="pl-k">from</span> <span class="pl-s1">gptcache</span> <span class="pl-k">import</span> <span class="pl-s1">cache</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">adapter</span> <span class="pl-k">import</span> <span class="pl-s1">openai</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">embedding</span> <span class="pl-k">import</span> <span class="pl-v">Onnx</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">manager</span> <span class="pl-k">import</span> <span class="pl-v">CacheBase</span>, <span class="pl-v">VectorBase</span>, <span class="pl-s1">get_data_manager</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">similarity_evaluation</span>.<span class="pl-s1">distance</span> <span class="pl-k">import</span> <span class="pl-v">SearchDistanceEvaluation</span>

<span class="pl-en">print</span>(<span class="pl-s">"Cache loading....."</span>)

<span class="pl-s1">onnx</span> <span class="pl-c1">=</span> <span class="pl-v">Onnx</span>()
<span class="pl-s1">data_manager</span> <span class="pl-c1">=</span> <span class="pl-en">get_data_manager</span>(<span class="pl-v">CacheBase</span>(<span class="pl-s">"sqlite"</span>), <span class="pl-v">VectorBase</span>(<span class="pl-s">"faiss"</span>, <span class="pl-s1">dimension</span><span class="pl-c1">=</span><span class="pl-s1">onnx</span>.<span class="pl-s1">dimension</span>))
<span class="pl-s1">cache</span>.<span class="pl-en">init</span>(
    <span class="pl-s1">embedding_func</span><span class="pl-c1">=</span><span class="pl-s1">onnx</span>.<span class="pl-s1">to_embeddings</span>,
    <span class="pl-s1">data_manager</span><span class="pl-c1">=</span><span class="pl-s1">data_manager</span>,
    <span class="pl-s1">similarity_evaluation</span><span class="pl-c1">=</span><span class="pl-v">SearchDistanceEvaluation</span>(),
    )
<span class="pl-s1">cache</span>.<span class="pl-en">set_openai_key</span>()

<span class="pl-s1">questions</span> <span class="pl-c1">=</span> [
    <span class="pl-s">"what's github"</span>,
    <span class="pl-s">"can you explain what GitHub is"</span>,
    <span class="pl-s">"can you tell me more about GitHub"</span>,
    <span class="pl-s">"what is the purpose of GitHub"</span>
]

<span class="pl-k">for</span> <span class="pl-s1">question</span> <span class="pl-c1">in</span> <span class="pl-s1">questions</span>:
    <span class="pl-s1">start_time</span> <span class="pl-c1">=</span> <span class="pl-s1">time</span>.<span class="pl-en">time</span>()
    <span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">openai</span>.<span class="pl-v">ChatCompletion</span>.<span class="pl-en">create</span>(
        <span class="pl-s1">model</span><span class="pl-c1">=</span><span class="pl-s">'gpt-3.5-turbo'</span>,
        <span class="pl-s1">messages</span><span class="pl-c1">=</span>[
            {
                <span class="pl-s">'role'</span>: <span class="pl-s">'user'</span>,
                <span class="pl-s">'content'</span>: <span class="pl-s1">question</span>
            }
        ],
    )
    <span class="pl-en">print</span>(<span class="pl-s">f'Question: <span class="pl-s1"><span class="pl-kos">{</span><span class="pl-s1">question</span><span class="pl-kos">}</span></span>'</span>)
    <span class="pl-en">print</span>(<span class="pl-s">"Time consuming: {:.2f}s"</span>.<span class="pl-en">format</span>(<span class="pl-s1">time</span>.<span class="pl-en">time</span>() <span class="pl-c1">-</span> <span class="pl-s1">start_time</span>))
    <span class="pl-en">print</span>(<span class="pl-s">f'Answer: <span class="pl-s1"><span class="pl-kos">{</span><span class="pl-en">response_text</span>(<span class="pl-s1">response</span>)<span class="pl-kos">}</span></span><span class="pl-cce">\n</span>'</span>)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import time


def response_text(openai_resp):
    return openai_resp['choices'][0]['message']['content']

from gptcache import cache
from gptcache.adapter import openai
from gptcache.embedding import Onnx
from gptcache.manager import CacheBase, VectorBase, get_data_manager
from gptcache.similarity_evaluation.distance import SearchDistanceEvaluation

print(&quot;Cache loading.....&quot;)

onnx = Onnx()
data_manager = get_data_manager(CacheBase(&quot;sqlite&quot;), VectorBase(&quot;faiss&quot;, dimension=onnx.dimension))
cache.init(
    embedding_func=onnx.to_embeddings,
    data_manager=data_manager,
    similarity_evaluation=SearchDistanceEvaluation(),
    )
cache.set_openai_key()

questions = [
    &quot;what's github&quot;,
    &quot;can you explain what GitHub is&quot;,
    &quot;can you tell me more about GitHub&quot;,
    &quot;what is the purpose of GitHub&quot;
]

for question in questions:
    start_time = time.time()
    response = openai.ChatCompletion.create(
        model='gpt-3.5-turbo',
        messages=[
            {
                'role': 'user',
                'content': question
            }
        ],
    )
    print(f'Question: {question}')
    print(&quot;Time consuming: {:.2f}s&quot;.format(time.time() - start_time))
    print(f'Answer: {response_text(response)}\n')" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAI API + GPTCache，使用温度</font></font></h4><a id="user-content-openai-api--gptcache-use-temperature" class="anchor" aria-label="永久链接：OpenAI API + GPTCache，使用温度" href="#openai-api--gptcache-use-temperature"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在请求 API 服务或模型时，您始终可以传递温度参数。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">取值范围</font></font><code>temperature</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为[0, 2]，默认值为0.0。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">温度越高，意味着越有可能跳过缓存搜索，直接请求大模型。当温度为2时，肯定会跳过缓存，直接向大模型发送请求。当温度为0时，会在请求大模型服务之前先查找缓存。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">默认</font></font><code>post_process_messages_func</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为</font></font><code>temperature_softmax</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">.在这种情况下，请参阅</font></font><a href="https://gptcache.readthedocs.io/en/latest/references/processor.html#module-gptcache.processor.post" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">API 参考</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">以了解如何</font></font><code>temperature</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">影响输出。</font></font></p>
</blockquote>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-s1">time</span>

<span class="pl-k">from</span> <span class="pl-s1">gptcache</span> <span class="pl-k">import</span> <span class="pl-s1">cache</span>, <span class="pl-v">Config</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">manager</span> <span class="pl-k">import</span> <span class="pl-s1">manager_factory</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">embedding</span> <span class="pl-k">import</span> <span class="pl-v">Onnx</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">processor</span>.<span class="pl-s1">post</span> <span class="pl-k">import</span> <span class="pl-s1">temperature_softmax</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">similarity_evaluation</span>.<span class="pl-s1">distance</span> <span class="pl-k">import</span> <span class="pl-v">SearchDistanceEvaluation</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">adapter</span> <span class="pl-k">import</span> <span class="pl-s1">openai</span>

<span class="pl-s1">cache</span>.<span class="pl-en">set_openai_key</span>()

<span class="pl-s1">onnx</span> <span class="pl-c1">=</span> <span class="pl-v">Onnx</span>()
<span class="pl-s1">data_manager</span> <span class="pl-c1">=</span> <span class="pl-en">manager_factory</span>(<span class="pl-s">"sqlite,faiss"</span>, <span class="pl-s1">vector_params</span><span class="pl-c1">=</span>{<span class="pl-s">"dimension"</span>: <span class="pl-s1">onnx</span>.<span class="pl-s1">dimension</span>})

<span class="pl-s1">cache</span>.<span class="pl-en">init</span>(
    <span class="pl-s1">embedding_func</span><span class="pl-c1">=</span><span class="pl-s1">onnx</span>.<span class="pl-s1">to_embeddings</span>,
    <span class="pl-s1">data_manager</span><span class="pl-c1">=</span><span class="pl-s1">data_manager</span>,
    <span class="pl-s1">similarity_evaluation</span><span class="pl-c1">=</span><span class="pl-v">SearchDistanceEvaluation</span>(),
    <span class="pl-s1">post_process_messages_func</span><span class="pl-c1">=</span><span class="pl-s1">temperature_softmax</span>
    )
<span class="pl-c"># cache.config = Config(similarity_threshold=0.2)</span>

<span class="pl-s1">question</span> <span class="pl-c1">=</span> <span class="pl-s">"what's github"</span>

<span class="pl-k">for</span> <span class="pl-s1">_</span> <span class="pl-c1">in</span> <span class="pl-en">range</span>(<span class="pl-c1">3</span>):
    <span class="pl-s1">start</span> <span class="pl-c1">=</span> <span class="pl-s1">time</span>.<span class="pl-en">time</span>()
    <span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">openai</span>.<span class="pl-v">ChatCompletion</span>.<span class="pl-en">create</span>(
        <span class="pl-s1">model</span><span class="pl-c1">=</span><span class="pl-s">"gpt-3.5-turbo"</span>,
        <span class="pl-s1">temperature</span> <span class="pl-c1">=</span> <span class="pl-c1">1.0</span>,  <span class="pl-c"># Change temperature here</span>
        <span class="pl-s1">messages</span><span class="pl-c1">=</span>[{
            <span class="pl-s">"role"</span>: <span class="pl-s">"user"</span>,
            <span class="pl-s">"content"</span>: <span class="pl-s1">question</span>
        }],
    )
    <span class="pl-en">print</span>(<span class="pl-s">"Time elapsed:"</span>, <span class="pl-en">round</span>(<span class="pl-s1">time</span>.<span class="pl-en">time</span>() <span class="pl-c1">-</span> <span class="pl-s1">start</span>, <span class="pl-c1">3</span>))
    <span class="pl-en">print</span>(<span class="pl-s">"Answer:"</span>, <span class="pl-s1">response</span>[<span class="pl-s">"choices"</span>][<span class="pl-c1">0</span>][<span class="pl-s">"message"</span>][<span class="pl-s">"content"</span>])</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import time

from gptcache import cache, Config
from gptcache.manager import manager_factory
from gptcache.embedding import Onnx
from gptcache.processor.post import temperature_softmax
from gptcache.similarity_evaluation.distance import SearchDistanceEvaluation
from gptcache.adapter import openai

cache.set_openai_key()

onnx = Onnx()
data_manager = manager_factory(&quot;sqlite,faiss&quot;, vector_params={&quot;dimension&quot;: onnx.dimension})

cache.init(
    embedding_func=onnx.to_embeddings,
    data_manager=data_manager,
    similarity_evaluation=SearchDistanceEvaluation(),
    post_process_messages_func=temperature_softmax
    )
# cache.config = Config(similarity_threshold=0.2)

question = &quot;what's github&quot;

for _ in range(3):
    start = time.time()
    response = openai.ChatCompletion.create(
        model=&quot;gpt-3.5-turbo&quot;,
        temperature = 1.0,  # Change temperature here
        messages=[{
            &quot;role&quot;: &quot;user&quot;,
            &quot;content&quot;: question
        }],
    )
    print(&quot;Time elapsed:&quot;, round(time.time() - start, 3))
    print(&quot;Answer:&quot;, response[&quot;choices&quot;][0][&quot;message&quot;][&quot;content&quot;])" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</details>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">独占使用GPTCache只需要以下几行代码，无需修改任何现有代码。</font></font></p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">from</span> <span class="pl-s1">gptcache</span> <span class="pl-k">import</span> <span class="pl-s1">cache</span>
<span class="pl-k">from</span> <span class="pl-s1">gptcache</span>.<span class="pl-s1">adapter</span> <span class="pl-k">import</span> <span class="pl-s1">openai</span>

<span class="pl-s1">cache</span>.<span class="pl-en">init</span>()
<span class="pl-s1">cache</span>.<span class="pl-en">set_openai_key</span>()</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="from gptcache import cache
from gptcache.adapter import openai

cache.init()
cache.set_openai_key()" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">更多文档：</font></font></p>
<ul dir="auto">
<li><a href="/zilliztech/GPTCache/blob/main/docs/usage.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">用法，如何更好的使用GPTCache</font></font></a></li>
<li><a href="/zilliztech/GPTCache/blob/main/docs/feature.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">特性，缓存当前支持的所有特性</font></font></a></li>
<li><a href="/zilliztech/GPTCache/blob/main/examples/README.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">示例，更好的学习自定义缓存</font></font></a></li>
<li><a href="/zilliztech/GPTCache/blob/main/docs/horizontal-scaling-usage.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">分布式缓存和水平扩展</font></font></a></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">🎓 训练营</font></font></h2><a id="user-content--bootcamp" class="anchor" aria-label="永久链接：🎓 训练营" href="#-bootcamp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPTCache 与</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LangChain</font></font></strong>
<ul dir="auto">
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/langchain/qa_generation.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">质量保证一代</font></font></a></li>
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/langchain/question_answering.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">问答</font></font></a></li>
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/langchain/sqlite.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">SQL链</font></font></a></li>
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/langchain/baby_agi.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">BabyAGI 用户指南</font></font></a></li>
</ul>
</li>
<li><font style="vertical-align: inherit;"><strong><font style="vertical-align: inherit;">带有Llama_index</font></strong><font style="vertical-align: inherit;">的 GPTCache</font></font><strong><font style="vertical-align: inherit;"></font></strong>
<ul dir="auto">
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/llama_index/webpage_qa.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">网页质量检查</font></font></a></li>
</ul>
</li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPTCache 与</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAI</font></font></strong>
<ul dir="auto">
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/openai/chat.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">聊天完成</font></font></a></li>
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/openai/language_translate.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">语言翻译</font></font></a></li>
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/openai/sql_translate.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">SQL 翻译</font></font></a></li>
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/openai/tweet_classifier.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">推特分类器</font></font></a></li>
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/openai/image_generation.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">多模态：图像生成</font></font></a></li>
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/openai/speech_to_text.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">多模式：语音转文本</font></font></a></li>
</ul>
</li>
<li><font style="vertical-align: inherit;"><strong><font style="vertical-align: inherit;">带复制的</font></strong><font style="vertical-align: inherit;">GPTCache</font></font><strong><font style="vertical-align: inherit;"></font></strong>
<ul dir="auto">
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/replicate/visual_question_answering.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">视觉问答</font></font></a></li>
</ul>
</li>
<li><font style="vertical-align: inherit;"><strong><font style="vertical-align: inherit;">带温度参数</font></strong><font style="vertical-align: inherit;">的 GPTCache</font></font><strong><font style="vertical-align: inherit;"></font></strong>
<ul dir="auto">
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/temperature/chat.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAI 聊天</font></font></a></li>
<li><a href="https://gptcache.readthedocs.io/en/latest/bootcamp/temperature/create_image.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAI 图像创建</font></font></a></li>
</ul>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">😎 这有什么帮助？</font></font></h2><a id="user-content--what-can-this-help-with" class="anchor" aria-label="永久链接： 😎 这有什么帮助？" href="#-what-can-this-help-with"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPTCache 具有以下主要优点：</font></font></p>
<ul dir="auto">
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">减少费用</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：大多数法学硕士服务根据请求数量和</font></font><a href="https://openai.com/pricing" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">令牌计数</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的组合收取费用。 GPTCache 通过缓存查询结果有效地最大限度地减少您的开支，从而减少发送到 LLM 服务的请求和令牌的数量。因此，您在使用该服务时可以享受更具成本效益的体验。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">增强的性能</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：法学硕士采用生成式人工智能算法来实时生成响应，这个过程有时可能非常耗时。但是，当缓存类似的查询时，响应时间会显着缩短，因为结果是直接从缓存中获取的，从而无需与 LLM 服务交互。在大多数情况下，与标准 LLM 服务相比，GPTCache 还可以提供卓越的查询吞吐量。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">适应性强的开发和测试环境</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：作为从事 LLM 应用程序的开发人员，您知道连接到 LLM API 通常是必要的，并且在将应用程序迁移到生产环境之前对其进行全面测试至关重要。 GPTCache 提供了一个镜像 LLM API 的接口，并可容纳 LLM 生成的数据和模拟数据的存储。此功能使您能够轻松开发和测试您的应用程序，无需连接到 LLM 服务。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">提高可扩展性和可用性</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：LLM 服务经常强制执行</font></font><a href="https://platform.openai.com/docs/guides/rate-limits" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">速率限制</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，这是 API 对用户或客户端在给定时间范围内访问服务器的次数施加的限制。达到速率限制意味着额外的请求将被阻止，直到经过一定时间，从而导致服务中断。借助 GPTCache，您可以轻松扩展以适应不断增加的查询量，从而确保随着应用程序用户群的扩展而保持一致的性能。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">🤔 它是如何运作的？</font></font></h2><a id="user-content--how-does-it-work" class="anchor" aria-label="永久链接： 🤔 它是如何工作的？" href="#-how-does-it-work"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在线服务通常表现出数据局部性，用户经常访问流行或趋势内容。缓存系统通过存储经常访问的数据来利用这种行为，从而减少数据检索时间，提高响应时间，并减轻后端服务器的负担。传统的缓存系统通常利用新查询和缓存的查询之间的精确匹配来确定所请求的内容在获取数据之前在缓存中是否可用。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">然而，由于LLM查询的复杂性和可变性，对LLM缓存使用精确匹配方法效果较差，导致缓存命中率较低。为了解决这个问题，GPTCache 采用了语义缓存等替代策略。语义缓存识别并存储相似或相关的查询，从而增加缓存命中概率并提高整体缓存效率。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPTCache 采用嵌入算法将查询转换为嵌入，并使用向量存储对这些嵌入进行相似性搜索。此过程允许 GPTCache 从缓存存储中识别并检索类似或相关的查询，如</font></font><a href="https://github.com/zilliztech/GPTCache#-modules"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模块部分</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">所示。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPTCache 采用模块化设计，使用户可以轻松定制自己的语义缓存。系统为每个模块提供了多种实现方式，用户甚至可以开发自己的实现方式来满足自己的特定需求。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在语义缓存中，您可能会在缓存命中期间遇到误报，在缓存未命中期间遇到误报。 GPTCache 提供了三个指标来衡量其性能，这有助于开发人员优化其缓存系统：</font></font></p>
<ul dir="auto">
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">命中率</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：该指标量化了缓存成功满足内容请求的能力（与其接收的请求总数相比）。命中率越高表明缓存越有效。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">延迟</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：该指标衡量处理查询以及从缓存检索相应数据所需的时间。更低的延迟意味着更高效、响应更灵敏的缓存系统。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">召回率</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：该指标表示缓存服务的查询占缓存应服务的查询总数的比例。较高的召回率表明缓存正在有效地提供适当的内容。</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">其中包含一个</font></font><a href="https://github.com/zilliztech/gpt-cache/blob/main/examples/benchmark/benchmark_sqlite_faiss_onnx.py"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">示例基准测试</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，供用户开始评估其语义缓存的性能。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">🤗 模块</font></font></h2><a id="user-content--modules" class="anchor" aria-label="永久链接：🤗 模块" href="#-modules"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="/zilliztech/GPTCache/blob/main/docs/GPTCacheStructure.png"><img src="/zilliztech/GPTCache/raw/main/docs/GPTCacheStructure.png" alt="GPT缓存结构" style="max-width: 100%;"></a></p>
<ul dir="auto">
<li>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LLM 适配器</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：LLM 适配器旨在通过统一 API 和请求协议来集成不同的 LLM 模型。 GPTCache 为此提供了一个标准化接口，目前支持 ChatGPT 集成。</font></font></p>
<ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持 OpenAI ChatGPT API。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://github.com/hwchase17/langchain"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">langchain</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://github.com/Vision-CAIR/MiniGPT-4.git"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">minipt4</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://github.com/ggerganov/llama.cpp.git"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">拉马普</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://github.com/databrickslabs/dolly.git"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">多莉</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持其他法学硕士，例如 Hugging Face Hub、Bard、Anthropic。</font></font></li>
</ul>
</li>
<li>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">多模式适配器（实验性）</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：多模式适配器旨在通过统一 API 和请求协议来集成不同的大型多模式模型。 GPTCache 为此提供了一个标准化接口，目前支持图像生成、音频转录的集成。</font></font></p>
<ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持OpenAI图像创建API。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持 OpenAI 音频转录 API。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持复制BLIP API。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持稳定性推断API。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持拥抱面稳定扩散管道（局部推理）。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持其他多式联运服务或自托管大型多式联运模型。</font></font></li>
</ul>
</li>
<li>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">嵌入生成器</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：创建此模块是为了从相似性搜索请求中提取嵌入。 GPTCache 提供了支持多种嵌入 API 的通用接口，并提供了一系列可供选择的解决方案。</font></font></p>
<ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">禁用嵌入。这会将 GPTCache 变成关键字匹配缓存。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持OpenAI嵌入API。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用 GPTCache/paraphrase-albert-onnx 模型</font><font style="vertical-align: inherit;">支持</font></font><a href="https://onnx.ai/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ONNX 。</font></font></a><font style="vertical-align: inherit;"></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font><font style="vertical-align: inherit;">使用 Transformer、ViTModel、Data2VecAudio 嵌入</font></font><a href="https://huggingface.co/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Hugging Face 。</font></font></a><font style="vertical-align: inherit;"></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://docs.cohere.ai/reference/embed" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Cohere</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">嵌入API。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://fasttext.cc" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">fastText</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">嵌入。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://www.sbert.net" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">SentenceTransformers</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">嵌入。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://timm.fast.ai/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Timm</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模型进行图像嵌入。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持其他嵌入API。</font></font></li>
</ul>
</li>
<li>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">缓存存储</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：
</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">缓存存储</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是存储来自 LLM（例如 ChatGPT）的响应的位置。检索缓存的响应以帮助评估相似性，如果存在良好的语义匹配，则将其返回给请求者。目前，GPTCache支持SQLite，并提供了一个通用的接口来扩展该模块。</font></font></p>
<ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://sqlite.org/docs.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">SQLite</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://duckdb.org/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">DuckDB</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://www.postgresql.org/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">PostgreSQL</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://www.mysql.com/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">MySQL</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://mariadb.org/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">玛丽亚数据库</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://www.microsoft.com/en-us/sql-server/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">SQL服务器</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://www.oracle.com/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">甲骨文</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://aws.amazon.com/dynamodb/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">DynamoDB</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://www.mongodb.com/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">MongoDB</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://redis.io/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Redis</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://min.io/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">迷你</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://hbase.apache.org/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">HBase</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://www.elastic.co/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">弹性搜索</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持其他存储。</font></font></li>
</ul>
</li>
<li>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Vector Store</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Vector Store</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模块帮助从输入请求的提取嵌入中找到 K 个最相似的请求。结果可以帮助评估相似性。 GPTCache 提供了用户友好的界面，支持各种向量存储，包括 Milvus、Zilliz Cloud 和 FAISS。未来将提供更多选择。</font></font></p>
<ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://milvus.io/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Milvus</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，这是一个用于生产就绪的 AI/LLM 应用程序的开源矢量数据库。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://cloud.zilliz.com/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Zilliz Cloud</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，一个基于 Milvus 的完全托管的云矢量数据库。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://github.com/milvus-io/milvus-lite"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Milvus Lite</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，这是 Milvus 的轻量级版本，可以嵌入到您的 Python 应用程序中。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://faiss.ai/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FAISS</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，一个用于高效相似性搜索和密集向量聚类的库。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://github.com/nmslib/hnswlib"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Hnswlib</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，仅头文件的 C++/python 库，用于快速近似最近邻。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://github.com/pgvector/pgvector"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">PGVector</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，Postgres 的开源向量相似性搜索。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font><font style="vertical-align: inherit;">AI 原生开源嵌入数据库</font></font><a href="https://github.com/chroma-core/chroma"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Chroma 。</font></font></a><font style="vertical-align: inherit;"></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font><a href="https://github.com/docarray/docarray"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">DocArray</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，DocArray 是一个用于表示、发送和存储多模态数据的库，非常适合机器学习应用。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持qdrant</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持取消</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持其他矢量数据库。</font></font></li>
</ul>
</li>
<li>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">缓存管理器</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">缓存管理器</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">负责控制</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">缓存存储</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">向量存储</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的操作。</font></font></p>
<ul dir="auto">
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">逐出策略</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：可以使用 python 在内存中管理缓存逐出</font></font><code>cachetools</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，也可以使用 Redis 作为键值存储以分布式方式进行管理。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">内存缓存</font></font></strong></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目前，GPTCache 仅根据行数做出驱逐决策。此方法可能会导致资源评估不准确，并可能导致内存不足 (OOM) 错误。我们正在积极研究和制定更复杂的策略。</font></font></p>
<ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持LRU驱逐政策。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持先进先出驱逐政策。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持LFU驱逐政策。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持RR驱逐政策。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持更复杂的驱逐政策。</font></font></li>
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">分布式缓存</font></font></strong></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您要使用内存缓存水平扩展 GPTCache 部署，这是不可能的。由于缓存的信息仅限于单个 Pod。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">通过分布式缓存，缓存信息在所有副本中保持一致，我们可以使用分布式缓存存储（例如 Redis）。</font></font></p>
<ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持Redis分布式缓存</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持memcached分布式缓存</font></font></li>
</ul>
</li>
<li>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">相似度评估器</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：该模块从缓存</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">存储</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">向量存储收集数据，并使用各种策略来确定输入请求与</font></font></strong><font style="vertical-align: inherit;"></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">向量存储</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的请求之间的相似性</font><font style="vertical-align: inherit;">。根据这种相似性，它确定请求是否与缓存匹配。 GPTCache 提供了一个用于集成各种策略的标准化接口，以及可供使用的实现集合。目前支持或将来支持以下相似度定义：</font></font></p>
<ul class="contains-task-list">
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们从Vector Store</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">获得的距离</font><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"></font><a href="https://onnx.ai/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用ONNX</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">的 GPTCache/albert-duplicate-onnx 模型确定基于模型的相似性</font><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">输入请求与从矢量存储</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中获取的请求之间完全匹配</font><font style="vertical-align: inherit;">。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox" checked=""><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">通过将 numpy 中的 linalg.norm 应用到嵌入来表示距离。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">BM25 和其他相似性测量。</font></font></li>
<li class="task-list-item"><input type="checkbox" id="" disabled="" class="task-list-item-checkbox"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持其他模型服务框架，例如 PyTorch。</font></font></li>
</ul>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：并非所有不同模块的组合都可以彼此兼容。例如，如果我们禁用</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">嵌入提取器</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">，</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">向量存储</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">可能无法按预期运行。我们目前正在致力于对</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GPTCache</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实施组合健全性检查。</font></font></p>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">😇 路线图</font></font></h2><a id="user-content--roadmap" class="anchor" aria-label="永久链接：😇 路线图" href="#-roadmap"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">即将推出！</font></font><a href="https://twitter.com/zilliz_universe" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">敬请关注！</font></font></a></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">😍 贡献</font></font></h2><a id="user-content--contributing" class="anchor" aria-label="永久链接：😍 贡献" href="#-contributing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们非常愿意接受贡献，无论是通过新功能、增强的基础设施还是改进的文档。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有关如何贡献的全面说明，请参阅我们的</font></font><a href="/zilliztech/GPTCache/blob/main/docs/contributing.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">贡献指南</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
</article></div>
