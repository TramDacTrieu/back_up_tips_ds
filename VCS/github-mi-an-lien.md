# Giới thiệu
> Git là gì?
{.is-info}

## Version Control System – VCS là gì?
![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

VCS là viết tắt của Version Control System là hệ thống kiểm soát các phiên bản phân tán mã nguồn mở. Các VCS sẽ lưu trữ tất cả các file trong toàn bộ dự án và ghi lại toàn bộ lịch sử thay đổi của file. Mỗi sự thay đổi được lưu lại sẽ được và thành một version (phiên bản).

VCS nghĩa là hệ thống giúp lập trình viên có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được nhân bản (clone) từ một kho chứa mã nguồn (repository), mỗi thay đổi vào mã nguồn trên local sẽ có thể ủy thác (commit) rồi đưa lên server nơi đặt kho chứa chính.

Và một máy tính khác nếu họ có quyền truy cập cũng có thể clone lại mã nguồn từ kho chứa hoặc clone lại một tập hợp các thay đổi mới nhất trên máy tính kia.

Lập trình viên có thể xem lại danh sách các sự thay đổi của file như xem một dòng thời gian của các phiên bản. Mỗi phiên bản bao gồm: nội dung file bị thay đổi, ngày giờ sửa đổi, người thay đổi là ai, lý do thay đổi hay tên phiên bản…

## VCS có tác dụng như thế nào?
1. Lưu lại lịch sử các version của bất kỳ thay đổi nào của dự án. Giúp xem lại các sự thay đổi hoặc khôi phục (revert) lại sau này.
2. Việc chia sẻ code trở nên dễ dàng hơn, lập trình viên có thể để public cho bất kỳ ai, hoặc private chỉ cho một số người có thẩm quyền có thể truy cập và lấy code về.
Vốn là một VCS nên Git cũng ghi nhớ lại toàn bộ lịch sử thay đổi của source code trong dự án. Lập trình sửa file, thêm dòng code tại đâu, xóa dòng code ở hàng nào…đều được Git ghi nhận và lưu trữ lại.

## Git có lợi ích gì?
1. Các dự án thực tế thường có nhiều lập trình viên làm việc song song. Vì vậy, một hệ thống kiểm soát phiên bản như Git là cần thiết để đảm bảo không có xung đột code giữa các lập trình viên.

2. Ngoài ra, các yêu cầu trong các dự án như vậy thay đổi thường xuyên. Vì vậy, một hệ thống kiểm soát phiên bản cho phép các nhà phát triển revert và quay lại phiên bản cũ hơn của code.

3. Cuối cùng, đôi khi một số dự án đang được chạy song song liên quan đến cùng một cơ sở code. Trong trường hợp như vậy, khái niệm phân nhánh trong Git là rất quan trọng.

- Dễ sử dụng, thao tác nhanh, gọn, lẹ và rất an toàn.
- Sễ dàng kết hợp các phân nhánh (branch), có thể giúp quy trình làm việc code theo nhóm đơn giản hơn rất nhiều.
- Chỉ cần clone mã nguồn từ kho chứa hoặc clone một phiên bản thay đổi nào đó từ kho chứa, hoặc một nhánh nào đó từ kho chứa là bạn có thể làm việc ở mọi lúc mọi nơi.
- Deployment sản phẩm của bạn một cách không thể nào dễ dàng hơn.

## Các thuật ngữ Git quan trọng
1. Branch
Các Branch (nhánh) đại diện cho các phiên bản cụ thể của một kho lưu trữ tách ra từ project chính của bạn.
Branch cho phép bạn theo dõi các thay đổi thử nghiệm bạn thực hiện đối với kho lưu trữ và có thể hoàn nguyên về các phiên bản cũ hơn.

2. Commit
Một commit đại diện cho một thời điểm cụ thể trong lịch sử dự án của bạn. Sử dụng lệnh commit kết hợp với lệnh git add để cho git biết những thay đổi bạn muốn lưu vào local repository.

3. Checkout
Sử dụng lệnh git checkout để chuyển giữa các branch. Chỉ cần nhập git checkout theo sau là tên của branch bạn muốn chuyển đến hoặc nhập git checkout master để trở về branch chính (master branch).

14. Remote
Một Remote (kho lưu trữ từ xa) là một bản sao của một chi nhánh. Remote giao tiếp ngược dòng với nhánh gốc (origin branch) của chúng và các Remote khác trong kho lưu trữ.

15. Repository
Kho lưu trữ Git chứa tất cả các tệp dự án của bạn bao gồm các branch, tags và commit.

12. Push
	Lệnh git push được sử dụng để cập nhật các nhánh từ xa với những thay đổi mới nhất mà bạn đã commit.
13. Pull 
Pull requests thể hiện các đề xuất thay đổi cho nhánh chính. Nếu bạn làm việc với một nhóm, bạn có thể tạo các pull request để yêu cầu người bảo trì kho lưu trữ xem xét các thay đổi và hợp nhất chúng.
Lệnh git pull được sử dụng để thêm các thay đổi vào nhánh chính.

## Một vòng đời git cơ bản mà mình thường dùng

1. Chưa có repository hoặc là repository trống

Init >> Remote >> Change some file >> Add >> Commit >> Push

2. Đã có repository và đã có data

Clone >> Remote >> Change some file >> Add >> Commit >> Push

2. Ngoài ra nếu bạn làm việc nhiều với team thì phải có update nữa

> Cực kỳ lưu ý là commit không đồng nghĩa với việc thay đổi của bạn đã được đưa lên repo liền đâu, phải thực hiện push thì thay đổi của bạn mới đc update
{.is-danger}


# Cài đặt
## Link

Dưới đây là link trang chủ của git

> https://git-scm.com/
> {.is-success}

bạn tải file này về rồi cài đặt, còn lại cứ next hết rồi finish là OK (～￣(OO)￣)ブ

## Giới thiệu git desktop

Đây là một phiên bản git dùng giao diện hẳn hoi

> https://desktop.github.com/
> {.is-success}

Lưu ý mình không recomemer sử dụng phiên bản này vì có thể khiến bạn bối rối nếu chuyển sang các hệ thống phải dùng cmd hoặc terminal của linux thì rất khó để sử dụng được thành thạo

# Tới Thôi

## 1. config
để làm việc với đầy đủ thông tin cũng như để git có thể chạy trơn tru thì bạn sau khi cài đặt xong bạn nên config lại git của mình

Ở bài này sẽ hướng dẫn trên windows (trên linux cũng tương tự à ╰（‵□′）╯)

> bật cmd lên (nhấn windows rồi nhấn cmd enter hoặc là Windows + R để mở hộp thoại run rồi nhấn cmd enter)
{.is-info}

gõ vào cái này rồi nhấn enter

`git config -- global user.name`
- để config user name

gõ vào cái này rồi nhấn enter

`git config -- global user.email`
- để config email

## 2. Init

Tác dụng : Khởi tạo 1 git repository 1 project mới hoặc đã có.
- khi dùng lệnh này sẽ tạo ra cho bạn 1 thư mục có dạng `.git`

Cách xài: `git init` trong thư mục gốc của dự án.

1. khi chưa có thư mục

để tạo mới hoàn toàn 1 thư mục thì bạn dùng lệnh

`mkdir direxample`

- di chuyển đến thư mục đó

`cd direxample`

- rồi dùng lệnh

`git init`


2. Khi đã có thư mục rồi

Bạn di chuyển vào thư mục đó bằng lệnh
`cd C:/trieu/direxample`
Rồi sao đó bạn dùng lệnh `git init`

## Git remote

Tác dụng: Để check remote/source bạn có hoặc add thêm remote

Cách dùng: git remote để kiểm tra và liệt kê. Và git remote add <: remote_url:> để thêm.

> Url này lấy từ đâu?
{.is-warning}

Khi bạn tạo ra 1 repository trên trang chủ hoặc từ 1 git đã có sẵn thì bạn luôn được cấp cho 1 URL cụ thể để có thể thao tác 

Ví dụ: `https://github.com/TramDacTrieu/AndroidAppResearch.git`

> Để có thể thực hiện cái thao tác commit, push, update thì bạn cần remote tới 1 repo
{.is-info}

## Git clone

Tác dụng: Copy 1 git repository từ remote source.

Cách xài: `git clone <clone git url>`

Khi dùng lệnh clone này thì bạn sẽ clone ra 1 souce code về máy dựa trên souce code đã có trên git

## Git status

Tác dụng: Để check trạng thái của những file bạn đã thay đổi trong thư mục làm việc. VD: Tất cả các thay đổi cuối cùng từ lần commit cuối cùng.

Cách xài: `git status` trong thư mục làm việc.

## Git add
Tác dụng: Thêm thay đổi đến stage/index trong thư mục làm việc.

Cách xài: `git add <file name>`

Thêm cái thay đổi để có thể commit được
Với cú pháp trên thì bạn có thể add từng file một

> Add từng file thì lâu quá, có cách nào để tôi add 1 lần hết luôn không ?
{.is-warning}

Có, bạn chỉ cần gõ lệnh

`git add .`

Dấu chấm có nghĩa là sẽ add tất cả

## Git commit

Tác dụng: commit nghĩa là một action để Git lưu lại một snapshot của các sự thay đổi trong thư mục làm việc. Và các tập tin, thư mục được thay đổi đã phải nằm trong Staging Area. Mỗi lần commit nó sẽ được lưu lại lịch sử chỉnh sửa của code kèm theo tên và địa chỉ email của người commit. Ngoài ra trong Git bạn cũng có thể khôi phục lại tập tin trong lịch sử commit của nó để chia cho một branch khác, vì vậy bạn sẽ dễ dàng khôi phục lại các thay đổi trước đó.

Cách dùng: git commit -m ”Đây là message, bạn dùng để note những thay đổi để sau này dễ dò lại”

## Git Push/Pull

Tác dụng: Push hoặc Pull các thay đổi đến remote. Nếu bạn đã added và committed các thay đổi và bạn muốn đẩy nó lên hoặc remote của bạn đã update và bạn apply tất cả thay đổi đó trên code của mình.

Cách dùng: 
`git pull <:remote:> <:branch:>`
`git push <:remote:> <:branch:>`

Ví dụ: `git push -f orgin master`

> orgin tức là tên remote của bạn, master tức là branch hiện tại bạn đang dùng nhớ dùng param này thật chính xác nhá, không commit nhầm branch thì hỏng (╯‵□′)╯︵┻━┻
{.is-warning}
