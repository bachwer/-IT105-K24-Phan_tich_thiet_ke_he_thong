## Ex 1: Use Case Diagram minh hoạ
Mô tả: Xem trailer và bình luận là các case phụ. Khi user chọn xem chi tiết thì có thể thực hiện thêm các bước này  
→ `<<include>>` thể hiện quan hệ bao hàm.

```mermaid
flowchart TD
    A[👤 User] --> B((Xem chi tiết phim))
    B -.->|<<include>>| C((Xem trailer))
    B -.->|<<include>>| D((Xem bình luận))
