# Introduction
This project examines the distributed mechanisms of Apache HBase, a NoSQL database built on Hadoop for managing massive datasets. It explores HBase's architecture, detailing components like the HMaster, HRegionServer, HRegions, and Zookeeper, highlighting their roles in data storage and cluster management. The paper analyzes HBase's master-slave architecture, where clients interact directly with Region Servers for efficient data read/write operations. A practical experiment showcasing data distribution across multiple nodes demonstrates HBase's ability to handle large-scale data and its effectiveness in real-world applications.

# Problem description
The experiment simulates a distributed database system for managing a chain of electronics stores called TechnoShop. With three branches located in Ho Chi Minh City, Khanh Hoa, and Hanoi, TechnoShop requires efficient data management across its geographically dispersed locations. The system handles functionalities like user logins, inventory management, customer and employee records, sales processing, and revenue reporting. Distributing the database across multiple nodes is crucial for this scenario. It enhances performance and scalability by allowing data to be stored and processed closer to its point of use, optimizes data access, and increases fault tolerance by replicating data across multiple locations. This approach ensures efficient data handling, improved responsiveness, and greater system resilience for TechnoShop's distributed operations.

# Data description
Database TechnoShop
CUAHANG (MaCH, TenCH, SDT, DiaDiem, ChiNhanh)
Tân từ: Mỗi cửa hàng có mã cửa hàng (MaCH) dùng để phân biệt các cửa hàng với nhau, ngoài ra còn lưu tên cửa hàng (TenCH), số điện thoại của cửa hàng đó (SDT), địa điểm cửa hàng(DiaDiem), chi nhánh cửa hàng hoạt động (ChiNhanh). Trường mã cửa hàng, tên cửa hàng, số điện thoại là duy nhất.
KHACHHANG (MaKH, TenKH, DiaChi, GT, SDT, DiemTichLuy)
Tân từ: Mỗi khách hàng có mã khách hàng (MaKH) dùng để phân biệt với các khách hàng khác, ngoài ra còn có lưu tên khách hàng (TenKH), địa chỉ để giao hàng (DiaChi), giới tính của khách hàng (GioiTinh), số điện thoại (SDT) và số điểm tích lũy dựa vào số lần mua hàng (DiemTichLuy).
NHANVIEN (MaNV, TenNV, NgSinh, NgayVL, SDT, GioiTinh)
Tân từ: Mỗi nhân viên có mã nhân viên (MaNV) để phân biệt với các nhân viên khác. Ngoài ra còn có lưu tên nhân viên (TenNV), ngày sinh (NgaySinh), ngày vào làm (NgayVL), số điện thoại liên lạc (DienThoai) và giới tính của nhân viên (GioiTinh).
SANPHAM (MaSP, TenSP, LoaiSP, Gia, ThuongHieu)
Tân từ: Mỗi sản phẩm có mã sản phẩm (MaSP) là duy nhất, ngoài ra còn có lưu tên sản phẩm, tên loại sản phẩm (LoaiSP), giá tiền (Gia) và thương hiệu của sản phẩm đó (ThuongHieu).
HOADON (MaHD, MaKH, MaCH, MaNV, NgayHD, ThanhTien)
Tân từ:  Mỗi hóa đơn sẽ có một mã hóa đơn (MaHD) là duy nhất, ngoài ra còn lưu thông tin ngày lập hóa đơn (NgayHD), mã khách hàng mua sản phẩm (MaKH), mã cửa hàng nơi sản phẩm được bán (MaCH), mã nhân viên lập hóa đơn (MaNV) và tổng thành tiền của hóa đơn đó (ThanhTien). 
CTHD (SoHD, MaSP, SoLuong)
Tân từ: Chi tiết hóa đơn lưu giữ thông tin sản phẩm và số lượng mà hóa đơn sở hữu nó có. Thông tin bao gồm số hóa đơn (SoHD), mã sản phẩm (MaSP), số lượng sản phẩm được mua (SoLuong).
Dữ liệu mẫu ở các bảng
# Architechture
![image](https://github.com/user-attachments/assets/dca1c911-77bd-4bb4-91b2-9b657820e4cb)


# Link videmo demo
https://drive.google.com/file/d/1dx-i1OGQgrPVRDVOEg0CVHPXRqKVRz4I/view?usp=drive_link
