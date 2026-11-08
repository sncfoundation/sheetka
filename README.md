<p align="center">
  <img src="https://sncfoundation.github.io/logos/sheetka.svg" width="96" alt="Sheetka logo">
</p>

<h1 align="center">Sheetka</h1>

<p align="center"><b>A log-structured streaming broker on an append-only tab.</b><br>
A <a href="https://sncfoundation.github.io">Sheet-Native Computing Foundation</a> project · the spreadsheet-native <b>Kafka / NATS</b></p>

---

**Status:** 📝 Unsaved Draft &#183; **design only**. Data & Storage TAG. This repository holds the design below and no code, no release, no reconcile loop. Implementation is tracked in [sncfoundation/sheeternetes#50](https://github.com/sncfoundation/sheeternetes/issues/50). Until then the Sheet is merely a spreadsheet, which we admit is embarrassing.

## The mapping

- **topic** = a sheet; **partition** = an append-only tab (or a column); ordering = row order.
- **producer** appends rows; **consumer** polls from a stored **offset**; **consumer group** = an offsets tab; **retention** = trim old rows.

## Honest limit

Throughput is bounded by the API/trigger rate; no exactly-once. Perfect model, modest speed.

## Connect with real clients

Once [SheetWire](https://github.com/sncfoundation/sheetwire) exists, real Kafka / NATS clients will be able to connect to a Google Sheet over the native wire protocol. Both halves are design-only for now.

- 🗺️ [SNCF Landscape](https://sncfoundation.github.io/landscape.html) · 🧩 [Projects](https://sncfoundation.github.io/projects.html) · 🎓 [Certification](https://sncfoundation.github.io/certification.html)

---

<sub>Apache-2.0. Do not run production data on a spreadsheet. If you do, please film the query plan.</sub>
