# Barcode Scanner Website

A mobile-friendly, single-page barcode scanner with:

- Front-facing camera access via `getUserMedia()`
- Native browser barcode detection via `BarcodeDetector`
- Scan history with barcode value, detected format, and timestamp
- Persistent storage in `localStorage`
- JSON export/download
- Manual barcode entry fallback

## Run it

For camera access, serve the folder from `localhost` or an HTTPS site. For example:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000` on the device/browser.

## Notes

Native barcode detection support varies by browser. Browsers without `BarcodeDetector` can still use the manual entry field, but camera scanning will not work without a compatible API or a third-party scanning library.

This version reads the information encoded in the barcode itself (the raw barcode value and format). It does not query an external product catalog.
