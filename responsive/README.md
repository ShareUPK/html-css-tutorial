- Responsive là gì ?
    + Responsive là kỹ thuật giúp website hiển thị tương thích với nhiều kích thước màn hình khác nhau ( Mobie, Tablet, PC, ... )
    + Tối ưu trải nghiệm người dùng:
        ` Hiển thị rõ ràng các thành phần ( hình ảnh, cỡ chữ, nút bấm, ... )
        ` Ẩn / hiện các thành phần phù hợp theo kích thước màn hình

- Chúng ta sẽ làm gì ?
    + Dùng CSS thay đổi kích thước phù hợp cho các thành phần hiển thi trên website ( hình ảnh, cỡ chữ, nút bấm, ... )
    + Dùng CSS để ẩn / hiển các thành phần phù hợp theo kích thước màn hình

- Sử dụng / cài đặt công cụ
    + Chrome development tool
    + Viewport resizer chrome extension

- Khái niệm Viewport
    + Màn hình có thể quan sát được trên thiết bị

- Media query ?
    + @media not | only mediatype and (mediafeature and|or|not mediafeature) {
        CSS-Code;
    }

    ` 1. Keywords:
        ^ not
        ^ only
        ^ and
        ^ or
    
    ` 2. Mediatypes: 
        ^ print
        ^ screen
        ^ speech
        ^ all - default

    ` 3. Media Features:
        ^ min-width
        ^ max-width
        ^ ...
    
    ` 4. Polyfill

    ! Lưu ý:
    - Không cần để only tự hiểu
    - https://cdnjs.com/libraries/respond.js
    - https://stackoverflow.com/questions/41430406/what-is-the-meaning-of-lt-in-if-lt-ie-9

- Breakpoints ?
    + Breakpoints là những điểm / vị trí mà bố cục website sẽ thay đổi - thích ứng để tạo nên giao diện responsive.
    + https://responsivedesign.is/develop/browser-feature-support/media-queries-for-common-device-breakpoints/

    + Mobie: width < 740px
    + Tablet: width >= 740px and width < 1024px
    + PC: width >= 1024px

- Grid System - [P1] ?
    + Xuất hiện từ đầu thế kỷ XX trong phong trào (Constructivism - Thuyết kiến tạo) nghệ thuật / kiến trúc
    + Tạo nên các khung nền, hỗ trợ việc sắp xếp bố cục theo trật tự / thống nhất / cân bằng 
    + Hệ thống lưới thường gặp: 
        ` Lưới nhiều cột (Multicolumn grid)
        ` Lưới một cột (Single column grid)
        ` Lưới module (Modular grid)
        ` Lưới đường cơ sở (Baseline grid)
    + Vai trò: 
        ` Tổ chức: Có các đường căn gióng tiện lợi, dễ dàng sắp xếp các thành phần được ngăn nắp
        ` Cân bằng: Dù là đối xứng / bất đối xứng, mang lại cái nhìn trực quan, đảm bảo sự cân bằng
        ` Tách biệt thành phần: Phân chia nội dung, tạo khoảng cách các thành phần hiệu quả 
    + Ứng dụng: 
        ` Lưới trong thiết kế UI UX: Vai trò đặc biệt quan trọng trong responsive web design
        ` Lưới trong in ấn: Google "Grid System"

    + Responsive web design: 
        ` Grid: Thành phần cha
        ` Row: Dòng
        ` Column: Cột
        ` Gutter: Khoảng cách 2 phía của Column

- Grid System - [P2] ?
    + Thành phần chính (lý thuyết)
        ` Column - Cột
            ~ Độ rộng sử dụng đơn vị % (tương đối) giúp linh động, dễ dàng tương thích với độ rộng khác nhau của các thiết bị.
            Số lượng cột trong grid system được xác định trước. 
            (VD: PC 12|16 cột, tablet 8 cột, mobile 4 cột)
        
        ` Gutter - Đường ngăn cách (rãnh ngăn)
            ~ Là khoảng cách 2 phía của 1 cột, tạo nên rãnh ngăn giữa các cột. Độ rộng rãnh ngăn có thể thay đổi cho phù hợp 
            với thiết kế hoặc độ rộng màn hình
            (VD: PC/Tablet 24px, mobie 16px)
        
        ` Margin - Phần lề 
            ~ Là khoảng cách 2 bên trái/phải của bố cục chính của website. Độ rộng phần lề thay đổi để phù hợp với các kích thước
            màn hình. 
            VD: Phần lề lớn thích hợp cho màn hình lớn như PC, phần lề nhỏ thích hợp cho màn hình nhỏ như Tablet, mobie, ...
    
    + Thành phần chính (làm việc với CSS)
        ` Grid - Lưới (Thường là phần cha, chứa Row và Column)
        ` Row - Dòng (Dòng - chiều ngang, chứa Column)
        ` Column - Cột (Chứa nội dung / thành phần trên website)
        
    + Tạo thư viện CSS ứng dụng Grid System
        ` KN: Một thư viện CSS nho nhỏ kết hợp giữa Grid system + Media queries sẽ giúp chúng ta dễ dàng tạo ra các bố cục website theo cách đơn giản, linh động, tiết kiệm thời gian và tương thích hiển thị trên nhiều thiết bị.

        !Kết quả:
            ` Tự tay xây dựng được thư viện CSS đầu tiên 
            ` Biết cách ứng dụng Grid System vào xây dựng layout 
            ` Hiểu về Grid layout của bootstrap 
    
    + Tạo đối tượng Grid
        ` KN:
            ~ Grid giúp chúng ta chứa nội dung chính và các thành phần của website
            ~ Grid được tạo dựng linh động
            ~ Grid tự thay đổi chiều rộng trên các thiết bị khác nhau

        ` Nguồn gốc
            ~ Chuẩn 1: Với màn hình độ phân giải 1024px - 960px 
            ~ Chuẩn 2: Với màn hình độ phân giải > 1024px - 1200px

        ` Tạo class
            ~ grid: full-width - Chiếm hết chiều ngang đối tượng chứa (cha)
            ~ wide: chiều ngang tối đa 1200px

        ` Đặt lại chiều rộng trên các thiết bị
            @media (min-width: 740px) and (max-width: 1023px) {
                .wide {
                    width: 644px;
                }
            }
    
    + Tạo đối tượng Row
        ` Vai trò
            ~ Chứa các columns, giúp các columns nằm theo chiều ngang
            ~ Khi tổng chiều ngang columns vượt quá kích thước Row, columns xuống hàng
            ~ Loại bỏ khoảng thừa do gutters tạo ra ở 2 phía 
            (Sử dụng margin với giá trị âm sang 2 phía trái/phải để "bù trừ" cho khoảng padding trái/phải của Columns)
        
        ` CSS: 
        @media (min-width: 740px) {
            .row {
                margin-left: -8px;
                margin-right: -8px;
            }
        }

        @media (min-width: 1113px) {
            .row {
                margin-left: -12px;
                margin-right: -12px;
            }
        }

        @media (min-width: 1024px) and (max-width: 1239px) {
            .wide .row {
                margin-left: -12px;
                margin-right: -12px;
            }
        }
    
    + Tạo đối tượng Column
        ` Vai trò: 
            ~ Chứa các thành phần trên website
            ~ Sử dụng padding trái/phải để tạo nên gutters - rãnh ngăn cách giữa các column trong Grid layout
            ~ Luôn luôn là con trực tiếp của Row.
        
        ` Mở rộng: Column được sử dụng với class "col", đi kèm theo đó là một số class "c-*" "m-*" và "l-*":
            ~ c-*: nghĩa là column, prefix class này có tác dụng trên mobile. * từ 0 tới 12. Trong đó 0 được sử dụng để ẩn column, 1 - 12 tương ứng với độ rộng chúng ta muốn sử dụng cho column (trên cơ sở 12 columns trong Grid system)
            ~ m-*: nghĩa là medium, prefix class này có tác dụng trên Tablet.
            ~ l-*: nghĩa là large, prefix class này có tác dụng trên PC.

        ` Một số khái niệm: 
            ~ Column offset: Sắp xếp vị trí của từng column với nhau
        
        !Chú ý:
            ` Nếu thiếu thuộc tính | box-sizing: border-box; | thì các column của bạn có thể không nằm trên một chiều ngang.
    
    + FLEX: 
        !NOTE: 
            ` flex-grow : 1; 
            // Điều này có nghĩa là div sẽ phát triển theo cùng một tỷ lệ với kích thước cửa sổ

            ` flex-shrink : 1; 
            // Điều này có nghĩa là div sẽ thu nhỏ lại theo cùng một tỷ lệ với kích thước cửa sổ 

            ` flex-basis : 0; 
            // Điều này có nghĩa là div không có giá trị bắt đầu như vậy và sẽ chiếm màn hình theo kích thước màn hình có sẵn cho. ví dụ: - nếu 3 div nằm trong wrapper thì mỗi div sẽ chiếm 33%.
    
    + Phím tắt: Ctrl + Shift + L : Bôi đen tất cả phần tử

        
