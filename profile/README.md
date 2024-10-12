# WORDWAVES - Website học tiếng anh trực tuyến

## Giới thiệu

WordWaves là nền tảng học tập trực tuyến cung cấp lộ trình học tập cụ thể. Các bộ từ vựng được chia theo cấp độ để người dùng dễ dàng chọn lựa theo cấp độ của mình. Giao diện dễ sử dụng, tập trung. 

## Tính năng chính

- **Đăng ký và đăng nhập**: Người dùng có thể tạo tài khoản và đăng nhập vào ứng dụng.
- **Học từ vựng**: Người dùng chọn bộ từ vựng và học tập.
- **Báo cáo tiến độ**: Tiến độ học tập của người dùng sẽ được hệ thống lưu lại và hiển thị trên giao diện.
- **Tạo bộ từ vựng**: Người dùng có thể tạo bộ từ vựng và thêm từ vựng và nghĩa để học tập.

## Cài đặt

1. **Clone repository từ GitHub:**
- Clone phần Frontend
   ```sh
  git clone https://github.com/G4-Tomorrow/frontend.git
  ```
- Clone phần Backend
   ```sh
  git clone https://github.com/G4-Tomorrow/frontend.git
   ```

2. **Chuẩn bị các gói cần thiết**
- Chạy lệnh ``npm i`` trong terminal tại thư mục phần frontend để cài đặt các package được khai báo sẵn trong file ``package.json``.
- Chạy lệnh ``mvn clean install`` hoặc ``./mvnw clean install`` nếu chưa cài đặt ``Maven`` trong terminal tại thư mục backend để tự động tải xuống các dependency được khai báo sẵn trong thư mục ``pom.xml``.

3. **Chạy ứng dụng:**
- Chạy lệnh ``npm start`` trong terminal để chạy frontend.
- Nhận nút ``Run`` trong IntelIJ hoặc các IDE khác đã cài đặt sẵn gói Pack của Spring để chạy ứng dụng.

## Sử dụng
1. **Đăng ký và Đăng nhập**
- Người dùng mới có thể tạo tài khoản bằng cách sử dụng tính năng đăng ký.



## Hình ảnh giao diện

<div style="display: flex; justify-content: center; align-items: center; margin: auto; width: 100%;">
 
</div>

## Công nghệ
- Frontend: ``NextJS``, ``TypeScript``, `Tailwind CSS`, `Redux`
- Backend: ``Spring Boot``, ``Spring Cloud``, ``MySQL``, ``Redis``, ``Firebase``
- Containerize: ``Docker``
- Quản lý dự án: ``Git``, ``GitHub``
- CI/CD: ``GitHub Actions``

## Cấu trúc dự án
```bash
C:.
|   .gitignore
|   Dockerfile
|   HELP.md
|   mvnw
|   mvnw.cmd
|   output.txt
|   pom.xml
|   README.md
|   tree.txt
|   
+---.github
|   \---workflows
|           pipeline-backend.yaml
|           
+---.idea
|       .gitignore
|       compiler.xml
|       encodings.xml
|       jarRepositories.xml
|       jpa-buddy.xml
|       misc.xml
|       uiDesigner.xml
|       vcs.xml
|       workspace.xml
|       
+---.mvn
|   \---wrapper
|           maven-wrapper.properties
|           
+---src
|   +---main
|   |   +---java
|   |   |   \---com
|   |   |       \---server
|   |   |           \---wordwaves
|   |   |               |   WordwavesApplication.java
|   |   |               |   
|   |   |               +---config
|   |   |               |       ApplicationInitConfig.java
|   |   |               |       CustomJwtDecoder.java
|   |   |               |       FirebaseConfig.java
|   |   |               |       JwtAuthenticationEntryPoint.java
|   |   |               |       JwtTokenProvider.java
|   |   |               |       PascalCaseNamingStrategy.java
|   |   |               |       RedisConfig.java
|   |   |               |       SecurityConfig.java
|   |   |               |       
|   |   |               +---constant
|   |   |               |       PredefinedRole.java
|   |   |               |       
|   |   |               +---controller
|   |   |               |       AuthenticationController.java
|   |   |               |       FileUploadController.java
|   |   |               |       TopicController.java
|   |   |               |       UserController.java
|   |   |               |       WordCollectionController.java
|   |   |               |       WordController.java
|   |   |               |       
|   |   |               +---dto
|   |   |               |   +---model
|   |   |               |   |   \---mail
|   |   |               |   |           RecipientModel.java
|   |   |               |   |           SenderModel.java
|   |   |               |   |           
|   |   |               |   +---request
|   |   |               |   |   +---auth
|   |   |               |   |   |       AuthenticationRequest.java
|   |   |               |   |   |       IntrospectRequest.java
|   |   |               |   |   |       LogoutRequest.java
|   |   |               |   |   |       RefreshTokenRequest.java
|   |   |               |   |   |       
|   |   |               |   |   +---common
|   |   |               |   |   |       EmailRequest.java
|   |   |               |   |   |       
|   |   |               |   |   +---file
|   |   |               |   |   |       FileUploadRequest.java
|   |   |               |   |   |       
|   |   |               |   |   +---user
|   |   |               |   |   |       ForgotPasswordRequest.java
|   |   |               |   |   |       ResetPasswordRequest.java
|   |   |               |   |   |       UserCreationRequest.java
|   |   |               |   |   |       UserUpdateRequest.java
|   |   |               |   |   |       VerifyEmailRequest.java
|   |   |               |   |   |       
|   |   |               |   |   \---vocabulary
|   |   |               |   |           TopicCreationRequest.java
|   |   |               |   |           WordCollectionCreationRequest.java
|   |   |               |   |           WordCreationRequest.java
|   |   |               |   |           
|   |   |               |   \---response
|   |   |               |       +---auth
|   |   |               |       |       AuthenticationResponse.java
|   |   |               |       |       IntrospectResponse.java
|   |   |               |       |       
|   |   |               |       +---common
|   |   |               |       |       ApiResponse.java
|   |   |               |       |       BaseAuthorResponse.java
|   |   |               |       |       BaseResponse.java
|   |   |               |       |       EmailResponse.java
|   |   |               |       |       Pagination.java
|   |   |               |       |       PaginationInfo.java
|   |   |               |       |       QueryOptions.java
|   |   |               |       |       
|   |   |               |       +---file
|   |   |               |       |       FileUploadResponse.java
|   |   |               |       |       
|   |   |               |       +---user
|   |   |               |       |       UserResponse.java
|   |   |               |       |       
|   |   |               |       \---vocabulary
|   |   |               |               TopicResponse.java
|   |   |               |               TopicsOfWordCollectionResponse.java
|   |   |               |               WordCollectionResponse.java
|   |   |               |               WordResponse.java
|   |   |               |               WordsOfTopicResponse.java
|   |   |               |               WordThumbnailResponse.java
|   |   |               |               
|   |   |               +---entity
|   |   |               |   +---common
|   |   |               |   |       BaseAuthor.java
|   |   |               |   |       BaseEntity.java
|   |   |               |   |       
|   |   |               |   +---user
|   |   |               |   |       Permission.java
|   |   |               |   |       Role.java
|   |   |               |   |       User.java
|   |   |               |   |       
|   |   |               |   \---vocabulary
|   |   |               |           Topic.java
|   |   |               |           Word.java
|   |   |               |           WordCollection.java
|   |   |               |           WordCollectionCategory.java
|   |   |               |           
|   |   |               +---exception
|   |   |               |       AppException.java
|   |   |               |       ErrorCode.java
|   |   |               |       GlobalExceptionHandler.java
|   |   |               |       
|   |   |               +---mapper
|   |   |               |       TopicMapper.java
|   |   |               |       UserMapper.java
|   |   |               |       WordCollectionMapper.java
|   |   |               |       WordMapper.java
|   |   |               |       
|   |   |               +---repository
|   |   |               |   |   PermissionRepository.java
|   |   |               |   |   RoleRepository.java
|   |   |               |   |   TopicRepository.java
|   |   |               |   |   UserRepository.java
|   |   |               |   |   WordCollectionCategoryRepository.java
|   |   |               |   |   WordCollectionRepository.java
|   |   |               |   |   WordRepository.java
|   |   |               |   |   
|   |   |               |   \---httpclient
|   |   |               |           DictionaryClient.java
|   |   |               |           EmailClient.java
|   |   |               |           ImageClient.java
|   |   |               |           
|   |   |               +---service
|   |   |               |   |   AuthenticationService.java
|   |   |               |   |   BaseRedisService.java
|   |   |               |   |   EmailService.java
|   |   |               |   |   FirebaseStorageService.java
|   |   |               |   |   TokenService.java
|   |   |               |   |   TopicService.java
|   |   |               |   |   UserService.java
|   |   |               |   |   WordCollectionService.java
|   |   |               |   |   WordService.java
|   |   |               |   |   
|   |   |               |   \---implement
|   |   |               |           AuthenticationServiceImp.java
|   |   |               |           BaseRedisServiceImp.java
|   |   |               |           EmailServiceImp.java
|   |   |               |           FirebaseStorageServiceImp.java
|   |   |               |           TokenServiceImp.java
|   |   |               |           TopicServiceImp.java
|   |   |               |           UserServiceImp.java
|   |   |               |           WordCollectionServiceImp.java
|   |   |               |           WordServiceImp.java
|   |   |               |           
|   |   |               \---utils
|   |   |                       MyStringUtils.java
|   |   |                       
|   |   \---resources
|   |       |   application-prod.yaml
|   |       |   application.yaml
|   |       |   firebase-credentials.json
|   |       |   
|   |       +---static
|   |       \---templates
|   |               forgot-password-template.html
|   |               register-template.html
|   |               
|   \---test
|       \---java
|           \---com
|               \---server
|                   \---wordwaves
|                           WordwavesApplicationTests.java


```

## Đóng góp
Chúng tôi hoan nghênh các đóng góp từ cộng đồng. Vui lòng fork repository và gửi pull request với các tính năng hoặc cải tiến mà bạn muốn thêm vào.
