# bandlik-bruno — Claude Qo'llanmasi

## Repo haqida

Bu repo **Bruno API kolleksiyasi** (`bandlik-bruno`) — Bandlik backend'ining
API dokumentatsiyasi (Bruno 3.3+ OpenCollection YAML formatida). Standalone repo
sifatida ham ishlaydi, ham asosiy loyihaga git submodule sifatida ulanadi:
`/var/www/xba/docs/bruno/`.

- **GitHub**: https://github.com/IlhomjonMuxtorov/bandlik-bruno
- Tuzilma va statistikalar uchun: [README.md](README.md)
- Bruno fayl/papka konventsiyalari (nomlash, `folder.yml`, `docs` maydoni va h.k.)
  asosiy loyiha `AGENTS.md` sining **Bruno API Collection** bo'limida — bu yerda
  takrorlanmaydi.

## Git Commit

- Commit message'ga **hech qachon** `Co-Authored-By: Claude ...` footer (yoki har qanday
  Claude / Anthropic co-author qatori, jumladan `<noreply@anthropic.com>`) qo'shilmaydi.
- PR body'ga ham Claude / Anthropic attribution (masalan "Generated with Claude Code")
  qo'shilmaydi — foydalanuvchi aniq so'ramaguncha.
- Commit **doim** foydalanuvchining aniq ruxsati bilan yaratiladi — avtomatik commit qilinmaydi.

## Submodule eslatmasi

Bu repo asosiy loyihada submodule. Bruno o'zgarishlari **submodule'ning o'z `main`
branchida** commit qilinadi (doim pathspec bilan — parallel ishni supurib ketmaslik
uchun) va shu repoga **push qilinadi**; so'ng asosiy repodagi gitlink (submodule pointer)
**shu o'zgarishni chaqirgan kod commit'i bilan birga** bump qilinadi.

- Gitlink bump — **default**, alohida so'rov talab qilmaydi
- Push majburiy: origin'da yo'q SHA'ga pointer boshqa clone'da `git submodule update` ni
  buzadi (`fatal: reference is not a tree`)
- To'liq oqim asosiy loyiha `AGENTS.md` → **Bruno API Collection → Submodule va gitlink**
