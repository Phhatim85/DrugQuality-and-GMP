# جودة الدواء — Vercel Deployment Guide

## المشروع
موقع جودة الدواء والممارسات الجيدة في الصناعات الدوائية مع PDF generation API.

## البنية
```
jawdat-aldawa/
├── public/
│   └── index.html          ← الموقع الرئيسي
├── api/
│   └── pdf.js              ← Puppeteer PDF API
├── package.json
├── vercel.json
└── README.md
```

## خطوات الرفع على Vercel

### 1. تثبيت Vercel CLI
```bash
npm install -g vercel
```

### 2. رفع المشروع
```bash
cd jawdat-aldawa
vercel
```

### 3. أو عبر GitHub
1. ارفع المجلد على GitHub
2. اربطه بـ Vercel من vercel.com
3. Vercel سيكتشف الإعدادات تلقائياً

## كيف يعمل الـ PDF API
- الزر يرسل HTML → `/api/pdf`
- Puppeteer يحوله لـ PDF حقيقي
- يتحمل مباشرة على جهاز المستخدم

## الذاكرة المطلوبة
- API function: 1024 MB (مُعيَّن في vercel.json)
- مدة التنفيذ: 30 ثانية كحد أقصى
