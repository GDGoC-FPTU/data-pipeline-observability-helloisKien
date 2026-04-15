[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574038&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** kienvuduc02@gmail.com
**Name:** Vũ Đức Kiên

---

## Mo ta

Trong bai lab nay, toi da xay dung mot ETL pipeline don gian bao gom cac buoc Extract, Validate, Transform va Load. Du lieu duoc doc tu file JSON, sau do duoc kiem tra de loai bo cac record khong hop le nhu gia <= 0 hoac category bi thieu. Tiep theo, du lieu duoc chuan hoa bang cach tinh gia sau khi giam 10% va format lai category ve dang Title Case. Cuoi cung, du lieu duoc luu vao file CSV.

Ngoai ra, toi da thuc hien stress test bang cach so sanh hieu suat cua agent khi su dung du lieu sach va du lieu rac, tu do thay duoc tac dong cua data quality den ket qua cua AI system.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)

# Tao du lieu rac
python generate_garbage.py 
# Chay agent voi du lieu sach va du lieu rac 
python agent_simulation.py

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Pipeline da xu ly thanh cong 5 records ban dau, trong do 2 records bi loai do gia <= 0 va category rong. Ket qua cuoi cung con lai 3 records hop le duoc luu vao file processed_data.csv.

Trong stress test, agent hoat dong chinh xac voi clean data, tra ve san pham hop ly. Tuy nhien, voi garbage data, agent dua ra ket qua sai do bi anh huong boi du lieu loi nhu outliers, duplicate ID va sai kieu du lieu. Dieu nay chung minh rang chat luong du lieu la yeu to rat quan trong trong cac he thong AI.
