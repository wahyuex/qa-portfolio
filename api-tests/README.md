# RMA DWP Group - API Testing Suite (Postman & Insomnia)

Welcome to the **API Testing & Automation Suite** for the RMA (Return Merchandise Authorization) System at DWP Group. This directory contains production-grade API collections used for integration testing, backend validation, and user acceptance testing (UAT) bridging ERP systems (Odoo) with customer/technician web portals.

---

## 📂 Included Test Artifacts

1. **`RMA.postman_collection.json`**
   - **Type:** Postman Collection (v2.1.0)
   - **Scope:** End-to-end API test suite covering Technician workflows, Customer portal actions, Odoo ERP responses, and digital signatures.
   - **Key Endpoints Covered:**
     - `/api/customer/get-documents` (Document verification & ticket tracking)
     - `/api/endpoint/ttd-surat` (Manager & Technician Digital Signature / Approval workflows)
     - `/api/endpoint/upload-images-evidence-do` (Delivery Order evidence attachment handling via multipart/form-data)
     - Sparepart management & repair history tracking.

2. **`Insomnia_API_Suite.yaml`**
   - **Type:** Insomnia Workspace Export (v4 YAML)
   - **Scope:** Alternative REST client environment containing request environments, auth headers, and trial endpoints (`trialrma-be.dwp.io`) used during staging environments and pre-production sanity tests.

---

## 🔍 Key Highlights & QA Testing Approach

- **ERP Integration Testing:** Validates seamless payload synchronization between custom web APIs and Odoo backend (`odoo_rma_ticket_id`).
- **Authorization & Security Validation:** Tests Bearer token authentication guardrails, role-based access control (Technician vs. Customer vs. Manager), and request parameter tampering.
- **File Upload & Multipart Handling:** Validates robust handling of image evidence uploads (`Upload evi DO`) with size and extension constraints.
- **Environment Agnostic:** Includes local development (`https://localhost:443`), staging trials (`https://trialrma-be.dwp.io`), and tunneling environments (`ngrok`).

---

## 🚀 How to Import and Execute

### In Postman:
1. Open Postman.
2. Click **Import** in the top left corner.
3. Drag and drop `RMA.postman_collection.json`.
4. Select your environment and execute requests individually or run the full collection via **Collection Runner**.

### In Insomnia:
1. Open Insomnia.
2. Go to **Application -> Preferences -> Data -> Import Data**.
3. Select `Insomnia_API_Suite.yaml` from this folder.
4. Explore environments and execute automated requests.
