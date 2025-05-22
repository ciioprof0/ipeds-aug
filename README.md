# IPEDS-Aug

This repository is a skeleton template; functionality and documentation will be added incrementally.

A hexagonal-architecture system for augmenting Integrated Postsecondary Education Data System (IPEDS) tables with web-scraped and NLP-enriched content, powered by DuckDB and full-text/semantic search.

---

## 📖 Overview

**IPEDS-Aug** is a modular data-augmentation framework designed to:

- Ingest core IPEDS tables (HD, IC, IC_CAMPUSES).
- Scrape and integrate unstructured web-text (department pages, job postings, mission statements).
- Store and query tabular and textual data via DuckDB (with FTS & VSS extensions).
- Support port interfaces and adapter-driven implementations for easy swapping of components (e.g., DuckDB ↔ SQLite, HTTP scrapers, vector stores).

---

## 🚀 Getting Started

1. **Clone the repo**
   ```bash
   git clone https://github.com/your-org/ipeds-aug.git
   cd ipeds-aug
````

2. **Install dependencies** (TBD)

   ```bash
   # Example:
   # pip install -r requirements.txt
   ```

3. **Configuration**

   * See `src/config/` for global settings (environment variables, DuckDB file locations).

4. **Run tests** (TBD)

   ```bash
   # pytest
   ```

---

## 📁 Project Structure

```
.ipeds-aug/
├── src/
│   ├── adapters/           # Adapter implementations (e.g., DuckDB, HTTP scrapers)
│   ├── domain/             # Core domain models & port interfaces
│   ├── entrypoints/        # CLI, API or other application entrypoints
│   ├── service_layer/      # Business logic / orchestration
│   ├── config.py           # Global configuration
│   └── __init__.py
├── data/                   # Raw, interim, and processed data files
│   ├── raw/
│   ├── interim/
│   └── processed/
├── docs/                   # Design docs, architecture notes, data dictionaries
├── tests/                  # Unit & integration tests
├── Makefile                # Common tasks (lint, test, build)
├── requirements.txt        # Python dependencies
├── requirements_dev.txt    # Dev & testing dependencies
└── README.md               # This file
```

---

## 🎯 Roadmap

* [ ] Define domain models & port interfaces
* [ ] Implement DuckDB adapter & data ingestion pipeline
* [ ] Build web-scraping service adapter
* [ ] Add full-text and semantic search capabilities
* [ ] Create CLI & API entrypoints
* [ ] Develop testing suite & CI/CD workflows

---

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request:

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add some feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License

This project is released under the [MIT License](LICENSE).

---

## 📬 Contact

Project Link: [https://github.com/your-org/ipeds-aug](https://github.com/your-org/ipeds-aug)
