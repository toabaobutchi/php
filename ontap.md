# Ôn tập

* Tên lớp và hàm/phương thức không phân biệt chữ hoa - thường

```php
$a = new A(); // OK
$a = new a(); // OK

$a->f(); // OK
$a->F(); // OK
```

* Tên biến/hằng, khoá trong mảng, tên tham số trên Query string có phân biệt chữ hoa - thường

```php
$a = 1;
echo $A; // lỗi biến $A không tồn tại

$a = ["a" => 1];
echo $a["A"]; // lỗi, khoá "A" không tồn tại

link: url?x=1&y=2
echo $_GET['X']; // lỗi, khoá "X" không tồn tại
```

* Tham chiếu (tham biến) tạo vùng nhớ ngay trên biến gốc, trong vòng lặp thì không bị huỷ sau khi kết thúc phiên lặp.

```php
$x = 1;
$y = &$x; // y tham chiếu trực tiếp đến x
$y = 2; // thay đổi y cũng là thay đổi x

echo $x; // x = 2
```

* Tên biến không bắt đầu bằng số hoặc là từ khoá như $this, ...

* Hằng số có thể khai báo bằng `define()` hoặc từ khoá `const`.

* `strip_tags(<string>, <exclusive_tags>)`: loại bỏ các thẻ HTML ngoại trừ các thẻ được chỉ định ở chuỗi `<exclusive_tags>`.

* Báo lỗi nếu sử dụng giá trị của `echo`

* Có thể truy xuất ký tự trong chuỗi bằng toán tử index `[]`.

* Có thể chuyển đổi (ép) kiểu từ chuỗi thành mảng.

* Chuỗi chứa số đầu tiên + số => giá trị của chuỗi số + số

* `array_search()`: trả về key tìm được

* `array_combine(keys, values)`: ghép 2 mảng trở thành `keys[i] => values[i]` với `count(keys) == count(values)`

* 
