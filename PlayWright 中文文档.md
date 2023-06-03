Version: 1.13.0   [官方地址](https://playwright.dev/docs/intro)
> Introduction
> Playwright Test
> Guides
> Integrations



说明：<br />1、这里边的“测试”我理解的是指的 我们使用 Playwright 编写的自动化脚本，因为翻译了一多半了不想改了，读起来有点别扭，但是不知改怎么称呼好。如果在阅读过程中有更好的翻译建议，请提出。<br />2、所有的“英文”跳转链接是到原文档的，“中文”的跳转链接是到本文档指定位置的<br />**Introduction**
<a name="zRxIn"></a>
# 什么是 Playwright?
playwright支持所有现代浏览器的快速、可靠和强大的自动化。本指南涵盖了那些关键的差异，以帮助您为自动化测试确定正确的工具。

- [支持所有浏览器](https://www.yuque.com/yumos/ru12wy/rlsgzb#LwXNW)（[Support for all browsers](https://playwright.dev/docs/why-playwright#support-for-all-browsers)）
- [快速可靠的执行](https://www.yuque.com/yumos/ru12wy/rlsgzb#iZydh)（[Fast and reliable execution](https://playwright.dev/docs/why-playwright#fast-and-reliable-execution)）
- [强大的自动化能力](https://www.yuque.com/yumos/ru12wy/rlsgzb#cgUyT)（[Powerful automation capabilities](https://playwright.dev/docs/why-playwright#powerful-automation-capabilities)）
- [与您的工作流集成](https://www.yuque.com/yumos/ru12wy/rlsgzb#cwZ00)（[Integrates with your workflow](https://playwright.dev/docs/why-playwright#integrates-with-your-workflow)）
- [限制](https://www.yuque.com/yumos/ru12wy/rlsgzb#0OHzO)（[Limitations](https://playwright.dev/docs/why-playwright#limitations)）
<a name="LwXNW"></a>
## [支持所有浏览器#](https://playwright.dev/docs/why-playwright/#support-for-all-browsers)

- **在 Chromium、Firefox 和 WebKit 上进行测试**. Playwright 拥有适用于所有现代浏览器的完整 API,包括 Google Chrome 和 Microsoft Edge (基于 [Chromium](https://www.chromium.org/)), Apple Safari (基于 [WebKit](https://webkit.org/)) 和 Mozilla Firefox.
- **跨平台 WebKit 测试**. 使用Playwright，使用适用于Windows、Linux和macOS的WebKit构建，测试您的应用程序在Apple Safari中的表现。在本地和CI上进行测试。
- **移动设备测试**. 借助 [移动设备模拟器]()（[device emulation](https://playwright.dev/docs/emulation)）的移动 Web 浏览器中测试您的响应式 Web 应用程序
- **Headless and headed**. Playwright 支持所有浏览器和所有平台的 headless（无浏览器 UI）和headed（带浏览器 UI）模式。 Headed 非常适合调试，而 Headless 速度更快，适合 CI/云执行。
<a name="iZydh"></a>
## [快速可靠的执行#](https://playwright.dev/docs/why-playwright/#fast-and-reliable-execution)

- **自动等待API（Auto-wait APIs）**. Playwright 操作会 [自动等待元素]()（[auto-wait for elements](https://playwright.dev/docs/actionability)） 准备就绪. 这提高了可靠性并简化了测试脚本的编写。
- **自动化无超时（Timeout-free automation)**. Playwright 接收浏览器信号, 如网络请求、页面导航和页面加载事件， to eliminate the need for sleep timeouts that cause flakiness.
- **Lean parallelization with browser contexts**. 为多个具有[浏览器上下文]()（[browser contexts](https://playwright.dev/docs/core-concepts)）的并行、隔离的执行环境重用单个浏览器实例。 .
- **灵活的元素选择器**. Playwright 可以依靠面向用户的字符串，比如文本内容和可访问性标签来 [选择元素]()（[select elements](https://playwright.dev/docs/selectors)）， 这些字符串比DOM结构紧密耦合的选择器更灵活。
<a name="cgUyT"></a>
## [强大的自动化能力#](https://playwright.dev/docs/why-playwright/#powerful-automation-capabilities)

- **多个域（Multiple），页面（Pages）和框架 （frames）**. 是一个进程外自动化驱动程序，它不受页面内JavaScript执行范围的限制，可以使用多个[多个页面]()（ [multiple pages](https://playwright.dev/docs/multi-pages).）实现场景自动化.
- **强大的网络控制**. Playwright引入了context-wide [network interception](https://playwright.dev/docs/network) to stub and mock network requests.
- **Modern web features**. Playwright supports web components through [shadow-piercing selectors](https://playwright.dev/docs/selectors), [geolocation, permissions](https://playwright.dev/docs/emulation), web workers and other modern web APIs.
- **覆盖所有场景的功能**. 支持[文件下载]()（[file downloads](https://playwright.dev/docs/downloads)）和[上传]()（[uploads](https://playwright.dev/docs/input)）, 进程外 iframes, 本地 [输入事件]()（[input events](https://playwright.dev/docs/input)）, 甚至是  [dark mode](https://playwright.dev/docs/emulation).
<a name="cwZ00"></a>
## [与您的工作流程集成#](https://playwright.dev/docs/why-playwright/#integrates-with-your-workflow)

- **一键安装**. 安装 Playwright 自动下载浏览器依赖项，使您的团队能够快速上手<br />
```shell
npm i playwright
```

- **TypeScript 支持**. Playwright ships with built-in types for auto-completion and other benefits.<br />
- **调试工具（Debugging tools）**. Playwright works with the [editor debugger and browser developer tools](https://playwright.dev/docs/debug) to pause execution and inspect the web page.<br />
- **支持多种语言**. Playwright 可用于 [Node.js](https://github.com/microsoft/playwright) [Python](https://github.com/microsoft/playwright-python), [.NET](https://github.com/microsoft/playwright-dotnet) 和 [Java](https://github.com/microsoft/playwright-java). 更多请参阅 [supported languages](https://playwright.dev/docs/languages).<br />
- **将测试部署到CI**. First-party [Docker image](https://playwright.dev/docs/docker) and [GitHub Actions](https://playwright.dev/docs/ci#github-actions) support to deploy tests to [your preferred CI/CD provider](https://playwright.dev/docs/ci).
<a name="0OHzO"></a>
## [限制#](https://playwright.dev/docs/why-playwright/#limitations)

- **传统Edge和IE11的支持问题**. Playwright 不支持传统的 Microsoft Edge 或者 IE11 ([deprecation notice](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666)). 仅支持 Microsoft Edge (基于Chromium) 的版本.
- **在真实的移动设备上进行测试**: Playwright 使用桌面浏览器来模拟移动设备。 [这里](https://playwright.dev/docs/mobile)有对Android的实验性支持. 如果你对iOS感兴趣, please [upvote this issue](https://github.com/microsoft/playwright/issues/1122).

---

<a name="RKzUP"></a>
# 入门#
Playwright 可以作为 Playwrigh 测试的一部分，或作为[Playwright Library](https://playwright.dev/docs/library). 如果您打算使用 Playwright 进行测试，请继续阅读。<br />Playwright 测试是专门为适应端到端测试的需要而创建的。 它可以完成所有您期望的常规测试，甚至更多。Playwright 允许:

- Run tests across all browsers（在所有浏览器上运行测试）.
- Execute tests in parallel（并行测试）.
- Enjoy context isolation out of the box（环境隔离）.
- Capture videos, screenshots and other artifacts on failure（捕获失败时的视频、屏幕截图和其他）.
- Integrate your POMs as extensible fixtures.

- [Installation](https://playwright.dev/docs/intro#installation)（[安装](https://www.yuque.com/yumos/ru12wy/rlsgzb#6iiig)）
- [First test](https://playwright.dev/docs/intro#first-test)（[第一个脚本](https://www.yuque.com/yumos/ru12wy/rlsgzb#EDbCc)）
- [Test fixtures](https://playwright.dev/docs/intro#test-fixtures)
- [Test and assertion features](https://playwright.dev/docs/intro#test-and-assertion-features)（[测试和断言特性](https://www.yuque.com/yumos/ru12wy/rlsgzb#J7r6m)）
- [Learn the command line](https://playwright.dev/docs/intro#learn-the-command-line)（[学习命令行](https://www.yuque.com/yumos/ru12wy/rlsgzb#m4eRv)）
- [Create a configuration file](https://playwright.dev/docs/intro#create-a-configuration-file)（[创建配置文件](https://www.yuque.com/yumos/ru12wy/rlsgzb#owbS9)）
- [Release notes](https://playwright.dev/docs/release-notes)

<a name="6iiig"></a>
## [安装#](https://playwright.dev/docs/intro#installation)
Playwright 有自己的 test runner用于端对端测试，我们称之为 Playwright Test.
```javascript
npm i -D @playwright/test
```
与 Playwright Library 不同，Playwright Test 默认不捆绑浏览器，因此您需要指定安装它们：
```javascript
npx playwright install
```
<a name="EDbCc"></a>
## [第一个脚本#](https://playwright.dev/docs/intro#installation)
创建 `tests/foo.spec.js` (或者 `tests/foo.spec.ts` 文件 TypeScript) 来定义你的测试脚本.
```javascript
const { test, expect } = require('@playwright/test');

test('basic test', async ({ page }) => {
  await page.goto('https://playwright.dev/');
  const name = await page.innerText('.navbar__title');
  expect(name).toBe('Playwright');
});
```
```typescript
import { test, expect } from '@playwright/test';

test('basic test', async ({ page }) => {
  await page.goto('https://playwright.dev/');
  const name = await page.innerText('.navbar__title');
  expect(name).toBe('Playwright');
});
```
现在运行你的测试脚本, assuming that test files are in the `tests` directory.
```javascript
npx playwright test
```
Playwright Test 刚刚使用 Chromium 浏览器以无GUI（headless）的方式运行了一个测试（Playwright Test）。让我们告诉它使用有GUI（headed）模式运行浏览器：
```javascript
npx playwright test --headed
```
其他浏览器呢？让我们使用 Firefox 运行相同的测试（Playwright Test）：
```javascript
npx playwright test --browser=firefox
```
最后，在所有三个浏览器上：
```javascript
npx playwright test --browser=all
```
请参阅[配置](https://playwright.dev/docs/test-configuration)部分以配置不同浏览器的不同模式下的测试运行。
<a name="Paqtb"></a>
## Test fixtures[#](https://playwright.dev/docs/intro#test-fixtures)
You noticed an argument `{ page }` that the test above has access to:
```javascript
test('basic test', async ({ page }) => {
  ...
```

```typescript
test('basic test', async ({ page }) => {
  ...
```
我们称这些参数为 `fixtures`.。Fixtures 是为每次测试运行创建的对象。Playwright Test 加载了这些 fixtures，您也可以添加自己的 fixtures。在运行测试时，Playwright Test 会查看每个测试声明，分析测试所需的 fixtures 并专门为测试准备这些 fixtures 。<br />以下是您可能常用的预定义 fixtures 的列表：

| Fixture | Type | Description |
| --- | --- | --- |
| page | [Page](https://playwright.dev/docs/api/class-page) | Isolated page for this test run |
| context | [BrowserContext](https://playwright.dev/docs/api/class-browsercontext) | Isolated context for this test run. The `page` fixture belongs to this context as well. Learn how to [configure context](https://playwright.dev/docs/test-configuration). |
| browser | [Browser](https://playwright.dev/docs/api/class-browser) | Browsers are shared across tests to optimize resources. Learn how to [configure browser](https://playwright.dev/docs/test-configuration). |
| browserName | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#String_type) | The name of the browser currently running the test. Either `chromium`, `firefox` or `webkit`. |

<a name="J7r6m"></a>
## [测试和断言特性#](https://playwright.dev/docs/intro#test-and-assertion-features)
如果您熟悉 Jest、Mocha 和 Ava 等测试运行程序，您会发现 Playwright Test 语法很熟悉。这些是您可以通过测试执行的基本操作：
<a name="zH8jC"></a>
### [聚焦测试#](https://playwright.dev/docs/intro#focus-a-test)
You can focus some tests. When there are focused tests, only they run.
```javascript
test.only('focus this test', async ({ page }) => {
  // Run only focused tests in the entire project.
});
```
```typescript
test.only('focus this test', async ({ page }) => {
  // Run only focused tests in the entire project.
});
```
<a name="rJg2K"></a>
### [跳过测试#](https://playwright.dev/docs/intro#skip-a-test)
您可以通过设置一些条件来跳过测试：
```typescript
test('skip this test', async ({ page, browserName }) => {
  test.skip(browserName === 'firefox', 'Still working on it');
});
```
```javascript
test('skip this test', async ({ page, browserName }) => {
  test.skip(browserName === 'firefox', 'Still working on it');
});
```
<a name="RrE56"></a>
### [分组测试#](https://playwright.dev/docs/intro#group-tests)
您可以对测试进行分组以给它们一个逻辑名称或将范围之前/之后关联到组。
```javascript
const { test, expect } = require('@playwright/test');

test.describe('two tests', () => {
  test('one', async ({ page }) => {
    // ...
  });

  test('two', async ({ page }) => {
    // ...
  });
});
```
```typescript
import { test, expect } from '@playwright/test';

test.describe('two tests', () => {
  test('one', async ({ page }) => {
    // ...
  });

  test('two', async ({ page }) => {
    // ...
  });
});
```
<a name="kFxzM"></a>
### [使用测试钩子#](https://playwright.dev/docs/intro#use-test-hooks)
您可以使用 `test.beforeAll` 和 `test.afterAll` 钩子来设置和拆除测试之间共享的资源。您可以使用 `test.beforeEach` 和 `test.afterEach` 钩子分别为每个测试设置和拆除资源。
```javascript
// example.spec.js
const { test, expect } = require('@playwright/test');

test.describe('feature foo', () => {
  test.beforeEach(async ({ page }) => {
    // Go to the starting url before each test.
    await page.goto('https://my.start.url/');
  });

  test('my test', async ({ page }) => {
    // Assertions use the expect API.
    expect(page.url()).toBe('https://my.start.url/');
  });
});
```
```typescript
// example.spec.ts
import { test, expect } from '@playwright/test';

test.describe('feature foo', () => {
  test.beforeEach(async ({ page }) => {
    // Go to the starting url before each test.
    await page.goto('https://my.start.url/');
  });

  test('my test', async ({ page }) => {
    // Assertions use the expect API.
    expect(page.url()).toBe('https://my.start.url/');
  });
});
```
<a name="I1EFV"></a>
### [写断言#](https://playwright.dev/docs/intro#write-assertions)
Playwright Test 使用 [expect](https://jestjs.io/docs/expect) 库进行测试断言。它提供了很多匹配器， `toEqual`, `toContain`, `toMatch`, `toMatchSnapshot` 等等。<br />将 expect 与各种 Playwright 方法相结合，来实现测试目标：

- [page.isVisible(selector[, options])](https://playwright.dev/docs/api/class-page#page-is-visible)
- [page.waitForSelector(selector[, options])](https://playwright.dev/docs/api/class-page#page-wait-for-selector)
- [page.textContent(selector[, options])](https://playwright.dev/docs/api/class-page#page-text-content)
- [page.getAttribute(selector, name[, options])](https://playwright.dev/docs/api/class-page#page-get-attribute)
- [page.screenshot([options])](https://playwright.dev/docs/api/class-page#page-screenshot)
- 在[断言](https://playwright.dev/docs/assertions)指南中了解更多信息
```typescript
// example.spec.ts
import { test, expect } from '@playwright/test';

test('my test', async ({ page }) => {
  await page.goto('https://playwright.dev/');

  // Expect a title "to contain" a substring.
  expect(await page.title()).toContain('Playwright');

  // Expect an attribute "to be strictly equal" to the value.
  expect(await page.getAttribute('text=Get Started', 'href')).toBe('/docs/intro');

  // Expect an element "to be visible".
  expect(await page.isVisible('text=Learn more')).toBeTruthy();

  await page.click('text=Get Started');
  // Expect some text to be visible on the page.
  expect(await page.waitForSelector('text=System requirements')).toBeTruthy();

  // Compare screenshot with a stored reference.
  expect(await page.screenshot()).toMatchSnapshot('get-started.png');
});
```
```javascript
// example.spec.js
const { test, expect } = require('@playwright/test');

test('my test', async ({ page }) => {
  await page.goto('https://playwright.dev/');

  // Expect a title "to contain" a substring.
  expect(await page.title()).toContain('Playwright');

  // Expect an attribute "to be strictly equal" to the value.
  expect(await page.getAttribute('text=Get Started', 'href')).toBe('/docs/intro');

  // Expect an element "to be visible".
  expect(await page.isVisible('text=Learn more')).toBeTruthy();

  await page.click('text=Get Started');
  // Expect some text to be visible on the page.
  expect(await page.waitForSelector('text=System requirements')).toBeTruthy();

  // Compare screenshot with a stored reference.
  expect(await page.screenshot()).toMatchSnapshot('get-started.png');
});
```
注意运行这个测试是如何输出的：
```javascript
Error: example.spec.ts-snapshots/get-started-chromium-darwin.png is missing in snapshots, writing actual.
```
That's because there was no golden file for your `get-started.png` snapshot. It is now created and is ready to be added to the repository. The name of the folder with the golden expectations starts with the name of your test file:
```javascript
drwxr-xr-x  5 user  group  160 Jun  4 11:46 .
drwxr-xr-x  6 user  group  192 Jun  4 11:45 ..
-rw-r--r--  1 user  group  231 Jun  4 11:16 example.spec.ts
drwxr-xr-x  3 user  group   96 Jun  4 11:46 example.spec.ts-snapshots
```
To update your golden files, you can use the `--update-snapshots` parameter.
```javascript
npx playwright test --update-snapshots
```
<a name="m4eRv"></a>
## [学习命令行#](https://playwright.dev/docs/intro#learn-the-command-line)
这里有常见的[命令行](https://playwright.dev/docs/test-cli)参数.

- Run tests in headed browsers（带浏览器UI模式运行）<br />
```shell
npx playwright test --headed
```

- Run tests in a particular browser（以指定的浏览器运行）
```shell
npx playwright test --browser=webkit
```

- Run tests in all browsers（在所有浏览器运行测试）
```shell
npx playwright test --browser=all
```

- Run a single test file（单测试文件）
```shell
npx playwright test tests/todo-page.spec.ts
```

- Run a set of test files（多测试文件）
```shell
npx playwright test tests/todo-page/ tests/landing-page/
```

- Run a test with specific title（使用特定的标题运行测试）
```shell
npx playwright test -g "add a todo item"
```

- Run tests [in parallel](https://playwright.dev/docs/test-parallel) - that's the default（并行测试-默认）
```shell
npx playwright test
```

- Disable [parallelization](https://playwright.dev/docs/test-parallel)（禁用并行）
```shell
npx playwright test --workers=1
```

- Choose a [reporter](https://playwright.dev/docs/test-reporters)
```shell
npx playwright test --reporter=dot
```

- Run in debug mode with [Playwright Inspector](https://playwright.dev/docs/inspector)
```shell
# Linux/macOS
PWDEBUG=1 npx playwright test

# Windows with cmd.exe
set PWDEBUG=1
npx playwright test

# Windows with PowerShell
$env:PWDEBUG=1
npx playwright test
```
<a name="owbS9"></a>
## [创建配置文件#](https://playwright.dev/docs/intro#create-a-configuration-file)
到目前为止，我们已经了解了 Playwright 测试的零配置操作。对于真实的应用程序，您很可能希望使用配置文件设置。<br />创建 `playwright.config.ts` (或者 `playwright.config.js`) 测配置你的测试. 您可以使用配置指定浏览器启动选项、在多个浏览器中运行测试等等. 下面是一个运行Chromium、Firefox和WebKit所有测试的配置示例，包括桌面版和移动版。 更多配置选项请查看[配置部分](https://playwright.dev/docs/test-configuration)（[configuration section](https://playwright.dev/docs/test-configuration)）.
```javascript
// playwright.config.js
// @ts-check
const { devices } = require('@playwright/test');

/** @type {import('@playwright/test').PlaywrightTestConfig} */
const config = {
  projects: [
    {
      name: 'Desktop Chromium',
      use: {
        browserName: 'chromium',
        // Test against Chrome Beta channel.
        channel: 'chrome-beta',
      },
    },
    {
      name: 'Desktop Safari',
      use: {
        browserName: 'webkit',
        viewport: { width: 1200, height: 750 },
      }
    },
    // Test against mobile viewports.
    {
      name: 'Mobile Chrome',
      use: devices['Pixel 5'],
    },
    {
      name: 'Mobile Safari',
      use: devices['iPhone 12'],
    },
    {
      name: 'Desktop Firefox',
      use: {
        browserName: 'firefox',
        viewport: { width: 800, height: 600 },
      }
    },
  ],
};

module.exports = config;
```
```typescript
// playwright.config.ts
import { PlaywrightTestConfig, devices } from '@playwright/test';

const config: PlaywrightTestConfig = {
  projects: [
    {
      name: 'Chrome Stable',
      use: {
        browserName: 'chromium',
        // Test against Chrome Stable channel.
        channel: 'chrome',
      },
    },
    {
      name: 'Desktop Safari',
      use: {
        browserName: 'webkit',
        viewport: { width: 1200, height: 750 },
      }
    },
    // Test against mobile viewports.
    {
      name: 'Mobile Chrome',
      use: devices['Pixel 5'],
    },
    {
      name: 'Mobile Safari',
      use: devices['iPhone 12'],
    },
    {
      name: 'Desktop Firefox',
      use: {
        browserName: 'firefox',
        viewport: { width: 800, height: 600 },
      }
    },
  ],
};
export default config;
```
配置 NPM 脚本运行测试. Playwright Test 会自动选择 `playwright.config.js` 或 `playwright.config.ts` 文件.
```javascript
{
  "scripts": {
    "test": "npx playwright test"
  }
}
```
如果您将配置文件放在不同的位置, 请使用 `--config` 参数来传递他们.
```javascript
{
  "scripts": {
    "test": "npx playwright test --config=tests/example.config.js"
  }
}
```

---

<a name="jzM2T"></a>
# 核心概念
Playwright 提供了一组 API 来自动化操作 Chromium、Firefox和WebKit浏览器。通过使用Playwright 的 API，您可以编写脚本来创建新的浏览器页面，导航到url，然后与页面上的元素进行交互。<br />与测试运行器一起，Playwright 可以用来自动化用户交互，以验证和测试 web 应用程序。Playwright API通过以下 primitives 实现了这一点。

- [Browser](https://playwright.dev/docs/core-concepts#browser)（[浏览器](https://www.yuque.com/yumos/ru12wy/rlsgzb#U7pjD)）
- [Browser contexts](https://playwright.dev/docs/core-concepts#browser-contexts)（[浏览器上下文](https://www.yuque.com/yumos/ru12wy/rlsgzb#df6y0)）
- [Pages and frames](https://playwright.dev/docs/core-concepts#pages-and-frames)（[页面和框架](https://www.yuque.com/yumos/ru12wy/rlsgzb#e3f1b85a)）
- [Selectors](https://playwright.dev/docs/core-concepts#selectors)（[选择器](https://www.yuque.com/yumos/ru12wy/rlsgzb#D66oY)）
- [Auto-waiting](https://playwright.dev/docs/core-concepts#auto-waiting)（[自动等待](https://www.yuque.com/yumos/ru12wy/rlsgzb#be29c5ce)）
- [Execution contexts: Playwright and Browser](https://playwright.dev/docs/core-concepts#execution-contexts-playwright-and-browser)（[执行上下文环境](https://www.yuque.com/yumos/ru12wy/rlsgzb#8ce9abe0)）
- [Evaluation Argument](https://playwright.dev/docs/core-concepts#evaluation-argument)（[评估参数](https://www.yuque.com/yumos/ru12wy/rlsgzb#qQ6mx)）

<a name="U7pjD"></a>
## Browser（浏览器）[#](https://playwright.dev/docs/core-concepts#browser)
[Browser](https://playwright.dev/docs/api/class-browser) 指的是Chromium、Firefox或WebKit的实例。Playwright 脚本通常以启动一个 browser 实例开始，以关闭 browser 结束。浏览器实例可以在headless（没有GUI）或headled（有GUI）模式下启动。
```javascript
const { chromium } = require('playwright');  // Or 'firefox' or 'webkit'.

const browser = await chromium.launch({ headless: false });
await browser.close();
```
启动一个 browser 实例成本可能会非常高，而 Playwright 旨在最大化单个实例在多个浏览器上下文中的作用。
<a name="j4B60"></a>
### API reference[#](https://playwright.dev/docs/core-concepts#api-reference)

- [Browser](https://playwright.dev/docs/api/class-browser)

<a name="df6y0"></a>
## Browser contexts（浏览器上下文）[#](https://playwright.dev/docs/core-concepts#browser-contexts)
[BrowserContext](https://playwright.dev/docs/api/class-browsercontext) 是Browser 中一个独立的隐身会话. 可以容易并且低成本的创建 Browser contexts。 We recommend running each test scenario in its own new Browser context, so that the browser state is isolated between the tests.
```javascript
const browser = await chromium.launch();
const context = await browser.newContext();
```
Browser contexts 还可以用来模拟涉及移动设备、权限、场所和配色方案的多页面场景。
```javascript
const { devices } = require('playwright');
const iPhone = devices['iPhone 11 Pro'];

const context = await browser.newContext({
  ...iPhone,
  permissions: ['geolocation'],
  geolocation: { latitude: 52.52, longitude: 13.39},
  colorScheme: 'dark',
  locale: 'de-DE'
});
```
<a name="122b1942"></a>
### API reference[#](https://playwright.dev/docs/core-concepts#api-reference-1)

- [BrowserContext](https://playwright.dev/docs/api/class-browsercontext)
- [browser.newContext([options])](https://playwright.dev/docs/api/class-browser#browser-new-context)

<a name="e3f1b85a"></a>
## Pages and frames（页面和框架）[#](https://playwright.dev/docs/core-concepts#pages-and-frames)
一个 Browser context 可以有多个页面. [Page](https://playwright.dev/docs/api/class-page) 指的是 browser context 中的单个选项卡或弹出窗口. 它应该用于导航到url并与页面内容交互.
```javascript
// Create a page.
const page = await context.newPage();

// Navigate explicitly, similar to entering a URL in the browser.
await page.goto('http://example.com');
// Fill an input.
await page.fill('#search', 'query');

// Navigate implicitly by clicking a link.
await page.click('#submit');
// Expect a new url.
console.log(page.url());

// Page can navigate from the script - this will be picked up by Playwright.
window.location.href = 'https://example.com';
```
> 详情请见 [page navigation and loading](https://playwright.dev/docs/navigations).

一个页面可以附加一个或多个 [Frame](https://playwright.dev/docs/api/class-frame) 对象。 每个页面都有一个主 Frame，页面级的交互 (如 `click`) 被假定在主 Frame 中操作。.<br />一个页面可以通过 HTML 的 `iframe` 标签来添加 Frame。这些 frame 可以通过 frame 内部的交互来访问。
```javascript
// Get frame using the frame's name attribute
const frame = page.frame('frame-login');

// Get frame using frame's URL
const frame = page.frame({ url: /.*domain.*/ });

// Get frame using any other selector
const frameElementHandle = await page.$('.frame-class');
const frame = await frameElementHandle.contentFrame();

// Interact with the frame
await frame.fill('#username-input', 'John');
```
<a name="3oVPf"></a>
### API reference[#](https://playwright.dev/docs/core-concepts#api-reference-2)

- [Page](https://playwright.dev/docs/api/class-page)
- [Frame](https://playwright.dev/docs/api/class-frame)
- [page.frame(frameSelector)](https://playwright.dev/docs/api/class-page#page-frame)

<a name="D66oY"></a>
## Selectors（选择器）[#](https://playwright.dev/docs/core-concepts#selectors)
Playwright 可以使用 `CSS` 选择器, `XPath` 选择器,  `id`, `data-test-id` 甚至文本内容等HTML属性搜索元素。<br />您可以显式指定正在使用的选择器引擎，或者让 Playwright 检测它。<br />默认情况下，所有选择器引擎(除了XPath)都会穿透 shadow DOM。如果想强制只操作显式的的DOM，可以使用选择器的 `*:light` 版本。你通常不需要这样做。<br />在这里（[here](https://playwright.dev/docs/selectors)）了解更多关于选择器和选择器引擎的信息。.<br />实例:
```javascript
// Using data-test-id= selector engine
await page.click('data-test-id=foo');

// CSS and XPath selector engines are automatically detected
await page.click('div');
await page.click('//html/body/div');

// Find node by text substring
await page.click('text=Hello w');

// Explicit CSS and XPath notation
await page.click('css=div');
await page.click('xpath=//html/body/div');

// Only search light DOM, outside WebComponent shadow DOM:
await page.click('css:light=div');
```
不同的选择器可以通过 `>>` 来结合使用，例如：
```javascript
// Click an element with text 'Sign Up' inside of a #free-month-promo.
await page.click('#free-month-promo >> text=Sign Up');

// Capture textContent of a section that contains an element with text 'Selectors'.
const sectionText = await page.$eval('*css=section >> text=Selectors', e => e.textContent);
```
<a name="be29c5ce"></a>
## Auto-waiting（自动等待）[#](https://playwright.dev/docs/core-concepts#auto-waiting)
如 [page.click(selector[, options])](https://playwright.dev/docs/api/class-page#page-click) 和 [page.fill(selector, value[, options])](https://playwright.dev/docs/api/class-page#page-fill) 等操作，Playwright 可以自动等待而目标元素加载完，这些行为都是可控的（[actionable](https://playwright.dev/docs/actionability)）. 例如, 点击（click） 操作将会:

- 等待带有给定选择器的元素出现在DOM中
- 等待目标元素可用: have non-empty bounding box and no `visibility:hidden`
- 等待它停止移动:例如，等待CSS过渡完成
- 将元素滚动到视图中
- wait for it to receive pointer events at the action point: 例如, 等待元素不再被其他元素遮挡
- retry if the element is detached during any of the above checks
```javascript
// Playwright waits for #search element to be in the DOM
await page.fill('#search', 'query');

// Playwright waits for element to stop animating
// and accept clicks.
await page.click('#search');
```
你可以显式地等待一个元素在DOM中出现或变得可见:
```javascript
// Wait for #search to appear in the DOM.
await page.waitForSelector('#search', { state: 'attached' });
// Wait for #promo to become visible, for example with `visibility:visible`.
await page.waitForSelector('#promo');
```
... 或变得隐藏（hidden）或分离（detached）
```javascript
// Wait for #details to become hidden, for example with `display:none`.
await page.waitForSelector('#details', { state: 'hidden' });
// Wait for #promo to be removed from the DOM.
await page.waitForSelector('#promo', { state: 'detached' });
```
<a name="sqgxB"></a>
### API reference[#](https://playwright.dev/docs/core-concepts#api-reference-3)

- [page.click(selector[, options])](https://playwright.dev/docs/api/class-page#page-click)
- [page.fill(selector, value[, options])](https://playwright.dev/docs/api/class-page#page-fill)
- [page.waitForSelector(selector[, options])](https://playwright.dev/docs/api/class-page#page-wait-for-selector)

<a name="8ce9abe0"></a>
## Execution contexts（执行上下文环境）: Playwright and Browser[#](https://playwright.dev/docs/core-concepts#execution-contexts-playwright-and-browser)
Playwright 脚本在您的 Playwright 环境中运行。页面脚本在浏览器页面环境中运行。这些环境并不相交，它们运行在不同的虚拟机上，在不同的进程中，甚至可能在不同的计算机上。<br />[page.evaluate(pageFunction[, arg])](https://playwright.dev/docs/api/class-page#page-evaluate) API 可以在网页的上下文中运行JavaScript函数，并将结果带回 Playwright 环境。 浏览器（Browser）全局变量例如 `window` 和 `document` 能够在 `evaluate` 方法中调用。
```javascript
const href = await page.evaluate(() => document.location.href);
```
如果结果是Promise或者异步函数，则会自动等待，直到它 resolved:
```javascript
const status = await page.evaluate(async () => {
  const response = await fetch(location.href);
  return response.status;
});
```
<a name="qQ6mx"></a>
## Evaluation Argument（评估参数）[#](https://playwright.dev/docs/core-concepts#evaluation-argument)
Playwright evaluation 方法如 [page.evaluate(pageFunction[, arg])](https://playwright.dev/docs/api/class-page#page-evaluate) 接受一个可选参数。这个参数可以是 [Serializable](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify#Description) values 和 [JSHandle](https://playwright.dev/docs/api/class-jshandle) 或者 [ElementHandle](https://playwright.dev/docs/api/class-elementhandle) 实例的混合. Handles 会自动转换为它们所表示的值
```javascript
// A primitive value.
await page.evaluate(num => num, 42);

// An array.
await page.evaluate(array => array.length, [1, 2, 3]);

// An object.
await page.evaluate(object => object.foo, { foo: 'bar' });

// A single handle.
const button = await page.$('button');
await page.evaluate(button => button.textContent, button);

// Alternative notation using elementHandle.evaluate.
await button.evaluate((button, from) => button.textContent.substring(from), 5);

// Object with multiple handles.
const button1 = await page.$('.button1');
const button2 = await page.$('.button2');
await page.evaluate(
    o => o.button1.textContent + o.button2.textContent,
    { button1, button2 });

// Object destructuring works. Note that property names must match
// between the destructured object and the argument.
// Also note the required parenthesis.
await page.evaluate(
    ({ button1, button2 }) => button1.textContent + button2.textContent,
    { button1, button2 });

// Array works as well. Arbitrary names can be used for destructuring.
// Note the required parenthesis.
await page.evaluate(
    ([b1, b2]) => b1.textContent + b2.textContent,
    [button1, button2]);

// Any non-cyclic mix of serializables and handles works.
await page.evaluate(
    x => x.button1.textContent + x.list[0].textContent + String(x.foo),
    { button1, list: [button2], foo: null });
```
正确:
```javascript
const data = { text: 'some data', value: 1 };
// Pass |data| as a parameter.
const result = await page.evaluate(data => {
  window.myApp.use(data);
}, data);
```
错误:
```javascript
const data = { text: 'some data', value: 1 };
const result = await page.evaluate(() => {
  // There is no |data| in the web page.
  window.myApp.use(data);
});
```
<a name="QhUv4"></a>
### API reference[#](https://playwright.dev/docs/core-concepts#api-reference-4)

- [page.evaluate(pageFunction[, arg])](https://playwright.dev/docs/api/class-page#page-evaluate)
- [frame.evaluate(pageFunction[, arg])](https://playwright.dev/docs/api/class-frame#frame-evaluate)
- [EvaluationArgument](https://playwright.dev/docs/core-concepts#evaluation-argument)

---

<a name="5J9NH"></a>
# 命令行接口
Playwright comes with the command line tools.

- [Usage](https://playwright.dev/docs/cli#usage)（[用法](https://www.yuque.com/yumos/ru12wy/rlsgzb#cHDSN)）
- [Install browsers](https://playwright.dev/docs/cli#install-browsers)（[安装浏览器](https://www.yuque.com/yumos/ru12wy/rlsgzb#451e1889)）
- [Generate code](https://playwright.dev/docs/cli#generate-code)（[生成代码](https://www.yuque.com/yumos/ru12wy/rlsgzb#0f87858c)）
- [Open pages](https://playwright.dev/docs/cli#open-pages)（[打开页面）](https://www.yuque.com/yumos/ru12wy/rlsgzb#xRvJn)
- [Inspect selectors](https://playwright.dev/docs/cli#inspect-selectors)（[检查选择器](https://www.yuque.com/yumos/ru12wy/rlsgzb#97eaeed4)）
- [Take screenshot](https://playwright.dev/docs/cli#take-screenshot)（[截屏](https://www.yuque.com/yumos/ru12wy/rlsgzb#CW6Hx)）
- [Generate PDF](https://playwright.dev/docs/cli#generate-pdf)（[生成PDF](https://www.yuque.com/yumos/ru12wy/rlsgzb#VrXKk)）
- [Install system dependencies](https://playwright.dev/docs/cli#install-system-dependencies)（[安装系统依赖）](https://www.yuque.com/yumos/ru12wy/rlsgzb#6fd32450)
- [Known limitations](https://playwright.dev/docs/cli#known-limitations)（[已知限制](https://www.yuque.com/yumos/ru12wy/rlsgzb#ed2cbe22)）
<a name="cHDSN"></a>
## 用法[#](https://playwright.dev/docs/cli#usage)
```shell
npx playwright --help
```
```shell
# Running from `package.json` script
{
  "scripts": {
    "help": "playwright --help"
  }
}
```
<a name="451e1889"></a>
## 安装浏览器[#](https://playwright.dev/docs/cli#install-browsers)
Playwright 安装支持的浏览器.
```shell
# Running without arguments will install default browsers
npx playwright install
```
您也可以通过指定参数来安装特定的浏览器:
```shell
# Install WebKit
npx playwright install webkit
```
查看所有支持的浏览器:
```shell
npx playwright install --help
```
<a name="0f87858c"></a>
## 生成代码[#](https://playwright.dev/docs/cli#generate-code)
```shell
npx playwright codegen wikipedia.org
```
执行 `codegen` 并运行浏览器。 Playwright CLI 将记录用户交互动作并生成JavaScript代码 `codegen` 将尝试生成基于文本的弹性选择器。<br />![92536033-7e7ebe00-f1ed-11ea-9e1a-7cbd912e3391.gif](https://cdn.nlark.com/yuque/0/2021/gif/22168665/1627114961718-eeac68b1-f87f-4e97-86b2-043830a7e59d.gif#align=left&display=inline&height=386&originHeight=386&originWidth=881&size=2792150&status=done&style=none&width=881)
<a name="WHm3K"></a>
### 保留已验证状态[#](https://playwright.dev/docs/cli#preserve-authenticated-state)
执行 `codegen` 并指定 `--save-storage` 参数来保存 [cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies) 和 [localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)。 这对于单独记录身份验证步骤并在以后负复用它非常有用。
```shell
npx playwright codegen --save-storage=auth.json
# Perform authentication and exit.
# auth.json will contain the storage state.
```
使用 `--load-storage` 参数来加载先前的存储。通过这种方式，所有的 [cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies) 和 [localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) 将被恢复，使大多数web应用程序进入认证状态。
```shell
npx playwright open --load-storage=auth.json my.web.app
npx playwright codegen --load-storage=auth.json my.web.app
# Perform actions in authenticated state.
```
<a name="AJ0Tq"></a>
### 具有自定义设置的Codegen[#](https://playwright.dev/docs/cli#codegen-with-custom-setup)
如果你想在一些非标准的设置中使用codegen (例如, 使用 [browserContext.route(url, handler)](https://playwright.dev/docs/api/class-browsercontext#browser-context-route)), 可以调用 [page.pause()](https://playwright.dev/docs/api/class-page#page-pause) ，它将打开一个带有代码生成控件的单独窗口。
```shell
const { chromium } = require('playwright');

(async () => {
  // Make sure to run headed.
  const browser = await chromium.launch({ headless: false });

  // Setup context however you like.
  const context = await browser.newContext({ /* pass any options */ });
  await context.route('**/*', route => route.continue());

  // Pause the page, and start recording manually.
  const page = await context.newPage();
  await page.pause();
})();
```
<a name="xRvJn"></a>
## 打开页面（Pages）[#](https://playwright.dev/docs/cli#open-pages)
使用 `open` 命令，您可以使用Playwright绑定的浏览器浏览网页。Playwright提供了跨平台WebKit构建，可用于跨Windows、Linux和macOS复制Safari渲染。
```shell
# Open page in Chromium
npx playwright open example.com

# Open page in WebKit
npx playwright wk example.com
```
<a name="rcYRa"></a>
### 模拟设备[#](https://playwright.dev/docs/cli#emulate-devices)
`open` 命令可以模拟 [`playwright.devices`](https://playwright.dev/docs/api/class-playwright#playwrightdevices) 列表中的移动和平板电脑设备。
```shell
# Emulate iPhone 11.
npx playwright open --device="iPhone 11" wikipedia.org
```
<a name="138d5403"></a>
### 模拟配色方案和视口大小[#](https://playwright.dev/docs/cli#emulate-color-scheme-and-viewport-size)
```shell
# Emulate screen size and color scheme.
npx playwright open --viewport-size=800,600 --color-scheme=dark twitter.com
```
<a name="87dfbe8f"></a>
### 模拟地理位置、语言和时区[#](https://playwright.dev/docs/cli#emulate-geolocation-language-and-timezone)
```shell
# Emulate timezone, language & location
# Once page opens, click the "my location" button to see geolocation in action
npx playwright open --timezone="Europe/Rome" --geolocation="41.890221,12.492348" --lang="it-IT" maps.google.com
```
<a name="97eaeed4"></a>
## 检查选择器（selectors）[#](https://playwright.dev/docs/cli#inspect-selectors)
在 `open` 或 `codegen` 期间，您可以在任何浏览器的developer tools控制台中使用以下API。<br />![92536317-37dd9380-f1ee-11ea-875d-daf1b206dd56.png](https://cdn.nlark.com/yuque/0/2021/png/22168665/1627115265760-bc7738fd-f072-48a3-a5c9-9ae2236a9715.png#align=left&display=inline&height=756&originHeight=756&originWidth=1694&size=255451&status=done&style=none&width=1694)
<a name="HEaAC"></a>
#### playwright.$(selector)[#](https://playwright.dev/docs/cli#playwrightselector)
Query Playwright selector, using the actual Playwright query engine, for example:
```shell
> playwright.$('.auth-form >> text=Log in');

<button>Log in</button>
```
<a name="7hidN"></a>
#### playwright.$$(selector)[#](https://playwright.dev/docs/cli#playwrightselector-1)
Same as `playwright.$`, but returns all matching elements.
```shell
> playwright.$$('li >> text=John')

> [<li>, <li>, <li>, <li>]
```
<a name="pJv6a"></a>
#### playwright.inspect(selector)[#](https://playwright.dev/docs/cli#playwrightinspectselector)
Reveal element in the Elements panel (if DevTools of the respective browser supports it).
```shell
> playwright.inspect('text=Log in')
```
<a name="9SICj"></a>
#### playwright.selector(element)[#](https://playwright.dev/docs/cli#playwrightselectorelement)
Generates selector for the given element.
```shell
> playwright.selector($0)

"div[id="glow-ingress-block"] >> text=/.*Hello.*/"
```
<a name="CW6Hx"></a>
## 截屏[#](https://playwright.dev/docs/cli#take-screenshot)
```shell
# See command help
npx playwright screenshot --help

# Wait 3 seconds before capturing a screenshot after page loads ('load' event fires)
npx playwright screenshot \
    --device="iPhone 11" \
    --color-scheme=dark \
    --wait-for-timeout=3000 \
    twitter.com twitter-iphone.png
    
    
 # Capture a full page screenshot
npx playwright screenshot --full-page en.wikipedia.org wiki-full.png
```
<a name="VrXKk"></a>
## 生成PDF[#](https://playwright.dev/docs/cli#generate-pdf)
生成PDF的功能仅支持 Headless Chromium.
```shell
# See command help
npx playwright pdf https://en.wikipedia.org/wiki/PDF wiki.pdf
```
<a name="6fd32450"></a>
## 安装系统依赖[#](https://playwright.dev/docs/cli#install-system-dependencies)
Ubuntu 18.04 和 Ubuntu 20.04 系统支持自动安装依赖组件.。This is useful for CI environments.
```shell
# See command help
npx playwright install-deps
```
也可以通过指定参数来为指定的浏览器安装依赖组件:
```shell
npx playwright install-deps chromium
```
<a name="ed2cbe22"></a>
## 已知限制[#](https://playwright.dev/docs/cli#known-limitations)
打开 WebKit Web Inspector 将断开 Playwright 与浏览器的连接。在这种情况下，代码生成将停止。

---

<a name="qbs0K"></a>
# 调试工具（Debugging）
Playwright 脚本与现有的调试工具一起使用，例如 Node.js 调试器和浏览器开发工具。 Playwright 还为浏览器自动化引入了新的调试功能。

- [Playwright Inspector](https://playwright.dev/docs/debug#playwright-inspector)
- [Playwright Trace Viewer](https://playwright.dev/docs/debug#playwright-trace-viewer)
- [Run in headed mode](https://playwright.dev/docs/debug#run-in-headed-mode)（[以GUI模式运行](https://www.yuque.com/yumos/ru12wy/rlsgzb#J2Jq2)）
- [Browser Developer Tools](https://playwright.dev/docs/debug#browser-developer-tools)（[浏览器开发工具](https://www.yuque.com/yumos/ru12wy/rlsgzb#14318fda)）
- [Run in Debug Mode](https://playwright.dev/docs/debug#run-in-debug-mode)（[在调试模式下运行](https://www.yuque.com/yumos/ru12wy/rlsgzb#tqTYp)）
- [Selectors in Developer Tools Console](https://playwright.dev/docs/debug#selectors-in-developer-tools-console)（[开发者工具台中的选择器](https://www.yuque.com/yumos/ru12wy/rlsgzb#af569dc1)）
- [Visual Studio Code debugger (Node.js)](https://playwright.dev/docs/debug#visual-studio-code-debugger-nodejs)（[Visual Studio 代码调试器](https://www.yuque.com/yumos/ru12wy/rlsgzb#RmEJd)）
- [Verbose API logs](https://playwright.dev/docs/debug#verbose-api-logs)（[详细的API日志](https://www.yuque.com/yumos/ru12wy/rlsgzb#QV9ML)）
<a name="LxrIT"></a>
## Playwright Inspector[#](https://playwright.dev/docs/debug#playwright-inspector)
[Playwright Inspector](https://playwright.dev/docs/inspector) 是一个 GUI 工具，可帮助创作和调试 Playwright 脚本。这是我们默认推荐的脚本故障排除工具。<br />![108614092-8c478a80-73ac-11eb-9597-67dfce110e00.png](https://cdn.nlark.com/yuque/0/2021/png/22168665/1627117896508-c96a2f34-f151-4081-bce8-94ee7eab7790.png#align=left&display=inline&height=1170&originHeight=1560&originWidth=1424&size=740936&status=done&style=none&width=1068)
<a name="RmTU6"></a>
## Playwright Trace Viewer[#](https://playwright.dev/docs/debug#playwright-trace-viewer)
[Playwright Trace Viewer](https://playwright.dev/docs/trace-viewer) 是一个 GUI 工具，可帮助以事后分析的方式对测试运行进行故障排除.<br />![108614092-8c478a80-73ac-11eb-9597-67dfce110e00.png](https://cdn.nlark.com/yuque/0/2021/png/22168665/1627119255426-69da0c26-da66-4068-a090-f9b91e6422e3.png#align=left&display=inline&height=1158&originHeight=1544&originWidth=2424&size=995158&status=done&style=none&width=1818)
<a name="J2Jq2"></a>
## 以GUI模式运行（Run in headed mode）[#](https://playwright.dev/docs/debug#run-in-headed-mode)
默认情况下，Playwright 以headless模式运行浏览器。. 要更改此行为,请使用 `headless: false` 作为启动选项. 您还可以使用 `slowMo` 选项来减慢执行速度并在调试时继续执行。
```shell
await chromium.launch({ headless: false, slowMo: 100 }); // or firefox, webkit
```
<a name="14318fda"></a>
## 浏览器开发工具（Browser Developer Tools）[#](https://playwright.dev/docs/debug#browser-developer-tools)
您可以在 Chromium、Firefox 和 WebKit 中使用浏览器开发工具，同时以 GUI（Headed）模式运行 Playwright 脚本。开发人员工具有助于：

- 检查 DOM 树并**查找元素选择器**
- 在执行期间**查看控制台日志 （**或了解如何 [通过 API 读取日志](https://playwright.dev/docs/verification#console-logs)）
- 检查**网络活动**和其他开发人员工具功能

![108614092-8c478a80-73ac-11eb-9597-67dfce110e00.png](https://cdn.nlark.com/yuque/0/2021/png/22168665/1627119302427-2c1a4891-b8e9-401e-a84b-e819de89ff6a.png#align=left&display=inline&height=688&originHeight=917&originWidth=1546&size=314059&status=done&style=none&width=1160)<br />使用 [page.pause()](https://playwright.dev/docs/api/class-page#page-pause) 方法是暂停 Playwright 脚本执行并在开发人员工具中检查页面的简单方法。它还将打开 [Playwright Inspector](https://playwright.dev/docs/inspector) 以帮助调试。

**对于 Chromium**: 您还可以通过启动选项打开开发人员工具。
```shell
await chromium.launch({ devtools: true });
```
<a name="i6JqX"></a>
##### ⚠ NOTE
**For WebKit**: launching WebKit Inspector during the execution will prevent the Playwright script from executing any further.
<a name="tqTYp"></a>
## 在调试模式下运行[#](https://playwright.dev/docs/debug#run-in-debug-mode)
设置 `PWDEBUG` 环境变量以在调试模式下运行您的脚本。使用 `PWDEBUG=1` 将打开 [Playwright Inspector](https://playwright.dev/docs/inspector).<br />使用 `PWDEBUG=console` 将配置浏览器以在开发者工具控制台中进行调试：

- **Runs headed**: 浏览器总以 headed 模式启动
- **Disables timeout**: 将默认超时设置为 0 (= no timeout)
- **Console helper**: Configures a `playwright` object in the browser to generate and highlight [Playwright selectors](https://playwright.dev/docs/selectors). This can be used to verify text or composite selectors.
```shell
# Linux/macOS
PWDEBUG=console npm run test

# Windows with cmd.exe
set PWDEBUG=console
npm run test

# Windows with PowerShell
$env:PWDEBUG="console"
npm run test
```
<a name="af569dc1"></a>
## 开发者工具控制台中的选择器（Selectors in Developer Tools Console）[#](https://playwright.dev/docs/debug#selectors-in-developer-tools-console)
在调试模式下使用 `PWDEBUG=console`运行时，可在开发人员工具控制台中使用 `playwright` 对象。

1. 使用 `PWDEBUG=console` 参数运行
2. 设置断点暂停执行
3. 在浏览器开发者工具中打开控制台面板
4. 使用 `playwright` API
   - `playwright.$(selector)`:突出显示第一次出现的选择器内容。这反映了 `page.$` 是如何看到页面的。
   - `playwright.$$(selector)`: 突出显示所有出现的选择器内容。这反映了 `page.$$` 是如何看到页面的。
   - `playwright.inspect(selector)`: 检查“元素”面板中的选择器。
   - `playwright.clear()`: 清除现有高亮标记。
   - `playwright.selector(element)`: 生成一个指向元素的选择器。

![108614092-8c478a80-73ac-11eb-9597-67dfce110e00.png](https://cdn.nlark.com/yuque/0/2021/png/22168665/1627119462689-65b6605a-0213-4f8f-b0ab-a4b43da1f038.png#align=left&display=inline&height=542&originHeight=722&originWidth=1461&size=241508&status=done&style=none&width=1096)
<a name="RmEJd"></a>
## Visual Studio 代码调试器 (Node.js)[#](https://playwright.dev/docs/debug#visual-studio-code-debugger-nodejs)
VS Code 调试器可用于通过断点暂停和恢复 Playwright 脚本的执行。调试器可以通过两种方式进行配置。
<a name="NaCoi"></a>
### 使用启动配置（config）[#](https://playwright.dev/docs/debug#use-launch-config)
为您的 Node.js 项目设置 [launch.json 配置](https://code.visualstudio.com/docs/nodejs/nodejs-debugging) 。配置完成后，使用 F5 启动脚本并使用断点。
<a name="8s7cg"></a>
### 使用 JavaScript 调试终端[#](https://playwright.dev/docs/debug#use-the-javascript-debug-terminal)

1. 打开 [JavaScript Debug Terminal](https://code.visualstudio.com/docs/nodejs/nodejs-debugging#_javascript-debug-terminal)
2. 在 VS Code 中设置断点
   - 或者在 VS Code UI中使用 `debugger` 关键字设置断点
3. 从终端运行你的 Node.js 脚本
<a name="QV9ML"></a>
## 详细的 API 日志（API logs）[#](https://playwright.dev/docs/debug#verbose-api-logs)
Playwright 支持使用  `DEBUG` 环境变量进行详细日志记录。
```shell
# Linux/macOS
DEBUG=pw:api npm run test

# Windows with cmd.exe
set DEBUG=pw:api
npm run test

# Windows with PowerShell
$env:DEBUG="pw:api"
npm run test
```

---

<a name="06c07ae7"></a>
# 支持的语言
Playwright API 支持多种语言

- [JavaScript and TypeScript](https://playwright.dev/docs/languages#javascript-and-typescript)
- [Python](https://playwright.dev/docs/languages#python)
- [Java](https://playwright.dev/docs/languages#java)
- [.NET](https://playwright.dev/docs/languages#net)
<a name="45559f22"></a>
## JavaScript and TypeScript[#](https://playwright.dev/docs/languages#javascript-and-typescript)
支持 [Playwright for Node.js](https://playwright.dev/docs/intro/) .

- [NPM](https://www.npmjs.com/package/playwright)
- [Documentation](https://playwright.dev/docs/intro/)
- [API](https://playwright.dev/docs/api/class-playwright)
- [GitHub repo](https://github.com/microsoft/playwright)
<a name="78b66dd5"></a>
## Python[#](https://playwright.dev/docs/languages#python)
支持 [Playwright for Python](https://playwright.dev/python/docs/intro/).

- [Documentation](https://playwright.dev/python/docs/intro/)
- [API](https://playwright.dev/python/docs/api/class-playwright)
- [Playwright on PyPI](https://pypi.org/project/playwright/)
- [GitHub repo](https://github.com/microsoft/playwright-python)
- [Pytest integration](https://github.com/microsoft/playwright-pytest)
<a name="4b84c96c"></a>
## Java[#](https://playwright.dev/docs/languages#java)
支持 [Playwright for Java](https://playwright.dev/java/docs/intro/).

- [Documentation](https://playwright.dev/java/docs/intro/)
- [API](https://playwright.dev/java/docs/api/class-playwright)
- [GitHub repo](https://github.com/microsoft/playwright-java)
<a name="fbcdb972"></a>
## .NET[#](https://playwright.dev/docs/languages#net)
支持 [Playwright for .NET](https://playwright.dev/dotnet/docs/intro/).

- [Documentation](https://playwright.dev/dotnet/docs/intro/)
- [API](https://playwright.dev/dotnet/docs/api/class-playwright)
- [GitHub repo](https://github.com/microsoft/playwright-dotnet)
- [Playwright on NuGet](https://www.nuget.org/packages/Microsoft.Playwright)
```shell
dotnet add package Microsoft.Playwright
```

---

<a name="kQQA5"></a>
# 发行说明（Release notes）

- [Version 1.13](https://playwright.dev/docs/release-notes#version-113)
- [Version 1.12](https://playwright.dev/docs/release-notes#version-112)
- [Version 1.11](https://playwright.dev/docs/release-notes#version-111)
- [Version 1.10](https://playwright.dev/docs/release-notes#version-110)
- [Version 1.9](https://playwright.dev/docs/release-notes#version-19)
- [Version 1.8](https://playwright.dev/docs/release-notes#version-18)
- [Version 1.7](https://playwright.dev/docs/release-notes#version-17)

---


