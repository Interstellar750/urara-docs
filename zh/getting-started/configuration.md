# 配置

## 配置文件

本項目使用 `/src/lib/config/` 作爲配置文件目錄，但多數配置在一般情況下無需修改。

從 site.ts 開始：

```ts
export const site: Site = {
  title: 'Urara', // 標題
  subtitle: 'Sweet & Powerful SvelteKit Blog Template', // 副標題
  lang: 'en-US', // 語言
  descr: 'Powered by SvelteKit/Urara', // 描述
  author: {
    name: 'John Doe', // 作者名稱
    avatar: '/assets/maskable@512.png', // 作者圖片
    status: '🌸', // 作者狀態
    bio: 'lorem ipsum dolor sit amet, consectetur adipiscing elit.' // 作者描述
  },
  url: (import.meta.env.URARA_SITE_URL as string) ?? 'https://example.com', // 域名
  themeColor: '#3D4451' // 主題顔色（目前僅用於 Manifest）
}
```

## 圖示

默認提供一些圖示以兼容 Web app manifests 及現代瀏覽器，可以自行替換。

```text
/urara/favicon.png - 網站圖示，32x32
/urara/assets/any@180.png - 網站圖示，180x180
/urara/assets/any@192.png - 網站 / Manifest 圖示，192x192
/urara/assets/any@512.png - Manifest 圖示，512x512
/urara/assets/manifest@192.png - Manifest 遮罩圖示，192x192
/urara/assets/manifest@512.png - Manifest 遮罩圖示，512x512
```

也可以通過修改 `/src/lib/config/icons.ts` 替換圖示數量及路徑。