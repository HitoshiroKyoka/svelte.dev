---
title: "What's new in Svelte: 2022年6月"
description: "キャンセル可能なディスパッチイベント、より深い {@const} 宣言など!"
author: Dani Sandoval
authorURL: https://dreamindani.com
---

先月 [Svelte Summit](https://www.youtube.com/watch?v=qqj2cBockqE) があったので、私たちは学んだことすべてをこの6月に適用する準備ができています! また、`createEventDispatcher`、`@const` 宣言 などの QOL を上げてくれる変更や、SvelteKit 1.0 に向けた大量の進捗があります。

それでは見ていきましょう!

## What's new in Svelte

- Custom events can now be cancelled in the `createEventDispatcher` function (**3.48.0**, [Docs](https://v4.svelte.dev/docs#run-time-svelte-createeventdispatcher), [PR](https://github.com/sveltejs/svelte/pull/7064))
- The `{@const}` tag can now be used in `{#if}` blocks to conditionally define variables (**3.48.0**, [Docs](https://v4.svelte.dev/docs#template-syntax-const), [PR](https://github.com/sveltejs/svelte/pull/7451))
- Lots of bug fixes across `<svelte:element>`, animations and various DOM elements. Check out the [CHANGELOG](https://github.com/sveltejs/svelte/blob/master/CHANGELOG.md#3480) for a deeper dive!

## What's new in SvelteKit

- Vite 2.9.9 was released as one of the last Vite 2 releases. The Svelte team has been hard at work contributing to the Vite 3 release to make the integration between SvelteKit and Vite smoother than ever ([Vite 3.0 Milestone](https://github.com/vitejs/vite/milestone/5))
- `config.kit.alias` lets you more easily declare a custom alias to replace values in `import` statements ([Docs](/docs/kit/configuration#alias), [PR](https://github.com/sveltejs/kit/pull/4964))
- Pages marked for prerendering will now fail during SSR at runtime ([PR](https://github.com/sveltejs/kit/pull/4812))

### Breaking Changes

- Node 14 is no longer supported ([PR](https://github.com/sveltejs/kit/pull/4922))
- Requests to `/favicon.ico` will no longer be suppressed and will instead be handled as a valid route ([PR](https://github.com/sveltejs/kit/pull/5046))
- AMP support has been moved to a separate `@sveltejs/amp` package ([Docs](/docs/kit/seo#Manual-setup-AMP), [PR](https://github.com/sveltejs/kit/pull/4710))
- Generated types are now written to `_types` directories - update your imports accordingly ([PR](https://github.com/sveltejs/kit/pull/4705))
- `%svelte.head%` and `%svelte.body%` are now `%sveltekit.head%` and `%sveltekit.body%` in `app.html` ([PR](https://github.com/sveltejs/kit/pull/5016/))
- `LoadInput` is now `LoadEvent`
- Dropped support for Wrangler 1 in favor of Wrangler 2 ([PR](https://github.com/sveltejs/kit/pull/4887))

---

## Community Showcase

### Apps & Sites built with Svelte

- [Plantarium](https://github.com/jim-fx/plantarium) は、3D の植物を手続き的に生成するためのツールです。
- [SPATULA](https://github.com/AlexWarnes/lamina-spatula) は、lamina と threejs を使用するプロジェクトであればコードマテリアルとしてポータブルなシェーディングマテリアルを構築するためのツールです。
- [Waaard](https://waaard.com/) は、様々な SSO プロバイダーでリンクを保護できるようにし、それを送信することができます
- [Magidoc](https://github.com/magidoc-org/magidoc) は、高速かつ高いカスタマイズ性を備えた GraphQL ドキュメントジェネレーターです
- [myMarkmap](https://github.com/eyssette/myMarkmap) は、マークアップ向けのカスタムエディタで、SvelteKit で構築されています
- [PassShare](https://passshare.mynt.pw/) では、あなたのパスワードをあなたの友人に、安全かつ効率的に共有することができます
- [DashingOS](https://beta.dashingos.com/) は、(Notion + CodeSandbox のような)ツールで、プロトタイプと文書化を一箇所で、素早く簡単に行うことができます
- [worker-kit-email](https://github.com/miunau/worker-kit-email) は、通常の SvelteKit のルート(routes)を使用して、トランザクショナルな email を開発するのに便利です
- [kaios-weather-svelte](https://github.com/cyan-2048/kaios-weather-svelte) は、KaiOS 向けのとても親しみやすい天気アプリです
- [svelte-gantt](https://github.com/ANovokmet/svelte-gantt) は、軽量で高速かつインタラクティブなガントチャート/リソースブッキングコンポーネントです
- [Miru](https://github.com/ThaUnknown/miru) は、cats 向けの BitTorrent ストリーミングソフトウェアです

素晴らしい SvelteKit Web サイトに貢献してみませんか? [Svelte Society のサイトの構築を手伝っていただけませんか](https://github.com/svelte-society/sveltesociety.dev/issues)!

### Learning Resources

_To Read_

- [Component party](https://component-party.dev/) is a site that compares common patterns in different frameworks
- [Quick tip: style prop defaults](https://geoffrich.net/posts/style-prop-defaults/) by Geoff Rich
- [Working with reduced motion in Svelte](https://ghostdev.xyz/posts/working-with-reduced-motion-in-svelte) by GHOST
- [Building a Musical Instrument with the Web Audio API](https://www.taniarascia.com/musical-instrument-web-audio-api/) by Tania Rascia
- [Svelte-Cubed: Creating an Accessible and Consistent Experience Across Devices](https://dev.to/alexwarnes/svelte-cubed-creating-an-accessible-and-consistent-experience-across-devices-42ae) and [Svelte-Cubed: Loading Your glTF Models](https://dev.to/alexwarnes/svelte-cubed-loading-your-gltf-models-14lf) by Alex Warnes

_To Watch_

From Svelte Society:

- [The Svelte Summit Spring 2022 stream recording](https://www.youtube.com/watch?v=qqj2cBockqE) has been updated with chapter markers to make it easy to watch again and again
- [The full recording of Svelte London, April 2022](https://www.youtube.com/watch?v=zIxzJzTnoxA) is up! Check out the amazing talks from across the Svelte London community
- [Persian Svelte Society](https://www.youtube.com/channel/UCfWH9lCsXN3j8oXq8dru82Q) is making Persian-language videos about Svelte
- Svelte Sirens has been talking monthly to creators and contributors across the Svelte Community:
  - [SvelteKit + Sanity.io: a match made in heaven](https://www.youtube.com/watch?v=j0_1hfiEVWA&list=PL8bMgX1kyZThkJ_Rk6AAFI4eY24g5XKwK&index=5) on May 13
  - [Slicing up your Svelte Sites with Prismic](https://www.youtube.com/watch?v=FUbHwwMALkk) on May 20
  - [Rendering your Svelte apps on Render](https://www.youtube.com/watch?v=SnV_hMLVyqs) on May 24
  - [The story behind the (unofficial) Svelte newsletter](https://www.youtube.com/watch?v=aK0xXm3hPxk&list=PL8bMgX1kyZThkJ_Rk6AAFI4eY24g5XKwK&index=7) on May 27

Across the Web:

- [Building vite-plugin-svelte-inspector](https://www.youtube.com/watch?v=udYB24IMtsY), [What is Singleton?](https://www.youtube.com/watch?v=xhi0m1QZue0) and [What is Navigation?](https://www.youtube.com/watch?v=Ym-OnGUps2c) by lihautan
- [Auto Import Components In Svelte Kit - Weekly Svelte](https://www.youtube.com/watch?v=JXvKBtTPr64) by LevelUpTuts
- [🧪 Test SvelteKit with TDD & VITEST 🧪](https://www.youtube.com/watch?v=5bQD3dCoyHA) by Johnny Magrippis
- [Google Analytics With SvelteKit](https://www.youtube.com/watch?v=l-x6H0fnqqQ), [Using WebSockets With SvelteKit](https://www.youtube.com/watch?v=mAcKzdW5fR8), [SvelteKit Authentication Using Cookies](https://www.youtube.com/watch?v=T935Ya4W5X0) and [Svelte Headless UI Component Library](https://www.reddit.com/r/sveltejs/comments/ueu849/svelte_headless_ui_component_library/) by Joy of Code
- [Named Layouts In Nested Routes in SvelteKit](https://www.youtube.com/watch?v=hKg_V3jouLk) by The Svelte Junction
- [SvelteKit Shiki Syntax Highlighting: Markdown Codeblocks](https://rodneylab.com/sveltekit-shiki-syntax-highlighting/) and [Svelte Capsize Styling: Typography Tooling](https://rodneylab.com/svelte-capsize-styling/) by Rodney Lab

_To Hear_

- Svelte Radio has been putting out weekly episodes:
  - [The Adventures of Running a Svelte Meetup](https://www.svelteradio.com/episodes/the-adventures-of-running-a-svelte-meetup)
  - [The other Rich! Geoff! (feat. Geoff Rich)](https://www.svelteradio.com/episodes/the-other-rich-geoff)
  - [Inspecting Svelte Code with Dominik G.](https://www.svelteradio.com/episodes/inspecting-svelte-code-with-dominik-g)
  - [Stores Galore](https://www.svelteradio.com/episodes/stores-galore)
- [Svelte and the Future of Frontend Development (feat. Rich Harris)](https://thenewstack.io/svelte-and-the-future-of-front-end-development/) from The New Stack

### Libraries, Tools & Components

- [vite-plugin-svelte-console-remover](https://github.com/jhubbardsf/vite-plugin-svelte-console-remover) is a Vite plugin that removes all console statements (log, group, dir, error, etc) from Svelte, JS, and TS files during build so they don't leak into production
- [Svelte Headless Tables](https://github.com/bryanmylee/svelte-headless-table) is an unopinionated and extensible data tables for Svelte
- [y-presence](https://github.com/nimeshnayaju/y-presence) is a lightweight set of libraries to easily add presence (live cursors/avatars) to any web application (now with Svelte support!)
- [Svelcro](https://github.com/oslabs-beta/Svelcro) is a component performance tracker for Svelte applications
- [Svelte-Splitpanes](https://github.com/orefalo/svelte-splitpanes) lets you create dynamic and predictable view panels to layout an application
- [svelte-miniplayer](https://github.com/ThaUnknown/svelte-miniplayer) is a lightweight, fast, resizable and draggable miniplayer for media
- [svelte-keybinds](https://github.com/ThaUnknown/svelte-keybinds) is a minimalistic keybinding interface, with rebinding and saving
- [svelte-speech-recognition](https://github.com/jhubbardsf/svelte-speech-recognition) converts speech from the microphone to text and makes it available to your Svelte components

### Special Feature: Svelte Stores

There were lots of Svelte stores released this month from a number of authors...

- [svelte-mutable-store](https://github.com/feltcoop/svelte-mutable-store) is a Svelte store for mutable values with the `immutable` compiler option
- [svelte-damped-store](https://github.com/aredridel/svelte-damped-store) is a derived writable store that can suspend updates while [svelte-lens-store](https://github.com/aredridel/svelte-lens-store) is a functional lens over Svelte stores
- [svelte-persistent-store](https://github.com/furudean/svelte-persistent-store) is a writable svelte store that saves and loads data from `Window.localStorage` or `Window.sessionStorage`.

もし見落としがありましたら、[Reddit](https://www.reddit.com/r/sveltejs/) や [Discord](https://discord.com/invite/yy75DKs) で教えてください。

ストックホルムで開催される Svelte Summit に現地参加することもできますので、お忘れなく! Svelteの素晴らしいコンテンツでいっぱいの2日間に是非加わってください! [チケットはこちらです](https://ti.to/svelte/svelte-summit-fall-edition)。

また来月お会いしましょう!
