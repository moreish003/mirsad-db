# Mirsad database / قاعدة بيانات مرصاد

Known stalkerware and commercial monitoring apps, used by the Mirsad Android app to detect spyware. The app downloads `stalkerware_ioc.json` and accepts it only if `stalkerware_ioc.json.sig` is a valid signature from the Mirsad key and the file is newer than the one it already has.

قائمة برامج التجسس وتطبيقات المراقبة المعروفة التي يستخدمها تطبيق مرصاد. التطبيق لا يقبل الملف إلا إذا كان توقيعه صحيحًا وكان أحدث من النسخة الموجودة عنده.

## Files

| File | Purpose |
|---|---|
| `stalkerware_ioc.json` | Package names and signing-certificate SHA-1 fingerprints per spyware family |
| `stalkerware_ioc.json.sig` | ECDSA P-256 / SHA-256 signature (DER) of the JSON file |

Public key (X.509, base64):

```
MFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAEn7tIamHpINFhIf5UIqi3Mkqp9hxVeW9D83nk/Q+HCHZsU/ieFhTROEg38n5iBJFR+oYeEWeXc+9367XT6vPpuQ==
```

## Source and license

Data comes from [stalkerware-indicators](https://github.com/AssoEchap/stalkerware-indicators) by Echap, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

Changes from the original: converted to a compact JSON format, and the public AOSP test-key certificate (`61ED377E85D386A8DFEE6B864BD85B0BFAA5AF81`) was removed because legitimate system components on some phones are signed with it.

This repository is not affiliated with or endorsed by Echap.
