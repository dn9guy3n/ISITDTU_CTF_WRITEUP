![screenshot 70](https://user-images.githubusercontent.com/21336403/43362889-090d392c-9320-11e8-9ef0-2d7668233c57.png)

Mở file bằng IDA thần thánh.

![screenshot 75](https://user-images.githubusercontent.com/21336403/43362950-d8a0c4e6-9321-11e8-8651-a5ca132b6a39.png)

Chuỗi nhập vào được lưu tại địa chỉ 0x602100. Độ dài là 28 ký tự. Sau đó, so sánh lần lượt mỗi 4 ký tự trong 12 ký tự đầu với 3 mã băm md5:
    ECFD4245812B86AB2A878CA8CB1200F9    ==>   'fl4g'
    88E3E2EDB64D39698A2CC0A08588B5FD    ==>   '_i5_'
    BBC86F9D0B90B9B08D1256B4EF76354B    ==>   'h3r3'

![screenshot 76](https://user-images.githubusercontent.com/21336403/43362954-e4513a82-9321-11e8-82e8-3810b60b1a6d.png)

Ký tự 13 có giá trị 33 ('!').
Các ký tự còn lại được xor với tất cả ký tự trước nó và lưu giá trị tại 0x6020A8
Chạy script python getFlagCool.py để được flag hoàn chỉnh:

FLAG: ISITDTU{fl4g_i5_h3r3!C0ngr4tul4ti0n!}
