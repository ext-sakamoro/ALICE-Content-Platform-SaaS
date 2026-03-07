# ALICE-Content-Platform

Content management with full-text search, font rendering, and CDN delivery

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-text, alice-search, alice-font, alice-cdn, alice-text-compression

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/publish` | コンテンツ公開 |
| `POST` | `/api/v1/search` | 全文検索 |
| `GET ` | `/api/v1/fonts` | フォント一覧・配信 |
| `GET ` | `/api/v1/cdn/status` | CDN配信ステータス |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
