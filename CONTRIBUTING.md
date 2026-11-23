# 🤝 CryptoHub 开源贡献指南 (Contributing Guide)

感谢你关注并愿意为 **CryptoHub** 做出贡献！本项目致力于打造一个中立、安全、高质量且持续更新的加密生态导航库。

为了保障所有 Web3 用户的资金与信息安全，所有提交的收录请求都必须经过严格的标准审核。

---

## 📌 收录原则与底线要求

1. **绝对拒绝一切恶意项目**：
   - 严禁提交任何空气币、传销盘、貔貅盘(Honeypot)、资金盘、杀猪盘及任何形式的恶意洗钱项目。
   - 严禁包含任何假冒、镜像、仿冒或钓鱼(Phishing)域名的链接。
2. **客观与真实活跃度**：
   - 工具或平台必须具备真实的链上或行业活跃度，已上线主网或成熟测试网。
   - 不收录完全无用户基础、代码无维护、甚至官方推特/社群均已停更的项目。
3. **域名真实可查**：
   - 必须提供项目官方推特认证（Twitter/X）、CoinMarketCap/CoinGecko官方认证或权威GitHub官方仓库背书的顶级真实主域名。
4. **分类规范**：
   - 遵守项目现有的十项大分类标准，尤其是交易所（CEX/DEX）置于核心顶部。

---

## 🛠️ 如何提交新增或修改

### 方式一：通过 GitHub Issue 建议
如果你不熟悉代码操作，可以直接在仓库提一个 **Issue**：
- **标题**：`[收录申请] 项目名称 - 分类名称`
- **内容模板**：
  ```markdown
  - **项目名称**：例如 Jupiter
  - **分类/子分类**：exchanges / dex
  - **官方网址**：https://jup.ag
  - **认证域名**：jup.ag
  - **核心功能与简介**：50字左右的客观精炼中文介绍
  - **标签**：["Solana龙头", "DEX聚合"]
  - **收录理由**：该项目在行业内的地位、TVL或活跃度简述
  ```

### 方式二：通过 Pull Request 直接修改静态数据 (推荐)
1. **Fork** 本仓库并 Clone 到本地；
2. 直接编辑静态数据文件 `data/navigation.json` 中的 `items` 列表：
   ```json
   {
     "id": "your-project-id",
     "name": "项目中文名 (English Name)",
     "name_en": "English Name",
     "category": "exchanges",
     "subcategory": "dex",
     "url": "https://example.com",
     "domains": ["example.com"],
     "description": "客观、中立、翔实的功能与优势说明（建议40-80字）",
     "tags": ["标签1", "标签2"],
     "is_featured": false
   }
   ```
3. 网页端部署上线后会自动动态读取 `data/navigation.json`；
4. 提交 PR 并附带必要的官方信源佐证即可。

---

## 🔍 审核与合规流程
- 维护者通常会在 24-48 小时内完成审查与域名合规校验；
- 若审核通过，PR 将被直接合并至 `main` 分支并由 GitHub Pages 自动部署上线！
