# 购物商城前端学习示例

使用 Vue 3、TypeScript、Vite 和 Tailwind CSS 实现的商品列表页面，包含站点头部、商品卡片与示例商品数据。

配套后端：[`shopping_cart_afterEnd`](https://github.com/YouRen1320/shopping_cart_afterEnd)。两个仓库目前尚未完成接口联调。

## 本地运行

```bash
pnpm install --frozen-lockfile
pnpm dev
```

类型检查与生产构建：`pnpm build`。

## 当前接口状态

`src/api/products.ts` 中的 `getProductList()` 返回本地模拟数据，没有向后端发起 HTTP 请求。商品图片使用第三方外链，是否可显示取决于外部服务。

当前没有登录、购物车持久化、订单结算或支付流程。后续接入后端时，需要把后端的统一响应与商品字段映射到 `src/types/products.ts`；仅启动后端不会自动切换数据来源。

## 目录

- `src/api/products.ts`：模拟商品数据与读取函数。
- `src/components/`：头部和商品卡片。
- `src/types/products.ts`：前端商品结构。
- `src/App.vue`：读取并展示商品列表。

本仓库用于学习，未声明独立开源许可证。
