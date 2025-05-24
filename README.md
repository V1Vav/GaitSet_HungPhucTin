Clone từ github GaitSet gốc https://github.com/AbnerHqC/GaitSet


Có thể tự xử lý dữ liệu hoặc lấy dữ liệu đã xử lý của nhóm (resize 64x64) ở 

https://drive.google.com/file/d/1gaoHgTzDqA5eFWdsXG4vYE52zf6uYOEx/view?usp=sharing
#1. train, test (model gốc)     
Cần sửa trong file config


dẫn work_path, dataset_path, lưu ý restore_inter rất hữu dụng khi train bằng colab (lưu 2 file encoder và optimizer để dùng).


Vì repo cũng khá lâu nên các file triplet.py và dataloader.py cần phải chỉnh sửa đôi chút, Nhóm đã up triplet.py và dataloader.py mới, copy và sử dụng như bình thường ( quan tâm thay đổi thì kép xuống dưới cũng mỗi file, nhóm note lại những thay đổi).


#2.max, mean, median,fuse


Sau khi clone github, trong file gaitset.py thì class SetNet có sẵn max, median. Nhóm tự định nghĩa thêm def mean và def fuse.


Muốn thay đổi giữa def max,mean,...  thay đổi file model.py bằng file Max_Mean_Median_Fuse. Sau đó thay đổi tên hàm khi cần dùng. (vd gl = self.gl_layer3(gl + self.frame_max(x)[0]) -> gl = self.gl_layer3(gl + self.frame_median(x)[0]) )


#3 Trích xuất feature từ video có sẵn. 

linkdrive: https://drive.google.com/file/d/1WlEYUL0DpazD-DWFVzTvZUttEcjBFc3_/view

#4. Đưa các file notebook vào thư mục model vào main, folder 125 đưa vào thư mục chứa data đã xử lý.

Nhóm đã hướng dẫn chạy từng bước sẵn trong file mỗi ipynb đính kèm
