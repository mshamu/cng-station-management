GREEN GAS CNG — SALES MANAGEMENT APP (Installable PWA)
======================================================

Sign in by ROLE; each role sees only its own screens.

ATTENDANT
  - Start shift: name, shift, shift DATE and START TIME.
  - Record refills: scan/enter plate -> vehicle type auto-classified
    (MC = Three-Wheeler, T = Four-Wheeler), enter CNG kg (0.5-25),
    choose payment (Cash or a mobile provider: Mixx by Yas, Airtel Money,
    Selcom, M-Pesa, HaloPesa, T-Pesa).
  - No-permit vehicles: tap "No Valid Permit - Not Refilled" -> records
    0.00 kg with a reason (kept for audit, excluded from sales).
  - My-shift counters: sales, CNG, 3-Wheeler / 4-Wheeler (transactions +
    unique), cash/mobile, no-permit. Export my shift to CSV.

STATION MANAGER (Erick Hussein Mshamu, demo PIN 1234)
  - Sees ALL attendants' transactions.
  - KPIs: total CNG, sales, transactions, 3W/4W, unique vehicles, denied.
  - Filters: date, attendant, shift, vehicle type, payment method,
    permit status, plate search.
  - Tables: vehicle-type performance, payment analytics (% of sales),
    sales by attendant, shift monitoring, no-permit drill-down, daily summary.
  - Export Sales Data (respects the current filter) to CSV.

DEMO NOTES
  - Data is in-memory; OCR is simulated; PIN is a demo stand-in.
    The production Power Apps build saves to SharePoint and enforces
    roles via Microsoft Entra. To see the manager reflect new refills on
    ONE device: record as Attendant, sign out, sign in as Manager.

INSTALL
  Host over HTTPS (e.g. drag this folder to https://app.netlify.com/drop),
  open the link on a phone:
    Android/Chrome: tap "Install app".
    iPhone/Safari:  Share -> Add to Home Screen.
  Camera + install require HTTPS (file:// will not work).
