# Introduction
This project examines the distributed mechanisms of Apache HBase, a NoSQL database built on Hadoop for managing massive datasets. It explores HBase's architecture, detailing components like the HMaster, HRegionServer, HRegions, and Zookeeper, highlighting their roles in data storage and cluster management. The paper analyzes HBase's master-slave architecture, where clients interact directly with Region Servers for efficient data read/write operations. A practical experiment showcasing data distribution across multiple nodes demonstrates HBase's ability to handle large-scale data and its effectiveness in real-world applications.

# Problem description
The experiment simulates a distributed database system for managing a chain of electronics stores called TechnoShop. With three branches located in Ho Chi Minh City, Khanh Hoa, and Hanoi, TechnoShop requires efficient data management across its geographically dispersed locations. The system handles functionalities like user logins, inventory management, customer and employee records, sales processing, and revenue reporting. Distributing the database across multiple nodes is crucial for this scenario. It enhances performance and scalability by allowing data to be stored and processed closer to its point of use, optimizes data access, and increases fault tolerance by replicating data across multiple locations. This approach ensures efficient data handling, improved responsiveness, and greater system resilience for TechnoShop's distributed operations.

# Data description
## Database: TechnoShop

### CUAHANG (MaCH, TenCH, SDT, DiaDiem, ChiNhanh)
- **Definition**: Each store has a store code (MaCH) used to distinguish it from others. Additionally, it records the store name (TenCH), store phone number (SDT), store location (DiaDiem), and branch (ChiNhanh). The store code, store name, and phone number are unique.
  
### KHACHHANG (MaKH, TenKH, DiaChi, GT, SDT, DiemTichLuy)
- **Definition**: Each customer has a customer code (MaKH) to distinguish them from others. It also includes the customer name (TenKH), delivery address (DiaChi), gender (GT), phone number (SDT), and loyalty points based on purchase history (DiemTichLuy).

### NHANVIEN (MaNV, TenNV, NgSinh, NgayVL, SDT, GioiTinh)
- **Definition**: Each employee has an employee code (MaNV) to distinguish them from others. It also records the employee name (TenNV), date of birth (NgSinh), date of joining (NgayVL), contact phone number (SDT), and gender (GioiTinh).

### SANPHAM (MaSP, TenSP, LoaiSP, Gia, ThuongHieu)
- **Definition**: Each product has a unique product code (MaSP). It also includes the product name (TenSP), product category (LoaiSP), price (Gia), and brand (ThuongHieu).

### HOADON (MaHD, MaKH, MaCH, MaNV, NgayHD, ThanhTien)
- **Definition**: Each invoice has a unique invoice code (MaHD). It also records the invoice date (NgayHD), customer code (MaKH), store code (MaCH), employee code (MaNV), and total amount (ThanhTien).

### CTHD (SoHD, MaSP, SoLuong)
- **Definition**: The invoice details table stores information about the products and quantities in the invoice. This includes the invoice number (SoHD), product code (MaSP), and quantity purchased (SoLuong).

### Sample Data in Tables

# Architechture
![image](https://github.com/user-attachments/assets/dca1c911-77bd-4bb4-91b2-9b657820e4cb)


# Link videmo demo
https://drive.google.com/file/d/1dx-i1OGQgrPVRDVOEg0CVHPXRqKVRz4I/view?usp=drive_link
