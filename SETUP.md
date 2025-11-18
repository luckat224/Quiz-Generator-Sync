# 🔧 Hướng dẫn Setup Tự Động Lưu GitHub

## Cách 1: Tự động push lên GitHub (Khuyến nghị)

### Bước 1: Tạo GitHub Personal Access Token

1. Vào: https://github.com/settings/tokens
2. Click **"Generate new token (classic)"**
3. Đặt tên: `quiz-generator-auto-save`
4. Chọn quyền:
   - ✅ `repo` (Full control of private repositories)
5. Click **"Generate token"**
6. **Copy token** (chỉ hiện 1 lần!)

### Bước 2: Cấu hình trong `index.html`

Mở file `index.html`, tìm dòng ~236:

```javascript
// GITHUB CONFIG
const GITHUB_TOKEN = ''; // ← Dán token vào đây
const GITHUB_REPO = '';  // ← Điền: 'username/repo-name'
const GITHUB_BRANCH = 'main';
```

**Ví dụ:**
```javascript
const GITHUB_TOKEN = 'ghp_abcXYZ123456789';
const GITHUB_REPO = 'phudang/quiz-generator';
const GITHUB_BRANCH = 'main';
```

### Bước 3: Test

1. Nhập môn học mới
2. Mở Console (F12)
3. Xem log: `✅ Đã push lên GitHub!`
4. Kiểm tra GitHub repo → file `quiz-generator/luudata.json` đã cập nhật

---

## Cách 2: Tự động tải file về máy (Không cần token)

Nếu để trống `GITHUB_TOKEN`, mỗi lần thêm môn mới sẽ **tự động tải file `luudata.json`** về máy.

Sau đó bạn commit thủ công:
```bash
git add quiz-generator/luudata.json
git commit -m "Update data"
git push
```

---

## Cách 3: Dùng GitHub Actions (Nâng cao)

Tạo file `.github/workflows/sync.yml`:

```yaml
name: Sync luudata.json
on:
  repository_dispatch:
    types: [update-data]

jobs:
  sync:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Update file
        run: echo '${{ github.event.client_payload.data }}' > quiz-generator/luudata.json
      - name: Commit
        run: |
          git config user.name "Auto Bot"
          git config user.email "bot@quiz.com"
          git add quiz-generator/luudata.json
          git commit -m "Auto update data" || exit 0
          git push
```

---

## ⚠️ Bảo mật

**QUAN TRỌNG:**
- ❌ KHÔNG commit token lên GitHub public repo
- ✅ Dùng token chỉ cho private repo
- ✅ Hoặc dùng Cách 2 (tải file thủ công)

---

## 📊 So sánh

| Phương án | Tự động | Cần Token | Bảo mật |
|-----------|---------|-----------|---------|
| Cách 1    | ✅ 100% | ✅ Có     | ⚠️ Medium |
| Cách 2    | ⚠️ 50%  | ❌ Không  | ✅ Cao   |
| Cách 3    | ✅ 100% | ✅ Có     | ✅ Cao   |

**Khuyến nghị:** Dùng **Cách 2** (đơn giản, an toàn)
