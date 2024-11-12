---
title: "What's new in Svelte: 2021年11月"
description: ショーケースを彩る5000個以上の星たち
author: Dani Sandoval
authorURL: https://dreamindani.com
---

SvelteKitの完成度が[80%を超え](https://github.com/sveltejs/kit/milestone/2)、GitHubで[5000スター](https://github.com/sveltejs/kit)を超え、Sapperよりも多くの利用者がいる現在、SvelteKitを試すには絶好の機会です。コミュニティの多くの人が試しているので、今月はかなり大きなショーケースになっています…。

また、11月20日には、世界各国のスピーカーが参加する[Svelte Summit](https://sveltesummit.com)も開催されますので、お見逃しなく。お住まいの地域で開催されるウォッチパーティーにもご注目ください👀

続いては新機能です！

## New in Svelte and SvelteKit

- [svelte.dev](/) now runs on SvelteKit alongside [sveltesociety.dev](https://sveltesociety.dev). svelte.dev is a relatively complicated site with live code editing, authentication, and a markdown-based blog - making it a great way for us to really test out SvelteKit
- A new compiler option, `enableSourcemap`, provides more control over the compiler output for JS and CSS sourcemaps (**3.44.0**). With this new feature, SvelteKit and the Vite Svelte plugin can now properly handle environment variables in `.svelte` templates (See [sveltejs/kit#720](https://github.com/sveltejs/kit/issues/720) and [sveltejs/vite-plugin-svelte#201](https://github.com/sveltejs/vite-plugin-svelte/pull/201))
- The Svelte Language Tools now support reading the configuration of the VS Code CSS settings ([#1219](https://github.com/sveltejs/language-tools/issues/1219))
- `vite-plugin-svelte` added a new `experimental.prebundleSvelteLibraries` option that makes it much faster to load Svelte libraries with many components like icon libraries and UI frameworks. The option can be set in the root of `svelte.config.js`. Please test it out and give us feedback!
- SvelteKit will only route endpoints on the client, unless marked as `rel="external"` - reducing the size of the client JS and making it easier to refactor the router in the future ([2656](https://github.com/sveltejs/kit/pull/2656))
- SvelteKit no longer supports Node 12 ([2604](https://github.com/sveltejs/kit/pull/2604))
- SvelteKit was upgraded from Vite 2.6.0 to Vite 2.6.12 fixing an issue where Vite would corrupt the Svelte runtime (https://github.com/vitejs/vite/issues/4306). It also included two fixes from the SvelteKit team to avoid or make diagnosing Vite issues in SvelteKit templates easier (https://github.com/vitejs/vite/pull/5192 and https://github.com/vitejs/vite/pull/5193). Vite 2.7 is currently available in beta with additional fixes for SSR

To see all updates to Svelte and SvelteKit, check out the [Svelte](https://github.com/sveltejs/svelte/blob/master/CHANGELOG.md) and [SvelteKit changelog](https://github.com/sveltejs/kit/blob/master/packages/kit/CHANGELOG.md), respectively.

---

## Community Showcase

### Apps & Sites

- [Tangent](http://tangentnotes.com/)は、クリーンでパワフルなMac & Windows用のメモアプリです。
- [The Pudding](https://pudding.cool/)は、文化の中で議論されているアイデアをビジュアル・エッセイで説明するデジタル出版物です - SvelteKitで再構築されました。
- [Power Switcher](https://powerswitcher.axpo.com/)は、エネルギー源がよりクリーンなものに移行していく中で、スイスの電力供給の発展をインタラクティブに紹介しています。
- [Sublive](https://sub.live/)は、世界中のミュージシャンを低レイテンシーかつ高品質なオーディオネットワークで繋ぎ、新しい音楽の作り方を提案します。
- [Vibify](https://www.vibify.me/)は、Spotifyの再生履歴を利用して、音楽の中に隠れたプレイリストを見つけることができます。
- [Browse Marvel Unlimited by Year](https://marvel.geoffrich.net/)はSveltekitサイトで、Marvel Unlimitedで入手可能な発行物を年ごとに探すことができます。
- [Files](https://files.community/)は、Windows用の最新のファイルエクスプローラーです。SvelteKitで再構築された新しいサイトを公開しています。
- [lil-hash](https://github.com/jackbow/lil-hash)は、覚えやすく、話しやすい短縮URLを生成するシンプルなURL短縮ツールです。
- [PWA Haven](https://github.com/ThaUnknown/pwa-haven)は、OSのネイティブアプリを置き換える、小さく、速く、シンプルなPWAのコレクションです。
- [DottoBit](https://dottobit.com/)は、URL共有機能を備えたマルチカラーの16bitドローイングプログラムです。
- [Former Fast Document for Print](https://github.com/zummon/former)は、美しいデザイン、国際言語対応、自動計算機能を備えた請求書作成ソフトです。
- [Helvetikon](https://github.com/noahsalvi/helvetikon)は、スイス・ドイツ語のコミュニティが運営する辞書です。
- [Palitra App](https://palitra.app/)は、検索ベースのカラーパレットジェネレータです。

### Podcasts Featuring Svelte

- [Svelte Radio](https://www.svelteradio.com/episodes/svelte-summit-is-coming-up-and-svelte-is-growing)では、先日リリースされたSvelte Summitのウェブサイトを支える技術や、その他の楽しいことをたくさん紹介しています！
- [PodRocket](https://podrocket.logrocket.com/rich-harris)は、LogRocketのポッドキャストで、Rich HarrisとともにSvelteについて話しています。
- [また、PodRocketではさらに](https://podrocket.logrocket.com/elderjs)、Elder.jsについてNick Reeseとともに掘り下げています。
- [PodRocket also dove deep](https://podrocket.logrocket.com/elderjs) Nick Reeseと一緒にElder.jsに導入しました。
- [Web Rush](https://webrush.io/episodes/episode-153-single-page-application-vs-multi-page-application-with-rich-harris)とリッチ・ハリスが、SPAとMPAの違い、サーバーレンダリングが果たす役割、クライアントサイドハイドレーションとは何か、SPAやMPAを開発するための最新ツールの状況などについて語ります。
- [devtools.fm](https://devtools.fm/episode/15)では、魅力的なデータビジュアライゼーションの開発とツール構築の将来について、リッチ・ハリスと語り合っています。

### Educational Content

- [Have Single-Page Apps Ruined the Web?](https://www.youtube.com/watch?v=860d8usGC0o) 今年のJamstack Confで、リッチ・ハリスが論争の的となった質問に答えました。
- [Svelte vs SvelteKit - What's The Difference?](https://www.youtube.com/watch?v=IKhtnhQKjxQ) LevelUpTutsでは、この2つのプロジェクトの関係を説明するクイックガイドを提供しています。Scott Tolinski氏によるSvelteに関するガイドの残りの部分は、彼の新シリーズである["Weekly Svelte"](https://www.youtube.com/playlist?list=PLLnpHn493BHF-Onm1MQgKC1psvW-rJuYi)でチェックできます。
- [WebJedaのSvelteKit Hooks](https://www.youtube.com/watch?v=RarufLoEL08&list=PLm_Qt4aKpfKgzcTiMT2cgWGBDBIPK06DQ)シリーズは、今月も第3回「クッキーセッション認証」をお届けします。
- [Writing Context Aware Styles in a Svelte App](https://www.ryanfiller.com/blog/tips/svelte-contex-aware-styles)は、親に動的に適応することができる自己完結型のコンポーネントを書くためのガイドです。
- [A Beginner's Guide to SvelteKit](https://www.sitepoint.com/a-beginners-guide-to-sveltekit/)では、SvelteとSvelteKitの両方を初心者向けに説明し、架空のユーザーのプロフィールページを表示するシンプルなウェブアプリを構築しています。
- [Svelte vs React: Ending the Debate](https://massivepixel.io/blog/svelte-vs-react/)は、昔からある議論を歴史的に捉えたものです。
- [Svelte Snacks | Custom Events for Modal Actions](https://jeremydayslice.hashnode.dev/svelte-snacks-or-custom-events-for-modal-actions)では、Svelteの便利なカスタムイベントシステムのしっかりとした実装を紹介しています。
- [What Svelte's accessibility warnings won't tell you](https://geoffrich.net/posts/svelte-a11y-limits/)では、Svelteのa11y警告がどのように機能するのか、また、アプリケーションをアクセシブルにするために警告をあてにしてはいけない理由を説明しています。

### Libraries, Tools & Components

- [svelte-adapter-azure-sw](https://github.com/geoffrich/svelte-adapter-azure-swa)は、動的なサーバーレンダリングにAzure関数を使用してAzure Static Web Appを作成するSvelteアプリ用のアダプタです。
- [Inlang](https://docs.inlang.dev/getting-started/svelte-kit)は、SvelteKitに対応したローカリゼーション・国際化ツールキットです。
- [svelte-translate-tools](https://github.com/noelmugnier/svelte-translate-tools) ビルド時にSvelteアプリの翻訳ファイルを抽出/生成/コンパイルします。
- [@egjs/svelte-infinitegrid](https://github.com/naver/egjs-infinitegrid/tree/master/packages/svelte-infinitegrid)では、サイズの異なるカード要素で構成された様々なグリッドを実装することができます。
- [svelte-reactive-css-preprocess](https://github.com/srmullen/svelte-reactive-css-preprocess)は、コンポーネントの状態が変化するたびに、css変数の値を簡単に更新することができます。
- [Sveltegen](https://github.com/snuffyDev/sveltegen)は、アクション、コンポーネント、ルートをシンプルかつ簡単に作成するためのCLIです。
- [svelte-advanced-multistep-form](https://www.npmjs.com/package/svelte-advanced-multistep-form)は、レンダリングされるコンポーネントにスタイルを渡すフォーム要素をラップするのに役立ち、また、各フォームステップを順序立ててスタイリッシュに表示します。
- [gQuery](https://github.com/leveluptuts/gQuery)は、SvelteKit用のGraphQL Fetcher & Cacheです。
- [date-picker-svelte](https://github.com/probablykasper/date-picker-svelte)は、Svelte用の日付と時間のピッカーです。
- [TwelveUI](https://twelveui.readme.io/reference/what-is-twelveui)は、アクセシビリティを内蔵したSvelteのコンポーネントライブラリです。
- [svelte-outclick](https://github.com/babakfp/svelte-outclick/)は、outclickイベントを提供することで、要素の外側でクリックをリッスンすることができるSvelteコンポーネントです。
- [svelte-zero-api](https://github.com/ymzuiku/svelte-zero-api)では、SvelteKit APIをクライアント関数のように使用することができます - TypeScriptをサポートしています。
- [svelte-recaptcha-v2](https://github.com/basaran/svelte-recaptcha-v2)は、Svelte SPA、SSR、sveltekitの静的サイト用のGoogle reCAPTCHA v2の実装です。
- [Svelte Body](https://github.com/ghostdevv/svelte-body)は、SvelteKitやRoutifyと連携して、ルートのボディにスタイルを適用することができます。
- [svelte-debug-console](https://github.com/basaran/svelte-debug-console)は、Svelte SPA、SSR、sveltekitの静的サイトのためのdebug.jsの実装で、デバッグ文をブラウザ上で確認することができます。
- [SVEO](https://github.com/didier/sveo)は、SvelteKitページのメタデータを宣言するための、依存性のないアプローチです。
- [@svelte-drama/suspense](https://www.npmjs.com/package/@svelte-drama/suspense)は、Reactの`<Suspense>`のコアアイデアを実装したSvelteコンポーネントです。また、[SWR for Svelte](https://www.npmjs.com/package/@svelte-drama/swr)をチェックすると、リフェッチがさらに簡単になります。
- [sveltekit-adapter-browser-extension](https://github.com/antony/sveltekit-adapter-browser-extension)は、アプリをクロスプラットフォームのブラウザ拡張にするSvelteKit用のアダプタです。

コミュニティサイト [sveltesociety.dev](https://sveltesociety.dev/templates)では、Svelte エコシステム全体からの templates、adders、adapters をご覧いただけます。

もっと更新情報をお探しですか？ [Reddit](https://www.reddit.com/r/sveltejs/)または[Discord](https://discord.com/invite/yy75DKs) にご参加ください！
