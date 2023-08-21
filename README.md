# docker.html
    1.docker và kubernetes giúp quản lí và triển khai cũng như phát triển các ứng dụng phức tạp

        đây không phải là 1 khóa học lập trình để học hiểu về 1 ngôn ngữ cụ thể
        
        ko yêu cầu các kiến thức về docker-kubernedes từ trước
        
    2. docker là gì ?
        
        docker là 1 công nghệ container(vùng chứa) như là 1 công cụ để tạo và quản lý các vùng chứa
        
        1 vùng chứa trong phát triển phần mềm cơ bản có nghĩa nó là 1 gói mã .Điều quan trọng là các phụ thuộc và công cụ cần thiết để chạy code
      
        các ưu điểm mà cùng 1 vùng chứa với cùng 1 nodeJS code và cùng 1 công cụ nodeJS và cùng thời gian chạy nodeJS cùng 1 
        version lẽ luôn luôn cung cấp cho mình cùng 1 hành vi và kết quả
       
        container cũng hoạt động giống như container ( thùng công tê nơ) chứa đồ và vận chuyển
        
        "chứa code và gộp chúng lại và ràng buộc để chạy code và có thể mang đi bất kì đâu"
        
        Docker chỉ là công cụ để xậy dựng các vùng chứa
    
    3.Tại sao lại cần thùng chứa(container) để phát triển phần mềm

        lí do cần các gói ứng dụng được tiêu chuẩn hóa độc lập trong phát triển phần mềm:
        
        trong trường hợp dùng Docker ta sẽ luôn thường có môi trường phát triển và sản xuất khác nhau
        
        khi có cùng 1 môi trường phát triển có trong quá trình sản xuất có thể có giá trị rất nhiều đấy là thứ docker và container có thể giúp
        
        nếu có nhiều dự án thì docker và container sẽ giúp ích rất nhiều
        
        khóa các dự án lại và mọi dự án sẽ đều có vùng chứa riêng của mình
        
    5. container và Docker
        
        máy chủ ảo có operating systeam (windows mac linux) hệ điều hành
        
        hiểu thêm về máy chủ ảo hoạt động ra sao
        
        ưu điểm: cho phép tạo ra các loại môi trường - cấu hình riêng đồng thời có thể chia sẻ và tái tạo lại
        
        nhược điểm: có sự trùng lặp gây lãng phí không gian, hiệu suất có thể kém, thiết lập cấu hình máy ảo phức tạp
        
        D và C dễ dùng hơn
    
    6-8.Docker setup

        hướng dẫn cài đặt docker
        
    11. cần docker engine
        
        docker hub : là 1 service cho phép lưu trữ hình ảnh của mình trên cloud, web
        
        docker compose là 1 công cụ xây dựng dựa trên docker , khiến cho các container phức tạp và các dự án nhiều container được quản lí trở nên dễ dàng hơn
        
    12.  các lệnh
        
        From node:14
        
        WORKIR /app
        
        COPY package.json
        
        Run npm install
        
        COPY ..
        
        expose 3000
        
        CMD [ "node", "app.mjs"]
        
        cài đặt Docker , prettier trong vscode
        
        prettier giúp định dạng code auto về cơ bản để làm sạch code
    
    13. ko  thực sự cần phải biết nodeJS để code , có thể sử dụng nhiều ngôn ngữ khác cho Docker

        Khởi tạo 1 file docker - run comande docker build 
        
    17. tìm hiểu cách sử dụng hình ảnh tùy chỉnh và tạo sẵn

            tìm hiểu xem cách ta có thể tạo, chạy và quản lí các vùng chứa docker
 
    18. sử dụng hình ảnh để tạo nhiều vùng chứa dựa trên hình ảnh đó
 
            hình ảnh trong đó là bản thiết kế, mẫu chứa mã và ứng dụng và vùng chứa, sau đó là ứng dụng chạy
 
    19. docker run node dùng để tạo 1 vùng chứa được gọi là dựa trên hình ảnh
 
            dùng docker PS -a
 
            ps là viết tắt của các quy trình , còn với -a là sẽ hiển thị cho bạn tất cả các quy trình tất các vùng chứa docker đã tạo ra cho cta
 
            dùng docker run -it node kiểm tra phiên bản tương tác
 
            Control +C để thoát khỏi vùng chứa