<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><h1 tabindex="-1" dir="auto"><a id="user-content-apriltag-3" class="anchor" aria-hidden="true" tabindex="-1" href="#apriltag-3"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">四月标签 3</font></font></h1>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AprilTag 是机器人研究中流行的视觉基准系统。</font><font style="vertical-align: inherit;">该存储库包含 AprilTag 的最新版本 AprilTag 3，其中包括更快（&gt; 2x）的检测器、改进的小标签检测率、灵活的标签布局和姿势估计。</font><font style="vertical-align: inherit;">AprilTag 由一个具有最小依赖性的小型 C 库组成。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://github.com/AprilRobotics/apriltag-imgs"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可以在此处</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">找到预生成布局的标签图像</font><font style="vertical-align: inherit;">。</font><font style="vertical-align: inherit;">我们建议使用 tagStandard41h12 布局。</font></font></p>
<h1 tabindex="-1" dir="auto"><a id="user-content-table-of-contents" class="anchor" aria-hidden="true" tabindex="-1" href="#table-of-contents"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录</font></font></h1>
<ul dir="auto">
<li><a href="#papers"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件</font></font></a></li>
<li><a href="#install"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">安装</font></font></a></li>
<li><a href="#usage"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">用法</font></font></a>
<ul dir="auto">
<li><a href="#choosing-a-tag-family"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">选择标签系列</font></font></a></li>
<li><a href="#getting-started-with-the-detector"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">探测器入门</font></font></a>
<ul dir="auto">
<li><a href="#python"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Python</font></font></a></li>
<li><a href="#c"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">C</font></font></a></li>
<li><a href="#matlab"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">MATLAB</font></font></a></li>
<li><a href="#julia"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">朱莉娅</font></font></a></li>
</ul>
</li>
<li><a href="#upgrading-from-aprilTag-2"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">从 AprilTag 2 升级</font></font></a></li>
<li><a href="#opencv-integration"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenCV 集成</font></font></a></li>
<li><a href="#tuning-the-detector-parameters"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">调整探测器参数</font></font></a>
<ul dir="auto">
<li><a href="#increasing-speed"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">增加速度。</font></font></a></li>
<li><a href="#increasing-detection-distance"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">增加检测距离。</font></font></a></li>
</ul>
</li>
<li><a href="#pose-estimation"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">姿势估计。</font></font></a></li>
</ul>
</li>
<li><a href="#debugging"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">调试</font></font></a></li>
<li><a href="#flexible-layouts"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">灵活的布局</font></font></a></li>
<li><a href="#support"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font></a></li>
</ul>
<h1 tabindex="-1" dir="auto"><a id="user-content-papers" class="anchor" aria-hidden="true" tabindex="-1" href="#papers"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件</font></font></h1>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AprilTag 是以下论文的主题。</font></font></p>
<p dir="auto"><a href="https://april.eecs.umich.edu/papers/details.php?name=olson2011tags" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AprilTag：强大且灵活的视觉基准系统</font></font></a></p>
<p dir="auto"><a href="https://april.eecs.umich.edu/papers/details.php?name=wang2016iros" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">四月标签 2：高效、稳健的基准检测</font></font></a></p>
<p dir="auto"><a href="https://april.eecs.umich.edu/papers/details.php?name=krogius2019iros" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">基准标签的灵活布局</font></font></a></p>
<h1 tabindex="-1" dir="auto"><a id="user-content-install" class="anchor" aria-hidden="true" tabindex="-1" href="#install"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">安装</font></font></h1>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">官方仅支持 Linux 操作系统，尽管用户也可以在 Windows 上成功安装。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">默认安装会将标头放置在 /usr/local/include 中，将共享库放置在 /usr/local/lib 中。</font><font style="vertical-align: inherit;">它还将 pkg-config 脚本安装到 /usr/local/lib/pkgconfig 中，并且如果安装了 python3，则会安装 python 包装器。</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --target install
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --target install" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">默认情况下，这将构建共享（*.so）库。</font><font style="vertical-align: inherit;">如果您需要静态 (*.a) 库，请设置</font></font><code>BUILD_SHARED_LIBS</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为</font></font><code>OFF</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cmake -B build -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=OFF
cmake --build build --target install
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cmake -B build -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=OFF
cmake --build build --target install" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您</font></font><code>sudo apt install ninja-build</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">安装了 Ninja ( )，您可以使用：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cmake -B build -GNinja -DCMAKE_BUILD_TYPE=Release
cmake --build build --target install
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cmake -B build -GNinja -DCMAKE_BUILD_TYPE=Release
cmake --build build --target install" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">通过 ninja 构建脚本生成和编译。</font><font style="vertical-align: inherit;">它比 cmake 的默认 Makefile 生成器快得多。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"></font><code>--target install</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您只想在本地使用而不安装，则</font><font style="vertical-align: inherit;">可以省略。</font></font></p>
<h1 tabindex="-1" dir="auto"><a id="user-content-usage" class="anchor" aria-hidden="true" tabindex="-1" href="#usage"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">用法</font></font></h1>
<h2 tabindex="-1" dir="auto"><a id="user-content-choosing-a-tag-family" class="anchor" aria-hidden="true" tabindex="-1" href="#choosing-a-tag-family"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">选择标签系列</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于绝大多数应用，tagStandard41h12 系列将是正确的选择。</font></font><a href="https://github.com/AprilRobotics/apriltag-imgs"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可以在apriltag-imgs repo</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中找到标签的图像</font><font style="vertical-align: inherit;">。</font><font style="vertical-align: inherit;">在您最喜欢的编辑器中放大图像并将其打印出来。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">关于何时选择其他标签系列的一些启发：</font></font></p>
<ol dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您需要更多标签，请使用 tagStandard52h13</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果需要最大限度地利用小圆形对象上的空间，请使用 tagCircle49h12（或 tagCircle21h7）。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您想创建递归标签，请使用 tagCustom48h12。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您想与 ArUcO 检测器兼容，请使用 tag36h11</font></font></li>
</ol>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果这些都不满足您的需求，请</font></font><a href="https://github.com/AprilRobotics/apriltag-generation"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在此处</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">生成您自己的自定义标签系列。</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-getting-started-with-the-detector" class="anchor" aria-hidden="true" tabindex="-1" href="#getting-started-with-the-detector"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">探测器入门</font></font></h2>
<h3 tabindex="-1" dir="auto"><a id="user-content-python" class="anchor" aria-hidden="true" tabindex="-1" href="#python"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Python</font></font></h3>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>import cv2
import numpy as np
from apriltag import apriltag

imagepath = 'test.jpg'
image = cv2.imread(imagepath, cv2.IMREAD_GRAYSCALE)
detector = apriltag("tagStandard41h12")

detections = detector.detect(image)
</code></pre><div class="zeroclipboard-container">
     
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://github.com/duckietown/apriltags3-py"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或者，您可以使用由duckietown</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">创建的 AprilTag python 绑定</font><font style="vertical-align: inherit;">。</font></font></p>
<h3 tabindex="-1" dir="auto"><a id="user-content-c" class="anchor" aria-hidden="true" tabindex="-1" href="#c"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">C</font></font></h3>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>image_u8_t* im = image_u8_create_from_pnm("test.png");
apriltag_detector_t *td = apriltag_detector_create();
apriltag_family_t *tf = tagStandard41h12_create();
apriltag_detector_add_family(td, tf);
zarray_t *detections = apriltag_detector_detect(td, im);

for (int i = 0; i &lt; zarray_size(detections); i++) {
    apriltag_detection_t *det;
    zarray_get(detections, i, &amp;det);

    // Do stuff with detections here.
}
// Cleanup.
apriltag_detections_destroy(detections);
tagStandard41h12_destroy(tf);
apriltag_detector_destroy(td);
</code></pre><div class="zeroclipboard-container">
 
  </div></div>
<h3 tabindex="-1" dir="auto"><a id="user-content-matlab" class="anchor" aria-hidden="true" tabindex="-1" href="#matlab"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">MATLAB</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://github.com/alddiaz/MATLAB_AprilTag3"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">此处</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">由第三方提供</font><font style="vertical-align: inherit;">。</font></font></p>
<h3 tabindex="-1" dir="auto"><a id="user-content-julia" class="anchor" aria-hidden="true" tabindex="-1" href="#julia"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">朱莉娅</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"><a href="https://github.com/JuliaRobotics/AprilTags.jl"><font style="vertical-align: inherit;">此处</font></a><font style="vertical-align: inherit;">由第三方提供</font></font><a href="https://github.com/JuliaRobotics/AprilTags.jl"><font style="vertical-align: inherit;"></font></a></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-upgrading-from-apriltag-2" class="anchor" aria-hidden="true" tabindex="-1" href="#upgrading-from-apriltag-2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">从 AprilTag 2 升级</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于大多数用例来说，这应该是替代品的下降。</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">选项 Fine_decode、refine_pose 和 black_border 已被删除。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您生成了自己的系列，则需要为这些系列重新生成 c 代码。</font><font style="vertical-align: inherit;">然而，java 代码不需要重新生成，因此这应该是快速且简单的。</font></font></li>
</ul>
<h2 tabindex="-1" dir="auto"><a id="user-content-opencv-integration" class="anchor" aria-hidden="true" tabindex="-1" href="#opencv-integration"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenCV 集成</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请注意，该库没有外部依赖项。</font><font style="vertical-align: inherit;">大多数应用至少需要一种获取图像的方法。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有关在 C++ 中与 OpenCV 结合使用 AprilTag 的示例，请参阅 example/opencv_demo.cc。</font><font style="vertical-align: inherit;">该示例应用程序可以通过执行以下命令来构建：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>$ cd examples
$ make opencv_demo
</code></pre><div class="zeroclipboard-container">
     
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">cv::Mat 对象中的图像数据可以传递到 AprilTag，而无需创建深层副本。</font><font style="vertical-align: inherit;">只需为 cv::Mat 数据缓冲区创建一个 image_u8_t 标头：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cv::Mat img;

image_u8_t img_header = { .width = img.cols,
    .height = img.rows,
    .stride = img.cols,
    .buf = img.data
};
</code></pre><div class="zeroclipboard-container">
    
  </div></div>
<h2 tabindex="-1" dir="auto"><a id="user-content-tuning-the-detector-parameters" class="anchor" aria-hidden="true" tabindex="-1" href="#tuning-the-detector-parameters"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">调整探测器参数</font></font></h2>
<h3 tabindex="-1" dir="auto"><a id="user-content-increasing-speed" class="anchor" aria-hidden="true" tabindex="-1" href="#increasing-speed"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">增加速度。</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">增加quad_decimate参数会以检测距离为代价来提高检测器的速度。</font><font style="vertical-align: inherit;">如果你有额外的 cpu 核心来解决这个问题，那么你可以增加 nthreads。</font><font style="vertical-align: inherit;">如果您的图像有些嘈杂，增加quad_sigma参数可以提高速度。</font></font></p>
<h3 tabindex="-1" dir="auto"><a id="user-content-increasing-detection-distance" class="anchor" aria-hidden="true" tabindex="-1" href="#increasing-detection-distance"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">增加检测距离。</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">首先选择一个示例图像并使用 debug=1 运行检测器以生成调试图像。</font><font style="vertical-align: inherit;">这些显示了检测器在检测管道中每个步骤的输出。</font><font style="vertical-align: inherit;">如果标签的边界未被检测为四边形，请减少quad_decimate（如有必要，一直到1）。</font><font style="vertical-align: inherit;">如果检测到标签的边界，则尝试更改decode_sharpening。</font></font></p>
<h2 tabindex="-1" dir="auto"><a id="user-content-pose-estimation" class="anchor" aria-hidden="true" tabindex="-1" href="#pose-estimation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">姿势估计。</font></font></h2>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们提供了一种计算标签位姿的方法，如下所示（或者使用 OpenCv 的 Pnp 求解器和 SOLVEPNP_IPPE_SQUARE）。</font><font style="vertical-align: inherit;">您需要包含 apriltag_pose.h 头文件，然后调用estimate_tag_pose 函数，如下所示：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>// First create an apriltag_detection_info_t struct using your known parameters.
apriltag_detection_info_t info;
info.det = det;
info.tagsize = tagsize;
info.fx = fx;
info.fy = fy;
info.cx = cx;
info.cy = cy;

// Then call estimate_tag_pose.
apriltag_pose_t pose;
double err = estimate_tag_pose(&amp;info, &amp;pose);
// Do something with pose.
...
</code></pre><div class="zeroclipboard-container">
   
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">其中参数如下：</font></font></p>
<ul dir="auto">
<li><code>det</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：标签检测结构（april_detection_t）。</font></font></li>
<li><code>tagsize</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：标签的大小（以米为单位）。</font><font style="vertical-align: inherit;">每个标签设计都有一个黑色边框和一个白色边框，但有些设计的内部有白色边框，有些设计的内部有黑色边框。</font><font style="vertical-align: inherit;">因此，标签大小是从两个边界相交的位置开始测量的，请参见下图的示例。</font></font></li>
<li><code>fx</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">, </font></font><code>fy</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">: 相机的焦距（以像素为单位）。</font><font style="vertical-align: inherit;">对于大多数相机来说</font></font><code>fx</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><code>fy</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">将相等或接近如此。</font></font></li>
<li><code>cx</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">, </font></font><code>cy</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：相机的焦点中心（以像素为单位）。</font><font style="vertical-align: inherit;">对于大多数相机来说，这与图像中心大致相同。</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：标签尺寸不应从标签外部测量。</font><font style="vertical-align: inherit;">标签尺寸定义为检测角之间的距离，或者白色边框和黑色边框之间的边缘长度。</font><font style="vertical-align: inherit;">下图对于 48h12Custom 标签系列中的标签，使用红色 X 标记检测角，并使用红色箭头标记标签大小。</font></font></p>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="/AprilRobotics/apriltag/blob/master/tag_size_48h12.png"><img src="/AprilRobotics/apriltag/raw/master/tag_size_48h12.png" alt="标签尺寸是白边框和黑边框之间的边缘宽度。" style="max-width: 100%;"></a></p>
<h3 tabindex="-1" dir="auto"><a id="user-content-coordinate-system" class="anchor" aria-hidden="true" tabindex="-1" href="#coordinate-system"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">坐标系</font></font></h3>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">坐标系的原点位于相机中心。</font><font style="vertical-align: inherit;">z 轴从相机中心指向相机镜头。</font><font style="vertical-align: inherit;">在相机拍摄的图像中，x 轴位于右侧，y 轴位于下方。</font><font style="vertical-align: inherit;">标签的坐标系以标签的中心为中心，x 轴向右，y 轴向下，z 轴进入标签。</font></font></p>
<h1 tabindex="-1" dir="auto"><a id="user-content-debugging" class="anchor" aria-hidden="true" tabindex="-1" href="#debugging"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">调试</font></font></h1>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可以通过设置选项启用</font></font><a href="https://clang.llvm.org/docs/AddressSanitizer.html" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AddressSanitizer</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">来调试调试版本的内存问题</font></font><code>ASAN</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cmake -B build -GNinja -DCMAKE_BUILD_TYPE=Debug -DASAN=ON
cmake --build build
</code></pre><div class="zeroclipboard-container">
    
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">大多数情况下，您可以像往常一样运行可执行文件并检查清理程序输出。</font><font style="vertical-align: inherit;">如果您收到类似消息，</font></font><code>ASan runtime does not come first in initial library list; you should either link runtime to your application or manually preload it with LD_PRELOAD.</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">则必须预加载相应的内容，</font></font><code>libasan.so.5</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如下所示：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>LD_PRELOAD=/usr/lib/x86_64-linux-gnu/libasan.so.5 ./build/opencv_demo
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="LD_PRELOAD=/usr/lib/x86_64-linux-gnu/libasan.so.5 ./build/opencv_demo" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<h1 tabindex="-1" dir="auto"><a id="user-content-flexible-layouts" class="anchor" aria-hidden="true" tabindex="-1" href="#flexible-layouts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">灵活的布局</font></font></h1>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">除了 AprilTag 2 支持的经典布局之外，AprilTag 3 还支持多种可能的标签布局。标签的数据位现在可以超出标签边界，并且还可以定义标签内部带有“孔”的布局没有数据位的边界。</font><font style="vertical-align: inherit;">在此存储库中，我们包括：</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">两个系列的新标准布局。</font><font style="vertical-align: inherit;">这种布局在标签边界外部添加了一层数据位，增加了数据密度和可能的标签数量，但代价是检测距离略有缩短。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">两个圆形标签系列。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有一个家庭，中间有一个洞。</font><font style="vertical-align: inherit;">例如，这可以用于无人机应用，通过将不同尺寸的标签放置在彼此内部，以允许在较宽的距离范围内进行检测。</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://github.com/AprilRobotics/apriltag-generation"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可以使用我们的其他存储库AprilTag-Generation</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">生成您自己的标签系列</font><font style="vertical-align: inherit;">。</font></font></p>
<h1 tabindex="-1" dir="auto"><a id="user-content-support" class="anchor" aria-hidden="true" tabindex="-1" href="#support"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font></font></h1>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果有任何问题，请在此 GitHub 上创建问题，而不是发送私人消息。</font><font style="vertical-align: inherit;">这可以让其他有相同问题的人找到您的答案。</font></font></p>
</article></div>
