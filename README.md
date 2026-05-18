# Yapay Zeka Kişi Sayaç Sistemi

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/YOLOv8-FF6B35?style=for-the-badge&logo=ultralytics&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Durum-Canlıda-brightgreen?style=flat-square" />
  <img src="https://img.shields.io/badge/Tür-Özel%20Kurumsal%20Yazılım-blue?style=flat-square" />
</p>

---

> Bu proje bir otomotiv bayilik grubu için özel kurumsal yazılım olarak geliştirilmiştir.
> Bu repo yalnızca proje yapısını ve dokümantasyonu **portfolyo amaçlı** paylaşmaktadır. Kaynak kod dahil edilmemiştir.

---

## Genel Bakış

Yemekhane kamerasından alınan **canlı RTSP görüntüsünü** özel eğitilmiş YOLOv8 modeliyle anlık analiz eden kişi sayma sistemi. Kaç tepsi/kişi geçtiğini otomatik sayar, günlük ve saatlik istatistikleri kaydederek öğle/akşam vardiyası bazında yemek yoğunluğunu raporlar.

---

## Teknoloji Yığını

```
Yapay Zeka   → YOLOv8 (özel eğitilmiş model)
Görüntü İşl. → OpenCV · Python
GPU Desteği  → CUDA (NVIDIA)
Backend      → FastAPI · Python
Veri Akışı   → RTSP kamera stream
```

---

## Mimari

```
cafeteria_counter/
├── app.py                 # Ana uygulama ve API
├── capture_frame.py       # RTSP stream yakalama
├── check_cv_build.py      # OpenCV/CUDA yapılandırma doğrulama
├── check_gpu.py           # GPU erişilebilirlik testi
├── check_rtsp_header.py   # Stream bağlantı testi
├── check_stream.py        # Canlı stream izleme
└── custom_model/          # Özel eğitilmiş YOLOv8 modeli
    ├── custom_dataset/
    ├── custom_dataset_v8/
    └── custom_dataset_v9/
```

---

## Temel Özellikler

- Canlı RTSP kamera görüntüsünden gerçek zamanlı kişi tespiti
- GPU hızlandırmalı çıkarım (NVIDIA CUDA)
- Özel dataset ile eğitilmiş model — yemekhane ortamına özgü
- Öğle / akşam vardiyası bazında otomatik istatistik ayrımı
- Günlük ve saatlik yoğunluk raporlama
- Stream bağlantı ve GPU sağlık kontrol araçları

