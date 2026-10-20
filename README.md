# SÖZÜM SÖZ · Grup 5
# My Word Is My Bond · Group 5

**Samsung Innovation Campus (SIC) AI, Cohort 18 · Dijital Bağımlılık Capstone, Yeşilay iş birliğiyle**
Eğitmen: Eda Nur Saruhan

[Türkçe](#türkçe) · [English](#english)

---

## Türkçe

SÖZÜM SÖZ, kullanıcının bir uygulamayı açmadan önce kullanım süresine dair kısa bir **söz** vermesini ve sistemin bu sözün tutulma olasılığını geçmiş davranıştan **öğrenerek tahmin etmesini** esas alan yapay zekâ destekli bir özdenetim uygulamasıdır. Sistem, kullanıcıya ulaşılabilir süreler önerir ve gerektiğinde uygun zamanda hatırlatma sunar. Proje, bu yılın **dijital bağımlılık** teması kapsamında yürütülen 18. dönem bitirme projesidir.

Bu depo, **Literatür, Veri ve Teknoloji İncelemesi** teslimini içerir. Rapor üç bölümden oluşur: **(1) Literatür İncelemesi**, **(2) Veri Araştırması** ve **(3) Teknoloji İncelemesi**.

### Veri kaynağı

Analiz, **LSApp — Large Dataset of Sequential Mobile App Usage** (Aliannejadi et al., 2021) açık veri seti üzerinde yürütülmüştür. Veriler, katılımcıların Android telefonlarındaki uSearch uygulaması aracılığıyla onaylı biçimde toplanmıştır (9 Eylül 2017 – 17 Mayıs 2018). Ham dosya yaklaşık **3,6 milyon** olay kaydı içerir. Veri setinde gerçek söz, hatırlatma yanıtı veya müdahale sonucu bulunmadığından bunlar sonraki kullanıcı çalışmalarıyla değerlendirilecektir.

### Öne çıkan bulgular

| Bulgu | Değer |
|---|---|
| Ham olay kaydı (yaklaşık) | 3,6 milyon |
| Temizlenmiş uygulama-oturumu | 1.096.411 |
| Simüle edilebilen örnek (en az 5 geçmiş oturum) | 1.076.135 |
| Simüle edilen sözlerin tutulma oranı | ~%53,5 |
| LightGBM ROC-AUC (kronolojik test) | **0,881** |
| Lojistik regresyon ROC-AUC | 0,784 |
| LightGBM kalibrasyon (ECE / Brier) | 0,012 / 0,132 |
| Gece (22.00–06.00) kullanım payı | ~%35 (kullanıcı ağırlıklı ~%36) |
| Besleme türü uygulamalarla başlayan oturum payı | ~%30 |
| Görev amaçlı başlayıp beslemeye kayan oturumlar | %21,6 (16.310 oturumun 3.524'ü) |

### Kullanılan teknolojiler

Python ve pandas (veri hazırlama) · lojistik regresyon / scikit-learn (açıklanabilir temel model) · LightGBM (ana tahmin modeli) · sağkalım analizi · hazır büyük dil modeli (haftalık yapay zekâ koçu) · mobil kullanım takibi ve geliştirme araçları. Ayrıntılar ve değerlendirme Bölüm 3'tedir.

---

## English

My Word Is My Bond is an AI-assisted self-control app built around a simple idea: before opening an app, the user makes a short **promise** about how long they intend to use it. The system **learns from past behavior** to predict how likely that promise is to be kept, suggests realistic durations, and offers a timely reminder when needed. The project is the Cohort 18 capstone carried out under this year's **digital addiction** theme.

This repository holds the **Literature, Data and Technology Review**. The report has three parts: **(1) Literature Review**, **(2) Data Research** and **(3) Technology Review**.

### Data source

The analysis runs on the **LSApp — Large Dataset of Sequential Mobile App Usage** open dataset (Aliannejadi et al., 2021). The data were collected with consent through the uSearch app on participants' Android phones (9 September 2017 – 17 May 2018). The raw file contains roughly **3.6 million** event records. Because the dataset has no real promises, reminder responses or intervention outcomes, these will be evaluated in later user studies.

### Key findings

| Finding | Value |
|---|---|
| Raw event records (approximately) | 3.6 million |
| Cleaned app-sessions | 1,096,411 |
| Simulatable samples (at least 5 past sessions) | 1,076,135 |
| Share of simulated promises kept | ~53.5% |
| LightGBM ROC-AUC (chronological test) | **0.881** |
| Logistic regression ROC-AUC | 0.784 |
| LightGBM calibration (ECE / Brier) | 0.012 / 0.132 |
| Night-time (22:00–06:00) usage share | ~35% (user-weighted ~36%) |
| Share of sessions starting in feed-type apps | ~30% |
| Sessions that start on a task app and slide to a feed app | 21.6% (3,524 of 16,310) |

### Technologies

Python and pandas (data preparation) · logistic regression / scikit-learn (interpretable baseline) · LightGBM (main prediction model) · survival analysis · a ready-made large language model (weekly AI coach) · mobile usage tracking and development tools. Details and evaluation are in Part 3.

---

## Deliverables / Teslim dosyaları

| File | Language | Format |
|---|---|---|
| `LiteratureReview_MyWordIsMyBond_Group5.pdf` | English | PDF (43 pages) |
| `LiteratureReview_MyWordIsMyBond_Group5.docx` | English | Word |
| `LiteratürTaramasıSÖZÜMSÖZ_Grup5.pdf` | Türkçe | PDF |
| `LiteratürTaramasıSÖZÜMSÖZ_Grup5.docx` | Türkçe | Word |

The same four files are also available under `deliverables/`.

## Team / Ekip

| Name | GitHub |
|---|---|
| Çağan Erdem Üstündağ | [@Caagan](https://github.com/Caagan) |
| Begüm Somay |[@begumsomay](https://github.com/begumsomay)|

## Repository layout / Depo yapısı

```
SIC_AI_18_Capstone_Group_5/
├── LiteratureReview_MyWordIsMyBond_Group5.docx   English report (Word)
├── LiteratureReview_MyWordIsMyBond_Group5.pdf    English report (PDF)
├── LiteratürTaramasıSÖZÜMSÖZ_Grup5.docx          Türkçe rapor (Word)
├── LiteratürTaramasıSÖZÜMSÖZ_Grup5.pdf           Türkçe rapor (PDF)
└── deliverables/                                 same files / aynı dosyalar
```

## Data and privacy / Veri ve gizlilik

The LSApp data files are **not** in this repository. Only aggregated results are published here, with no participant codes, app package names or exact timestamps. LSApp veri dosyaları bu depoda **yer almaz**; yalnızca toplulaştırılmış sonuçlar paylaşılır. The dataset's repository lists no explicit data licence, so the data are used for coursework analysis only; public access is not treated as permission for redistribution or commercial use.

## Main source / Ana kaynak

Aliannejadi, M., Zamani, H., Crestani, F., & Croft, W. B. (2021). *Context-aware target apps selection and recommendation for enhancing personal mobile assistants.* ACM Transactions on Information Systems, 39(3), Article 29. https://doi.org/10.1145/3447678
