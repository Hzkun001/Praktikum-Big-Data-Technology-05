# Praktikum Big Data Technology #05

Proyek ini adalah implementasi pipeline data streaming transportasi menggunakan **PySpark Structured Streaming**. Data trip disimulasikan secara real-time, diproses menjadi metrik analitik, ditampilkan pada dashboard **Streamlit**, dan dilengkapi modul alert untuk monitoring kondisi transportasi.

## Tech Stack

- Python
- PySpark Structured Streaming
- Streamlit

## Struktur Singkat

- `scripts/transportation/` - generator data trip dan job streaming
- `analytics/` - logika analitik transportasi
- `alerts/` - logika alert/monitoring
- `dashboard/` - aplikasi dashboard Streamlit
- `stream_data/` - data trip simulasi
- `data/` - output streaming, checkpoints, dan serving layer

## Quick Start

Jalankan komponen utama berikut (di terminal terpisah):

```bash
python scripts/transportation/trip_generator.py
```

```bash
spark-submit scripts/transportation/streaming_trip_layer.py
```

```bash
streamlit run dashboard/dashboard_transportation.py
```