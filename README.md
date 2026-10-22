# ksj-p11-bus-stop-greater-tokyo

Reproducible collection of the bus stops (国土数値情報 P11, 2022 edition) of Saitama, Chiba, Tokyo
and Kanagawa. The dataset card is generated into `data/README.md` (not tracked; the data is
published at https://huggingface.co/datasets/yuiseki/ksj-p11-bus-stop-greater-tokyo).

```
uv run python scripts/01_download.py      # 4 zips + the data page, terms, code list (data/raw/<date>, data/docs)
uv run python scripts/02_export_parquet.py
uv run python scripts/03_verify.py        # Parquet vs the .shp/.dbf of the zips
uv run python scripts/04_card.py
uv run python src/publish.py [--push]     # dry run by default
```

Code: MIT. Data: CC BY 4.0, see the card.
