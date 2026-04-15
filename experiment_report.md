# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600338
**Name:** Vũ Đức Kiên
**Date:** 15/4/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent: Based on my data, the best choice is Laptop at $1200. | | |
| Garbage Data (`garbage_data.csv`) | Agent: Based on my data, the best choice is Nuclear Reactor at $999999. | | |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Khi su dung garbage data, agent dua ra ket qua sai chu yeu do chat luong du lieu dau vao khong dam bao. Dau tien, du lieu chua duplicate ID (id = 1 xuat hien 2 lan), co the gay nham lan khi xu ly. Thu hai, truong price co gia tri sai kieu du lieu ("ten dollars") khien viec so sanh hoac tinh toan co the bi loi hoac bi bo qua. Ngoai ra, ton tai gia tri null (id va category bi thieu) lam giam do tin cay cua du lieu. Mot van de quan trong la outlier (Nuclear Reactor voi gia 999999), gia tri nay qua lon so voi cac san pham con lai, khien agent chon no la "tot nhat" du khong hop ly trong thuc te. Tat ca cac van de nay cho thay neu khong validate du lieu truoc, agent se dua ra quyet dinh sai lech.

---

## 3. Ket luan

**Quality Data > Quality Prompt?**

Dong y. Du lieu chat luong cao quan trong hon prompt, vi du la nen tang de agent hoat dong. Neu du lieu sai hoac nhiu, thi du prompt co tot den dau thi ket qua van sai. Trong bai nay, cung mot truy van nhung voi du lieu khac nhau da dan den ket qua hoan toan khac, chung to data quality la yeu to quyet dinh.