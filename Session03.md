## Ex 1: Use Case Diagram minh hoạ
Mô tả:  Xem trailer vs bình luộn là case phụ, Khi user chọn xem chi tiết thì có thể thực hiện thêm các bước này
  - << include >> Quan hệ bao hàm, chỉ ra rằng Use Case chính gọi đến phụ

```mermaid
flowchart TD
    A[ User] --> B((Xem chi tiết phim))
    B -.->|<<include>>| C((Xem trailer))
    B -.->|<<include>>| D((Xem bình luận))
