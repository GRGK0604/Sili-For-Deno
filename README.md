# 硅基流动账号池

## 简介

硅基流动账号池是一个基于 [Deno](https://deno.com/) 的高效、轻量级账号管理系统。它允许用户动态创建、管理和使用多个账号，适用于需要频繁切换账号的应用场景，例如爬虫、自动化测试等。

## 特性

- **高性能**：基于Deno构建，充分利用其异步特性，提高处理效率。
- **简洁易用**：API设计简洁，便于快速上手和集成。
- **动态管理**：支持动态创建、删除和更新账号信息。
- **数据持久化**：账号信息可以持久保存到数据库，支持多种数据库选项。
- **安全性**：内置基本的安全机制，保护账号信息。

## 安装

1. 确保你已安装 [Deno](https://deno.com/#installation)。
2. 克隆项目：

   ```bash
   git clone https://github.com/grgk0604/silicon-flow-account-pool.git
   cd silicon-flow-account-pool
   ```

3. 运行项目：

   ```bash
   deno run --allow-net --allow-read --allow-write server.ts
   ```

## 使用

### 创建账号

通过API接口创建新的账号：

```bash
curl -X POST http://localhost:8000/accounts -H "Content-Type: application/json" -d '{"username": "your_username", "password": "your_password"}'
```

### 获取所有账号

获取当前所有账号的列表：

```bash
curl http://localhost:8000/accounts
```

### 删除账号

通过账号ID删除指定账号：

```bash
curl -X DELETE http://localhost:8000/accounts/{account_id}
```

## 配置

在项目根目录下创建一个 `.env` 文件，配置你的数据库连接信息：

```
DB_HOST=localhost
DB_USER=username
DB_PASS=password
DB_NAME=account_pool
```

## 贡献

欢迎提出问题和建议，或者为项目贡献代码！请遵循以下步骤：

1. Fork 这个仓库
2. 创建你的特性分支 (`git checkout -b feature/YourFeature`)
3. 提交你的更改 (`git commit -m 'Add some feature'`)
4. 推送到分支 (`git push origin feature/YourFeature`)
5. 创建一个 Pull Request

## 许可证

此项目使用 MIT 许可证，详情请参见 [LICENSE](LICENSE) 文件。

## 联系

如有问题，请通过以下方式联系我：

- 邮箱: grgk0604@163.com
- GitHub: [grgk0604](https://github.com/grgk0604)
