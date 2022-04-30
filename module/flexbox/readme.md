<!-- 
    1. Giới thiệu

    - Xây dựng Layout của 1 ứng dụng web thường sử dụng nhất đó là: 
     
        + Grid CSS
        + FlexBox CSS

    - FlexBox CSS sắp xếp và phân phối không gian giữa các khối trong 1 container.
    - FlexBox CSS linh hoạt hơn Grid CSS 
    - FlexBox CSS -> website có bố cục và quy mô nhỏ
    - Grid CSS -> website có bố cục và quy mô lớn
-->


<!-- 
    2. Đặc tính

    - Flex item phải là con trực tiếp Flex container

-->


<!-- 
    3. Sử dụng

    - Khi sử dụng display: flex -> flex-direction: row -> nằm song song với chục main axis
    - Trong layout flex chứa nhiều item mà chỉ có 1 ông có giá trị >= 1 thì chiếm hết khoảng không gian theo trục main axis.
    - Mặc định web sử dụng nowrap => chuyển thành wrap để xuống dòng.  
-->

<!-- 
    4. ND

    - display         : flex        | inline-flex
    - flex-direction  : row         | column
    - flex-wrap       : nowrap      | wrap          | wrap-reverse
    - flex-basic      : <length>
    - justify-content : flex-start  | flex-end      | center        | space-between | space-around
    - justify-self    : flex-start  | flex-end      | center 
    - align-content   : flex-start  | flex-end      | center
    - align-self      : flex-start  | flex-end      | center
    - flex-grow       : <number>
    - flex-shrink     : <number>
    - flex            : <flex-grow> | <flex-shrink> | <flex-basic>
    - flex-flow       : <flex-direction>            | <flex-wrap>
    - order           : <number>

-->