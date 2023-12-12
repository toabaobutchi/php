# Ôn tập

* Tên lớp và hàm/phương thức không phân biệt chữ hoa - thường

```php
$a = new A(); // OK
$a = new a(); // OK

$a->f(); // OK
$a->F(); // OK
```

* Tên biến, khoá trong mảng, tên tham số trên Query string có phân biệt chữ hoa - thường

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

