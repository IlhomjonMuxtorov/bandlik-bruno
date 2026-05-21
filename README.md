# 🚀 XBA — Bruno API Collections

Global SkillHub API dokumentatsiyasi Bruno formatida.

## 📁 Structure

```
/docs/bruno/
├── opencollection.yml        # Main collection config
├── README.md                 # This file
├── environments/             # Environment configurations
│   ├── development.yml       # Dev environment (consistent variables)
│   └── production.yml        # Prod environment (same variable names)
├── mobile/                   # Mobile API (72 requests)
│   ├── folder.yml
│   ├── 🔐 Auth/
│   ├── 👤 Candidate/
│   ├── 📱 Device/
│   ├── 📄 CV/
│   ├── 🌍 Reference/
│   ├── 🪪 MyID/
│   ├── 💼 Vacancies/
│   └── 👤 Candidate Profile/
│
└── admin/                    # Admin API (185 requests)
    ├── folder.yml
    ├── 🔐 Auth/
    ├── 🌍 Reference/
    ├── 🏢 XBA Organizations/
    ├── 🛂 Visa Organizations/
    ├── 🏛️ Notarius Organizations/
    ├── 🚚 Logistika Organizations/
    ├── 🛡️ Sug'urta Organizations/
    ├── 🏢 Ish beruvchi Organizations/
    ├── 👤 Rekruter Organizations/
    └── [Plus Services, Employees, and other folders]
```

## 🔗 Repository

- **GitHub**: https://github.com/IlhomjonMuxtorov/bandlik-bruno
- **Standalone collection** (API docs only, backend'dan erkli)
- **Main repo'da**: `/var/www/xba/docs/bruno/` (git submodule sifatida)

### Clone

**Standalone repo sifatida:**
```bash
git clone https://github.com/IlhomjonMuxtorov/bandlik-bruno.git
bruno open bandlik-bruno/
```

**Asosiy repo ichida (submodule):**
```bash
git clone --recurse-submodules https://github.com/yourorg/xba.git
# yoki:
git clone https://github.com/yourorg/xba.git
cd xba
git submodule update --init --recursive
```

---

## 🚀 Quick Start

### In Bruno 3.3+

```bash
# Open the collection
bruno open ./

# Or in Bruno GUI:
# File → Open Collection → [Bruno folder path]
```

### Environment Setup

Environment'lar `environments/` folderida saqlanadi:

**Development Environment** (`development.yml`):
```yaml
name: development
variables:
  - name: base_url
    value: http://api.bandlik.loc
  - name: admin_token
    value: ""
  - name: access_token
    value: ""
  - name: guest_token
    value: ""
  - name: device_id
    value: "550e8400-e29b-41d4-a716-446655440000"
```

**Production Environment** (`production.yml`):
```yaml
name: production
variables:
  - name: base_url
    value: http://api.bandlik.uz
  - name: admin_token
    value: ""
  - name: access_token
    value: ""
  - name: guest_token
    value: ""
  - name: device_id
    value: "550e8400-e29b-41d4-a716-446655440000"
```

**Variable Format in Requests:**
```
{{base_url}}          ← Bruno template syntax
{{ admin_token }}
{{ access_token }}
{{ device_id }}
```

**Setup:**
1. Collection ochilgandan keyin, environment dropdown'dan **development** yoki **production** tanlang
2. Variables avtomatik to'lidi (bir xil nomlar, boshqa qiymatlar)
3. Login qilganda token avtomatik saqlanadi ✅

### First Request

**Mobile API:**
1. Navigate to: `mobile` → `🔐 Auth` → `1. Register Guest`
2. Click "Send"
3. Token saved to `access_token`

**Admin API:**
1. Navigate to: `admin` → `🔐 Auth` → `1. Admin / Organization Login`
2. Use credentials
3. Token saved to `admin_token`

## 📊 Statistics

| Metrika | Qiymat |
|---------|--------|
| Mobile Requests | 72 |
| Admin Requests | 185 |
| Total Requests | 257 |
| Total YAML Files | 297 |
| Folders | 38 |
| Environments | 2 (Dev + Prod) |

## 🔑 Key Features

✅ Full Mobile API documentation  
✅ Full Admin API documentation  
✅ Bearer token auto-save scripts  
✅ Environment variable templates  
✅ Request/response examples  
✅ Error handling documentation  

## 📖 Documentation

- Full guide: See `/var/www/xba/docs/BRUNO_CONVERSION_SUMMARY.md`
- Usage guide: See `/var/www/xba/docs/BRUNO_USAGE_GUIDE.md`

## 🔄 Version History

- **2026-05-20**: Initial conversion from Insomnia JSON to Bruno YAML format
- **Format**: Bruno 3.3+ OpenCollection YAML
- **Conversion Tool**: Python script (automatic)

## 💡 Tips

1. Use Ctrl+K to search requests quickly
2. Right-click folders to run all requests in bulk
3. Check "Tests" tab after each response
4. Use environment variables for flexible configuration

---

**Last Updated**: 2026-05-20  
**Status**: ✅ Ready to use
