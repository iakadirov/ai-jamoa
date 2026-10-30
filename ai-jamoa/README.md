# AI jamoa — Claude plugini

vibecoding.uz «AI xodimlar» praktikumi uchun. Claude bilan 10 daqiqalik tanlovli savol-javob: biznesingizdagi ishlarni
ko'rib chiqadi, qaysi ishni qaysi AI xodim olishini, qanday nazorat bilan va qaysi tartibda joriy qilishni aniqlaydi.
Natija — chatda interaktiv xarita: AI jamoa, har agent qanday ishlaydi, sizdan nima kerak, 0-hafta → 3-oy rejasi va
nusxa olinadigan yo'riqnomalar. Oxirida birinchi AI xodimingizni tayyor skill qilib beradi.

## O'rnatish

1. claude.ai yoki Claude desktop → **Customize → Plugins → Add**
2. **Upload plugin** → `ai-jamoa.zip` (yoki **Add marketplace** → repo manzili)
3. **Settings → Capabilities → Code execution and file creation** — yoqiq bo'lsin

## Ishlatish

Yangi chatda `/` → **diagnostika** (yoki «AI jamoa diagnostikasini boshlaymiz» deb yozing).
Diagnostikadan keyin: `/` → **ai-xodim** — birinchi AI xodimingiz skill paketi.

## Qanday ishlaydi

- Savollar va variantlar — `skills/diagnostika/references/malumot.json` (9 soha, 60 ish, 10 rol).
- Daraja (L0–L4), soat, jamoa va reja — `scripts/hisob.py` qoidalari bilan hisoblanadi, model o'zgartirmaydi.
  Pul, qaror va telefon — L1 dan yuqori emas; ommaga chiqadigan — L2 dan yuqori emas.
- Model faqat savol beradi, javoblarni yig'adi va shaxsiy izoh yozadi.
- AI xodim odamni almashtirmaydi — vaqtini bo'shatadi; nazorat odamda qoladi.
